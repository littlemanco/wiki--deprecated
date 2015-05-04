# Logging

## Event Logging
### Style
| Structure | Guideline      |
|:---------:|:--------------:|
| Case      | Lower case     |

### Meta Log Information
| Field       | Description                          |
|:-----------:|:------------------------------------:|
| Environment | development, staging or production   |
| Type        | event, error, performance            |
| Format      | json, string, xml                    |

### Base Event Information
| Field       | Description                                                            |
|:-----------:|:----------------------------------------------------------------------:|
| Code        | 200                                                                    |
| File        | index.php                                                              |
| Level       | Emergency, Alert, Critical, Error, Warning, Notice, Information, Debug |
| Payload     | This is an event                                                       |
| URL         | http://dev.howden.io                                                   |
| UserID      | 58                                                                     |
| Tags        | PHP, Magento                                                           |

### Error Event Information
| Field       | Description                                                              |
|:-----------:|:------------------------------------------------------------------------:|

#### Canonical Tags
| Tag        | Alternatives   |
|:----------:|:--------------:|
| ECMAScript | Javascript, JS |
| Magento    | Mage, Varien   |
| PHP        |                |

## Performance Logging Information

### Service Usage Information <sup>[1]</sup>
 - Saturation (or queue)
 - Utilisation (or % usage)
 - Error Count

## Code Samples
 
### Nginx
``` 
    log_format json '{ "time": "$time_local", '
        '"remote_addr": "$remote_addr", '
        '"request_time": "$request_time", '
        '"code": "$status", '
        '"file": "$request_uri", '
        '"level": "info", '
        '"payload": "$request", '
        '"request_method": "$request_method", '
        '"http_user_agent": "$http_user_agent" }';
```

- [2] - Michael Bouvy, (2013). Ship logs to Logstash with Lumberjack / Logstash Forwarder. [online] Available at: http://michael.bouvy.net/blog/en/2013/12/06/use-lumberjack-logstash-forwarder-to-forward-logs-logstash/ [Accessed 2 May 2015].