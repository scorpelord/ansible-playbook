# Ansible Playbook

## Результаты выполнения задания

### 1. Запуск на test.yml
- **some_fact значение**: `12`

### 2. Файл с переменными
- **Файл**: `group_vars/all/examp.yml`
- **Изменено на**: `all default fact`

### 4. Запуск на prod.yml (после изменения)
- **deb** (ubuntu): `all default fact`
- **el** (centos7): `all default fact`

### 6. Запуск после добавления group_vars
- **deb** (ubuntu): `deb default fact`
- **el** (centos7): `el default fact`

### 8. Запуск с зашифрованными переменными
- **Пароль vault**: `netology`
- **Результат**: успешный запуск с расшифровкой переменных

### 9. Плагины подключения
- **Подходящий плагин для control node**: `local`

### 11. Финальный запуск с localhost
- **deb** (ubuntu): `deb default fact`
- **el** (centos7): `el default fact`
- **localhost**: `all default fact`

## Структура проекта
- `site.yml` - основной playbook
- `inventory/` - inventory файлы
- `group_vars/` - переменные групп (deb, el зашифрованы)
- `vault.key` - ключ шифрования

## Использование
```bash
ansible-playbook -i inventory/prod.yml site.yml --ask-vault-pass
