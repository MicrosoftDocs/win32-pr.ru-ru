---
title: Поиск систем узлов сервера
description: Поиск систем узлов сервера с помощью строковых привязок и запрос к базе данных службы имен для расположения серверной программы.
ms.assetid: 4aadda88-2109-481f-aa4b-b1983d81dec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2357fcafa35d4f64cfb4f6841c0b56e1e94b7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888535"
---
# <a name="finding-server-host-systems"></a><span data-ttu-id="5f20f-103">Поиск систем узлов сервера</span><span class="sxs-lookup"><span data-stu-id="5f20f-103">Finding Server Host Systems</span></span>

<span data-ttu-id="5f20f-104">Хост-система сервера — это компьютер, на котором выполняется серверная программа распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="5f20f-104">A server host system is the computer that executes the distributed application's server program.</span></span> <span data-ttu-id="5f20f-105">В сети может быть одна или несколько серверных систем размещения.</span><span class="sxs-lookup"><span data-stu-id="5f20f-105">There may be one or many server host systems on a network.</span></span> <span data-ttu-id="5f20f-106">Способ обнаружения сервера для подключения клиентской программой зависит от потребностей программы.</span><span class="sxs-lookup"><span data-stu-id="5f20f-106">How your client program finds a server to connect to depends on the needs of your program.</span></span>

<span data-ttu-id="5f20f-107">Существует два способа поиска систем размещения сервера:</span><span class="sxs-lookup"><span data-stu-id="5f20f-107">There are two methods of finding server host systems:</span></span>

-   <span data-ttu-id="5f20f-108">Использование сведений, хранящихся в строках исходного кода клиента, переменных среды или файлов конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="5f20f-108">Using information stored in strings in the client source code, environment variables, or application-specific configuration files.</span></span> <span data-ttu-id="5f20f-109">Клиентское приложение может использовать данные в строке для создания привязки между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="5f20f-109">Your client application can use the data in the string to compose a binding between the client and the server.</span></span>
-   <span data-ttu-id="5f20f-110">Запрос к базе данных службы имен для расположения серверной программы.</span><span class="sxs-lookup"><span data-stu-id="5f20f-110">Querying a name service database for the location of a server program.</span></span>

<span data-ttu-id="5f20f-111">В этом разделе представлены сведения об этих методах в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="5f20f-111">This section presents information on both of these techniques in the following topics:</span></span>

