# Golang Redis Job Queueing Service
Этот проект представляет собой сервис очередей заданий, реализованный на языке Go с использованием Redis. Он включает в себя функции продюсера и консюмера для обработки задач.
## Установка
1. Убедитесь, что у вас установлен [Go](https://golang.org/dl/) и [Docker](https://www.docker.com/get-started).
2. Клонируйте репозиторий:

bash
   git clone https://github.com/Mukam21/Golang-Redis_job_queueing_service.git
   cd Golang-Redis_job_queueing_service
3. Установите зависимости:

bash
   go mod tidy

## Запуск с использованием Docker
Для запуска Redis-сервиса с использованием Docker выполните следующую команду:

bash
docker-compose up -d

## Запуск приложения
### Продюсер
Чтобы запустить продюсер, выполните следующую команду:

bash
go run main.go producer

### Консумер
Чтобы запустить консюмера, выполните следующую команду:

bash
go run main.go consumer

## Веб-интерфейс
После запуска продюсера вы можете получить доступ к веб-интерфейсу, перейдя по адресу [http://localhost:3333/start](http://localhost:3333/start) для просмотра статистики очереди.
## Зависимости
- [rmq](https://github.com/adjust/rmq): библиотека для работы с Redis как с системой очередей.
- [urfave/cli](https://github.com/urfave/cli): библиотека для создания командных интерфейсов.
