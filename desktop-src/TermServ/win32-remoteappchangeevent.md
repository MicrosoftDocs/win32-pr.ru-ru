---
title: Класс Win32_RemoteAppChangeEvent
description: Представляет изменение параметров удаленного рабочего стола Windows Server 2008 R2 на сервере узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).
ms.assetid: 3434ee4e-283e-4147-a73b-c131e8af6c57
ms.tgt_platform: multiple
keywords:
- Класс Win32_RemoteAppChangeEvent службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RemoteAppChangeEvent, описание
topic_type:
- apiref
api_name:
- Win32_RemoteAppChangeEvent
- Win32_RemoteAppChangeEvent.SECURITY_DESCRIPTOR
- Win32_RemoteAppChangeEvent.TIME_CREATED
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5355d057038e97e9f381646134ff6487541f67f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135895"
---
# <a name="win32_remoteappchangeevent-class"></a><span data-ttu-id="0c1ae-105">\_Класс Win32 ремотеаппчанжеевент</span><span class="sxs-lookup"><span data-stu-id="0c1ae-105">Win32\_RemoteAppChangeEvent class</span></span>

<span data-ttu-id="0c1ae-106">Представляет изменение параметров удаленного рабочего стола Windows Server 2008 R2 на сервере узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="0c1ae-106">Represents a change to Windows Server 2008 R2 RemoteApp settings on the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c1ae-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c1ae-107">Syntax</span></span>

``` syntax
class Win32_RemoteAppChangeEvent : ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="0c1ae-108">Члены</span><span class="sxs-lookup"><span data-stu-id="0c1ae-108">Members</span></span>

<span data-ttu-id="0c1ae-109">Класс **Win32 \_ ремотеаппчанжеевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0c1ae-109">The **Win32\_RemoteAppChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="0c1ae-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0c1ae-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0c1ae-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="0c1ae-111">Properties</span></span>

<span data-ttu-id="0c1ae-112">Класс **Win32 \_ ремотеаппчанжеевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0c1ae-112">The **Win32\_RemoteAppChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c1ae-113">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="0c1ae-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c1ae-114">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0c1ae-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="0c1ae-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c1ae-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c1ae-116">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="0c1ae-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="0c1ae-117">Это свойство наследуется от [**\_ \_ события**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="0c1ae-117">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="0c1ae-118">Дополнительные сведения о константах, используемых для задания этого дескриптора безопасности, см. в разделе [константы безопасности WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="0c1ae-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="0c1ae-119">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="0c1ae-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c1ae-120">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0c1ae-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0c1ae-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c1ae-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c1ae-122">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="0c1ae-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="0c1ae-123">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="0c1ae-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="0c1ae-124">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="0c1ae-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="0c1ae-125">Это свойство наследуется от [**\_ \_ события**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="0c1ae-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="0c1ae-126">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0c1ae-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c1ae-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c1ae-127">Remarks</span></span>

<span data-ttu-id="0c1ae-128">Чтобы подключиться к \\ \\ пространству имен root cimv2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="0c1ae-128">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="0c1ae-129">Для вызовов C/C++ это уровень проверки подлинности " **PKT" RPC \_ C \_ AUTHN \_ Level \_ \_**, который можно задать с помощью функции [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) com.</span><span class="sxs-lookup"><span data-stu-id="0c1ae-129">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="0c1ae-130">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="0c1ae-130">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="0c1ae-131">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="0c1ae-131">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="0c1ae-132">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="0c1ae-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0c1ae-133">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="0c1ae-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0c1ae-134">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="0c1ae-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0c1ae-135">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0c1ae-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c1ae-136">Требования</span><span class="sxs-lookup"><span data-stu-id="0c1ae-136">Requirements</span></span>



| <span data-ttu-id="0c1ae-137">Требование</span><span class="sxs-lookup"><span data-stu-id="0c1ae-137">Requirement</span></span> | <span data-ttu-id="0c1ae-138">Значение</span><span class="sxs-lookup"><span data-stu-id="0c1ae-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c1ae-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c1ae-139">Minimum supported client</span></span><br/> | <span data-ttu-id="0c1ae-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0c1ae-140">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0c1ae-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c1ae-141">Minimum supported server</span></span><br/> | <span data-ttu-id="0c1ae-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c1ae-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0c1ae-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0c1ae-143">Namespace</span></span><br/>                | <span data-ttu-id="0c1ae-144">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="0c1ae-144">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0c1ae-145">MOF</span><span class="sxs-lookup"><span data-stu-id="0c1ae-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c1ae-146"><dt>Тсаллов. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c1ae-146"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="0c1ae-147">DLL</span><span class="sxs-lookup"><span data-stu-id="0c1ae-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c1ae-148"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c1ae-148"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

