---
title: Поиск с помощью объекты данных ActiveX (ADO)
description: Модель объектов данных ActiveX (ADO) состоит из объектов, перечисленных в следующей таблице.
ms.assetid: 27298f53-a652-49f2-a6e6-d92c7c6022af
ms.tgt_platform: multiple
keywords:
- Объекты данных ActiveX ADSI, поиск с помощью ADO
- Поиск с помощью объекты данных ActiveX ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e73f630892169c7086daf9bb1e7b6c13bfdf0a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654375"
---
# <a name="searching-with-activex-data-objects-ado"></a><span data-ttu-id="d18a0-105">Поиск с помощью объекты данных ActiveX (ADO)</span><span class="sxs-lookup"><span data-stu-id="d18a0-105">Searching with ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="d18a0-106">Модель объектов данных ActiveX (ADO) состоит из объектов, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d18a0-106">The ActiveX Data Object (ADO) model consists of objects listed in the following table.</span></span>



| <span data-ttu-id="d18a0-107">Объект</span><span class="sxs-lookup"><span data-stu-id="d18a0-107">Object</span></span>         | <span data-ttu-id="d18a0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d18a0-108">Description</span></span>                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d18a0-109">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="d18a0-109">**Connection**</span></span> | <span data-ttu-id="d18a0-110">Открытое соединение с OLE DBным источником данных, например ADSI.</span><span class="sxs-lookup"><span data-stu-id="d18a0-110">An open connection to an OLE DB data source such as ADSI.</span></span>                                                                          |
| <span data-ttu-id="d18a0-111">**Команда**</span><span class="sxs-lookup"><span data-stu-id="d18a0-111">**Command**</span></span>    | <span data-ttu-id="d18a0-112">Определяет определенную команду для запуска в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="d18a0-112">Defines a specific command to run against the data source.</span></span>                                                                         |
| <span data-ttu-id="d18a0-113">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="d18a0-113">**Parameter**</span></span>  | <span data-ttu-id="d18a0-114">Необязательная коллекция для любых параметров, предоставляемых объекту Command.</span><span class="sxs-lookup"><span data-stu-id="d18a0-114">An optional collection for any parameters to provide to the command object.</span></span>                                                        |
| <span data-ttu-id="d18a0-115">**Записей**</span><span class="sxs-lookup"><span data-stu-id="d18a0-115">**RecordSet**</span></span>  | <span data-ttu-id="d18a0-116">Набор записей из таблицы, объекта команды или синтаксиса SQL.</span><span class="sxs-lookup"><span data-stu-id="d18a0-116">A set of records from a table, command object, or SQL syntax.</span></span> <span data-ttu-id="d18a0-117">Набор записей может быть создан без базового объекта соединения.</span><span class="sxs-lookup"><span data-stu-id="d18a0-117">A recordset can be created without any underlying connection object.</span></span> |
| <span data-ttu-id="d18a0-118">**Поле**</span><span class="sxs-lookup"><span data-stu-id="d18a0-118">**Field**</span></span>      | <span data-ttu-id="d18a0-119">Один столбец данных в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="d18a0-119">A single column of data in a recordset.</span></span>                                                                                            |
| <span data-ttu-id="d18a0-120">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="d18a0-120">**Property**</span></span>   | <span data-ttu-id="d18a0-121">Коллекция значений, предоставляемых поставщиком для ADO.</span><span class="sxs-lookup"><span data-stu-id="d18a0-121">A collection of values supplied by the provider for ADO.</span></span>                                                                           |
| <span data-ttu-id="d18a0-122">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="d18a0-122">**Error**</span></span>      | <span data-ttu-id="d18a0-123">Содержит данные об ошибках доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="d18a0-123">Contains data about data access errors.</span></span> <span data-ttu-id="d18a0-124">Обновляется при возникновении ошибки в одной операции.</span><span class="sxs-lookup"><span data-stu-id="d18a0-124">Refreshed when an error occurs in a single operation.</span></span>                                      |



 

