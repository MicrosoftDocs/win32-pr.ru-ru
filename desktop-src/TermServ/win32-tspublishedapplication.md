---
title: Класс Win32_TSPublishedApplication
description: Определяет приложения, которые становятся доступными для удаленного использования через Windows Server 2008 R2 RemoteApp.
ms.assetid: 5b9cb36b-3d8d-4105-acea-c79440d977fe
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSPublishedApplication службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSPublishedApplication, описание
topic_type:
- apiref
api_name:
- Win32_TSPublishedApplication
- Win32_TSPublishedApplication.Caption
- Win32_TSPublishedApplication.Description
- Win32_TSPublishedApplication.InstallDate
- Win32_TSPublishedApplication.Name
- Win32_TSPublishedApplication.Status
- Win32_TSPublishedApplication.Alias
- Win32_TSPublishedApplication.SecurityDescriptor
- Win32_TSPublishedApplication.Path
- Win32_TSPublishedApplication.PathExists
- Win32_TSPublishedApplication.VPath
- Win32_TSPublishedApplication.IconPath
- Win32_TSPublishedApplication.IconIndex
- Win32_TSPublishedApplication.IconContents
- Win32_TSPublishedApplication.CommandLineSetting
- Win32_TSPublishedApplication.RequiredCommandLine
- Win32_TSPublishedApplication.ShowInPortal
- Win32_TSPublishedApplication.RDPFileContents
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3825087d05b622818c74f011f30b325ed8ff7f60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681860"
---
# <a name="win32_tspublishedapplication-class"></a><span data-ttu-id="13cbb-105">\_Класс Win32 тспублишедаппликатион</span><span class="sxs-lookup"><span data-stu-id="13cbb-105">Win32\_TSPublishedApplication class</span></span>

<span data-ttu-id="13cbb-106">Определяет приложения, которые становятся доступными для удаленного использования через Windows Server 2008 R2 RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="13cbb-106">Defines the applications that are made available for remote use through Windows Server 2008 R2 RemoteApp.</span></span>

## <a name="syntax"></a><span data-ttu-id="13cbb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13cbb-107">Syntax</span></span>

``` syntax
class Win32_TSPublishedApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  string   SecurityDescriptor;
  string   Path;
  boolean  PathExists;
  string   VPath;
  string   IconPath;
  sint32   IconIndex;
  uint8    IconContents[];
  uint32   CommandLineSetting;
  string   RequiredCommandLine;
  boolean  ShowInPortal;
  string   RDPFileContents;
};
```

## <a name="members"></a><span data-ttu-id="13cbb-108">Члены</span><span class="sxs-lookup"><span data-stu-id="13cbb-108">Members</span></span>

<span data-ttu-id="13cbb-109">Класс **Win32 \_ тспублишедаппликатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="13cbb-109">The **Win32\_TSPublishedApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="13cbb-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="13cbb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13cbb-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="13cbb-111">Properties</span></span>

<span data-ttu-id="13cbb-112">Класс **Win32 \_ тспублишедаппликатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="13cbb-112">The **Win32\_TSPublishedApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13cbb-113">**Псевдоним**</span><span class="sxs-lookup"><span data-stu-id="13cbb-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cbb-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13cbb-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-115">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="13cbb-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-116">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="13cbb-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="13cbb-117">Псевдоним приложения.</span><span class="sxs-lookup"><span data-stu-id="13cbb-117">The alias of the application.</span></span> <span data-ttu-id="13cbb-118">Псевдоним — это уникальный идентификатор программы, используемой по умолчанию для имени файла программы (без расширения).</span><span class="sxs-lookup"><span data-stu-id="13cbb-118">The alias is a unique identifier for the program that defaults to the program's file name (without the extension).</span></span>

</dd> <dt>

<span data-ttu-id="13cbb-119">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="13cbb-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cbb-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13cbb-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13cbb-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-122">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="13cbb-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="13cbb-123">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="13cbb-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="13cbb-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13cbb-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13cbb-125">**коммандлинесеттинг**</span><span class="sxs-lookup"><span data-stu-id="13cbb-125">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cbb-126">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13cbb-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="13cbb-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13cbb-128">Параметр аргументов командной строки для приложения.</span><span class="sxs-lookup"><span data-stu-id="13cbb-128">The command-line arguments setting for the application.</span></span> <span data-ttu-id="13cbb-129">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="13cbb-129">The following values are possible.</span></span>

<dt>

<span data-ttu-id="13cbb-130">0</span><span class="sxs-lookup"><span data-stu-id="13cbb-130">0</span></span>
</dt> <dd>

