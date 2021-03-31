---
title: Поиск объектов
description: Юлия Банкерт должна находить номера телефонов для всех руководителей программ, работающих в отделе 101. Для этого она может создать сценарий, использующий ADO и ADSI.
ms.assetid: c6325068-4ae2-4348-9938-96402262cd43
ms.tgt_platform: multiple
keywords:
- Поиск объектов ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3c26f05b63524e3a657c0c460efb921978bd19
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "103890275"
---
# <a name="searching-for-objects"></a>Поиск объектов

Юлия Банкерт должна находить номера телефонов для всех руководителей программ, работающих в отделе 101. Для этого она может создать сценарий, использующий ADO и ADSI.

При использовании поставщика ADO для выполнения запроса результирующий набор будет возвращать только первые 1000 объектов. По этой причине важно использовать постраничный запрос, чтобы извлечь все объекты в результирующем наборе, если служба каталогов не настроена для ограничения количества элементов в результирующем наборе. Возвращаемые наборы будут содержать количество элементов, указанных в размере страницы, и постраничные наборы будут по-прежнему возвращаться, пока не будет возвращено все элементы результирующего набора.


```VB
' Create the connection and command object.
Set oConnection1 = CreateObject("ADODB.Connection")
Set oCommand1 = CreateObject("ADODB.Command")
' Open the connection.
oConnection1.Provider = "ADsDSOObject"  ' This is the ADSI OLE-DB provider name
oConnection1.Open "Active Directory Provider"
' Create a command object for this connection.
Set oCommand1.ActiveConnection = oConnection1

' Compose a search string.
oCommand1.CommandText = "select name,telephoneNumber " & _
"from 'LDAP://DC=Fabrikam,DC=com'" & _
"WHERE objectCategory='Person'" & _
"AND objectClass='user'" & _
"AND title='Program Manager'" & _
"AND department=101"

' Execute the query.
Set rs = oCommand1.Execute
'--------------------------------------
' Navigate the record set
'--------------------------------------
While Not rs.EOF
    Debug.Print rs.Fields("Name") & " , " & rs.Fields("telephoneNumber")
    rs.MoveNext
Wend
```



Для выполнения поиска ADSI в Visual Basic или среде сценариев требуются три компонента ADO: **Подключение**, **команда** и **набор записей**. Объект **Connection** позволяет указать имя поставщика, альтернативные учетные данные, если применимо, и другие флаги. Объект **Command** позволяет указать параметры поиска и строку запроса. Необходимо связать объект **соединения** с объектом **Command** перед выполнением запроса. Наконец, объект **Recordset** используется для прохода по результирующему набору.

ADSI поддерживает два типа строк запросов или диалектов. В предыдущем примере кода используется диалект SQL. Также можно использовать диалект LDAP. Строка запроса диалекта LDAP основана на стандарте [rfc 2254](https://www.ietf.org/rfc/rfc2254.txt) (RFC — это документ запроса комментариев, который является основанием для разработки стандартов LDAP). Предыдущий пример можно преобразовать в следующий пример кода.


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



Почему слово «поддерево» находится в конце строки? В мире каталога можно указать область поиска. Доступны следующие варианты: "базовый", "одноуровневой" и "поддерево". "Base" используется для чтения самого объекта; "одноуровневой" ссылается на непосредственные дочерние элементы, аналогичные команде **dir** ; "поддерево" используется для поиска на нескольких уровнях с глубиной или вниз (аналогично **dir/s**).

С помощью диалекта SQL можно указать область в свойстве Command, как показано в следующем примере кода.


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



Если область не указана, по умолчанию используется поиск по поддереву.

> [!Note]  
> При использовании C++ можно использовать интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) из ADSI.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Реорганизации](reorganization.md)
</dt> </dl>

 

 