<span data-ttu-id="d18a0-125">Для взаимодействия ADO с ADSI необходимо, по крайней мере, два объекта ADO: **Connection** и **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d18a0-125">For ADO to communicate with ADSI, there must be, at least, two ADO objects: **Connection** and **RecordSet**.</span></span> <span data-ttu-id="d18a0-126">Эти объекты ADO служат для проверки подлинности пользователей и перечисления результатов соответственно.</span><span class="sxs-lookup"><span data-stu-id="d18a0-126">These ADO objects serve to authenticate users and enumerate results, respectively.</span></span> <span data-ttu-id="d18a0-127">Как правило, для поддержания активного соединения также используется объект **Command** , укажите параметры запроса, такие как размер страницы и область поиска, и выполните запрос.</span><span class="sxs-lookup"><span data-stu-id="d18a0-127">Typically, you will also use a **Command** object to maintain an active connection, specify query parameters, such as page size and search scope, and perform a query.</span></span> <span data-ttu-id="d18a0-128">Дополнительные сведения о синтаксисе фильтра поиска см. в разделе [синтаксис фильтра поиска](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="d18a0-128">For more information about the search filter syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

<span data-ttu-id="d18a0-129">Объект **Connection** загружает поставщик OLE DB и проверяет учетные данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="d18a0-129">The **Connection** object loads the OLE DB provider, and validates user credentials.</span></span> <span data-ttu-id="d18a0-130">В Visual Basic вызовите функцию **CreateObject** с помощью ADODB. Connection "для создания экземпляра объекта **Connection** , а затем для свойства **provider** объекта **Connection** устанавливается значение" адсдсубжект ".</span><span class="sxs-lookup"><span data-stu-id="d18a0-130">In Visual Basic, call the **CreateObject** function with "ADODB.Connection" to create an instance of a **Connection** object, and then set the **Provider** property of the **Connection** object to "ADsDSOObject".</span></span> <span data-ttu-id="d18a0-131">ADODB. Connection — идентификатор ProgID объекта **Connection** , а «адсдсубжект» — имя поставщика OLE DB в ADSI.</span><span class="sxs-lookup"><span data-stu-id="d18a0-131">"ADODB.Connection" is the ProgID of the **Connection** object and "ADsDSOObject" is the name of the OLE DB provider in ADSI.</span></span> <span data-ttu-id="d18a0-132">Если учетные данные не указаны, используются учетные данные пользователя, выполнившего вход в систему.</span><span class="sxs-lookup"><span data-stu-id="d18a0-132">If no credentials are specified, the credentials of the currently logged on user are used.</span></span>

<span data-ttu-id="d18a0-133">В следующем примере кода показано, как создать экземпляр объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="d18a0-133">The following code example shows how to create an instance of a **Connection** object.</span></span>


```VB
Set con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
```



<span data-ttu-id="d18a0-134">В следующем примере кода показано, как создать экземпляр объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="d18a0-134">The following code example shows how to create an instance of a **Connection** object.</span></span>


```VB
<%
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
%>
```



<span data-ttu-id="d18a0-135">В следующем примере кода показано, как создать экземпляр объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="d18a0-135">The following code example shows how to create an instance of a **Connection** object.</span></span> <span data-ttu-id="d18a0-136">Имейте в виду, что необходимо включить библиотеку типов ADO (msadoXX.dll) в качестве одной из ссылок в проекте Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d18a0-136">Be aware that you must include the ADO type library (msadoXX.dll) as one of the references in the Visual Basic project.</span></span>


```VB
Dim Con As New Connection
con.Provider = "ADsDSOObject"
```



<span data-ttu-id="d18a0-137">Укажите данные проверки подлинности пользователя, задав свойства объекта **соединения** .</span><span class="sxs-lookup"><span data-stu-id="d18a0-137">Specify user authentication data by setting the properties of the **Connection** object.</span></span> <span data-ttu-id="d18a0-138">В следующей таблице перечислены поддерживаемые в ADSI свойства проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="d18a0-138">The following table lists ADSI-supported user-authentication properties.</span></span>