<span data-ttu-id="13cbb-131">Не разрешать аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="13cbb-131">Do not allow command-line arguments.</span></span>

</dd> <dt>

<span data-ttu-id="13cbb-132">1</span><span class="sxs-lookup"><span data-stu-id="13cbb-132">1</span></span>
</dt> <dd>

<span data-ttu-id="13cbb-133">Разрешить любые аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="13cbb-133">Allow any command-line arguments.</span></span>

</dd> <dt>

<span data-ttu-id="13cbb-134">2</span><span class="sxs-lookup"><span data-stu-id="13cbb-134">2</span></span>
</dt> <dd>

<span data-ttu-id="13cbb-135">Всегда используйте обязательные аргументы командной строки (указанные в **рекуиредкоммандлине**).</span><span class="sxs-lookup"><span data-stu-id="13cbb-135">Always use the required command-line arguments (specified in **RequiredCommandLine**).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="13cbb-136">**Описание**</span><span class="sxs-lookup"><span data-stu-id="13cbb-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cbb-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13cbb-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13cbb-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13cbb-139">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="13cbb-139">Description of the object.</span></span>

<span data-ttu-id="13cbb-140">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13cbb-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13cbb-141">**иконконтентс**</span><span class="sxs-lookup"><span data-stu-id="13cbb-141">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cbb-142">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="13cbb-142">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13cbb-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13cbb-144">Байтовое содержимое значка, соответствующего приложению.</span><span class="sxs-lookup"><span data-stu-id="13cbb-144">The byte contents of the icon that corresponds to the application.</span></span>

</dd> <dt>

<span data-ttu-id="13cbb-145">**икониндекс**</span><span class="sxs-lookup"><span data-stu-id="13cbb-145">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cbb-146">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="13cbb-146">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-147">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="13cbb-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13cbb-148">Индекс или идентификатор значка.</span><span class="sxs-lookup"><span data-stu-id="13cbb-148">The index or ID of the icon.</span></span>

</dd> <dt>

<span data-ttu-id="13cbb-149">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="13cbb-149">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cbb-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13cbb-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="13cbb-151">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13cbb-152">Путь к значку приложения.</span><span class="sxs-lookup"><span data-stu-id="13cbb-152">The path of the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="13cbb-153">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="13cbb-153">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cbb-154">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="13cbb-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13cbb-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-156">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="13cbb-156">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="13cbb-157">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="13cbb-157">The date the object was installed.</span></span> <span data-ttu-id="13cbb-158">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="13cbb-158">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="13cbb-159">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13cbb-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13cbb-160">**Name**</span><span class="sxs-lookup"><span data-stu-id="13cbb-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cbb-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13cbb-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13cbb-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13cbb-163">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="13cbb-163">The name of the object.</span></span>

<span data-ttu-id="13cbb-164">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13cbb-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13cbb-165">**Путь**</span><span class="sxs-lookup"><span data-stu-id="13cbb-165">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cbb-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13cbb-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-167">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="13cbb-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13cbb-168">Путь к приложению.</span><span class="sxs-lookup"><span data-stu-id="13cbb-168">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="13cbb-169">**пасексистс**</span><span class="sxs-lookup"><span data-stu-id="13cbb-169">**PathExists**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cbb-170">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="13cbb-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13cbb-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13cbb-172">Указывает, является ли допустимым путь к приложению.</span><span class="sxs-lookup"><span data-stu-id="13cbb-172">Indicates whether the application path is valid.</span></span>

</dd> <dt>

<span data-ttu-id="13cbb-173">**рдпфилеконтентс**</span><span class="sxs-lookup"><span data-stu-id="13cbb-173">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cbb-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13cbb-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="13cbb-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13cbb-176">Содержимое RDP-файла, соответствующего приложению.</span><span class="sxs-lookup"><span data-stu-id="13cbb-176">The contents of the RDP file that correspond to the application.</span></span>

</dd> <dt>

<span data-ttu-id="13cbb-177">**рекуиредкоммандлине**</span><span class="sxs-lookup"><span data-stu-id="13cbb-177">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cbb-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13cbb-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-179">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="13cbb-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13cbb-180">Аргументы командной строки, необходимые для приложения.</span><span class="sxs-lookup"><span data-stu-id="13cbb-180">The command-line arguments that are required for the application.</span></span>

</dd> <dt>

