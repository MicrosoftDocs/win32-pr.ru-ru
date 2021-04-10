---
title: Класс Win32_TSRemoteDesktop
description: Описание подключения к удаленному рабочему столу, доступного с помощью удаленный рабочий стол Веб-доступ (RD Веб-доступ).
ms.assetid: 40c7d8f1-cc45-4f0a-8c07-8215342ca02e
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSRemoteDesktop службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSRemoteDesktop, описание
topic_type:
- apiref
api_name:
- Win32_TSRemoteDesktop
- Win32_TSRemoteDesktop.Caption
- Win32_TSRemoteDesktop.Description
- Win32_TSRemoteDesktop.InstallDate
- Win32_TSRemoteDesktop.Name
- Win32_TSRemoteDesktop.Status
- Win32_TSRemoteDesktop.Alias
- Win32_TSRemoteDesktop.SecurityDescriptor
- Win32_TSRemoteDesktop.IconPath
- Win32_TSRemoteDesktop.IconIndex
- Win32_TSRemoteDesktop.IconContents
- Win32_TSRemoteDesktop.ShowInPortal
- Win32_TSRemoteDesktop.RDPFileContents
- Win32_TSRemoteDesktop.IsVmFarm
- Win32_TSRemoteDesktop.VmFarmSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3a23e63d5c79313933b7ce6951265a85740bc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135239"
---
# <a name="win32_tsremotedesktop-class"></a><span data-ttu-id="867f3-105">\_Класс Win32 тсремотедесктоп</span><span class="sxs-lookup"><span data-stu-id="867f3-105">Win32\_TSRemoteDesktop class</span></span>

<span data-ttu-id="867f3-106">Описание подключения к удаленному рабочему столу, доступного с помощью удаленный рабочий стол Веб-доступ (RD Веб-доступ).</span><span class="sxs-lookup"><span data-stu-id="867f3-106">Describes a remote desktop connection that is available through Remote Desktop Web Access (RD Web Access).</span></span>

## <a name="syntax"></a><span data-ttu-id="867f3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="867f3-107">Syntax</span></span>

``` syntax
class Win32_TSRemoteDesktop : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  string   SecurityDescriptor;
  string   IconPath;
  sint32   IconIndex;
  uint8    IconContents[];
  boolean  ShowInPortal;
  string   RDPFileContents;
  boolean  IsVmFarm;
  string   VmFarmSettings;
};
```

## <a name="members"></a><span data-ttu-id="867f3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="867f3-108">Members</span></span>

<span data-ttu-id="867f3-109">Класс **Win32 \_ тсремотедесктоп** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="867f3-109">The **Win32\_TSRemoteDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="867f3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="867f3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="867f3-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="867f3-111">Properties</span></span>

<span data-ttu-id="867f3-112">Класс **Win32 \_ тсремотедесктоп** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="867f3-112">The **Win32\_TSRemoteDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="867f3-113">**Псевдоним**</span><span class="sxs-lookup"><span data-stu-id="867f3-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="867f3-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="867f3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="867f3-115">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="867f3-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="867f3-116">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="867f3-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="867f3-117">Псевдоним подключения к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="867f3-117">The alias of the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="867f3-118">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="867f3-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="867f3-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="867f3-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="867f3-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="867f3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="867f3-121">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="867f3-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="867f3-122">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="867f3-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="867f3-123">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="867f3-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="867f3-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="867f3-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="867f3-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="867f3-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="867f3-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="867f3-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="867f3-127">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="867f3-127">Description of the object.</span></span>

<span data-ttu-id="867f3-128">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="867f3-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="867f3-129">**иконконтентс**</span><span class="sxs-lookup"><span data-stu-id="867f3-129">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="867f3-130">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="867f3-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="867f3-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="867f3-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="867f3-132">Байтовое содержимое значка, соответствующего подключению к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="867f3-132">The byte contents of the icon that corresponds to the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="867f3-133">**икониндекс**</span><span class="sxs-lookup"><span data-stu-id="867f3-133">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="867f3-134">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="867f3-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="867f3-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="867f3-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="867f3-136">Индекс или идентификатор значка для подключения к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="867f3-136">The index or ID of the icon for the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="867f3-137">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="867f3-137">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="867f3-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="867f3-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="867f3-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="867f3-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="867f3-140">Путь к значку для подключения к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="867f3-140">Path of the icon for the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="867f3-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="867f3-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="867f3-142">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="867f3-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="867f3-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="867f3-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="867f3-144">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="867f3-144">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="867f3-145">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="867f3-145">The date the object was installed.</span></span> <span data-ttu-id="867f3-146">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="867f3-146">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="867f3-147">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="867f3-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="867f3-148">**исвмфарм**</span><span class="sxs-lookup"><span data-stu-id="867f3-148">**IsVmFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="867f3-149">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="867f3-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="867f3-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="867f3-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="867f3-151">Указывает, является ли это подключение к удаленному рабочему столу частью фермы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="867f3-151">Indicates if this remote desktop connection is part of a virtual machine farm.</span></span>

</dd> <dt>

<span data-ttu-id="867f3-152">**Name**</span><span class="sxs-lookup"><span data-stu-id="867f3-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="867f3-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="867f3-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="867f3-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="867f3-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="867f3-155">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="867f3-155">The name of the object.</span></span>