| <span data-ttu-id="d18a0-139">Свойство</span><span class="sxs-lookup"><span data-stu-id="d18a0-139">Property</span></span>           | <span data-ttu-id="d18a0-140">Описание</span><span class="sxs-lookup"><span data-stu-id="d18a0-140">Description</span></span>                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d18a0-141">"Идентификатор пользователя"</span><span class="sxs-lookup"><span data-stu-id="d18a0-141">"User ID"</span></span>          | <span data-ttu-id="d18a0-142">Строка, идентифицирующая пользователя, контекст безопасности которого используется при выполнении поиска.</span><span class="sxs-lookup"><span data-stu-id="d18a0-142">A string that identifies the user whose security context is used when performing the search.</span></span> <span data-ttu-id="d18a0-143">Дополнительные сведения о формате строки имени пользователя см. в разделе [**иадсопендсобжект:: опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject).</span><span class="sxs-lookup"><span data-stu-id="d18a0-143">For more information about the format of the user name string, see [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject).</span></span> <span data-ttu-id="d18a0-144">Если значение не указано, по умолчанию используется пользователь, выполнивший вход в систему, или пользователь, олицетворяющий вызывающий процесс.</span><span class="sxs-lookup"><span data-stu-id="d18a0-144">If not specified, the default is the logged on user, or the user impersonated by the calling process.</span></span> |
| <span data-ttu-id="d18a0-145">"Пароль".</span><span class="sxs-lookup"><span data-stu-id="d18a0-145">"Password"</span></span>         | <span data-ttu-id="d18a0-146">Строка, указывающая пароль пользователя, определяемый "ИДЕНТИФИКАТОРом пользователя".</span><span class="sxs-lookup"><span data-stu-id="d18a0-146">A string that specifies the password of the user identified by "User ID".</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d18a0-147">"Зашифровать пароль"</span><span class="sxs-lookup"><span data-stu-id="d18a0-147">"Encrypt Password"</span></span> | <span data-ttu-id="d18a0-148">Логическое значение, указывающее, зашифрован ли пароль.</span><span class="sxs-lookup"><span data-stu-id="d18a0-148">A Boolean value that specifies whether the password is encrypted.</span></span> <span data-ttu-id="d18a0-149">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="d18a0-149">The default is **false**.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="d18a0-150">"Флаг ADSI"</span><span class="sxs-lookup"><span data-stu-id="d18a0-150">"ADSI Flag"</span></span>        | <span data-ttu-id="d18a0-151">Набор флагов из перечисления с [**\_ проверкой \_ подлинности ADS**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) , задающих параметры проверки подлинности привязки.</span><span class="sxs-lookup"><span data-stu-id="d18a0-151">A set of flags from the [**ADS\_AUTHENTICATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) enumeration that specify the binding authentication options.</span></span> <span data-ttu-id="d18a0-152">По умолчанию используется значение ноль.</span><span class="sxs-lookup"><span data-stu-id="d18a0-152">The default is zero.</span></span>                                                                                                                                                                         |



 

<span data-ttu-id="d18a0-153">В следующем примере кода показано, как свойства задаются перед созданием объекта **команды** .</span><span class="sxs-lookup"><span data-stu-id="d18a0-153">The following code example shows how the properties are set before creating the **Command** object.</span></span>


```VB
Set oConnect = CreateObject("ADODB.Connection")
oConnect.Provider = "ADsDSOObject"
oConnect.Properties("User ID") = stUser
oConnect.Properties("Password") = stPass
oConnect.Properties("Encrypt Password") = True
oConnect.Open "DS Query", stUser, stPass
```



<span data-ttu-id="d18a0-154">Второй объект ADO — это объект **Command** .</span><span class="sxs-lookup"><span data-stu-id="d18a0-154">The second ADO object is the **Command** object.</span></span> <span data-ttu-id="d18a0-155">ProgID объекта **команды** — ADODB. Command.</span><span class="sxs-lookup"><span data-stu-id="d18a0-155">The ProgID of the **Command** object is "ADODB.Command".</span></span> <span data-ttu-id="d18a0-156">Этот объект позволяет выдавать инструкции запросов и другие команды ADSI с помощью активного соединения.</span><span class="sxs-lookup"><span data-stu-id="d18a0-156">This object enables you to issue query statements and other commands to ADSI using the active connection.</span></span> <span data-ttu-id="d18a0-157">Объект **Command** использует свойство **ActiveConnection** для поддержания активного соединения.</span><span class="sxs-lookup"><span data-stu-id="d18a0-157">The **Command** object uses its **ActiveConnection** property to maintain an active connection.</span></span> <span data-ttu-id="d18a0-158">Он также поддерживает свойство **CommandText** для хранения инструкций запроса, выданных пользователем.</span><span class="sxs-lookup"><span data-stu-id="d18a0-158">It also maintains the **CommandText** property to hold query statements issued by a user.</span></span> <span data-ttu-id="d18a0-159">Инструкции запроса выражаются либо в [диалекте SQL](sql-dialect.md) , либо на [диалекте LDAP](ldap-dialect.md).</span><span class="sxs-lookup"><span data-stu-id="d18a0-159">The query statements are expressed in either the [SQL dialect](sql-dialect.md) or the [LDAP dialect](ldap-dialect.md).</span></span>

