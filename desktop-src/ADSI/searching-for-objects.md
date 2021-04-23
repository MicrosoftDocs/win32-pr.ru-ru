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
# <a name="searching-for-objects"></a><span data-ttu-id="f2edb-105">Поиск объектов</span><span class="sxs-lookup"><span data-stu-id="f2edb-105">Searching for Objects</span></span>

<span data-ttu-id="f2edb-106">Юлия Банкерт должна находить номера телефонов для всех руководителей программ, работающих в отделе 101.</span><span class="sxs-lookup"><span data-stu-id="f2edb-106">Julie Bankert must find telephone numbers for all Program Managers who work in Department 101.</span></span> <span data-ttu-id="f2edb-107">Для этого она может создать сценарий, использующий ADO и ADSI.</span><span class="sxs-lookup"><span data-stu-id="f2edb-107">She can create a script that uses ADO and ADSI to accomplish this.</span></span>

<span data-ttu-id="f2edb-108">При использовании поставщика ADO для выполнения запроса результирующий набор будет возвращать только первые 1000 объектов.</span><span class="sxs-lookup"><span data-stu-id="f2edb-108">When using the ADO provider to perform a query, the result set will only return the first 1000 objects.</span></span> <span data-ttu-id="f2edb-109">По этой причине важно использовать постраничный запрос, чтобы извлечь все объекты в результирующем наборе, если служба каталогов не настроена для ограничения количества элементов в результирующем наборе.</span><span class="sxs-lookup"><span data-stu-id="f2edb-109">For this reason, it is important to use a paged query so that you can retrieve all of the objects in the result set, as long as the directory service has not been set to limit the number of items in a result set.</span></span> <span data-ttu-id="f2edb-110">Возвращаемые наборы будут содержать количество элементов, указанных в размере страницы, и постраничные наборы будут по-прежнему возвращаться, пока не будет возвращено все элементы результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="f2edb-110">Return sets will contain the number of items that you specify in the page size, and paged sets will continue to be returned until all items in the result set have been returned.</span></span>


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



<span data-ttu-id="f2edb-111">Для выполнения поиска ADSI в Visual Basic или среде сценариев требуются три компонента ADO: **Подключение**, **команда** и **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="f2edb-111">To perform an ADSI search in Visual Basic or a scripting environment, three ADO components are required: **Connection**, **Command**, and **Recordset**.</span></span> <span data-ttu-id="f2edb-112">Объект **Connection** позволяет указать имя поставщика, альтернативные учетные данные, если применимо, и другие флаги.</span><span class="sxs-lookup"><span data-stu-id="f2edb-112">The **Connection** object enables you to specify the provider name, alternate credentials, if applicable, and other flags.</span></span> <span data-ttu-id="f2edb-113">Объект **Command** позволяет указать параметры поиска и строку запроса.</span><span class="sxs-lookup"><span data-stu-id="f2edb-113">The **Command** object enables you to specify search preferences and the query string.</span></span> <span data-ttu-id="f2edb-114">Необходимо связать объект **соединения** с объектом **Command** перед выполнением запроса.</span><span class="sxs-lookup"><span data-stu-id="f2edb-114">You must associate the **Connection** object to a **Command** object before the execution of the query.</span></span> <span data-ttu-id="f2edb-115">Наконец, объект **Recordset** используется для прохода по результирующему набору.</span><span class="sxs-lookup"><span data-stu-id="f2edb-115">Finally, the **Recordset** object is used to iterate the result set.</span></span>

<span data-ttu-id="f2edb-116">ADSI поддерживает два типа строк запросов или диалектов.</span><span class="sxs-lookup"><span data-stu-id="f2edb-116">ADSI supports two types of query strings or dialects.</span></span> <span data-ttu-id="f2edb-117">В предыдущем примере кода используется диалект SQL.</span><span class="sxs-lookup"><span data-stu-id="f2edb-117">The preceding code example uses the SQL dialect.</span></span> <span data-ttu-id="f2edb-118">Также можно использовать диалект LDAP.</span><span class="sxs-lookup"><span data-stu-id="f2edb-118">You can also use the LDAP dialect.</span></span> <span data-ttu-id="f2edb-119">Строка запроса диалекта LDAP основана на стандарте [rfc 2254](https://www.ietf.org/rfc/rfc2254.txt) (RFC — это документ запроса комментариев, который является основанием для разработки стандартов LDAP).</span><span class="sxs-lookup"><span data-stu-id="f2edb-119">The LDAP dialect query string is based on [RFC 2254](https://www.ietf.org/rfc/rfc2254.txt) (an RFC is a Request For Comments document, which is the basis for developing LDAP standards).</span></span> <span data-ttu-id="f2edb-120">Предыдущий пример можно преобразовать в следующий пример кода.</span><span class="sxs-lookup"><span data-stu-id="f2edb-120">The preceding example can be translated to the following code example.</span></span>


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



<span data-ttu-id="f2edb-121">Почему слово «поддерево» находится в конце строки?</span><span class="sxs-lookup"><span data-stu-id="f2edb-121">Why is the word "subtree" at the end of the string?</span></span> <span data-ttu-id="f2edb-122">В мире каталога можно указать область поиска.</span><span class="sxs-lookup"><span data-stu-id="f2edb-122">In the directory world, you can specify the scope of search.</span></span> <span data-ttu-id="f2edb-123">Доступны следующие варианты: "базовый", "одноуровневой" и "поддерево".</span><span class="sxs-lookup"><span data-stu-id="f2edb-123">The choices are: "base", "onelevel", and "subtree".</span></span> <span data-ttu-id="f2edb-124">"Base" используется для чтения самого объекта; "одноуровневой" ссылается на непосредственные дочерние элементы, аналогичные команде **dir** ; "поддерево" используется для поиска на нескольких уровнях с глубиной или вниз (аналогично **dir/s**).</span><span class="sxs-lookup"><span data-stu-id="f2edb-124">"base" is used to read the object itself; "onelevel" refers to the immediate children, similar to the **dir** command; "subtree" is used to search deep or down multiple levels (similar to **dir /s**).</span></span>

<span data-ttu-id="f2edb-125">С помощью диалекта SQL можно указать область в свойстве Command, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="f2edb-125">With the SQL dialect, you can specify scope in the command property, such as in the following code example.</span></span>


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



<span data-ttu-id="f2edb-126">Если область не указана, по умолчанию используется поиск по поддереву.</span><span class="sxs-lookup"><span data-stu-id="f2edb-126">If scope is not specified, by default it uses a subtree search.</span></span>

> [!Note]  
> <span data-ttu-id="f2edb-127">При использовании C++ можно использовать интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) из ADSI.</span><span class="sxs-lookup"><span data-stu-id="f2edb-127">If you use C++, you can use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface from ADSI.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f2edb-128">См. также</span><span class="sxs-lookup"><span data-stu-id="f2edb-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2edb-129">Реорганизации</span><span class="sxs-lookup"><span data-stu-id="f2edb-129">Reorganization</span></span>](reorganization.md)
</dt> </dl>

 

 




