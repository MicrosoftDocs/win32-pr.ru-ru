---
description: Описание сеанса входа или сеансов, связанных с пользователем, вошедшим в систему на компьютере под Windows.
ms.assetid: d09a115b-95a3-47c7-a04d-c810d044ccc8
ms.tgt_platform: multiple
title: Класс Win32_LogonSession
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSession
- Win32_LogonSession.Caption
- Win32_LogonSession.Description
- Win32_LogonSession.InstallDate
- Win32_LogonSession.Name
- Win32_LogonSession.Status
- Win32_LogonSession.StartTime
- Win32_LogonSession.AuthenticationPackage
- Win32_LogonSession.LogonId
- Win32_LogonSession.LogonType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78e14bbd41c2fd8bb0c10a7bfeeda0dc9d426b0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807138"
---
# <a name="win32_logonsession-class"></a><span data-ttu-id="9b023-103">\_Класс Win32 LogonSession</span><span class="sxs-lookup"><span data-stu-id="9b023-103">Win32\_LogonSession class</span></span>

<span data-ttu-id="9b023-104">Класс **WMI \_ LogonSession для Win32** (см. раздел [Получение класса WMI](/windows/desktop/wmisdk/retrieving-a-class)) описывает сеанс входа в систему или сеансы, связанные с пользовательским компьютером, работающим в системе Windows.</span><span class="sxs-lookup"><span data-stu-id="9b023-104">The **Win32\_LogonSession** WMI class (see [Retrieving a WMI class](/windows/desktop/wmisdk/retrieving-a-class)) describes the logon session or sessions associated with a user logged on to a computer system running Windows.</span></span>