<span data-ttu-id="d18a0-160">В следующих примерах кода показано, как создать объект **Command** .</span><span class="sxs-lookup"><span data-stu-id="d18a0-160">The following code examples show how to create a **Command** object.</span></span>


```VB
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = oConnect
command.CommandText = 
"SELECT AdsPath, cn FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectClass = '*'"
```



<span data-ttu-id="d18a0-161">В следующем примере кода включите в качестве одной из ссылок библиотеку типов ADO (msadoXX.dll).</span><span class="sxs-lookup"><span data-stu-id="d18a0-161">In the following code example, include ADO type library (msadoXX.dll) as one of the references.</span></span>


```VB
Dim command As New Command
Set command.ActiveConnection = oConnect
command.CommandText = "<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn; subTree"
```



<span data-ttu-id="d18a0-162">Параметры поиска для объекта **Command** задаются путем установки свойства **Properties** .</span><span class="sxs-lookup"><span data-stu-id="d18a0-162">Search options for the **Command** object are specified by setting the **Properties** property.</span></span> <span data-ttu-id="d18a0-163">В следующей таблице перечислены допустимые именованные свойства для **свойств**.</span><span class="sxs-lookup"><span data-stu-id="d18a0-163">The following table lists acceptable named properties for **Properties**.</span></span>



