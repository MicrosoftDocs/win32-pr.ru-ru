---
title: Класс Win32_TSPublishedApplicationList
description: Представляет список программ, которые находятся в списке программы RemoteApp на сервере узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).
ms.assetid: 3dbefe54-8c31-439f-a87a-5148214a07d5
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSPublishedApplicationList службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSPublishedApplicationList, описание
topic_type:
- apiref
api_name:
- Win32_TSPublishedApplicationList
- Win32_TSPublishedApplicationList.Caption
- Win32_TSPublishedApplicationList.Description
- Win32_TSPublishedApplicationList.InstallDate
- Win32_TSPublishedApplicationList.Name
- Win32_TSPublishedApplicationList.Status
- Win32_TSPublishedApplicationList.Disabled
- Win32_TSPublishedApplicationList.PolicySourceDisabled
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1f87a87dc6f95bcdb33c7dbd1364ad6b3114ddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071491"
---
# <a name="win32_tspublishedapplicationlist-class"></a><span data-ttu-id="b0e6a-105">\_Класс Win32 тспублишедаппликатионлист</span><span class="sxs-lookup"><span data-stu-id="b0e6a-105">Win32\_TSPublishedApplicationList class</span></span>

<span data-ttu-id="b0e6a-106">Представляет список программ, которые находятся в списке программы RemoteApp на сервере узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="b0e6a-106">Represents the list of programs that are in the RemoteApp Programs list on a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0e6a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0e6a-107">Syntax</span></span>

``` syntax
class Win32_TSPublishedApplicationList : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  Disabled;
  uint32   PolicySourceDisabled;
};
```

## <a name="members"></a><span data-ttu-id="b0e6a-108">Члены</span><span class="sxs-lookup"><span data-stu-id="b0e6a-108">Members</span></span>

<span data-ttu-id="b0e6a-109">Класс **Win32 \_ тспублишедаппликатионлист** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b0e6a-109">The **Win32\_TSPublishedApplicationList** class has these types of members:</span></span>

