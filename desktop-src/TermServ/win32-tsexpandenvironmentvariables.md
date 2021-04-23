---
title: Класс Win32_TSExpandEnvironmentVariables
description: Расширяет переменные среды, определенные системой. | Класс Win32_TSExpandEnvironmentVariables
ms.assetid: f79d4fa2-1a6e-4a2f-a637-b62f05cfd2ad
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSExpandEnvironmentVariables службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSExpandEnvironmentVariables, описание
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables
- Win32_TSExpandEnvironmentVariables.Caption
- Win32_TSExpandEnvironmentVariables.Description
- Win32_TSExpandEnvironmentVariables.InstallDate
- Win32_TSExpandEnvironmentVariables.Name
- Win32_TSExpandEnvironmentVariables.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d6bbd1a4167de703204fcf5abe345fd1bb216c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914524"
---
# <a name="win32_tsexpandenvironmentvariables-class"></a><span data-ttu-id="308cc-106">\_Класс Win32 тсекспанденвиронментвариаблес</span><span class="sxs-lookup"><span data-stu-id="308cc-106">Win32\_TSExpandEnvironmentVariables class</span></span>

<span data-ttu-id="308cc-107">Расширяет переменные среды, определенные системой.</span><span class="sxs-lookup"><span data-stu-id="308cc-107">Expands system-defined environment variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="308cc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="308cc-108">Syntax</span></span>

``` syntax
class Win32_TSExpandEnvironmentVariables : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="308cc-109">Члены</span><span class="sxs-lookup"><span data-stu-id="308cc-109">Members</span></span>

<span data-ttu-id="308cc-110">Класс **Win32 \_ тсекспанденвиронментвариаблес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="308cc-110">The **Win32\_TSExpandEnvironmentVariables** class has these types of members:</span></span>

-   [<span data-ttu-id="308cc-111">Методы</span><span class="sxs-lookup"><span data-stu-id="308cc-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="308cc-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="308cc-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="308cc-113">Методы</span><span class="sxs-lookup"><span data-stu-id="308cc-113">Methods</span></span>

<span data-ttu-id="308cc-114">Класс **Win32 \_ тсекспанденвиронментвариаблес** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="308cc-114">The **Win32\_TSExpandEnvironmentVariables** class has these methods.</span></span>



| <span data-ttu-id="308cc-115">Метод</span><span class="sxs-lookup"><span data-stu-id="308cc-115">Method</span></span>                                                                                  | <span data-ttu-id="308cc-116">Описание</span><span class="sxs-lookup"><span data-stu-id="308cc-116">Description</span></span>                                              |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="308cc-117">**EnvironmentVariables**</span><span class="sxs-lookup"><span data-stu-id="308cc-117">**EnvironmentVariables**</span></span>](environmentvariables-win32-tsexpandenvironmentvariables.md) | <span data-ttu-id="308cc-118">Расширяет переменные среды, определенные системой.</span><span class="sxs-lookup"><span data-stu-id="308cc-118">Expands system-defined environment variables.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="308cc-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="308cc-119">Properties</span></span>

<span data-ttu-id="308cc-120">Класс **Win32 \_ тсекспанденвиронментвариаблес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="308cc-120">The **Win32\_TSExpandEnvironmentVariables** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="308cc-121">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="308cc-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cc-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="308cc-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="308cc-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="308cc-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cc-124">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="308cc-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="308cc-125">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="308cc-125">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="308cc-126">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="308cc-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cc-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="308cc-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cc-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="308cc-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="308cc-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="308cc-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="308cc-130">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="308cc-130">Description of the object.</span></span>

<span data-ttu-id="308cc-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="308cc-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cc-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="308cc-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cc-133">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="308cc-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="308cc-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="308cc-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cc-135">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="308cc-135">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="308cc-136">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="308cc-136">The date the object was installed.</span></span> <span data-ttu-id="308cc-137">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="308cc-137">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="308cc-138">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="308cc-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cc-139">**Name**</span><span class="sxs-lookup"><span data-stu-id="308cc-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cc-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="308cc-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="308cc-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="308cc-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="308cc-142">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="308cc-142">The name of the object.</span></span>

<span data-ttu-id="308cc-143">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="308cc-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="308cc-144">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="308cc-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="308cc-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="308cc-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="308cc-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="308cc-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="308cc-147">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="308cc-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="308cc-148">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="308cc-148">Current status of the object.</span></span> <span data-ttu-id="308cc-149">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="308cc-149">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="308cc-150">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="308cc-150">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="308cc-151">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="308cc-151">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="308cc-152">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="308cc-152">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="308cc-153">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="308cc-153">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="308cc-154">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="308cc-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="308cc-155">("ОК")</span><span class="sxs-lookup"><span data-stu-id="308cc-155">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="308cc-156">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="308cc-156">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="308cc-157">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="308cc-157">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="308cc-158">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="308cc-158">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="308cc-159">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="308cc-159">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="308cc-160">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="308cc-160">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="308cc-161">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="308cc-161">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="308cc-162">("Служба")</span><span class="sxs-lookup"><span data-stu-id="308cc-162">("Service")</span></span>


<span data-ttu-id="308cc-163"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="308cc-163"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="308cc-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="308cc-164">Remarks</span></span>

<span data-ttu-id="308cc-165">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="308cc-165">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="308cc-166">Для вызовов C/C++ это уровень проверки подлинности " **PKT" RPC \_ C \_ AUTHN \_ Level \_ \_**, который можно задать с помощью функции [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) com.</span><span class="sxs-lookup"><span data-stu-id="308cc-166">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="308cc-167">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="308cc-167">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="308cc-168">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="308cc-168">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="308cc-169">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="308cc-169">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="308cc-170">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="308cc-170">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="308cc-171">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="308cc-171">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="308cc-172">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="308cc-172">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="308cc-173">Требования</span><span class="sxs-lookup"><span data-stu-id="308cc-173">Requirements</span></span>



| <span data-ttu-id="308cc-174">Требование</span><span class="sxs-lookup"><span data-stu-id="308cc-174">Requirement</span></span> | <span data-ttu-id="308cc-175">Значение</span><span class="sxs-lookup"><span data-stu-id="308cc-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="308cc-176">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="308cc-176">Minimum supported client</span></span><br/> | <span data-ttu-id="308cc-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="308cc-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="308cc-178">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="308cc-178">Minimum supported server</span></span><br/> | <span data-ttu-id="308cc-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="308cc-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="308cc-180">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="308cc-180">Namespace</span></span><br/>                | <span data-ttu-id="308cc-181">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="308cc-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="308cc-182">MOF</span><span class="sxs-lookup"><span data-stu-id="308cc-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="308cc-183"><dt>Тсаллов. mof</dt></span><span class="sxs-lookup"><span data-stu-id="308cc-183"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="308cc-184">DLL</span><span class="sxs-lookup"><span data-stu-id="308cc-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="308cc-185"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="308cc-185"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

