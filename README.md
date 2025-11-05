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


Task #5

<img width="1103" height="91" alt="image" src="https://github.com/user-attachments/assets/e11a1414-6a71-4d56-991f-8844c7b46aa3" />

Task #6

<img width="1223" height="100" alt="image" src="https://github.com/user-attachments/assets/481b79ec-0be7-444c-ad69-bb2432cddf2d" />

Task #7

<img width="1223" height="100" alt="image" src="https://github.com/user-attachments/assets/9e917182-c66e-4fac-9c34-6b4e02474ac8" />

Task #8.1

<img width="1223" height="100" alt="image" src="https://github.com/user-attachments/assets/7182784a-8de5-4fb7-92a3-b1ebe88d97c3" />

Task #8.2

<img width="1223" height="100" alt="image" src="https://github.com/user-attachments/assets/4982abba-cbf5-45b5-9843-eea9170c50ef" />
