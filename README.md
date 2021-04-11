# MocksSpringBoot


Дополнен метод createPet() таким образом, что в ответ на запрос возвращался текст об успешном создании питомца;
Реализовано удаление и изменение питомцев используя аннотации @DeleteMapping и @PutMapping соответственно.

Создан REST веб-сервис (компас) используя технологию Spring, который определяет сторону света по введенным градусам (от 0 до 359). 
Точка отсчета север - 0 градусов. 
Изначально нужно дать понять сервису с помощью POST-запроса какие диапазоны градусов будут отвечать за какие стороны света. 
В примере ниже рассмотрены 4 диапазона (север, юг, запад, восток), а в проекте необходимо создать 8 (северо-восток, юго-запад и тд). 

Передавать стороны света с маленькой буквы.

Пример запроса:

{
    "north": "316-45",
    "east":  "46-135",
    "south": "136-225",
    "west": "226-315"
}

В качестве GET-запроса необходимо реализован вывод стороны света по запрашиваемому градусу, например:
Запрос:
{
    "degree": 56
}

Ответ:
{
    "side": "east"
}