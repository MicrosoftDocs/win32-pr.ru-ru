---
title: Поиск объектов
description: Юлия Банкерт должна находить номера телефонов для всех руководителей программ, работающих в отделе 101. Для этого она может создать сценарий, использующий ADO и ADSI.
ms.assetid: c6325068-4ae2-4348-9938-96402262cd43
ms.tgt_platform: multiple
keywords:
- Поиск объектов ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd41e87ad3396694b2f87158b15278c1dfbe28b044ad03ebbb09ddded705910a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973510"
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



для выполнения поиска ADSI в Visual Basic или среде сценариев требуются три компонента ADO: **подключение**, **команда** и **набор записей**. Объект **Connection** позволяет указать имя поставщика, альтернативные учетные данные, если применимо, и другие флаги. Объект **Command** позволяет указать параметры поиска и строку запроса. Необходимо связать объект **соединения** с объектом **Command** перед выполнением запроса. Наконец, объект **Recordset** используется для прохода по результирующему набору.

ADSI поддерживает два типа строк запросов или диалектов. в предыдущем примере кода используется диалект SQL. Также можно использовать диалект LDAP. Строка запроса диалекта LDAP основана на стандарте [rfc 2254](https://www.ietf.org/rfc/rfc2254.txt) (RFC — это документ запроса комментариев, который является основанием для разработки стандартов LDAP). Предыдущий пример можно преобразовать в следующий пример кода.


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



Почему слово «поддерево» находится в конце строки? В мире каталога можно указать область поиска. Доступны следующие варианты: "базовый", "одноуровневой" и "поддерево". "Base" используется для чтения самого объекта; "одноуровневой" ссылается на непосредственные дочерние элементы, аналогичные команде **dir** ; "поддерево" используется для поиска на нескольких уровнях с глубиной или вниз (аналогично **dir/s**).

используя диалект SQL, можно указать область в свойстве command, как показано в следующем примере кода.


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



Если область не указана, по умолчанию используется поиск по поддереву.

> [!Note]  
> При использовании C++ можно использовать интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) из ADSI.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Реорганизации](reorganization.md)
</dt> </dl>

 

 




