---
title: Соединение разнородных данных
description: Типичные организации хранят данные в нескольких разнородных базах данных. Данные отдела кадров могут храниться в SQL Server, а данные управления учетной записью хранятся в каталоге. Другие данные могут храниться в собственных форматах.
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1099028bc85dc6492eade0315b7308b4c6aaa9
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314617"
---
# <a name="joining-heterogeneous-data"></a><span data-ttu-id="105e6-105">Соединение разнородных данных</span><span class="sxs-lookup"><span data-stu-id="105e6-105">Joining Heterogeneous Data</span></span>

<span data-ttu-id="105e6-106">Типичные организации хранят данные в нескольких разнородных базах данных.</span><span class="sxs-lookup"><span data-stu-id="105e6-106">Typical organizations store data in multiple heterogeneous databases.</span></span> <span data-ttu-id="105e6-107">Данные отдела кадров могут храниться в SQL Server, а данные управления учетной записью хранятся в каталоге.</span><span class="sxs-lookup"><span data-stu-id="105e6-107">Human Resources data may be stored in SQL Server, while account management data is stored in the directory.</span></span> <span data-ttu-id="105e6-108">Другие данные могут храниться в собственных форматах.</span><span class="sxs-lookup"><span data-stu-id="105e6-108">Other data may be stored in proprietary formats.</span></span>

<span data-ttu-id="105e6-109">В SQL Server 7,0, ADSI и поставщике OLE DB можно объединить данные из Active Directory с данными в SQL Server и создать представление Объединенных данных.</span><span class="sxs-lookup"><span data-stu-id="105e6-109">With, SQL Server 7.0, ADSI, and the OLE DB Provider, it is possible to join data from Active Directory to data in SQL Server and create a view of the joined data.</span></span>

<span data-ttu-id="105e6-110">**Соединение Active Directory данных с SQL Server данными**</span><span class="sxs-lookup"><span data-stu-id="105e6-110">**To join Active Directory Data with SQL Server Data**</span></span>