<span data-ttu-id="9b023-105">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="9b023-105">The following syntax is simplified from Managed Object Format (MOF) code, and includes all of the inherited properties.</span></span> <span data-ttu-id="9b023-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="9b023-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b023-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b023-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{9083C21E-7D58-4e0e-BC30-0BC8922AFB8B}"), AMENDMENT]
class Win32_LogonSession : Win32_Session
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime StartTime;
  string   AuthenticationPackage;
  string   LogonId;
  uint32   LogonType;
};
```

## <a name="members"></a><span data-ttu-id="9b023-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9b023-108">Members</span></span>

<span data-ttu-id="9b023-109">Класс **Win32 \_ LogonSession** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9b023-109">The **Win32\_LogonSession** class has these types of members:</span></span>

-   [<span data-ttu-id="9b023-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="9b023-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b023-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="9b023-111">Properties</span></span>

<span data-ttu-id="9b023-112">Класс **Win32 \_ LogonSession** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9b023-112">The **Win32\_LogonSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b023-113">**аусентикатионпаккаже**</span><span class="sxs-lookup"><span data-stu-id="9b023-113">**AuthenticationPackage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b023-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9b023-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b023-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b023-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b023-116">Имя подсистемы, используемой для проверки подлинности сеанса входа в систему.</span><span class="sxs-lookup"><span data-stu-id="9b023-116">Name of the subsystem used to authenticate the logon session.</span></span>

</dd> <dt>

<span data-ttu-id="9b023-117">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="9b023-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b023-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9b023-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b023-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b023-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b023-120">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9b023-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9b023-121">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9b023-121">A short textual description of the object.</span></span>

<span data-ttu-id="9b023-122">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b023-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b023-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9b023-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b023-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9b023-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b023-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b023-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b023-126">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="9b023-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9b023-127">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9b023-127">A textual description of the object.</span></span>

<span data-ttu-id="9b023-128">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b023-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b023-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9b023-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b023-130">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9b023-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9b023-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b023-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b023-132">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="9b023-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9b023-133">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="9b023-133">Indicates when the object was installed.</span></span> <span data-ttu-id="9b023-134">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="9b023-134">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9b023-135">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b023-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b023-136">**логонид**</span><span class="sxs-lookup"><span data-stu-id="9b023-136">**LogonId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b023-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9b023-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b023-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b023-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b023-139">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9b023-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9b023-140">Идентификатор, назначенный сеансу входа в систему.</span><span class="sxs-lookup"><span data-stu-id="9b023-140">ID assigned to the logon session.</span></span>

</dd> <dt>

<span data-ttu-id="9b023-141">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="9b023-141">**LogonType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b023-142">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b023-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b023-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b023-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b023-144">Числовое значение, указывающее тип сеанса входа в систему.</span><span class="sxs-lookup"><span data-stu-id="9b023-144">Numeric value that indicates the type of logon session.</span></span>

<dt>

<span data-ttu-id="9b023-145">0</span><span class="sxs-lookup"><span data-stu-id="9b023-145">0</span></span>
</dt> <dd>

<span data-ttu-id="9b023-146">Используется только системной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="9b023-146">Used only by the System account.</span></span>

</dd> <dt>

<span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>

<span data-ttu-id="9b023-147"><span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>**Интерактивный** (2)</span><span class="sxs-lookup"><span data-stu-id="9b023-147"><span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>**Interactive** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9b023-148">Предназначен для пользователей, работающих на компьютере в интерактивном режиме, например для входа в систему с помощью сервера терминалов, удаленной оболочки или аналогичного процесса.</span><span class="sxs-lookup"><span data-stu-id="9b023-148">Intended for users who are interactively using the machine, such as a user being logged on by a terminal server, remote shell, or similar process.</span></span>

</dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

<span data-ttu-id="9b023-149"><span id="Network"></span><span id="network"></span><span id="NETWORK"></span>**Сеть** (3)</span><span class="sxs-lookup"><span data-stu-id="9b023-149"><span id="Network"></span><span id="network"></span><span id="NETWORK"></span>**Network** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9b023-150">Предназначен для высокопроизводительных серверов для проверки подлинности паролей в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="9b023-150">Intended for high-performance servers to authenticate clear text passwords.</span></span> <span data-ttu-id="9b023-151">LogonUser не кэширует учетные данные для этого типа входа.</span><span class="sxs-lookup"><span data-stu-id="9b023-151">LogonUser does not cache credentials for this logon type.</span></span>

</dd> <dt>

<span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>

<span data-ttu-id="9b023-152"><span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>**Пакетная** службы (4)</span><span class="sxs-lookup"><span data-stu-id="9b023-152"><span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>**Batch** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9b023-153">Предназначен для пакетных серверов, где процессы могут выполняться от имени пользователя без их прямого вмешательства; или для более производительных серверов, которые обрабатывают много одновременных попыток проверки подлинности, таких как почта или веб-серверы.</span><span class="sxs-lookup"><span data-stu-id="9b023-153">Intended for batch servers, where processes can be executed on behalf of a user without their direct intervention; or for higher performance servers that process many clear-text authentication attempts at a time, such as mail or web servers.</span></span> <span data-ttu-id="9b023-154">LogonUser не кэширует учетные данные для этого типа входа.</span><span class="sxs-lookup"><span data-stu-id="9b023-154">LogonUser does not cache credentials for this logon type.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9b023-155"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Служба** (5)</span><span class="sxs-lookup"><span data-stu-id="9b023-155"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9b023-156">Указывает на тип входа в службу.</span><span class="sxs-lookup"><span data-stu-id="9b023-156">Indicates a service-type logon.</span></span> <span data-ttu-id="9b023-157">Предоставленная учетная запись должна иметь права на доступ к службе.</span><span class="sxs-lookup"><span data-stu-id="9b023-157">The account provided must have the service privilege enabled.</span></span>

</dd> <dt>

<span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>

<span data-ttu-id="9b023-158"><span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>**Прокси-сервер** (6)</span><span class="sxs-lookup"><span data-stu-id="9b023-158"><span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>**Proxy** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9b023-159">Указывает на вход типа прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="9b023-159">Indicates a proxy-type logon.</span></span>

</dd> <dt>

<span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>

<span data-ttu-id="9b023-160"><span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>**Разблокировать** (7)</span><span class="sxs-lookup"><span data-stu-id="9b023-160"><span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>**Unlock** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9b023-161">Этот тип входа предназначен для библиотек DLL GINA, выполняющих вход в систему пользователей, работающих на компьютере в интерактивном режиме.</span><span class="sxs-lookup"><span data-stu-id="9b023-161">This logon type is intended for GINA DLLs logging on users who are interactively using the machine.</span></span> <span data-ttu-id="9b023-162">Этот тип входа позволяет формировать уникальную запись аудита, которая показывает, когда Рабочая станция была разблокирована.</span><span class="sxs-lookup"><span data-stu-id="9b023-162">This logon type allows a unique audit record to be generated that shows when the workstation was unlocked.</span></span>

</dd> <dt>

<span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>

<span data-ttu-id="9b023-163"><span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>**Нетворкклеартекст** (8)</span><span class="sxs-lookup"><span data-stu-id="9b023-163"><span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>**NetworkCleartext** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9b023-164">Сохраняет имя и пароль в пакетах проверки подлинности, позволяя серверу выполнять подключения к другим сетевым серверам при олицетворении клиента.</span><span class="sxs-lookup"><span data-stu-id="9b023-164">Preserves the name and password in the authentication packages, allowing the server to make connections to other network servers while impersonating the client.</span></span> <span data-ttu-id="9b023-165">Это позволяет серверу принимать учетные данные от клиента с открытым текстом, вызывать метод LogonUser, проверять, что пользователь может получить доступ к системе по сети и по-прежнему взаимодействовать с другими серверами.</span><span class="sxs-lookup"><span data-stu-id="9b023-165">This allows a server to accept clear text credentials from a client, call LogonUser, verify that the user can access the system across the network, and still communicate with other servers.</span></span>

</dd> <dt>

<span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>

<span data-ttu-id="9b023-166"><span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>**Невкредентиалс** (9)</span><span class="sxs-lookup"><span data-stu-id="9b023-166"><span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>**NewCredentials** (9)</span></span>


</dt> <dd>

<span data-ttu-id="9b023-167">Позволяет вызывающему объекту клонировать текущий маркер и указывать новые учетные данные для исходящих соединений.</span><span class="sxs-lookup"><span data-stu-id="9b023-167">Allows the caller to clone its current token and specify new credentials for outbound connections.</span></span> <span data-ttu-id="9b023-168">Новый сеанс входа в систему имеет то же локальное указание, но использует другие учетные данные для других сетевых подключений.</span><span class="sxs-lookup"><span data-stu-id="9b023-168">The new logon session has the same local identify, but uses different credentials for other network connections.</span></span>

</dd> <dt>

<span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>

<span data-ttu-id="9b023-169"><span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>**Ремотеинтерактиве** (10)</span><span class="sxs-lookup"><span data-stu-id="9b023-169"><span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>**RemoteInteractive** (10)</span></span>


</dt> <dd>

<span data-ttu-id="9b023-170">Сеанс служб терминалов, который является удаленным и интерактивным.</span><span class="sxs-lookup"><span data-stu-id="9b023-170">Terminal Services session that is both remote and interactive.</span></span>

</dd> <dt>

<span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>

<span data-ttu-id="9b023-171"><span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>**Качединтерактиве** (11)</span><span class="sxs-lookup"><span data-stu-id="9b023-171"><span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>**CachedInteractive** (11)</span></span>


</dt> <dd>

<span data-ttu-id="9b023-172">Попытайтесь выполнить кэшированные учетные данные без доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="9b023-172">Attempt cached credentials without accessing the network.</span></span>

</dd> <dt>

<span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>

<span data-ttu-id="9b023-173"><span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>**Качедремотеинтерактиве** (12)</span><span class="sxs-lookup"><span data-stu-id="9b023-173"><span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>**CachedRemoteInteractive** (12)</span></span>


</dt> <dd>

<span data-ttu-id="9b023-174">То же, что и Ремотеинтерактиве.</span><span class="sxs-lookup"><span data-stu-id="9b023-174">Same as RemoteInteractive.</span></span> <span data-ttu-id="9b023-175">Используется для внутреннего аудита.</span><span class="sxs-lookup"><span data-stu-id="9b023-175">This is used for internal auditing.</span></span>

</dd> <dt>

<span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>

<span data-ttu-id="9b023-176"><span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>**Качедунлокк** (13)</span><span class="sxs-lookup"><span data-stu-id="9b023-176"><span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>**CachedUnlock** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9b023-177">Вход в рабочую станцию.</span><span class="sxs-lookup"><span data-stu-id="9b023-177">Workstation logon.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9b023-178">**Name**</span><span class="sxs-lookup"><span data-stu-id="9b023-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b023-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9b023-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b023-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b023-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b023-181">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="9b023-181">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9b023-182">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="9b023-182">Label by which the object is known.</span></span> <span data-ttu-id="9b023-183">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="9b023-183">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9b023-184">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b023-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b023-185">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="9b023-185">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b023-186">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9b023-186">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9b023-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b023-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b023-188">Время начала сеанса.</span><span class="sxs-lookup"><span data-stu-id="9b023-188">Time at which the session started.</span></span>

<span data-ttu-id="9b023-189">Это свойство наследуется [**из \_ сеанса Win32**](win32-session.md).</span><span class="sxs-lookup"><span data-stu-id="9b023-189">This property is inherited from [**Win32\_Session**](win32-session.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b023-190">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="9b023-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b023-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9b023-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b023-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b023-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b023-193">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="9b023-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9b023-194">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="9b023-194">String that indicates the current status of the object.</span></span> <span data-ttu-id="9b023-195">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="9b023-195">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="9b023-196">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="9b023-196">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="9b023-197">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="9b023-197">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="9b023-198">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="9b023-198">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9b023-199">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="9b023-199">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9b023-200">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="9b023-200">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9b023-201">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b023-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9b023-202">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="9b023-202">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9b023-203">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="9b023-203">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9b023-204">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="9b023-204">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9b023-205">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="9b023-205">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b023-206">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="9b023-206">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9b023-207">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="9b023-207">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9b023-208">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="9b023-208">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9b023-209">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="9b023-209">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9b023-210">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="9b023-210">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9b023-211">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="9b023-211">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9b023-212">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="9b023-212">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9b023-213">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="9b023-213">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9b023-214">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="9b023-214">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="9b023-215"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9b023-215"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="examples"></a><span data-ttu-id="9b023-216">Примеры</span><span class="sxs-lookup"><span data-stu-id="9b023-216">Examples</span></span>

<span data-ttu-id="9b023-217">Образец PowerShell [сведения о сеансе входа в систему](https://Gallery.TechNet.Microsoft.Com/scriptcenter/64cc7ab5-f1cd-460c-9d37-e6f989444de3) возвращает сведения о сеансах входа, связанных с пользователем, который в данный момент вошел в систему на компьютере.</span><span class="sxs-lookup"><span data-stu-id="9b023-217">The [List Logon Session Information](https://Gallery.TechNet.Microsoft.Com/scriptcenter/64cc7ab5-f1cd-460c-9d37-e6f989444de3) PowerShell sample returns information about logon sessions associated with the user currently logged on to a computer.</span></span>

<span data-ttu-id="9b023-218">Следующий пример PowerShell проверяет, открыт ли удаленный сеанс для указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="9b023-218">The following PowerShell example checks for remote session open for a specified user.</span></span>


```PowerShell
$user = "<user name>"
$servers = gci servers.txt 

     foreach ($server in $servers){
     $logons = gwmi win32_loggedonuser -computername $server

          foreach ($logon in $logons){
               if ($logon.antecedent -match $user){
               $logonid = $logon.dependent.split("=")[1] 
               $session =gwmi win32_logonsession |? {$_.logonid -match $logonid}
               if ($session.logontype -eq "10"){
               Write-host "You have an active Terminal Server session on server $($server)"
                }
          }
```



## <a name="requirements"></a><span data-ttu-id="9b023-219">Требования</span><span class="sxs-lookup"><span data-stu-id="9b023-219">Requirements</span></span>



| <span data-ttu-id="9b023-220">Требование</span><span class="sxs-lookup"><span data-stu-id="9b023-220">Requirement</span></span> | <span data-ttu-id="9b023-221">Значение</span><span class="sxs-lookup"><span data-stu-id="9b023-221">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b023-222">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b023-222">Minimum supported client</span></span><br/> | <span data-ttu-id="9b023-223">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b023-223">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b023-224">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b023-224">Minimum supported server</span></span><br/> | <span data-ttu-id="9b023-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b023-225">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b023-226">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9b023-226">Namespace</span></span><br/>                | <span data-ttu-id="9b023-227">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9b023-227">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9b023-228">MOF</span><span class="sxs-lookup"><span data-stu-id="9b023-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b023-229"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b023-229"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b023-230">DLL</span><span class="sxs-lookup"><span data-stu-id="9b023-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b023-231"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b023-231"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b023-232">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b023-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b023-233">**\_Сеанс Win32**</span><span class="sxs-lookup"><span data-stu-id="9b023-233">**Win32\_Session**</span></span>](win32-session.md)
</dt> <dt>

<span data-ttu-id="9b023-234">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9b023-234">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