| <span data-ttu-id="d18a0-164">Именованное свойство</span><span class="sxs-lookup"><span data-stu-id="d18a0-164">Named property</span></span>      | <span data-ttu-id="d18a0-165">Описание</span><span class="sxs-lookup"><span data-stu-id="d18a0-165">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d18a0-166">Асинхронной</span><span class="sxs-lookup"><span data-stu-id="d18a0-166">"Asynchronous"</span></span>      | <span data-ttu-id="d18a0-167">Логическое значение, указывающее, является ли поиск синхронным или асинхронным.</span><span class="sxs-lookup"><span data-stu-id="d18a0-167">A Boolean value that specifies whether the search is synchronous or asynchronous.</span></span> <span data-ttu-id="d18a0-168">Значение по умолчанию — false (синхронное).</span><span class="sxs-lookup"><span data-stu-id="d18a0-168">The default is False (synchronous).</span></span> <span data-ttu-id="d18a0-169">Синхронный поиск блокируется до тех пор, пока сервер не возвратит весь результат или для страничного поиска — всей страницы.</span><span class="sxs-lookup"><span data-stu-id="d18a0-169">A synchronous search blocks until the server returns the entire result, or for a paged search, the entire page.</span></span> <span data-ttu-id="d18a0-170">Асинхронный поиск блокируется до тех пор, пока не будет доступна одна строка результатов поиска или пока не истечет время, заданное свойством Timeout.</span><span class="sxs-lookup"><span data-stu-id="d18a0-170">An asynchronous search blocks until one row of the search results is available, or until the time specified by the "Timeout" property elapses.</span></span>                           |
| <span data-ttu-id="d18a0-171">"Результаты кэша"</span><span class="sxs-lookup"><span data-stu-id="d18a0-171">"Cache results"</span></span>     | <span data-ttu-id="d18a0-172">Логическое значение, указывающее, должен ли результат кэшироваться на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="d18a0-172">A Boolean value that specifies whether the result should be cached on the client side.</span></span> <span data-ttu-id="d18a0-173">Значение по умолчанию — **true**; ADSI кэширует результирующий набор.</span><span class="sxs-lookup"><span data-stu-id="d18a0-173">The default is **true**; ADSI caches the result set.</span></span> <span data-ttu-id="d18a0-174">Отключение этого параметра может оказаться желательным для больших результирующих наборов.</span><span class="sxs-lookup"><span data-stu-id="d18a0-174">Turning off this option may be desirable for large result sets.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="d18a0-175">"Следовать по ссылкам"</span><span class="sxs-lookup"><span data-stu-id="d18a0-175">"Chase referrals"</span></span>   | <span data-ttu-id="d18a0-176">Значение из [**объявления ADS \_ отслеживают \_ \_ перечисление ссылок**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) , которое указывает, как поиск осуществляется по ссылкам.</span><span class="sxs-lookup"><span data-stu-id="d18a0-176">A value from the [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) that specifies how the search chases referrals.</span></span> <span data-ttu-id="d18a0-177">По умолчанию **баннеры не имеют \_ \_ ссылок \_**. Дополнительные сведения об этом свойстве см. в разделе [ссылки](/windows/desktop/AD/referrals).</span><span class="sxs-lookup"><span data-stu-id="d18a0-177">The default is **ADS\_CHASE\_REFERRALS\_NEVER**.For more information about this property, see [Referrals](/windows/desktop/AD/referrals).</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="d18a0-178">"Только имена столбцов"</span><span class="sxs-lookup"><span data-stu-id="d18a0-178">"Column Names Only"</span></span> | <span data-ttu-id="d18a0-179">Логическое значение, указывающее, что при поиске должны извлекаться только имена атрибутов, которым были присвоены значения.</span><span class="sxs-lookup"><span data-stu-id="d18a0-179">A Boolean value that indicates that the search should retrieve only the name of attributes to which values have been assigned.</span></span> <span data-ttu-id="d18a0-180">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="d18a0-180">The default is **false**.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d18a0-181">«Псевдонимы Deref»</span><span class="sxs-lookup"><span data-stu-id="d18a0-181">"Deref Aliases"</span></span>     | <span data-ttu-id="d18a0-182">Логическое значение, указывающее, разрешены ли псевдонимы найденных объектов.</span><span class="sxs-lookup"><span data-stu-id="d18a0-182">A Boolean value that specifies whether aliases of found objects are resolved.</span></span> <span data-ttu-id="d18a0-183">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="d18a0-183">The default is **false**.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d18a0-184">"Размер страницы"</span><span class="sxs-lookup"><span data-stu-id="d18a0-184">"Page size"</span></span>         | <span data-ttu-id="d18a0-185">Целочисленное значение, которое включает подкачку и указывает максимальное количество объектов, возвращаемых в результирующем наборе.</span><span class="sxs-lookup"><span data-stu-id="d18a0-185">An integer value that turns on paging and specifies the maximum number of objects to return in a results set.</span></span> <span data-ttu-id="d18a0-186">По умолчанию размер страницы отсутствует.</span><span class="sxs-lookup"><span data-stu-id="d18a0-186">The default is no page size.</span></span> <span data-ttu-id="d18a0-187">Дополнительные сведения см. в разделе [получение больших наборов результатов](retrieving-large-results-sets.md).</span><span class="sxs-lookup"><span data-stu-id="d18a0-187">For more information, see [Retrieving Large Results Sets](retrieving-large-results-sets.md).</span></span>                                                                                                                                                                       |
| <span data-ttu-id="d18a0-188">SearchScope</span><span class="sxs-lookup"><span data-stu-id="d18a0-188">"SearchScope"</span></span>       | <span data-ttu-id="d18a0-189">Значение из перечисления [**ADS \_ скопинум**](/windows/win32/api/iads/ne-iads-ads_scopeenum) , которое указывает область поиска.</span><span class="sxs-lookup"><span data-stu-id="d18a0-189">A value from the [**ADS\_SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum) enumeration that specifies the search scope.</span></span> <span data-ttu-id="d18a0-190">По умолчанию **используется \_ \_ поддерево области объявлений**.</span><span class="sxs-lookup"><span data-stu-id="d18a0-190">The default is **ADS\_SCOPE\_SUBTREE**.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d18a0-191">"Предельный размер"</span><span class="sxs-lookup"><span data-stu-id="d18a0-191">"Size Limit"</span></span>        | <span data-ttu-id="d18a0-192">Целочисленное значение, указывающее предельный размер поиска.</span><span class="sxs-lookup"><span data-stu-id="d18a0-192">An integer value that specifies the size limit for the search.</span></span> <span data-ttu-id="d18a0-193">Для Active Directory ограничение размера определяет максимальное число возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="d18a0-193">For Active Directory, the size limit specifies the maximum number of returned objects.</span></span> <span data-ttu-id="d18a0-194">Сервер прекращает поиск по достижении предельного размера и возвращает накопленные результаты.</span><span class="sxs-lookup"><span data-stu-id="d18a0-194">The server stops searching when the size limit is reached and returns the results accumulated.</span></span> <span data-ttu-id="d18a0-195">Значение по умолчанию не ограничено.</span><span class="sxs-lookup"><span data-stu-id="d18a0-195">The default is no limit.</span></span>                                                                                                                                  |
| <span data-ttu-id="d18a0-196">"Сортировать по"</span><span class="sxs-lookup"><span data-stu-id="d18a0-196">"Sort on"</span></span>           | <span data-ttu-id="d18a0-197">Строка, указывающая список атрибутов с разделителями-запятыми для использования в качестве ключей сортировки.</span><span class="sxs-lookup"><span data-stu-id="d18a0-197">A string that specifies a comma-separated list of attributes to use as sort keys.</span></span> <span data-ttu-id="d18a0-198">Это свойство работает только для серверов каталогов, поддерживающих элемент управления LDAP для сортировки на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="d18a0-198">This property works only for directory servers that support the LDAP control for server-side sorting.</span></span> <span data-ttu-id="d18a0-199">Active Directory поддерживает элемент управления Sort, но он может повлиять на производительность сервера, особенно если результирующий набор имеет большой размер.</span><span class="sxs-lookup"><span data-stu-id="d18a0-199">Active Directory supports the sort control, but it can impact server performance, particularly if the results set is large.</span></span> <span data-ttu-id="d18a0-200">Имейте в виду, что Active Directory поддерживает только один ключ сортировки.</span><span class="sxs-lookup"><span data-stu-id="d18a0-200">Be aware that Active Directory supports only a single sort key.</span></span> <span data-ttu-id="d18a0-201">По умолчанию сортировка отсутствует.</span><span class="sxs-lookup"><span data-stu-id="d18a0-201">The default is no sorting.</span></span> |
| <span data-ttu-id="d18a0-202">"Предельное время"</span><span class="sxs-lookup"><span data-stu-id="d18a0-202">"Time Limit"</span></span>        | <span data-ttu-id="d18a0-203">Целочисленное значение, указывающее предельное время в секундах для поиска.</span><span class="sxs-lookup"><span data-stu-id="d18a0-203">An integer value that specifies the time limit, in seconds, for the search.</span></span> <span data-ttu-id="d18a0-204">По достижении предельного времени сервер прекращает поиск и возвращает накопленные результаты.</span><span class="sxs-lookup"><span data-stu-id="d18a0-204">When the time limit is reached, the server stops searching and returns the results accumulated.</span></span> <span data-ttu-id="d18a0-205">Значение по умолчанию — без ограничения по времени.</span><span class="sxs-lookup"><span data-stu-id="d18a0-205">The default is no time limit.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="d18a0-206">Счетчик</span><span class="sxs-lookup"><span data-stu-id="d18a0-206">"Timeout"</span></span>           | <span data-ttu-id="d18a0-207">Целочисленное значение, указывающее значение времени ожидания на стороне клиента в секундах.</span><span class="sxs-lookup"><span data-stu-id="d18a0-207">An integer value that specifies the client-side timeout value, in seconds.</span></span> <span data-ttu-id="d18a0-208">Это значение указывает время ожидания клиентом результатов с сервера перед остановкой поиска.</span><span class="sxs-lookup"><span data-stu-id="d18a0-208">This value indicates the time the client waits for results from the server before stopping the search.</span></span> <span data-ttu-id="d18a0-209">Значение по умолчанию — без времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="d18a0-209">The default is no time-out.</span></span>                                                                                                                                                                                                  |



 

