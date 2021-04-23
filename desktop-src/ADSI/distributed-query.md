---
title: Распределенный запрос
description: Поскольку ADSI является поставщиком OLE DB, он может участвовать в распределенном запросе, представленном в Microsoft SQL Server 7,0.
ms.assetid: 0a93ec2e-397a-47f7-b00c-f0f9aaa06de6
ms.tgt_platform: multiple
keywords:
- запросы к ADSI, распределенный запрос
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8675f0a5ba9faa6ece78783eb4f61f17aafabc8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "105654263"
---
# <a name="distributed-query"></a><span data-ttu-id="240be-104">Распределенный запрос</span><span class="sxs-lookup"><span data-stu-id="240be-104">Distributed Query</span></span>

<span data-ttu-id="240be-105">Поскольку ADSI является поставщиком OLE DB, он может участвовать в распределенном запросе, представленном в Microsoft SQL Server 7,0.</span><span class="sxs-lookup"><span data-stu-id="240be-105">Because ADSI is an OLE DB Provider, it can participate in Distributed Query introduced in Microsoft SQL Server 7.0.</span></span> <span data-ttu-id="240be-106">Ниже приведены возможные сценарии.</span><span class="sxs-lookup"><span data-stu-id="240be-106">The following are possible scenarios:</span></span>

-   <span data-ttu-id="240be-107">Объединение Active Directory объектов с SQL Server данными.</span><span class="sxs-lookup"><span data-stu-id="240be-107">Joining Active Directory objects with SQL Server data.</span></span>
-   <span data-ttu-id="240be-108">Обновление данных SQL из Active Directory объектов.</span><span class="sxs-lookup"><span data-stu-id="240be-108">Updating SQL data from Active Directory objects.</span></span>
-   <span data-ttu-id="240be-109">Создание трехстороннее и двустороннего соединений с другими поставщиками OLE DB.</span><span class="sxs-lookup"><span data-stu-id="240be-109">Creating three-way or four-way joins with other OLE DB Providers.</span></span> <span data-ttu-id="240be-110">Например, сервер индекса, SQL Server и Active Directory.</span><span class="sxs-lookup"><span data-stu-id="240be-110">For example, Index Server, SQL Server, and Active Directory.</span></span>

<span data-ttu-id="240be-111">Поставщик OLE DB поддерживает два диалекта команд: LDAP и SQL, чтобы получить доступ к службе каталогов и вернуть результаты в виде табличной формы, которая может быть запрошена SQL Server распределенными запросами.</span><span class="sxs-lookup"><span data-stu-id="240be-111">The OLE DB Provider supports two command dialects, LDAP and SQL, to access the directory service and return results in a tabular form that can be queried with SQL Server distributed queries.</span></span>

<span data-ttu-id="240be-112">**Запуск анализатора запросов SQL**</span><span class="sxs-lookup"><span data-stu-id="240be-112">**To start the SQL Query Analyzer**</span></span>