<span data-ttu-id="13cbb-181">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="13cbb-181">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cbb-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13cbb-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-183">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="13cbb-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13cbb-184">Дескриптор безопасности, управляющий доступом к приложению в формате SDDL.</span><span class="sxs-lookup"><span data-stu-id="13cbb-184">A security descriptor that controls access to the application, in SDDL format.</span></span> <span data-ttu-id="13cbb-185">Пустая строка подразумевает разрешение любой доступ.</span><span class="sxs-lookup"><span data-stu-id="13cbb-185">An empty string implies allow all access.</span></span> <span data-ttu-id="13cbb-186">Этот дескриптор безопасности не поддерживает ЗАПРЕЩЕНные ACE или записи ACE, ссылающиеся на пользователей и группы, не являющиеся доменами.</span><span class="sxs-lookup"><span data-stu-id="13cbb-186">This security descriptor does not support DENY ACEs, or ACEs that refer to nondomain users or groups.</span></span>

</dd> <dt>

<span data-ttu-id="13cbb-187">**шовинпортал**</span><span class="sxs-lookup"><span data-stu-id="13cbb-187">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cbb-188">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="13cbb-188">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-189">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="13cbb-189">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13cbb-190">Указывает, должно ли приложение отображаться в Веб-доступ удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="13cbb-190">Indicates whether the application should be shown in RD Web Access.</span></span>

</dd> <dt>

<span data-ttu-id="13cbb-191">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="13cbb-191">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cbb-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13cbb-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="13cbb-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-194">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="13cbb-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="13cbb-195">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="13cbb-195">Current status of the object.</span></span> <span data-ttu-id="13cbb-196">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="13cbb-196">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="13cbb-197">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="13cbb-197">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="13cbb-198">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="13cbb-198">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="13cbb-199">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="13cbb-199">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="13cbb-200">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="13cbb-200">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="13cbb-201">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13cbb-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="13cbb-202">("ОК")</span><span class="sxs-lookup"><span data-stu-id="13cbb-202">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="13cbb-203">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="13cbb-203">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="13cbb-204">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="13cbb-204">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="13cbb-205">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="13cbb-205">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="13cbb-206">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="13cbb-206">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="13cbb-207">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="13cbb-207">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="13cbb-208">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="13cbb-208">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="13cbb-209">("Служба")</span><span class="sxs-lookup"><span data-stu-id="13cbb-209">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="13cbb-210">**впас**</span><span class="sxs-lookup"><span data-stu-id="13cbb-210">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13cbb-211">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="13cbb-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13cbb-212">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="13cbb-212">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13cbb-213">Виртуальный путь к приложению, то есть путь с переменными среды.</span><span class="sxs-lookup"><span data-stu-id="13cbb-213">The virtual path of the application, meaning the path with environment variables included.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13cbb-214">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13cbb-214">Remarks</span></span>

<span data-ttu-id="13cbb-215">Для задания свойств с помощью этого класса необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="13cbb-215">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="13cbb-216">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="13cbb-216">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="13cbb-217">Для вызовов C/C++ это уровень проверки подлинности " **PKT" RPC \_ C \_ AUTHN \_ Level \_ \_**, который можно задать с помощью функции [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) com.</span><span class="sxs-lookup"><span data-stu-id="13cbb-217">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="13cbb-218">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="13cbb-218">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="13cbb-219">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="13cbb-219">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="13cbb-220">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="13cbb-220">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="13cbb-221">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="13cbb-221">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="13cbb-222">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="13cbb-222">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="13cbb-223">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="13cbb-223">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="13cbb-224">Требования</span><span class="sxs-lookup"><span data-stu-id="13cbb-224">Requirements</span></span>



| <span data-ttu-id="13cbb-225">Требование</span><span class="sxs-lookup"><span data-stu-id="13cbb-225">Requirement</span></span> | <span data-ttu-id="13cbb-226">Значение</span><span class="sxs-lookup"><span data-stu-id="13cbb-226">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13cbb-227">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13cbb-227">Minimum supported client</span></span><br/> | <span data-ttu-id="13cbb-228">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="13cbb-228">None supported</span></span><br/>                                                               |
| <span data-ttu-id="13cbb-229">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13cbb-229">Minimum supported server</span></span><br/> | <span data-ttu-id="13cbb-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13cbb-230">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13cbb-231">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="13cbb-231">Namespace</span></span><br/>                | <span data-ttu-id="13cbb-232">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="13cbb-232">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="13cbb-233">MOF</span><span class="sxs-lookup"><span data-stu-id="13cbb-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13cbb-234"><dt>Тсаллов. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13cbb-234"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="13cbb-235">DLL</span><span class="sxs-lookup"><span data-stu-id="13cbb-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13cbb-236"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13cbb-236"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