-   [<span data-ttu-id="5f20f-112">Использование строковых привязок</span><span class="sxs-lookup"><span data-stu-id="5f20f-112">Using String Bindings</span></span>](#using-string-bindings)
-   [<span data-ttu-id="5f20f-113">Импорт из баз данных службы имен</span><span class="sxs-lookup"><span data-stu-id="5f20f-113">Importing from Name Service Databases</span></span>](#importing-from-name-service-databases)

## <a name="using-string-bindings"></a><span data-ttu-id="5f20f-114">Использование строковых привязок</span><span class="sxs-lookup"><span data-stu-id="5f20f-114">Using String Bindings</span></span>

<span data-ttu-id="5f20f-115">Приложения могут создавать привязки из информации, хранящейся в строках.</span><span class="sxs-lookup"><span data-stu-id="5f20f-115">Applications can create bindings from information stored in strings.</span></span> <span data-ttu-id="5f20f-116">Клиентское приложение формирует эти сведения в виде строки, а затем вызывает функцию [**рпкбиндингфромстрингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) .</span><span class="sxs-lookup"><span data-stu-id="5f20f-116">Your client application composes this information as a string, then calls the [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) function.</span></span> <span data-ttu-id="5f20f-117">Для обнаружения сервера клиент должен предоставить следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="5f20f-117">The client must supply the following information to identify the server:</span></span>

-   <span data-ttu-id="5f20f-118">Имя интерфейса, глобальный уникальный идентификатор (GUID) объекта или UUID объекта.</span><span class="sxs-lookup"><span data-stu-id="5f20f-118">The interface name, the globally unique identifier (GUID) of the object, or UUID of the object.</span></span> <span data-ttu-id="5f20f-119">Дополнительные сведения см. в разделе [создание идентификаторов UUID интерфейса](generating-interface-uuids.md) и [строкового UUID](string-uuid.md).</span><span class="sxs-lookup"><span data-stu-id="5f20f-119">For more information, see [Generating Interface UUIDs](generating-interface-uuids.md) and [String UUID](string-uuid.md).</span></span>
-   <span data-ttu-id="5f20f-120">Тип транспорта для взаимодействия, например именованные каналы или TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="5f20f-120">The transport type to communicate over, such as named pipes or TCP/IP.</span></span> <span data-ttu-id="5f20f-121">Дополнительные сведения см. в разделе [Основная терминология привязки RPC](essential-rpc-binding-terminology.md) и [Выбор последовательности протокола](selecting-a-protocol-sequence.md).</span><span class="sxs-lookup"><span data-stu-id="5f20f-121">For details, see [Essential RPC Binding Terminology](essential-rpc-binding-terminology.md) and [Selecting a Protocol Sequence](selecting-a-protocol-sequence.md).</span></span>
-   <span data-ttu-id="5f20f-122">Сетевой адрес или имя главного компьютера сервера.</span><span class="sxs-lookup"><span data-stu-id="5f20f-122">The network address or the name of the server host computer.</span></span>
-   <span data-ttu-id="5f20f-123">Конечная точка серверной программы на главном компьютере сервера.</span><span class="sxs-lookup"><span data-stu-id="5f20f-123">The endpoint of the server program on the server host computer.</span></span> <span data-ttu-id="5f20f-124">Дополнительные сведения см. в разделе [Поиск конечных точек](finding-endpoints.md)и [Указание конечных точек](specifying-endpoints.md).</span><span class="sxs-lookup"><span data-stu-id="5f20f-124">For more information, see [Finding Endpoints](finding-endpoints.md), and [Specifying Endpoints](specifying-endpoints.md).</span></span>

<span data-ttu-id="5f20f-125">(Идентификатор объекта и сведения о конечной точке являются необязательными.)</span><span class="sxs-lookup"><span data-stu-id="5f20f-125">(The object UUID and the endpoint information are optional.)</span></span>

<span data-ttu-id="5f20f-126">В следующих примерах параметр *псзнетворкаддресс* и другие параметры включают в себя встроенные символы обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="5f20f-126">In the following examples, the *pszNetworkAddress* parameter and other parameters include embedded backslashes.</span></span> <span data-ttu-id="5f20f-127">Обратная косая черта — это escape-символ в языке программирования C.</span><span class="sxs-lookup"><span data-stu-id="5f20f-127">The backslash is an escape character in the C programming language.</span></span> <span data-ttu-id="5f20f-128">Две обратные косые черты необходимы для представления каждого отдельного символа обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="5f20f-128">Two backslashes are needed to represent each single literal backslash character.</span></span> <span data-ttu-id="5f20f-129">Структура строковой привязки должна содержать четыре символа обратной косой черты, представляющие два литерала обратной косой черты, предшествующие имени сервера.</span><span class="sxs-lookup"><span data-stu-id="5f20f-129">The string-binding structure must contain four backslash characters to represent the two literal backslash characters that precede the server name.</span></span>

<span data-ttu-id="5f20f-130">В следующем примере показано, что перед именем сервера должны стоять восемь обратных косых черт, чтобы в структуре данных привязки строк отображались четыре литеральных символа обратной косой черты после того, как функция **sprintf \_ s** обработает строку.</span><span class="sxs-lookup"><span data-stu-id="5f20f-130">The following example shows that the server name must be preceded by eight backslashes so that four literal backslash characters will appear in the string-binding data structure after the **sprintf\_s** function processes the string.</span></span>


```C++
/* client application */

char * pszUuid = "6B29FC40-CA47-1067-B31D-00DD010662DA";
char * pszProtocol = "ncacn_np";
char * pszNetworkAddress = "\\\\\\\\servername";
char * pszEndpoint = "\\\\pipe\\\\pipename";
char * pszString;
 
int len = 0;
 
len  = sprintf_s(pszString, strlen(pszUuid), "%s", pszUuid);
len += sprintf_s(pszString + len, strlen(pszProtocolSequence) + 2, "@%s:",
    pszProtocolSequence);
if (pszNetworkAddress != NULL)
    len += sprintf_s(pszString + len, strlen(pszNetworkAddress), "%s",
    pszNetworkAddress);
len += sprintf_s(pszString + len, strlen(pszEndpoint) + 2, "[%s]", pszEndpoint);
```



<span data-ttu-id="5f20f-131">В следующем примере строковая привязка выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5f20f-131">In the following example, the string binding appears as:</span></span>

<span data-ttu-id="5f20f-132">6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_NP: \\ \\ \\ \\ *имя_сервера* \[ \\ \\ pipe \\ \\ *pipeName*\]</span><span class="sxs-lookup"><span data-stu-id="5f20f-132">6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_np:\\\\\\\\*servername*\[\\\\pipe\\\\*pipename*\]</span></span>

<span data-ttu-id="5f20f-133">Затем клиент вызывает [**рпкбиндингфромстрингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) для получения маркера привязки:</span><span class="sxs-lookup"><span data-stu-id="5f20f-133">The client then calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to obtain the binding handle:</span></span>


```C++
RPC_BINDING_HANDLE hBinding;
 
status = RpcBindingFromStringBinding(pszString, &hBinding);
//...
```



<span data-ttu-id="5f20f-134">Для удобства работы [**рпкстрингбиндингкомпосе**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) собирает идентификатор объекта, последовательность протокола, сетевой адрес и конечную точку в правильном синтаксисе для вызова [**рпкбиндингфромстрингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).</span><span class="sxs-lookup"><span data-stu-id="5f20f-134">A convenience function, [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) assembles the object UUID, protocol sequence, network address, and endpoint in the correct syntax for the call to [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).</span></span> <span data-ttu-id="5f20f-135">Не нужно беспокоиться о размещении амперсанда, двоеточия и различных компонентов для каждой последовательности протоколов в нужном месте; Вы просто предоставляете строки в качестве параметров функции.</span><span class="sxs-lookup"><span data-stu-id="5f20f-135">You do not have to worry about putting the ampersand, colon, and the various components for each protocol sequence in the right place; you just supply the strings as parameters to the function.</span></span> <span data-ttu-id="5f20f-136">Библиотека времени выполнения даже выделяет память, необходимую для привязки строк.</span><span class="sxs-lookup"><span data-stu-id="5f20f-136">The run-time library even allocates the memory needed for the string binding.</span></span>


```C++
char * pszNetworkAddress = "\\\\server";
char * pszEndpoint = "\\pipe\\pipename";
status = RpcStringBindingCompose(
            pszUuid,
            pszProtocolSequence,
            pszNetworkAddress,
            pszEndpoint,
            pszOptions,
            &pszString);
//...
status = RpcBindingFromStringBinding(
            pszString,
            &hBinding);
//...
```



<span data-ttu-id="5f20f-137">Другая удобная функция, [**рпкбиндингтострингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), принимает в качестве входных данных обработчик привязки и создает соответствующую строковую привязку.</span><span class="sxs-lookup"><span data-stu-id="5f20f-137">Another convenience function, [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), takes a binding handle as input and produces the corresponding string binding.</span></span>

## <a name="importing-from-name-service-databases"></a><span data-ttu-id="5f20f-138">Импорт из баз данных службы имен</span><span class="sxs-lookup"><span data-stu-id="5f20f-138">Importing from Name Service Databases</span></span>

<span data-ttu-id="5f20f-139">Службы Name databases сохраняют, помимо прочего, дескрипторы привязки и UUID.</span><span class="sxs-lookup"><span data-stu-id="5f20f-139">Name service databases store, among other things, binding handles and UUIDs.</span></span> <span data-ttu-id="5f20f-140">Клиентское приложение может выполнять поиск одного или обоих элементов, когда требуется выполнить привязку к серверу.</span><span class="sxs-lookup"><span data-stu-id="5f20f-140">Your client application can search for either or both of these when it needs to bind to the server.</span></span> <span data-ttu-id="5f20f-141">Описание сведений, хранимых службой имен, и формата хранения см. в разделе [база данных службы имен RPC](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="5f20f-141">For a discussion of the information that a name service stores, and the storage format, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

<span data-ttu-id="5f20f-142">Библиотека RPC предоставляет два набора функций, которые клиентская программа может использовать для поиска в базе данных службы имен.</span><span class="sxs-lookup"><span data-stu-id="5f20f-142">The RPC library provides two sets of functions that your client program can use to search the name service database.</span></span> <span data-ttu-id="5f20f-143">Имена одного набора начинаются с Рпкнсбиндингимпорт.</span><span class="sxs-lookup"><span data-stu-id="5f20f-143">The names of one set begin with RpcNsBindingImport.</span></span> <span data-ttu-id="5f20f-144">Имена других наборов начинаются с Рпкнсбиндинглукуп.</span><span class="sxs-lookup"><span data-stu-id="5f20f-144">The names of the other set begin with RpcNsBindingLookup.</span></span> <span data-ttu-id="5f20f-145">Различие между двумя группами функций заключается в том, что функции Рпкнсбиндингимпорт возвращают один дескриптор привязки на вызов, а функции Рпкнсбиндинглукуп возвращают группы дескрипторов на вызов.</span><span class="sxs-lookup"><span data-stu-id="5f20f-145">The difference between the two groups of functions is that the RpcNsBindingImport functions return a single binding handle per call and the RpcNsBindingLookup functions return groups of handles per call.</span></span>

<span data-ttu-id="5f20f-146">Чтобы начать поиск с помощью функций Рпкнсбиндингимпорт, сначала вызовите [**рпкнсбиндингимпортбегин**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="5f20f-146">To begin a search with the RpcNsBindingImport functions, first call [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), as shown in the following code fragment.</span></span>


```C++
RPC_STATUS status;
RPC_NS_HANDLE hNameServiceHandle;
 
status = RpcNsBindingImportBegin(
    RPC_C_NS_SYNTAX_DEFAULT,
    NULL,
    MyInterface_v1_0_c_ifspec,
    NULL,
    &hNameServiceHandle);
```



<span data-ttu-id="5f20f-147">Когда функции RPC выполняют поиск в базе данных службы имен, им нужно место для начала поиска.</span><span class="sxs-lookup"><span data-stu-id="5f20f-147">When the RPC functions search the name service database, they need a place to begin the search.</span></span> <span data-ttu-id="5f20f-148">В терминологии RPC это имя записи называется.</span><span class="sxs-lookup"><span data-stu-id="5f20f-148">In RPC terminology, this is called the entry name.</span></span> <span data-ttu-id="5f20f-149">Клиентская программа передает имя записи в качестве второго параметра в [**рпкнсбиндингимпортбегин**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span><span class="sxs-lookup"><span data-stu-id="5f20f-149">Your client program passes the entry name as the second parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="5f20f-150">Этот параметр может иметь **значение NULL** , если требуется выполнить поиск по всей базе данных службы имен.</span><span class="sxs-lookup"><span data-stu-id="5f20f-150">This parameter can be **NULL** if you want to search the entire name service database.</span></span> <span data-ttu-id="5f20f-151">Кроме того, можно выполнить поиск записи на сервере, передав имя записи сервера или выполнив поиск в записи группы, передав имя записи группы.</span><span class="sxs-lookup"><span data-stu-id="5f20f-151">Alternatively, you can search the server entry by passing a server-entry name or search the group entry by passing a group-entry name.</span></span> <span data-ttu-id="5f20f-152">Если передать имя записи, поиск будет ограничен содержимым этой записи.</span><span class="sxs-lookup"><span data-stu-id="5f20f-152">Passing an entry name restricts the search to the contents of that entry.</span></span>

<span data-ttu-id="5f20f-153">В приведенном выше примере значение \_ \_ \_ по умолчанию для синтаксиса RPC C NS \_ передается в качестве первого параметра в [**рпкнсбиндингимпортбегин**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span><span class="sxs-lookup"><span data-stu-id="5f20f-153">In the preceding example, the value RPC\_C\_NS\_SYNTAX\_DEFAULT is passed as the first parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="5f20f-154">При этом выбирается синтаксис имени записи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5f20f-154">This selects the default entry name syntax.</span></span> <span data-ttu-id="5f20f-155">В настоящее время это единственный поддерживаемый синтаксис имени входа.</span><span class="sxs-lookup"><span data-stu-id="5f20f-155">Currently, this is the only supported entry-name syntax.</span></span>

<span data-ttu-id="5f20f-156">Клиентское приложение может искать в базе данных службы имен имя интерфейса, UUID или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="5f20f-156">Your client application can search the name service database for an interface name, a UUID, or both.</span></span> <span data-ttu-id="5f20f-157">Если требуется, чтобы он выполнял поиск интерфейса по имени, передайте глобальную переменную интерфейса, созданную компилятором MIDL, из IDL-файла в качестве третьего параметра в [**рпкнсбиндингимпортбегин**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span><span class="sxs-lookup"><span data-stu-id="5f20f-157">If you want to have it search for an interface by name, pass the global interface variable that the MIDL compiler generates from your IDL file as the third parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="5f20f-158">Его объявление можно найти в файле заголовка, созданном компилятором MIDL при создании клиентской заглушки.</span><span class="sxs-lookup"><span data-stu-id="5f20f-158">You'll find its declaration in the header file that the MIDL compiler generated when it generated the client stub.</span></span> <span data-ttu-id="5f20f-159">Если требуется, чтобы клиентская программа была искать только по UUID, установите для третьего параметра **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5f20f-159">If you want your client program to search by UUID only, set the third parameter to **NULL**.</span></span>

<span data-ttu-id="5f20f-160">При поиске идентификатора UUID в базе данных службы имен установите четвертый параметр [**рпкнсбиндингимпортбегин**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) на UUID, который требуется найти.</span><span class="sxs-lookup"><span data-stu-id="5f20f-160">When searching the name service database for a UUID, set the fourth parameter of [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) to the UUID that you want to search for.</span></span> <span data-ttu-id="5f20f-161">Если вы не ищете UUID, присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5f20f-161">If you are not searching for a UUID, set this parameter to **NULL**.</span></span>

<span data-ttu-id="5f20f-162">Функция [**рпкнсбиндингимпортбегин**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) передает адрес службы имен — обработчик контекста поиска через его пятый параметр.</span><span class="sxs-lookup"><span data-stu-id="5f20f-162">The [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) function passes the address of a name service–search context handle through its fifth parameter.</span></span> <span data-ttu-id="5f20f-163">Этот параметр передается другим функциям Рпкнсбиндингимпорт.</span><span class="sxs-lookup"><span data-stu-id="5f20f-163">You pass this parameter to other RpcNsBindingImport functions.</span></span>

<span data-ttu-id="5f20f-164">В частности, следующая функция, которой будет вызываться клиентское приложение, — это [**рпкнсбиндингимпортнекст**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span><span class="sxs-lookup"><span data-stu-id="5f20f-164">In particular, the next function your client application would call is [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span></span> <span data-ttu-id="5f20f-165">Клиентские программы используют эту функцию для получения совместимых дескрипторов привязки из базы данных службы имен.</span><span class="sxs-lookup"><span data-stu-id="5f20f-165">Client programs use this function to retrieve compatible binding handles from the name service database.</span></span> <span data-ttu-id="5f20f-166">В следующем фрагменте кода показано, как можно вызвать эту функцию:</span><span class="sxs-lookup"><span data-stu-id="5f20f-166">The following code fragment demonstrates how this function might be called:</span></span>


```C++
RPC_STATUS status;
RPC_BINDING_HANDLE hBindingHandle;
// The variable hNameServiceHandle is a valid name service search 
// context handle obtained from the RpcNsBindingBegin function.
 
status = RpcNsBindingImportNext(hNameServiceHandle, &hBindingHandle);
```



<span data-ttu-id="5f20f-167">После вызова функции [**рпкнсбиндингимпортнекст**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) для получения маркера привязки клиентское приложение может определить, приемлем ли полученный обработчик.</span><span class="sxs-lookup"><span data-stu-id="5f20f-167">Once it has called the [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) function to obtain a binding handle, your client application can determine if the handle it received is acceptable.</span></span> <span data-ttu-id="5f20f-168">В противном случае клиентская программа может выполнить цикл и вызвать **рпкнсбиндингимпортнекст** еще раз, чтобы узнать, содержит ли служба имен более подходящий обработчик.</span><span class="sxs-lookup"><span data-stu-id="5f20f-168">If not, your client program can execute a loop and call **RpcNsBindingImportNext** again to see if the name service contains a more appropriate handle.</span></span> <span data-ttu-id="5f20f-169">Для каждого вызова **рпкнсбиндингимпортнекст** должен быть соответствующий вызов рпкнсбиндингфри.</span><span class="sxs-lookup"><span data-stu-id="5f20f-169">For each call to **RpcNsBindingImportNext**, there must be a corresponding call to RpcNsBindingFree.</span></span> <span data-ttu-id="5f20f-170">По завершении поиска вызовите функцию [**рпкнсбиндингимпортдоне**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) , чтобы освободить контекст поиска.</span><span class="sxs-lookup"><span data-stu-id="5f20f-170">When your search is complete, call the [**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) function to free the lookup context.</span></span>

<span data-ttu-id="5f20f-171">После того как у клиентского приложения будет приемлемый маркер привязки, он должен проверить, что серверное приложение работает.</span><span class="sxs-lookup"><span data-stu-id="5f20f-171">After your client application has an acceptable binding handle, it should check to ensure that the server application is running.</span></span> <span data-ttu-id="5f20f-172">Для выполнения этой проверки клиент может использовать два метода.</span><span class="sxs-lookup"><span data-stu-id="5f20f-172">There are two methods your client can use to perform this verification.</span></span> <span data-ttu-id="5f20f-173">Первый — вызов функции в клиентском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="5f20f-173">The first is to call a function in the client interface.</span></span> <span data-ttu-id="5f20f-174">Если серверная программа запущена, вызов будет завершен.</span><span class="sxs-lookup"><span data-stu-id="5f20f-174">If the server program is running, the call will complete.</span></span> <span data-ttu-id="5f20f-175">В противном случае вызов завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5f20f-175">If not, the call will fail.</span></span> <span data-ttu-id="5f20f-176">Лучший способ убедиться, что сервер работает, — вызвать [**рпцепресолвебиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), а затем вызвать [**рпкмгмтиссерверлистенинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening).</span><span class="sxs-lookup"><span data-stu-id="5f20f-176">A better way to verify that the server is running is to invoke [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), followed by a call to [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening).</span></span> <span data-ttu-id="5f20f-177">Дополнительные сведения о базе данных службы имен см. [в разделе База данных службы имен RPC](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="5f20f-177">For more information on the name service database, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

 

 




