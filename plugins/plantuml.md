# UML

[PlantUML in GitBook](https://github.com/GitbookIO/plugin-puml)

安装

```bash
npm install gitbook-plugin-puml
"plugins": ["puml"]
```

或者

```bash
"plugins": ["puml"]
gitbook install
```

```uml
{% plantuml %}

Class Stage
Class Timeout {
    +constructor:function(cfg)
        +timeout:function(ctx)
        +overdue:function(ctx)
        +stage: Stage
}
Stage <|-- Timeout

{% endplantuml %}
```

{% plantuml %}
Bob->Alice : hello
{% endplantuml %}


{% plantuml %}
object john {
    name = 'John'
    birth = 1985
}
{% endplantuml %}


{% plantuml %}
Class Stage
Class Timeout {
    +constructor:function(cfg)
        +timeout:function(ctx)
        +overdue:function(ctx)
        +stage: Stage
}
Stage <|-- Timeout
{% endplantuml %}