-   [<span data-ttu-id="b0e6a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="b0e6a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b0e6a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b0e6a-111">Properties</span></span>

<span data-ttu-id="b0e6a-112">Класс **Win32 \_ тспублишедаппликатионлист** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-112">The **Win32\_TSPublishedApplicationList** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0e6a-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="b0e6a-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0e6a-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b0e6a-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0e6a-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0e6a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0e6a-116">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b0e6a-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b0e6a-117">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-117">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="b0e6a-118">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b0e6a-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0e6a-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b0e6a-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0e6a-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b0e6a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0e6a-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0e6a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0e6a-122">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-122">Description of the object.</span></span>

<span data-ttu-id="b0e6a-123">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b0e6a-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0e6a-124">**Отключено**</span><span class="sxs-lookup"><span data-stu-id="b0e6a-124">**Disabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0e6a-125">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b0e6a-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0e6a-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b0e6a-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b0e6a-127">Указывает, ограничивают ли сервер узла сеансов удаленных рабочих столов программы, которые пользователь может запускать при начальном подключении к программам из списка программ RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-127">Indicates whether the RD Session Host server restricts the programs that a user can start on initial connection to the programs that are in the RemoteApp Programs list.</span></span>

</dd> <dt>

<span data-ttu-id="b0e6a-128">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b0e6a-128">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0e6a-129">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b0e6a-129">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b0e6a-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0e6a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0e6a-131">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="b0e6a-131">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="b0e6a-132">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-132">The date the object was installed.</span></span> <span data-ttu-id="b0e6a-133">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-133">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b0e6a-134">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b0e6a-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0e6a-135">**Name**</span><span class="sxs-lookup"><span data-stu-id="b0e6a-135">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0e6a-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b0e6a-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0e6a-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0e6a-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0e6a-138">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-138">The name of the object.</span></span>

<span data-ttu-id="b0e6a-139">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b0e6a-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0e6a-140">**полицисаурцедисаблед**</span><span class="sxs-lookup"><span data-stu-id="b0e6a-140">**PolicySourceDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0e6a-141">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0e6a-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0e6a-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0e6a-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0e6a-143">Указывает, где настроено **отключенное** свойство.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-143">Indicates where the **Disabled** property is configured.</span></span> <span data-ttu-id="b0e6a-144">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="b0e6a-144">Possible values include:</span></span>

<dt>

<span data-ttu-id="b0e6a-145">0</span><span class="sxs-lookup"><span data-stu-id="b0e6a-145">0</span></span>
</dt> <dd>

<span data-ttu-id="b0e6a-146">Этот параметр настраивается на сервере с помощью диспетчер удаленных приложений RemoteApp или поставщика WMI RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-146">The setting is configured on the server through RemoteApp Manager or the RemoteApp WMI provider.</span></span>

</dd> <dt>

<span data-ttu-id="b0e6a-147">1</span><span class="sxs-lookup"><span data-stu-id="b0e6a-147">1</span></span>
</dt> <dd>

<span data-ttu-id="b0e6a-148">Этот параметр настраивается с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-148">The setting is configured through group policy.</span></span>

</dd> <dt>

<span data-ttu-id="b0e6a-149">2</span><span class="sxs-lookup"><span data-stu-id="b0e6a-149">2</span></span>
</dt> <dd>

<span data-ttu-id="b0e6a-150">Параметр не настроен.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-150">The setting is not configured.</span></span> <span data-ttu-id="b0e6a-151">Значение по умолчанию **false** используется для свойства **disabled** .</span><span class="sxs-lookup"><span data-stu-id="b0e6a-151">The default value of **FALSE** is used for the **Disabled** property.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b0e6a-152">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="b0e6a-152">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0e6a-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b0e6a-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0e6a-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0e6a-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0e6a-155">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="b0e6a-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="b0e6a-156">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-156">Current status of the object.</span></span> <span data-ttu-id="b0e6a-157">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-157">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b0e6a-158">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="b0e6a-158">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b0e6a-159">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="b0e6a-159">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b0e6a-160">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-160">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b0e6a-161">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-161">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b0e6a-162">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b0e6a-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="b0e6a-163">("ОК")</span><span class="sxs-lookup"><span data-stu-id="b0e6a-163">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b0e6a-164">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="b0e6a-164">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b0e6a-165">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="b0e6a-165">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b0e6a-166">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="b0e6a-166">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b0e6a-167">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="b0e6a-167">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b0e6a-168">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="b0e6a-168">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b0e6a-169">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="b0e6a-169">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b0e6a-170">("Служба")</span><span class="sxs-lookup"><span data-stu-id="b0e6a-170">("Service")</span></span>


<span data-ttu-id="b0e6a-171"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b0e6a-171"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="b0e6a-172">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0e6a-172">Remarks</span></span>

<span data-ttu-id="b0e6a-173">Для задания свойств с помощью этого класса необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-173">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="b0e6a-174">Свойство **disabled** не запрещает пользователям удаленно запускать удаленные программы после подключения к серверу узла сеансов удаленных рабочих столов с помощью программы RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-174">The **Disabled** property does not prevent users from starting unlisted programs remotely after they connect to the RD Session Host server by using a RemoteApp program.</span></span>

<span data-ttu-id="b0e6a-175">Свойству **disabled** будет присвоено значение 2, только если отсутствует следующая запись реестра:</span><span class="sxs-lookup"><span data-stu-id="b0e6a-175">The **Disabled** property will be set to a value of 2 only if the following registry entry is missing:</span></span>

<span data-ttu-id="b0e6a-176">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **другая** \\ **CurrentVersion** \\ **терминалсервер** \\ **тсаппалловлист** \\ **фдисабледалловлист**</span><span class="sxs-lookup"><span data-stu-id="b0e6a-176">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WindowsNT**\\**CurrentVersion**\\**TerminalServer**\\**TSAppAllowList**\\**fDisabledAllowList**</span></span>

<span data-ttu-id="b0e6a-177">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-177">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="b0e6a-178">Для вызовов C/C++ это уровень проверки подлинности " **PKT" RPC \_ C \_ AUTHN \_ Level \_ \_**, который можно задать с помощью функции [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) com.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-178">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="b0e6a-179">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-179">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="b0e6a-180">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-180">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="b0e6a-181">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="b0e6a-181">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b0e6a-182">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="b0e6a-182">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b0e6a-183">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="b0e6a-183">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b0e6a-184">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b0e6a-184">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0e6a-185">Требования</span><span class="sxs-lookup"><span data-stu-id="b0e6a-185">Requirements</span></span>



| <span data-ttu-id="b0e6a-186">Требование</span><span class="sxs-lookup"><span data-stu-id="b0e6a-186">Requirement</span></span> | <span data-ttu-id="b0e6a-187">Значение</span><span class="sxs-lookup"><span data-stu-id="b0e6a-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e6a-188">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0e6a-188">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e6a-189">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b0e6a-189">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b0e6a-190">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0e6a-190">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e6a-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0e6a-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b0e6a-192">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b0e6a-192">Namespace</span></span><br/>                | <span data-ttu-id="b0e6a-193">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="b0e6a-193">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b0e6a-194">MOF</span><span class="sxs-lookup"><span data-stu-id="b0e6a-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0e6a-195"><dt>Тсаллов. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0e6a-195"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="b0e6a-196">DLL</span><span class="sxs-lookup"><span data-stu-id="b0e6a-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0e6a-197"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0e6a-197"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

