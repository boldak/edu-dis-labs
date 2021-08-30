# Проєктування системи


Вбудовування зображень діаграм здійснюється з використанням сервісу [plantuml.com](https://plantuml.com/). 

В markdown-файлі використовується опис діаграми

```md

<center style="
    border-radius:4px;
    border: 1px solid #cfd7e6;
    box-shadow: 0 1px 3px 0 rgba(89,105,129,.05), 0 1px 1px 0 rgba(0,0,0,.025);
    padding: 1em;"
>

@startuml

participant Client

participant SR as "Service Registry"

participant Service

Service -> SR : register
SR -> SR
SR --> Service
...

SR -> Service: heartbeat
SR <-- Service: health
...

Client -> SR: find
Client <-- SR: service endpoint
Client -> Service: request
Client <-- Service: response



@enduml

</center>
```

яка буде відображена наступним чином

<center style="
    border-radius:4px;
    border: 1px solid #cfd7e6;
    box-shadow: 0 1px 3px 0 rgba(89,105,129,.05), 0 1px 1px 0 rgba(0,0,0,.025);
    padding: 1em;"
>

@startuml

    @startuml

participant Client

participant SR as "Service Registry"

participant Service

Service -> SR : register
SR -> SR
SR --> Service
...

SR -> Service: heartbeat
SR <-- Service: health
...

Client -> SR: find
Client <-- SR: service endpoint
Client -> Service: request
Client <-- Service: response



@enduml

</center>



