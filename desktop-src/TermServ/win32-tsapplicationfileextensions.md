---
title: Класс Win32_TSApplicationFileExtensions
description: Расширения имен файлов, обрабатываемые приложением на сервере узла сеансов удаленный рабочий стол.
ms.assetid: beefc266-5ad6-49ee-b761-98764e2905d6
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSApplicationFileExtensions службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSApplicationFileExtensions, описание
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions
- Win32_TSApplicationFileExtensions.Caption
- Win32_TSApplicationFileExtensions.Description
- Win32_TSApplicationFileExtensions.InstallDate
- Win32_TSApplicationFileExtensions.Name
- Win32_TSApplicationFileExtensions.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e28f84ff122b77abf1474b5686edab627177424b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682060"
---
# <a name="win32_tsapplicationfileextensions-class"></a><span data-ttu-id="49581-105">\_Класс Win32 тсаппликатионфиликстенсионс</span><span class="sxs-lookup"><span data-stu-id="49581-105">Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="49581-106">Описывает расширения имен файлов, обрабатываемые приложением на сервере узла сеансов удаленный рабочий стол (на узле сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="49581-106">Describes the file name extensions that are handled by an application on a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="49581-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49581-107">Syntax</span></span>

``` syntax
class Win32_TSApplicationFileExtensions : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="49581-108">Члены</span><span class="sxs-lookup"><span data-stu-id="49581-108">Members</span></span>

<span data-ttu-id="49581-109">Класс **Win32 \_ тсаппликатионфиликстенсионс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="49581-109">The **Win32\_TSApplicationFileExtensions** class has these types of members:</span></span>

-   [<span data-ttu-id="49581-110">Методы</span><span class="sxs-lookup"><span data-stu-id="49581-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="49581-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="49581-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="49581-112">Методы</span><span class="sxs-lookup"><span data-stu-id="49581-112">Methods</span></span>

<span data-ttu-id="49581-113">Класс **Win32 \_ тсаппликатионфиликстенсионс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="49581-113">The **Win32\_TSApplicationFileExtensions** class has these methods.</span></span>



| <span data-ttu-id="49581-114">Метод</span><span class="sxs-lookup"><span data-stu-id="49581-114">Method</span></span>                                                                         | <span data-ttu-id="49581-115">Описание</span><span class="sxs-lookup"><span data-stu-id="49581-115">Description</span></span>                                                                                |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49581-116">**филеассоЦиатионс**</span><span class="sxs-lookup"><span data-stu-id="49581-116">**FileAssociations**</span></span>](fileassociations-win32-tsapplicationfileextensions.md) | <span data-ttu-id="49581-117">Сканирует реестр для получения текущих сопоставлений файлов для приложения.</span><span class="sxs-lookup"><span data-stu-id="49581-117">Scans the registry to get the current file associations for an application.</span></span><br/>     |
| [<span data-ttu-id="49581-118">**FileExtensions**</span><span class="sxs-lookup"><span data-stu-id="49581-118">**FileExtensions**</span></span>](fileextensions-win32-tsapplicationfileextensions.md)     | <span data-ttu-id="49581-119">Предоставляет список расширений имен файлов, обрабатываемых приложением.</span><span class="sxs-lookup"><span data-stu-id="49581-119">Provides a list of the file name extensions that are handled by an application.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="49581-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="49581-120">Properties</span></span>

<span data-ttu-id="49581-121">Класс **Win32 \_ тсаппликатионфиликстенсионс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="49581-121">The **Win32\_TSApplicationFileExtensions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49581-122">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="49581-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49581-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="49581-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49581-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="49581-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49581-125">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="49581-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="49581-126">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="49581-126">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="49581-127">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="49581-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49581-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="49581-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49581-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="49581-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49581-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="49581-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49581-131">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="49581-131">Description of the object.</span></span>

<span data-ttu-id="49581-132">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="49581-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49581-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="49581-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49581-134">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="49581-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="49581-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="49581-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49581-136">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="49581-136">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="49581-137">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="49581-137">The date the object was installed.</span></span> <span data-ttu-id="49581-138">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="49581-138">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="49581-139">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="49581-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49581-140">**Name**</span><span class="sxs-lookup"><span data-stu-id="49581-140">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49581-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="49581-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49581-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="49581-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49581-143">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="49581-143">The name of the object.</span></span>

<span data-ttu-id="49581-144">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="49581-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49581-145">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="49581-145">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49581-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="49581-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49581-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="49581-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49581-148">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="49581-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="49581-149">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="49581-149">Current status of the object.</span></span> <span data-ttu-id="49581-150">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="49581-150">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="49581-151">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="49581-151">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="49581-152">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="49581-152">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="49581-153">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="49581-153">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="49581-154">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="49581-154">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="49581-155">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="49581-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="49581-156">("ОК")</span><span class="sxs-lookup"><span data-stu-id="49581-156">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="49581-157">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="49581-157">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="49581-158">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="49581-158">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="49581-159">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="49581-159">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="49581-160">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="49581-160">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="49581-161">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="49581-161">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="49581-162">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="49581-162">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="49581-163">("Служба")</span><span class="sxs-lookup"><span data-stu-id="49581-163">("Service")</span></span>


<span data-ttu-id="49581-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="49581-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="49581-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49581-165">Remarks</span></span>

<span data-ttu-id="49581-166">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="49581-166">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="49581-167">Для вызовов C/C++ это уровень проверки подлинности " **PKT" RPC \_ C \_ AUTHN \_ Level \_ \_**, который можно задать с помощью функции [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) com.</span><span class="sxs-lookup"><span data-stu-id="49581-167">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="49581-168">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="49581-168">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span>

<span data-ttu-id="49581-169">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="49581-169">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="49581-170">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="49581-170">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="49581-171">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="49581-171">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="49581-172">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="49581-172">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="49581-173">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="49581-173">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="49581-174">Требования</span><span class="sxs-lookup"><span data-stu-id="49581-174">Requirements</span></span>



| <span data-ttu-id="49581-175">Требование</span><span class="sxs-lookup"><span data-stu-id="49581-175">Requirement</span></span> | <span data-ttu-id="49581-176">Значение</span><span class="sxs-lookup"><span data-stu-id="49581-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49581-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49581-177">Minimum supported client</span></span><br/> | <span data-ttu-id="49581-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49581-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49581-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49581-179">Minimum supported server</span></span><br/> | <span data-ttu-id="49581-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49581-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49581-181">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="49581-181">Namespace</span></span><br/>                | <span data-ttu-id="49581-182">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="49581-182">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="49581-183">MOF</span><span class="sxs-lookup"><span data-stu-id="49581-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49581-184"><dt>Тсаллов. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49581-184"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="49581-185">DLL</span><span class="sxs-lookup"><span data-stu-id="49581-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49581-186"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49581-186"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

