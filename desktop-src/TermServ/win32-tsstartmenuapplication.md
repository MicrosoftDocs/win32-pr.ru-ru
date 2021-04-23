---
title: Класс Win32_TSStartMenuApplication
description: Описание приложений, которые находятся в меню "Пуск" на сервере узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).
ms.assetid: 88b412b8-139f-4266-b7d8-c34f93940a72
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSStartMenuApplication службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSStartMenuApplication, описание
topic_type:
- apiref
api_name:
- Win32_TSStartMenuApplication
- Win32_TSStartMenuApplication.Caption
- Win32_TSStartMenuApplication.Description
- Win32_TSStartMenuApplication.InstallDate
- Win32_TSStartMenuApplication.Name
- Win32_TSStartMenuApplication.Status
- Win32_TSStartMenuApplication.Path
- Win32_TSStartMenuApplication.VPath
- Win32_TSStartMenuApplication.IconPath
- Win32_TSStartMenuApplication.IconIndex
- Win32_TSStartMenuApplication.CommandLineArguments
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dae7610381745f6ced2a01e76f8545b33d1205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803845"
---
# <a name="win32_tsstartmenuapplication-class"></a><span data-ttu-id="88b67-105">\_Класс Win32 тсстартменуаппликатион</span><span class="sxs-lookup"><span data-stu-id="88b67-105">Win32\_TSStartMenuApplication class</span></span>

<span data-ttu-id="88b67-106">Описание приложений, которые находятся в меню "Пуск" на сервере узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="88b67-106">Describes the applications that are on the Start menu of a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="88b67-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88b67-107">Syntax</span></span>

``` syntax
class Win32_TSStartMenuApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Path;
  string   VPath;
  string   IconPath;
  sint32   IconIndex;
  string   CommandLineArguments;
};
```

## <a name="members"></a><span data-ttu-id="88b67-108">Члены</span><span class="sxs-lookup"><span data-stu-id="88b67-108">Members</span></span>

<span data-ttu-id="88b67-109">Класс **Win32 \_ тсстартменуаппликатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="88b67-109">The **Win32\_TSStartMenuApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="88b67-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="88b67-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88b67-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="88b67-111">Properties</span></span>

<span data-ttu-id="88b67-112">Класс **Win32 \_ тсстартменуаппликатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="88b67-112">The **Win32\_TSStartMenuApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88b67-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="88b67-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b67-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88b67-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88b67-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b67-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b67-116">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="88b67-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="88b67-117">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="88b67-117">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="88b67-118">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88b67-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88b67-119">**коммандлинеаргументс**</span><span class="sxs-lookup"><span data-stu-id="88b67-119">**CommandLineArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b67-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88b67-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88b67-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b67-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88b67-122">Используемые аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="88b67-122">The command-line arguments to use.</span></span>

</dd> <dt>

<span data-ttu-id="88b67-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="88b67-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b67-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88b67-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88b67-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b67-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88b67-126">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="88b67-126">Description of the object.</span></span>

<span data-ttu-id="88b67-127">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88b67-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88b67-128">**икониндекс**</span><span class="sxs-lookup"><span data-stu-id="88b67-128">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b67-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="88b67-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="88b67-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b67-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88b67-131">Индекс или идентификатор значка.</span><span class="sxs-lookup"><span data-stu-id="88b67-131">The index or ID of the icon.</span></span>

</dd> <dt>

<span data-ttu-id="88b67-132">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="88b67-132">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b67-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88b67-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88b67-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b67-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88b67-135">Путь к значку приложения.</span><span class="sxs-lookup"><span data-stu-id="88b67-135">The path of the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="88b67-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="88b67-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b67-137">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="88b67-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88b67-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b67-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b67-139">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="88b67-139">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="88b67-140">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="88b67-140">The date the object was installed.</span></span> <span data-ttu-id="88b67-141">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="88b67-141">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="88b67-142">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88b67-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88b67-143">**Name**</span><span class="sxs-lookup"><span data-stu-id="88b67-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b67-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88b67-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88b67-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b67-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88b67-146">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="88b67-146">The name of the object.</span></span>

<span data-ttu-id="88b67-147">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88b67-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88b67-148">**Путь**</span><span class="sxs-lookup"><span data-stu-id="88b67-148">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b67-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88b67-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88b67-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b67-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b67-151">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="88b67-151">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="88b67-152">Путь к приложению.</span><span class="sxs-lookup"><span data-stu-id="88b67-152">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="88b67-153">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="88b67-153">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b67-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88b67-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88b67-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b67-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88b67-156">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="88b67-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="88b67-157">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="88b67-157">Current status of the object.</span></span> <span data-ttu-id="88b67-158">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="88b67-158">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="88b67-159">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="88b67-159">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="88b67-160">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="88b67-160">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="88b67-161">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="88b67-161">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="88b67-162">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="88b67-162">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="88b67-163">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88b67-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="88b67-164">("ОК")</span><span class="sxs-lookup"><span data-stu-id="88b67-164">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88b67-165">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="88b67-165">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88b67-166">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="88b67-166">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88b67-167">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="88b67-167">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88b67-168">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="88b67-168">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88b67-169">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="88b67-169">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88b67-170">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="88b67-170">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88b67-171">("Служба")</span><span class="sxs-lookup"><span data-stu-id="88b67-171">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88b67-172">**впас**</span><span class="sxs-lookup"><span data-stu-id="88b67-172">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88b67-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88b67-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88b67-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88b67-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88b67-175">Виртуальный путь приложения.</span><span class="sxs-lookup"><span data-stu-id="88b67-175">The virtual path of the application.</span></span> <span data-ttu-id="88b67-176">К ним относятся системные переменные среды, такие как% WINDIR%.</span><span class="sxs-lookup"><span data-stu-id="88b67-176">This includes system environment variables, such as %windir%.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88b67-177">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88b67-177">Remarks</span></span>

<span data-ttu-id="88b67-178">Для использования этого класса необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="88b67-178">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="88b67-179">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="88b67-179">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="88b67-180">Для вызовов C/C++ это уровень проверки подлинности " **PKT" RPC \_ C \_ AUTHN \_ Level \_ \_**, который можно задать с помощью функции [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) com.</span><span class="sxs-lookup"><span data-stu-id="88b67-180">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="88b67-181">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="88b67-181">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="88b67-182">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="88b67-182">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="88b67-183">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="88b67-183">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="88b67-184">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="88b67-184">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="88b67-185">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="88b67-185">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="88b67-186">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="88b67-186">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="88b67-187">Требования</span><span class="sxs-lookup"><span data-stu-id="88b67-187">Requirements</span></span>



| <span data-ttu-id="88b67-188">Требование</span><span class="sxs-lookup"><span data-stu-id="88b67-188">Requirement</span></span> | <span data-ttu-id="88b67-189">Значение</span><span class="sxs-lookup"><span data-stu-id="88b67-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88b67-190">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88b67-190">Minimum supported client</span></span><br/> | <span data-ttu-id="88b67-191">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="88b67-191">None supported</span></span><br/>                                                               |
| <span data-ttu-id="88b67-192">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88b67-192">Minimum supported server</span></span><br/> | <span data-ttu-id="88b67-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88b67-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88b67-194">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="88b67-194">Namespace</span></span><br/>                | <span data-ttu-id="88b67-195">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="88b67-195">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="88b67-196">MOF</span><span class="sxs-lookup"><span data-stu-id="88b67-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88b67-197"><dt>Тсаллов. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88b67-197"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="88b67-198">DLL</span><span class="sxs-lookup"><span data-stu-id="88b67-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88b67-199"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88b67-199"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

