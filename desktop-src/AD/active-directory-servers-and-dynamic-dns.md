---
title: Серверы Active Directory и динамические DNS
description: Active Directory серверы публикуют свои адреса, чтобы клиенты могли найти их, зная только имя домена.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- динамическое DNS-Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9828a2d6d14d862e98d3c5c4129bbc70f5c411
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880064"
---
# <a name="active-directory-servers-and-dynamic-dns"></a>Серверы Active Directory и динамические DNS

Active Directory серверы публикуют свои адреса, чтобы клиенты могли найти их, зная только имя домена. Active Directory серверы публикуются с помощью записей ресурсов службы (RR SRV) в DNS. SRV RR — это запись DNS, используемая для соответствия имени службы адресу сервера, который предлагает службу. Имя RR SRV имеет следующий вид:


```C++
<service>.<protocol>.<domain>
```



Active Directory серверы предлагают службу LDAP по протоколу TCP, чтобы опубликованные имена были "LDAP. TCP". &lt; домен &gt; ". Таким же параметром SRV RR для fabrikam.com является «ldap.tcp.fabrikam.com». Дополнительные данные о записи ресурса SRV указывают приоритет и вес для сервера, позволяя клиентам выбирать оптимальный сервер в соответствии с потребностями.

При установке сервера Active Directory он использует динамическое DNS для публикации. Так как TCP/IP-адреса могут быть изменены, серверы периодически проверяют свои регистрации, чтобы убедиться в их правильности, и при необходимости обновляйте их.

Динамическое DNS — это последнее дополнение к стандарту DNS. Динамическая DNS определяет протокол для динамического обновления DNS-сервера новыми данными. До динамического DNS администраторам требовалось вручную настраивать записи, хранящиеся в DNS-серверах.

 

 




