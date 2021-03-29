---
title: Серверы Active Directory и динамические DNS
description: Active Directory серверы публикуют свои адреса, чтобы клиенты могли найти их, зная только имя домена.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- динамическое DNS-Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971987cb73b65e46b36eda4c713054ba2796e63b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772758"
---
# <a name="active-directory-servers-and-dynamic-dns"></a>Серверы Active Directory и динамические DNS

Active Directory серверы публикуют свои адреса, чтобы клиенты могли найти их, зная только имя домена. Active Directory серверы публикуются с помощью записей ресурсов службы (RR SRV) в DNS. SRV RR — это запись DNS, используемая для соответствия имени службы адресу сервера, который предлагает службу. Имя RR SRV имеет следующий вид:


```C++
<service>.<protocol>.<domain>
```



Active Directory серверы предлагают службу LDAP по протоколу TCP, чтобы опубликованные имена были "LDAP. TCP <domain> ". Таким же параметром SRV RR для fabrikam.com является «ldap.tcp.fabrikam.com». Дополнительные данные о записи ресурса SRV указывают приоритет и вес для сервера, позволяя клиентам выбирать оптимальный сервер в соответствии с потребностями.

При установке сервера Active Directory он использует динамическое DNS для публикации. Так как TCP/IP-адреса могут быть изменены, серверы периодически проверяют свои регистрации, чтобы убедиться в их правильности, и при необходимости обновляйте их.

Динамическое DNS — это последнее дополнение к стандарту DNS. Динамическая DNS определяет протокол для динамического обновления DNS-сервера новыми данными. До динамического DNS администраторам требовалось вручную настраивать записи, хранящиеся в DNS-серверах.

 

 




