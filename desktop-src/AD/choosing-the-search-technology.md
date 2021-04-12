---
title: Выбор технологии поиска
description: Этот раздел содержит список технологий, используемых для поиска Active Directory.
ms.assetid: c9e887e3-7de4-4461-bc32-03db71c3e272
ms.tgt_platform: multiple
keywords:
- Поиск технологий в Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6edba5c87ed438bc0047e0381d7e366cd6cc865
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487496"
---
# <a name="choosing-the-search-technology"></a>Выбор технологии поиска

Технологии, перечисленные в следующей таблице, можно использовать для поиска в службах домен Active Directory.



| Технология                                                                     | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DirectorySearcher](/dotnet/api/system.directoryservices.directorysearcher?view=dotnet-plat-ext-3.1)<br/> | Класс [DirectorySearcher](/dotnet/api/system.directoryservices.directorysearcher?view=dotnet-plat-ext-3.1) предоставляется пространством имен [System. DirectoryServices](/dotnet/api/system.directoryservices?view=dotnet-plat-ext-3.1) , чтобы разрешить поиск в службах домен Active Directory с платформа .NET Framework. Дополнительные сведения см. [в разделе Поиск в каталоге](/previous-versions/ms180879(v=vs.90)).<br/>                                                                                                                                  |
| [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch)<br/>                       | ADSI предоставляет интерфейс [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) для запроса сервера Active Directory, а также для других служб каталогов, таких как NDS, с помощью протокола LDAP. **IDirectorySearch** — это COM-интерфейс, который возвращает расширенные типизированные данные, такие как Integer, Строка октета, строка, дескриптор безопасности, время в формате UTC, большое целое число или логическое значение. Дополнительные сведения об использовании **IDirectorySearch** см. в разделе [Поиск с помощью интерфейса IDirectorySearch](/windows/desktop/ADSI/searching-with-idirectorysearch).<br/> |
| OLE DB<br/>                                                              | OLE DB — это набор COM-интерфейсов, предоставляющих приложениям единообразный доступ к данным, хранящимся в различных источниках данных, независимо от расположения или типа. ADSI также предоставляет поставщик OLE DB для ADSI, который позволяет приложениям использовать OLE DB для доступа к домен Active Directory службам. Поставщик OLE DB ADSI использует интерфейсы [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) для отправки запросов в службы домен Active Directory и для получения результатов.<br/>                                     |
| ADO и другие технологии доступа к данным на основе OLE DB<br/>                 | Поставщик OLE DB ADSI позволяет использовать любую технологию доступа к данным на основе OLE DB, например ADO, для поиска в домен Active Directory службах.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| API LDAP<br/>                                                            | Контроллеры домена Windows 2000 — это серверы каталогов, соответствующие LDAP версии 3. API LDAP — это библиотека функций в стиле C. Приложения могут использовать API LDAP для поиска в домен Active Directoryных службах.<br/>                                                                                                                                                                                                                                                                              |



 

При выборе технологии необходимо учитывать следующее.

-   Для Microsoft Visual Basic и Visual Basic Scripting Edition (VBScript) рекомендуется использовать ADO.
-   Для C/C++ можно выбрать любую из технологий.
-   Если приложение широко использует ADSI, может быть проще использовать [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch). При использовании [**идиректорйобжект**](/windows/desktop/api/iads/nn-iads-idirectoryobject) для управления объектами в домен Active Directory Services используйте **IDirectorySearch** , чтобы упростить обработку свойств, возвращаемых из поиска. **IDirectorySearch** использует те же структуры [**адсвалуе**](/windows/desktop/api/iads/ns-iads-adsvalue) , что и **идиректорйобжект** , для представления свойств. Кроме того, **IDirectorySearch** предоставляется почти во всех COM-объектах ADSI. Если у вас есть указатель на COM-объект ADSI, можно вызвать метод **QueryInterface** , чтобы получить указатель **IDirectorySearch** , который можно использовать для выполнения поиска, начиная с объекта каталога, представленного COM-объектом ADSI.
-   Если приложение уже использует API OLE DB, ADO или LDAP, можно продолжать использовать эти технологии для поиска в службах домен Active Directory.
-   Если приложение должно соединять данные из службы домен Active Directory и базы данных SQL Server 7, используйте OLE DB. С помощью OLE DB приложение может выполнять распределенные запросы, которые ссылаются на домен Active Directory службы, таблицы и наборы строк из одной или нескольких баз данных Microsoft SQL Server 7.

 

