# Версия для ARM (macOS)
## Особенности 
- Изменена архитектура, используется [Ubuntu ARM](https://app.vagrantup.com/spox/boxes/ubuntu-arm)
- Изменен провайдер на Vmware Fusion
- Изменены некоторые директивы Ansible, но функицонал сохранён 
- Всегда включен GUI гипервизора, т.к. рекомендуется в гайдах  

## Подготовка 
Вот неплохая [инструкция](https://habr.com/ru/companies/bar/articles/708950/). Необходимо установить Vmware Fusion, Vagrant и плагин, свзяывающий их. 

Необходимо клонировать этот репозиторий с параметром `-b branch-name`.

После чего убедиться что вы на нужной ветке командой `git branch` и если это не так, сменить ветку командой `git checkout arm-version`.

Далее запуск и управление идентично x86 версии.

# ВНИМАНИЕ
**Устанавливаемые инструменты изначально не предназначены для работы на архитктуре, отличной от X86. Стабильная работа не гарантируется.** 