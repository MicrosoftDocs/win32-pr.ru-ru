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
# <a name="ldap-dialect"></a><span data-ttu-id="cf25d-105">Диалект LDAP</span><span class="sxs-lookup"><span data-stu-id="cf25d-105">LDAP Dialect</span></span>

<span data-ttu-id="cf25d-106">Диалект LDAP — это формат инструкций запроса, использующих [синтаксис фильтра поиска LDAP](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="cf25d-106">The LDAP dialect is a format for query statements that use the [LDAP search filter syntax](search-filter-syntax.md).</span></span> <span data-ttu-id="cf25d-107">Используйте инструкцию запроса LDAP со следующими интерфейсами поиска ADSI:</span><span class="sxs-lookup"><span data-stu-id="cf25d-107">Use an LDAP query statement with the following ADSI search interfaces:</span></span>

-   <span data-ttu-id="cf25d-108">Интерфейсы [объектов данных ActiveX (ADO)](searching-with-activex-data-objects-ado.md) , которые являются интерфейсами автоматизации, использующими OLE DB.</span><span class="sxs-lookup"><span data-stu-id="cf25d-108">The [ActiveX Data Object (ADO)](searching-with-activex-data-objects-ado.md) interfaces, which are Automation interfaces that use OLE DB.</span></span>
-   <span data-ttu-id="cf25d-109">[OLE DB](searching-with-ole-db.md), который представляет собой набор интерфейсов C/C++ для запросов к базам данных.</span><span class="sxs-lookup"><span data-stu-id="cf25d-109">[OLE DB](searching-with-ole-db.md), which is a set of C/C++ interfaces for querying databases.</span></span>
-   <span data-ttu-id="cf25d-110">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)— интерфейс C/C++ для Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cf25d-110">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), which is the C/C++ interface for Active Directory.</span></span>

<span data-ttu-id="cf25d-111">Строка диалекта LDAP состоит из четырех частей, разделенных точкой с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="cf25d-111">An LDAP dialect string consists of four parts separated by semicolons (;).</span></span>

-   <span data-ttu-id="cf25d-112">Базовое различающееся имя.</span><span class="sxs-lookup"><span data-stu-id="cf25d-112">Base distinguished name.</span></span> <span data-ttu-id="cf25d-113">Пример:</span><span class="sxs-lookup"><span data-stu-id="cf25d-113">For example:</span></span>

    ```VB
    <LDAP://DC=Fabrikam,DC=COM>
    ```

    

-   <span data-ttu-id="cf25d-114">Фильтры поиска LDAP.</span><span class="sxs-lookup"><span data-stu-id="cf25d-114">LDAP search filters.</span></span> <span data-ttu-id="cf25d-115">Дополнительные сведения о фильтрах поиска см. в разделе [синтаксис фильтра поиска](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="cf25d-115">For more information about search filters, see [Search Filter Syntax](search-filter-syntax.md).</span></span>
-   <span data-ttu-id="cf25d-116">Отображаемое имя LDAP извлекаемых атрибутов.</span><span class="sxs-lookup"><span data-stu-id="cf25d-116">The LDAP display name of the attributes to retrieve.</span></span> <span data-ttu-id="cf25d-117">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="cf25d-117">Multiple attributes are separated by a comma.</span></span>
-   <span data-ttu-id="cf25d-118">Задает область поиска.</span><span class="sxs-lookup"><span data-stu-id="cf25d-118">Specifies the scope of the search.</span></span> <span data-ttu-id="cf25d-119">Допустимые значения: "Base", "одноуровневой" и "subtree".</span><span class="sxs-lookup"><span data-stu-id="cf25d-119">Valid values are "base", "onelevel", and "subtree".</span></span> <span data-ttu-id="cf25d-120">Область, указанная в строке запроса LDAP, переопределяет любую область поиска, указанную с помощью свойства "SearchScope" объекта команды ADO.</span><span class="sxs-lookup"><span data-stu-id="cf25d-120">The scope specified in an LDAP query string overrides any search scope specified with the "SearchScope" property of the ADO Command object.</span></span>

<span data-ttu-id="cf25d-121">Ниже приведен пример кода диалекта LDAP в ADSI, который ищет все объекты в поддереве.</span><span class="sxs-lookup"><span data-stu-id="cf25d-121">The following is a code example of the LDAP dialect in ADSI that searches all the objects in the subtree.</span></span>


```VB
"<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn;subTree"
```



<span data-ttu-id="cf25d-122">Не все параметры поиска (например, размер страницы поиска) могут быть выражены в диалекте LDAP, поэтому необходимо задать параметры перед началом фактического выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="cf25d-122">Not all search options (search page size, for example) can be expressed in the LDAP dialect, so you must set the options before the actual query execution starts.</span></span>

## <a name="example-code-for-performing-an-ldap-query"></a><span data-ttu-id="cf25d-123">Пример кода для выполнения запроса LDAP</span><span class="sxs-lookup"><span data-stu-id="cf25d-123">Example Code for Performing an LDAP Query</span></span>

<span data-ttu-id="cf25d-124">В следующем примере кода показано, как использовать запрос LDAP.</span><span class="sxs-lookup"><span data-stu-id="cf25d-124">The following code example shows how to use an LDAP query</span></span>


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



<span data-ttu-id="cf25d-125">Дополнительные сведения о синтаксисе запросов см. в разделе [синтаксис фильтра поиска](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="cf25d-125">For details about the query syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf25d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="cf25d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf25d-127">Синтаксис фильтра поиска</span><span class="sxs-lookup"><span data-stu-id="cf25d-127">Search Filter Syntax</span></span>](search-filter-syntax.md)
</dt> <dt>

[<span data-ttu-id="cf25d-128">Диалект SQL</span><span class="sxs-lookup"><span data-stu-id="cf25d-128">SQL dialect</span></span>](sql-dialect.md)
</dt> <dt>

[<span data-ttu-id="cf25d-129">Поиск с помощью интерфейса IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="cf25d-129">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="cf25d-130">Поиск с помощью объекты данных ActiveX</span><span class="sxs-lookup"><span data-stu-id="cf25d-130">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="cf25d-131">Поиск с помощью OLE DB</span><span class="sxs-lookup"><span data-stu-id="cf25d-131">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 