1.  <span data-ttu-id="105e6-111">Запуск **анализатора запросов SQL** (запуск \| программ \| Microsoft SQL Server 7,0)</span><span class="sxs-lookup"><span data-stu-id="105e6-111">Run the **SQL Query Analyzer** (Start \| Programs \| Microsoft SQL Server 7.0)</span></span>
2.  <span data-ttu-id="105e6-112">Войдите на компьютер SQL Server.</span><span class="sxs-lookup"><span data-stu-id="105e6-112">Log on to the SQL Server computer.</span></span>
3.  <span data-ttu-id="105e6-113">Выполните следующую строку (выделите ее и нажмите клавиши CTRL + E):</span><span class="sxs-lookup"><span data-stu-id="105e6-113">Execute the following line (by highlighting it and pressing CTRL+E):</span></span>

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    <span data-ttu-id="105e6-114">В этой строке для системной хранимой процедуры [ \_ аддлинкедсервер](https://msdn.microsoft.com/library/Aa259589.aspx) используются следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="105e6-114">In this line, the arguments for the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure are as follows:</span></span>

    -   <span data-ttu-id="105e6-115">«ADSI» — это аргумент **сервера** , который будет именем этого связанного сервера.</span><span class="sxs-lookup"><span data-stu-id="105e6-115">" ADSI" is the **server** argument, which will be the name of this linked server.</span></span>
    -   <span data-ttu-id="105e6-116">"Active Directory Services" — это аргумент **срвпродукт** , который представляет собой имя источника данных OLE DB, добавляемого в качестве связанного сервера.</span><span class="sxs-lookup"><span data-stu-id="105e6-116">"Active Directory Services" is the **srvproduct** argument, which is the name of the OLE DB data source that you are adding as a linked server.</span></span>
    -   <span data-ttu-id="105e6-117">"Адсдсубжект" — это **аргумент \_ имени поставщика** и указывает, что вы используете поставщик OLE DB.</span><span class="sxs-lookup"><span data-stu-id="105e6-117">"ADSDSOObject" is the **provider\_name** argument and indicates you are using the OLE DB Provider.</span></span>
    -   <span data-ttu-id="105e6-118">"адсдатасаурце" — это **\_ аргумент источника данных**, который представляет собой имя источника данных, интерпретируемое поставщиком OLE DB.</span><span class="sxs-lookup"><span data-stu-id="105e6-118">"adsdatasource" is the **data\_source argument**, which is the name of the data source as interpreted by the OLE DB Provider.</span></span>

    <span data-ttu-id="105e6-119">Теперь можно использовать связанный сервер для доступа к Active Directory из SQL Server.</span><span class="sxs-lookup"><span data-stu-id="105e6-119">You can now use the linked server to access Active Directory from SQL Server.</span></span>

4.  <span data-ttu-id="105e6-120">В следующем примере выполняется запрос с помощью инструкции [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) .</span><span class="sxs-lookup"><span data-stu-id="105e6-120">The next example performs a query using the [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement.</span></span> <span data-ttu-id="105e6-121">Эта инструкция имеет два аргумента: ADSI, то есть имя только что созданного связанного сервера и Инструкция запроса.</span><span class="sxs-lookup"><span data-stu-id="105e6-121">This statement has two arguments: ADSI, which is the name of the linked server that you just created, and a query statement.</span></span> <span data-ttu-id="105e6-122">Инструкция запроса содержит следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="105e6-122">The query statement contains the following items:</span></span>

    -   <span data-ttu-id="105e6-123">Инструкция [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) содержит список данных, которые будут получены из службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="105e6-123">The [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service.</span></span> <span data-ttu-id="105e6-124">Для указания искомых данных необходимо использовать отображаемое имя LDAP.</span><span class="sxs-lookup"><span data-stu-id="105e6-124">You will need to use the LDAP display name to indicate which data you are searching for.</span></span>
    -   <span data-ttu-id="105e6-125">Инструкция [from](https://msdn.microsoft.com/library/Aa258869.aspx) содержит имя связанного сервера каталогов, из которого будут получены эти сведения.</span><span class="sxs-lookup"><span data-stu-id="105e6-125">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from.</span></span>
    -   <span data-ttu-id="105e6-126">Оператор [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) предоставляет условия поиска.</span><span class="sxs-lookup"><span data-stu-id="105e6-126">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="105e6-127">В этом примере выполняется поиск пользователей.</span><span class="sxs-lookup"><span data-stu-id="105e6-127">In this example, it is searching for users.</span></span>

    <span data-ttu-id="105e6-128">Введите и выполните:</span><span class="sxs-lookup"><span data-stu-id="105e6-128">Type and execute:</span></span>

    ```sql
    SELECT * FROM OPENQUERY( ADSI, 
        'SELECT name, adsPath 
         FROM 'LDAP://DC=Fabrikam,DC=com' 
         WHERE objectCategory = 'Person' AND objectClass= 'user'')
    ```

    

    <span data-ttu-id="105e6-129">Также можно использовать [диалект LDAP](ldap-dialect.md)ADSI.</span><span class="sxs-lookup"><span data-stu-id="105e6-129">You can also use the ADSI [LDAP dialect](ldap-dialect.md).</span></span> <span data-ttu-id="105e6-130">Пример:</span><span class="sxs-lookup"><span data-stu-id="105e6-130">For example:</span></span>

    ```sql
    SELECT * FROM OPENQUERY(ADSI,
        '<LDAP://DC=Fabrikam,DC=COM>;(&(objectCategory=Person)(objectClass=user));name, adspath;subtree')
    ```

    

    <span data-ttu-id="105e6-131">В предыдущем примере запрос LDAP состоит из четырех частей:</span><span class="sxs-lookup"><span data-stu-id="105e6-131">In the previous example, the LDAP query has four parts:</span></span>

    -   <span data-ttu-id="105e6-132">" \<LDAP://DC=Fabrikam,DC=COM> " — это различающееся имя сервера каталогов для поиска.</span><span class="sxs-lookup"><span data-stu-id="105e6-132">"\<LDAP://DC=Fabrikam,DC=COM>" is the distinguished name of the directory server to search.</span></span>
    -   <span data-ttu-id="105e6-133">"(& (objectCategory = Person) (objectClass = пользователь))" является фильтром поиска LDAP (см. [синтаксис фильтра поиска](search-filter-syntax.md)).</span><span class="sxs-lookup"><span data-stu-id="105e6-133">"(&(objectCategory=Person)(objectClass=user))" is the LDAP search filter (see [Search Filter Syntax](search-filter-syntax.md)).</span></span>
    -   <span data-ttu-id="105e6-134">«Name, ADsPath» — это имена извлекаемых атрибутов (с использованием формата отображаемого имени LDAP).</span><span class="sxs-lookup"><span data-stu-id="105e6-134">"name, adspath" are the names (using the LDAP display name format) of the attributes to retrieve.</span></span>
    -   <span data-ttu-id="105e6-135">"поддерево" указывает [область](scope-of-query.md) поиска.</span><span class="sxs-lookup"><span data-stu-id="105e6-135">"subtree" indicates the [scope](scope-of-query.md) of the search.</span></span>

## <a name="related-topics"></a><span data-ttu-id="105e6-136">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="105e6-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="105e6-137">Создание и исполнение представления</span><span class="sxs-lookup"><span data-stu-id="105e6-137">Creating and Executing a View</span></span>](creating-and-executing-a-view.md)
</dt> </dl>

 

 