<span data-ttu-id="867f3-156">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="867f3-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="867f3-157">**рдпфилеконтентс**</span><span class="sxs-lookup"><span data-stu-id="867f3-157">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="867f3-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="867f3-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="867f3-159">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="867f3-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="867f3-160">Содержимое RDP-файла, соответствующего подключению к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="867f3-160">Contents of the RDP file that correspond to the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="867f3-161">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="867f3-161">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="867f3-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="867f3-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="867f3-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="867f3-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="867f3-164">Дескриптор безопасности, управляющий доступом к подключению к удаленному рабочему столу в формате SDDL.</span><span class="sxs-lookup"><span data-stu-id="867f3-164">A security descriptor that controls access to the remote desktop connection, in SDDL format.</span></span> <span data-ttu-id="867f3-165">Пустая строка подразумевает разрешение любой доступ.</span><span class="sxs-lookup"><span data-stu-id="867f3-165">An empty string implies allow all access.</span></span> <span data-ttu-id="867f3-166">Этот дескриптор безопасности не поддерживает ЗАПРЕЩЕНные ACE или записи ACE, ссылающиеся на пользователей и группы, не являющиеся доменами.</span><span class="sxs-lookup"><span data-stu-id="867f3-166">This security descriptor does not support DENY ACEs, or ACEs that refer to nondomain users or groups.</span></span>

</dd> <dt>

<span data-ttu-id="867f3-167">**шовинпортал**</span><span class="sxs-lookup"><span data-stu-id="867f3-167">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="867f3-168">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="867f3-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="867f3-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="867f3-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="867f3-170">Указывает, должно ли отображаться подключение к удаленному рабочему столу в Веб-доступ удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="867f3-170">Indicates whether the remote desktop connection should be shown in RD Web Access.</span></span>

</dd> <dt>

<span data-ttu-id="867f3-171">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="867f3-171">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="867f3-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="867f3-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="867f3-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="867f3-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="867f3-174">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="867f3-174">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="867f3-175">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="867f3-175">Current status of the object.</span></span> <span data-ttu-id="867f3-176">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="867f3-176">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="867f3-177">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="867f3-177">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="867f3-178">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="867f3-178">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="867f3-179">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="867f3-179">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="867f3-180">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="867f3-180">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="867f3-181">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="867f3-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="867f3-182">("ОК")</span><span class="sxs-lookup"><span data-stu-id="867f3-182">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="867f3-183">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="867f3-183">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="867f3-184">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="867f3-184">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="867f3-185">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="867f3-185">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="867f3-186">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="867f3-186">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="867f3-187">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="867f3-187">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="867f3-188">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="867f3-188">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="867f3-189">("Служба")</span><span class="sxs-lookup"><span data-stu-id="867f3-189">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="867f3-190">**вмфармсеттингс**</span><span class="sxs-lookup"><span data-stu-id="867f3-190">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="867f3-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="867f3-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="867f3-192">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="867f3-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="867f3-193">Параметры фермы виртуальных машин для подключения к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="867f3-193">Virtual machine farm settings for the remote desktop connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="867f3-194">Комментарии</span><span class="sxs-lookup"><span data-stu-id="867f3-194">Remarks</span></span>

<span data-ttu-id="867f3-195">Для задания свойств с помощью этого класса необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="867f3-195">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="867f3-196">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="867f3-196">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="867f3-197">Для вызовов C/C++ это уровень проверки подлинности " **PKT" RPC \_ C \_ AUTHN \_ Level \_ \_**, который можно задать с помощью функции [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) com.</span><span class="sxs-lookup"><span data-stu-id="867f3-197">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="867f3-198">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="867f3-198">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="867f3-199">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="867f3-199">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="867f3-200">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="867f3-200">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="867f3-201">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="867f3-201">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="867f3-202">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="867f3-202">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="867f3-203">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="867f3-203">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="867f3-204">Требования</span><span class="sxs-lookup"><span data-stu-id="867f3-204">Requirements</span></span>



| <span data-ttu-id="867f3-205">Требование</span><span class="sxs-lookup"><span data-stu-id="867f3-205">Requirement</span></span> | <span data-ttu-id="867f3-206">Значение</span><span class="sxs-lookup"><span data-stu-id="867f3-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="867f3-207">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="867f3-207">Minimum supported client</span></span><br/> | <span data-ttu-id="867f3-208">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="867f3-208">None supported</span></span><br/>                                                               |
| <span data-ttu-id="867f3-209">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="867f3-209">Minimum supported server</span></span><br/> | <span data-ttu-id="867f3-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="867f3-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="867f3-211">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="867f3-211">Namespace</span></span><br/>                | <span data-ttu-id="867f3-212">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="867f3-212">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="867f3-213">MOF</span><span class="sxs-lookup"><span data-stu-id="867f3-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="867f3-214"><dt>Тсаллов. mof</dt></span><span class="sxs-lookup"><span data-stu-id="867f3-214"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="867f3-215">DLL</span><span class="sxs-lookup"><span data-stu-id="867f3-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="867f3-216"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="867f3-216"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

