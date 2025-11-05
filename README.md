# Ansible Playbook для установки Vector

## Описание
Playbook устанавливает и настраивает Vector - высокопроизводительный пайплайн для обработки observability данных.

## Что делает playbook?
- Проверяет, установлен ли Vector
- Создает пользователя и группу `vector`
- Скачивает Vector с официального сайта
- Распаковывает архив в `/opt/vector`
- Создает симлинк на бинарник в `/usr/local/bin/vector`
- Настраивает конфигурацию через Jinja2 шаблон
- Создает systemd службу
- Запускает и включает службу Vector

## Параметры
- `vector_version`: версия Vector (по умолчанию: "0.37.0")
- `vector_install_dir`: директория установки (по умолчанию: "/opt/vector")
- `vector_config_dir`: директория конфигурации (по умолчанию: "/etc/vector")
- `vector_user`: пользователь Vector (по умолчанию: "vector")
- `vector_group`: группа Vector (по умолчанию: "vector")

## Использование
```bash
# Проверка синтаксиса
ansible-playbook -i prod.yml site.yml --syntax-check

# Проверка ansible-lint
ansible-lint site.yml

# Запуск в режиме проверки
ansible-playbook -i prod.yml site.yml --check

# Запуск с показом изменений
ansible-playbook -i prod.yml site.yml --diff

# Обычный запуск
ansible-playbook -i prod.yml site.yml