<span data-ttu-id="d18a0-210">В следующем примере кода показано, как задать параметры поиска.</span><span class="sxs-lookup"><span data-stu-id="d18a0-210">The following code example shows how to set search options.</span></span>


```VB
Const ADS_SCOPE_ONELEVEL = 1
Const ADS_CHASE_REFERRALS_EXTERNAL = &H40

Dim Com As New Command
 
Com.Properties("Page Size") = 999
Com.Properties("Timeout") = 30     ' Seconds
Com.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Com.Properties("Chase referrals") = ADS_CHASE_REFERRALS_EXTERNAL
Com.Properties("Cache Results") = False     ' Do not cache the result set.
```



<span data-ttu-id="d18a0-211">Третьим объектом ADO является **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="d18a0-211">The third ADO object is **RecordSet**.</span></span> <span data-ttu-id="d18a0-212">Этот объект получается при вызове метода **EXECUTE** для объекта **Command** .</span><span class="sxs-lookup"><span data-stu-id="d18a0-212">You obtain this object when you invoke the **Execute** method on a **Command** object.</span></span> <span data-ttu-id="d18a0-213">Основной функцией объекта **Recordset** является перечисление результирующего набора и получение данных.</span><span class="sxs-lookup"><span data-stu-id="d18a0-213">The primary function of the **RecordSet** object is to enumerate the result set and obtain the data.</span></span> <span data-ttu-id="d18a0-214">Результирующий набор может содержать значения для атрибутов, имеющих как одно, так и несколько значений.</span><span class="sxs-lookup"><span data-stu-id="d18a0-214">The result set can contain values for attributes that have both single or multiple values.</span></span> <span data-ttu-id="d18a0-215">Получение атрибута с одним значением является простым, аналогично получению значения столбца в реляционной базе данных, например:</span><span class="sxs-lookup"><span data-stu-id="d18a0-215">Getting a single-valued attribute is simple, similar to getting the column value in the relational database, for example:</span></span>