1.  <span data-ttu-id="240be-113">Сначала откройте [анализатор запросов SQL](https://msdn.microsoft.com/library/Aa216983.aspx) на SQL Server, связанном со службой каталогов (см. раздел Создание связанного сервера).</span><span class="sxs-lookup"><span data-stu-id="240be-113">First, open the [SQL Query Analyzer](https://msdn.microsoft.com/library/Aa216983.aspx) on the SQL Server that is linked to the directory service (see Creating a Linked Server).</span></span>
2.  <span data-ttu-id="240be-114">Запуск **анализатора запросов SQL** (запуск \| программ \| Microsoft SQL Server 7,0)</span><span class="sxs-lookup"><span data-stu-id="240be-114">Run the **SQL Query Analyzer** (Start \| Programs \| Microsoft SQL Server 7.0)</span></span>
3.  <span data-ttu-id="240be-115">Войдите на компьютер SQL Server.</span><span class="sxs-lookup"><span data-stu-id="240be-115">Log on to the SQL Server computer.</span></span>
4.  <span data-ttu-id="240be-116">Введите запрос SQL в область редактора окна запроса.</span><span class="sxs-lookup"><span data-stu-id="240be-116">Enter the SQL Query into the Editor pane of the query window.</span></span>
5.  <span data-ttu-id="240be-117">Выполните запрос, нажав клавишу F5.</span><span class="sxs-lookup"><span data-stu-id="240be-117">Execute the query by pressing F5.</span></span>

<span data-ttu-id="240be-118">Дополнительные сведения приведены в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="240be-118">The following sections provide more detail:</span></span>

-   [<span data-ttu-id="240be-119">Создание связанного сервера</span><span class="sxs-lookup"><span data-stu-id="240be-119">Creating a Linked Server</span></span>](#creating-a-linked-server)
-   [<span data-ttu-id="240be-120">Создание SQL Server с проверкой подлинности имени входа</span><span class="sxs-lookup"><span data-stu-id="240be-120">Creating a SQL Server Authenticated Login</span></span>](#creating-a-sql-server-authenticated-login)
-   [<span data-ttu-id="240be-121">Запрос к службе каталогов</span><span class="sxs-lookup"><span data-stu-id="240be-121">Querying the Directory Service</span></span>](#querying-the-directory-service)

## <a name="creating-a-linked-server"></a><span data-ttu-id="240be-122">Создание связанного сервера</span><span class="sxs-lookup"><span data-stu-id="240be-122">Creating a Linked Server</span></span>

<span data-ttu-id="240be-123">Чтобы настроить распределенное соединение в службе каталогов Windows 2000 Server, создайте связанный сервер.</span><span class="sxs-lookup"><span data-stu-id="240be-123">To set up a distributed join on a Windows 2000 Server directory service, create a linked server.</span></span> <span data-ttu-id="240be-124">Для этого настройте сопоставление ADSI с помощью системной хранимой процедуры [SP \_ аддлинкедсервер](https://msdn.microsoft.com/library/Aa259589.aspx) .</span><span class="sxs-lookup"><span data-stu-id="240be-124">To do this, set up ADSI mapping by using the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure.</span></span> <span data-ttu-id="240be-125">Эта процедура связывает имя с именем поставщика OLE DB.</span><span class="sxs-lookup"><span data-stu-id="240be-125">This procedure links a name to an OLE DB Provider name.</span></span>

<span data-ttu-id="240be-126">В следующем примере обратите внимание, что в системной хранимой процедуре [SP \_ аддлинкедсервер](https://msdn.microsoft.com/library/Aa259589.aspx) используются несколько аргументов:</span><span class="sxs-lookup"><span data-stu-id="240be-126">In the following example, note that there are several arguments used with the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure:</span></span>

-   <span data-ttu-id="240be-127">«ADSI» — это аргумент **сервера** , который будет именем этого связанного сервера.</span><span class="sxs-lookup"><span data-stu-id="240be-127">"ADSI" is the **server** argument and will be the name of this linked server.</span></span>
-   <span data-ttu-id="240be-128">"Active Directory Services 2,5" — это аргумент **срвпродукт** , который представляет собой имя источника данных OLE DB, добавляемого в качестве связанного сервера.</span><span class="sxs-lookup"><span data-stu-id="240be-128">"Active Directory Services 2.5" is the **srvproduct** argument, which is the name of the OLE DB data source that you are adding as a linked server.</span></span>
-   <span data-ttu-id="240be-129">"Адсдсубжект" — это **аргумент \_ имени поставщика** .</span><span class="sxs-lookup"><span data-stu-id="240be-129">"ADSDSOObject" is the **provider\_name** argument.</span></span>
-   <span data-ttu-id="240be-130">"адсдатасаурце" — это **аргумент \_ источника данных** , который представляет собой имя источника данных, интерпретируемое поставщиком OLE DB.</span><span class="sxs-lookup"><span data-stu-id="240be-130">"adsdatasource" is the **data\_source** argument, which is the name of the data source as interpreted by the OLE DB Provider.</span></span>

<span data-ttu-id="240be-131">Команда [exec](https://msdn.microsoft.com/library/Aa258848.aspx) используется для выполнения системных хранимых процедур.</span><span class="sxs-lookup"><span data-stu-id="240be-131">The [EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) command is used to execute System Stored Procedures.</span></span>


```sql
EXEC sp_addlinkedserver 'ADSI', 'Active Directory Services 2.5', 
'ADSDSOObject', 'adsdatasource'
GO
```



<span data-ttu-id="240be-132">Для имен входа, прошедших проверку подлинности Windows, для доступа к каталогу с помощью SQL Serverного делегирования безопасности достаточно самостоятельного сопоставления.</span><span class="sxs-lookup"><span data-stu-id="240be-132">For Windows-authenticated logins, the self-mapping is sufficient to access the directory with SQL Server Security Delegation.</span></span> <span data-ttu-id="240be-133">Так как Самосопоставление создается по умолчанию для связанных серверов, созданных с помощью [SP \_ аддлинкедсервер](https://msdn.microsoft.com/library/Aa259589.aspx), никаких других сопоставлений имен входа не требуется.</span><span class="sxs-lookup"><span data-stu-id="240be-133">Because the self-mapping is created by default for linked servers created through [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx), no other login mapping is necessary.</span></span>

<span data-ttu-id="240be-134">Для имен входа, прошедших проверку подлинности SQL Server, можно настроить подходящие имена входа и пароли для подключения к службе каталогов с помощью системной хранимой процедуры [SP \_ аддлинкедсрвлогин](https://msdn.microsoft.com/library/Aa259581.aspx) .</span><span class="sxs-lookup"><span data-stu-id="240be-134">For SQL Server–authenticated logins, you can configure suitable logins and passwords for connecting to the directory service by using the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure.</span></span>

> [!Note]  
> <span data-ttu-id="240be-135">По возможности используйте аутентификацию Windows.</span><span class="sxs-lookup"><span data-stu-id="240be-135">When possible, use Windows Authentication.</span></span>

 

## <a name="creating-a-sql-server-authenticated-login"></a><span data-ttu-id="240be-136">Создание SQL Server с проверкой подлинности имени входа</span><span class="sxs-lookup"><span data-stu-id="240be-136">Creating a SQL Server Authenticated Login</span></span>

<span data-ttu-id="240be-137">Если вы предпочитаете использовать вход с проверкой подлинности SQL Server, а не проверку подлинности Windows, добавьте имя входа на связанный сервер (см. предыдущий раздел).</span><span class="sxs-lookup"><span data-stu-id="240be-137">If you prefer to use a SQL Server–authenticated login rather than Windows Authentication, add a login to the linked server (see the previous section).</span></span> <span data-ttu-id="240be-138">Для этого используйте системную хранимую процедуру [SP \_ аддлинкедсрвлогин](https://msdn.microsoft.com/library/Aa259581.aspx) .</span><span class="sxs-lookup"><span data-stu-id="240be-138">To do this, use the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure.</span></span>

<span data-ttu-id="240be-139">В следующем примере существует несколько аргументов, которые используются с системной хранимой процедурой [SP \_ аддлинкедсрвлогин](https://msdn.microsoft.com/library/Aa259581.aspx) :</span><span class="sxs-lookup"><span data-stu-id="240be-139">In the following example, there are several arguments that are used with the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure:</span></span>

-   <span data-ttu-id="240be-140">"ADSI" — это аргумент **рмтсврнаме** , который представляет собой имя связанного сервера, созданного в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="240be-140">"ADSI" is the **rmtsvrname** argument, which is the name of the linked server created in the previous example.</span></span>
-   <span data-ttu-id="240be-141">" \\ Администратор Fabrikam" — это аргумент **локаллогин** , который является именем входа на локальном сервере и может быть SQL Server именем входа или пользователем Windows NT.</span><span class="sxs-lookup"><span data-stu-id="240be-141">"Fabrikam\\Administrator" is the **locallogin** argument, which is the login on the local server and can be the SQL Server login or a Windows NT user.</span></span>
-   <span data-ttu-id="240be-142">"CN = Administrator, OU = Sales, DC = активедс, DC = Fabrikam, DC = com" — это аргумент **рмтусер** , который является именем пользователя, используемым для подключения, так как **useself** имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="240be-142">"CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com" is the **rmtuser** argument, which is the user name that you use to connect because **useself** is **false**.</span></span>
-   <span data-ttu-id="240be-143">"Secret \* \* 2000" — это **рмтпассворд**, который является паролем, связанным с **рмтусер**</span><span class="sxs-lookup"><span data-stu-id="240be-143">"secret\*\*2000" is the **rmtpassword**, which is the password associated to **rmtuser**</span></span>

<span data-ttu-id="240be-144">Команда [exec](https://msdn.microsoft.com/library/Aa258848.aspx) используется для выполнения системных хранимых процедур.</span><span class="sxs-lookup"><span data-stu-id="240be-144">The [EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) command is used to execute System Stored Procedures.</span></span>


```sql
EXEC sp_addlinkedsrvlogin 'ADSI', false, 'Fabrikam\Administrator', 
'CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com', 'secret**2000'
```



## <a name="querying-the-directory-service"></a><span data-ttu-id="240be-145">Запрос к службе каталогов</span><span class="sxs-lookup"><span data-stu-id="240be-145">Querying the Directory Service</span></span>

<span data-ttu-id="240be-146">После создания связанного сервера используйте инструкцию [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) для отправки запроса в службу каталогов.</span><span class="sxs-lookup"><span data-stu-id="240be-146">After you have created a linked server, use an [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement to send a query to the Directory Service.</span></span> <span data-ttu-id="240be-147">Следующий SQL-запрос создает виртуальную таблицу для хранения результатов запроса с помощью инструкции [Create View](https://msdn.microsoft.com/library/Aa258253.aspx) .</span><span class="sxs-lookup"><span data-stu-id="240be-147">The following SQL query creates a virtual table to hold your query results by using the [CREATE VIEW](https://msdn.microsoft.com/library/Aa258253.aspx) statement.</span></span> <span data-ttu-id="240be-148">Созданное представление называется "Виевадконтактс".</span><span class="sxs-lookup"><span data-stu-id="240be-148">The view that is created is named "viewADContacts".</span></span>

<span data-ttu-id="240be-149">Первая инструкция [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) определяет сведения, запрашиваемые из службы каталогов, и сопоставляет их со столбцом в таблице.</span><span class="sxs-lookup"><span data-stu-id="240be-149">The first [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement defines the information that is being queried from the directory service and maps it to a column in the table.</span></span> <span data-ttu-id="240be-150">Сведения, заключенные в квадратные скобки, указывают на данные, помещаемые в виртуальную таблицу.</span><span class="sxs-lookup"><span data-stu-id="240be-150">Information surrounded by brackets indicates the data that is put into the virtual table.</span></span> <span data-ttu-id="240be-151">Сведения, отсутствующие в квадратных скобках, указывают на данные, получаемые из службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="240be-151">The information that is not in brackets indicates the data that is retrieved from the directory service.</span></span> <span data-ttu-id="240be-152">Обратите внимание, что сведения, получаемые из службы каталогов, должны ссылаться по отображаемому имени LDAP.</span><span class="sxs-lookup"><span data-stu-id="240be-152">Notice that the information that is being retrieved from the directory service must be referenced by its LDAP display name.</span></span>

<span data-ttu-id="240be-153">Следующий оператор является инструкцией [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) .</span><span class="sxs-lookup"><span data-stu-id="240be-153">The next statement is the [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement.</span></span> <span data-ttu-id="240be-154">Эта инструкция имеет два аргумента: ADSI, то есть имя созданного связанного сервера и Инструкция запроса.</span><span class="sxs-lookup"><span data-stu-id="240be-154">This statement has two arguments: ADSI, which is the name of the linked server that you created, and a query statement.</span></span> <span data-ttu-id="240be-155">Инструкция запроса содержит следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="240be-155">The query statement contains the following items:</span></span>

-   <span data-ttu-id="240be-156">Инструкция [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) содержит список данных, которые будут получены из службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="240be-156">The [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service.</span></span> <span data-ttu-id="240be-157">Для указания искомых данных необходимо использовать отображаемое имя LDAP.</span><span class="sxs-lookup"><span data-stu-id="240be-157">You will need to use the LDAP display name to indicate which data you are searching for.</span></span>
-   <span data-ttu-id="240be-158">Инструкция [from](https://msdn.microsoft.com/library/Aa258869.aspx) содержит имя связанного сервера каталогов, из которого будут получены эти сведения.</span><span class="sxs-lookup"><span data-stu-id="240be-158">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from.</span></span>
-   <span data-ttu-id="240be-159">Оператор [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) предоставляет условия поиска.</span><span class="sxs-lookup"><span data-stu-id="240be-159">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="240be-160">В этом примере выполняется поиск контактов.</span><span class="sxs-lookup"><span data-stu-id="240be-160">In this example, it is searching for contacts.</span></span>

<span data-ttu-id="240be-161">Последняя инструкция [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) используется для отбора результатов из отображаемого представления.</span><span class="sxs-lookup"><span data-stu-id="240be-161">The final [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement is used to pick up results from the view to display.</span></span>


```sql
CREATE VIEW viewADContacts
AS
SELECT  [Name], sn [Last Name], street [Street], l [City], st [State]
FROM OPENQUERY( ADSI, 
     'SELECT name, sn, street, l, st
      FROM 'LDAP:// OU=Sales,DC=activeds,DC=Fabrikam,DC=Com'
      WHERE objectCategory='Person' AND 
      objectClass = 'contact'')
GO
SELECT * FROM viewADContacts
```



 

 




