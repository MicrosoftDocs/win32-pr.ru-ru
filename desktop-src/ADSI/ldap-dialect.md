---
title: Диалект LDAP
description: Диалект LDAP — это формат инструкций запроса, использующих синтаксис фильтра поиска LDAP.
ms.assetid: 29aca7e6-3ed5-4efd-8b03-6a2ee0571f1f
ms.tgt_platform: multiple
keywords:
- Диалекты ADSI для LDAP
- диалекты ADSI, диалект LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f7d1f65a41655596d0a14cf6e2a3595916c2cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887524"
---
# <a name="ldap-dialect"></a>Диалект LDAP

Диалект LDAP — это формат инструкций запроса, использующих [синтаксис фильтра поиска LDAP](search-filter-syntax.md). Используйте инструкцию запроса LDAP со следующими интерфейсами поиска ADSI:

-   Интерфейсы [объектов данных ActiveX (ADO)](searching-with-activex-data-objects-ado.md) , которые являются интерфейсами автоматизации, использующими OLE DB.
-   [OLE DB](searching-with-ole-db.md), который представляет собой набор интерфейсов C/C++ для запросов к базам данных.
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)— интерфейс C/C++ для Active Directory.

Строка диалекта LDAP состоит из четырех частей, разделенных точкой с запятой (;).

-   Базовое различающееся имя. Пример:

    ```VB
    <LDAP://DC=Fabrikam,DC=COM>
    ```

    

-   Фильтры поиска LDAP. Дополнительные сведения о фильтрах поиска см. в разделе [синтаксис фильтра поиска](search-filter-syntax.md).
-   Отображаемое имя LDAP извлекаемых атрибутов. Несколько атрибутов разделяются запятыми.
-   Задает область поиска. Допустимые значения: "Base", "одноуровневой" и "subtree". Область, указанная в строке запроса LDAP, переопределяет любую область поиска, указанную с помощью свойства "SearchScope" объекта команды ADO.

Ниже приведен пример кода диалекта LDAP в ADSI, который ищет все объекты в поддереве.


```VB
"<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn;subTree"
```



Не все параметры поиска (например, размер страницы поиска) могут быть выражены в диалекте LDAP, поэтому необходимо задать параметры перед началом фактического выполнения запроса.

## <a name="example-code-for-performing-an-ldap-query"></a>Пример кода для выполнения запроса LDAP

В следующем примере кода показано, как использовать запрос LDAP.


```VB
Dim con As New Connection, rs As New Recordset
Dim adVariant
Dim i 'Used for counter
Dim j 'Used for counter
Dim Com As New Command
Dim strDomain As String
Dim strPassword As String
 
' Open a Connection object.
con.Provider = "ADsDSOObject"
con.Properties("ADSI Flag") = 1
con.Properties("User ID") = strDomain + "\" + strUserID
con.Properties("Password") = strPassword

con.Open "Active Directory Provider"
 
' Create a command object on this connection.
Set Com.ActiveConnection = con
 
' Set the query string.
Com.CommandText = "<LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com>;
     (objectClass=*);ADsPath, objectclass;base"
 
' Set search preferences.
Com.Properties("Page Size") = 1000
Com.Properties("Timeout") = 30 'seconds
 
' Execute the query.
Set rs = Com.Execute
 
' Navigate the record set.
rs.MoveFirst
While Not rs.EOF
    For i = 0 To rs.Fields.Count - 1
        If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
            Debug.Print rs.Fields(i).Name, " = "
            For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
                Debug.Print rs.Fields(i).Value(j), " # "
            Next j
        Else
            Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
        End If
    Next i
    rs.MoveNext
Wend
 
rs.MoveLast
Debug.Print "No. of rows = ", rs.RecordCount
```



Дополнительные сведения о синтаксисе запросов см. в разделе [синтаксис фильтра поиска](search-filter-syntax.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Синтаксис фильтра поиска](search-filter-syntax.md)
</dt> <dt>

[Диалект SQL](sql-dialect.md)
</dt> <dt>

[Поиск с помощью интерфейса IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Поиск с помощью объекты данных ActiveX](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Поиск с помощью OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