```VB
Fields('name').Value
```



<span data-ttu-id="d18a0-216">Однако получение атрибута с несколькими значениями является более сложной задачей.</span><span class="sxs-lookup"><span data-stu-id="d18a0-216">Getting an attribute with multiple values, however, is more challenging.</span></span> <span data-ttu-id="d18a0-217">В этом случае **поле. Value** является массивом, и необходимо проверить нижнюю и верхнюю границы массива, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="d18a0-217">In this case, the **Field.Value** is an array and you must check the lower and upper bound of the array, as shown in the following code example.</span></span>


```VB
Set rs = Com.Execute
 
For i = 0 To rs.Fields.Count - 1
    Debug.Print rs.Fields(i).Name, rs.Fields(i).Type
Next i
 
'--------------------------
' Navigate the record set.
'--------------------------
rs.MoveFirst
lstResult.Clear      ' Clear the user interface.
While Not rs.EOF
For i = 0 To rs.Fields.Count - 1
    ' For Multi Value attribute
    If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
        Debug.Print rs.Fields(i).Name, " = "
        For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
            Debug.Print rs.Fields(i).Value(j), " # "
            lstResult.AddItem rs.Fields(i).Value(j)
        Next j
    Else
        ' For Single Value attribute.
         Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
         lstResult.AddItem rs.Fields(i).Value
    End If
Next i
rs.MoveNext
Wend
```



<span data-ttu-id="d18a0-218">В следующем примере кода отключаются учетные записи пользователей на сервере LDAP.</span><span class="sxs-lookup"><span data-stu-id="d18a0-218">The following code example disables the user accounts on an LDAP server.</span></span>


```VB
Dim X as IADs
Dim con As New Connection, rs As New Recordset
Dim MyUser As IADsUser
 
con.Provider = "ADsDSOObject"
con.Open "Active Directory Provider", "CN=Test,CN=Users,DC=Fabrikam,DC=COM,O=INTERNET", "Password"
Set rs = con.Execute("<LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com>;(objectClass=User);ADsPath;onelevel")
 
While Not rs.EOF
    ' Bind to the object to make changes 
    ' to it because ADO is currently read-only.
    MyUser = GetObject(rs.Fields(0).Value)
    MyUser.AccountDisabled = True
    MyUser.SetInfo
    rs.MoveNext
Wend
```



<span data-ttu-id="d18a0-219">Дополнительные сведения об объектной модели ADO см. в разделе [Microsoft объекты данных ActiveX](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).</span><span class="sxs-lookup"><span data-stu-id="d18a0-219">For more information about the ADO object model, see [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).</span></span>

 

