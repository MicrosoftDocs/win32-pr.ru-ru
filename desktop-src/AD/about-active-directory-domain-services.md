---
title: Сведения о службах домен Active Directory
description: В этом справочном материале содержится основная информация по интеграции Active Directory Майкрософт в распределенные приложения, предназначенные для операционных систем, поддерживающих Active Directory.
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, сведения
- Active Directory домен Active Directory Services, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e4ef886409b435e1687d8ca6cf530b940852f3569818bb3afab69f57ab6b97c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841078"
---
# <a name="about-active-directory-domain-services"></a>Сведения о службах домен Active Directory

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a>Написание мощных приложений, использующих службы домен Active Directory

Это руководство содержит подробную информацию по интеграции домен Active Directory служб в распределенные приложения, предназначенные для операционных систем, которые поддерживают службы домен Active Directory, в том числе:

-   Windows Server 2008
-   Windows Server 2008 R2
-   Windows Server 2012
-   Windows Server 2012 R2
-   Windows Server 2016

> [!Note]  
> Эти разделы предназначены для разработчиков программного обеспечения. Сведения о проблемах поддержки см. в разделе [Служба поддержки Майкрософт](https://windows.microsoft.com/windows/support#1tc). Сведения об администрировании Active Directory см. в разделе [домен Active Directory Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) на сайте TechNet.

 

## <a name="fundamental-directory-features"></a>Основные возможности каталога

Служба каталогов — это фундаментальная служба для распределенных приложений. Служба каталогов должна предоставлять функции, перечисленные в следующей таблице.



| Компонент               | Описание                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Прозрачность расположения | Возможность поиска пользователей, групп, сетевых служб или ресурсов, данных без адреса объекта           |
| Хранилище данных объектов           | Возможность хранения данных пользователя, группы, Организации и службы в иерархическом дереве                    |
| Расширенный запрос            | Возможность поиска объекта путем запроса свойств объекта                                          |
| Высокая доступность     | Возможность поиска реплики каталога в расположении, которое эффективно для операций чтения и записи |



 

## <a name="advanced-features-of-active-directory-domain-services"></a>Дополнительные возможности служб домен Active Directory Services

Службы домен Active Directory Services предоставляют функции, перечисленные в следующей таблице.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Компонент</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Поддержка стандартов Интернета</td>
<td>Службы домен Active Directory Services реализуют свои функции в соответствии с опубликованными интернет-стандартами, такими как LDAP и DNS.</td>
</tr>
<tr class="even">
<td>Тесно интегрированная и гибкая безопасность</td>
<td>Преимущества (список неполон):<br/>
<ul>
<li>Выбранные пакеты проверки подлинности. Kerberos, SSL (SSL) или сочетание; Например, установите канал SSL для шифрования, а затем используйте Kerberos для проверки подлинности.</li>
<li>Централизованное управление доступом к службам и ресурсам с помощью пользователей и групп в службах домен Active Directory Services.</li>
<li>Делегирование администрирования, чтобы администраторы центрального администратора могли делегировать административные задачи, такие как изменение пароля или создание и удаление конкретного объекта.</li>
<li>сервер Active Directory использует те же механизмы контроля доступа, которые используются в файловых системах в Windows операционных системах. Таким же средствами, которые управляют доступом к файловой системе, работают с домен Active Directory Services.</li>
<li>Комплексная инфраструктура открытых ключей. Сервер сертификатов (Майкрософт) и поддержка смарт-карт интегрированы со службами домен Active Directory Services для обеспечения входа и управления сертификатами с помощью смарт-карт.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Легко программировать</td>
<td>К серверу Active Directory можно обращаться и администрировать программно с помощью API <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">интерфейсов служб Active Directory</a> , API <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">протокола Lightweight Directory Access</a> или пространства имен <a href="/dotnet/api/system.directoryservices">System. DirectoryServices</a> .</td>
</tr>
<tr class="even">
<td>Системные службы с поддержкой каталога</td>
<td>клиентское приложение можно легко развернуть на распределенных настольных компьютерах, создав пакет установщик Windows и используя функцию развертывания приложений, доступную в операционных системах Windows.</td>
</tr>
<tr class="odd">
<td>Интеграция ключевых приложений</td>
<td>ключевые распределенные приложения, такие как Exchange, интегрируются со службами домен Active Directory. Таким же компаниям можно сократить количество управляемых служб каталогов.</td>
</tr>
<tr class="even">
<td>Расширенная и расширяемая схема</td>
<td>Схема определяет, какие объекты и свойства могут быть записаны и прочитаны из службы каталогов. Схема Active Directory является богатой. Большая часть объектов и свойств, необходимых службе, доступна. В противном случае распределенное приложение может расширить схему для поддержки требований приложения.</td>
</tr>
</tbody>
</table>



 

Дополнительные сведения о службах домен Active Directory см. в следующих статьях:

-   [Основные понятия домен Active Directory служб](core-concepts-of-active-directory-domain-services.md)
-   [Архитектура Active Directory](active-directory-domain-services-architecture.md)
-   [Схема Active Directory](active-directory-schema.md)

