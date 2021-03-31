---
title: Класс Win32_RDCentralPublishedRemoteApplication
description: Описывает приложение, опубликованное на другом компьютере для удаленного использования через службы терминалов.
ms.assetid: 8605bd1e-e825-4fd9-b14f-9d3bdac489f1
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDCentralPublishedRemoteApplication службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDCentralPublishedRemoteApplication, описание
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedRemoteApplication
- Win32_RDCentralPublishedRemoteApplication.Caption
- Win32_RDCentralPublishedRemoteApplication.Description
- Win32_RDCentralPublishedRemoteApplication.InstallDate
- Win32_RDCentralPublishedRemoteApplication.Name
- Win32_RDCentralPublishedRemoteApplication.Status
- Win32_RDCentralPublishedRemoteApplication.PublishingFarm
- Win32_RDCentralPublishedRemoteApplication.Alias
- Win32_RDCentralPublishedRemoteApplication.SecurityDescriptor
- Win32_RDCentralPublishedRemoteApplication.Path
- Win32_RDCentralPublishedRemoteApplication.VPath
- Win32_RDCentralPublishedRemoteApplication.IconContents
- Win32_RDCentralPublishedRemoteApplication.CommandLineSetting
- Win32_RDCentralPublishedRemoteApplication.RequiredCommandLine
- Win32_RDCentralPublishedRemoteApplication.ShowInPortal
- Win32_RDCentralPublishedRemoteApplication.AppID
- Win32_RDCentralPublishedRemoteApplication.RDPFileContents
- Win32_RDCentralPublishedRemoteApplication.Folders
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd837f62d8d0787d992e8eed7316ed1ef3f199ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988519"
---
# <a name="win32_rdcentralpublishedremoteapplication-class"></a><span data-ttu-id="a8c51-105">\_Класс Win32 рдцентралпублишедремотеаппликатион</span><span class="sxs-lookup"><span data-stu-id="a8c51-105">Win32\_RDCentralPublishedRemoteApplication class</span></span>

<span data-ttu-id="a8c51-106">Описывает приложение, опубликованное на другом компьютере для удаленного использования через службы терминалов.</span><span class="sxs-lookup"><span data-stu-id="a8c51-106">Describes an application published on another computer, for remote use through Terminal Services.</span></span>

<span data-ttu-id="a8c51-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a8c51-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8c51-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8c51-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedRemoteApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  string   Alias;
  string   SecurityDescriptor;
  string   Path;
  string   VPath;
  uint8    IconContents[];
  uint32   CommandLineSetting;
  string   RequiredCommandLine;
  boolean  ShowInPortal;
  string   AppID;
  string   RDPFileContents;
  string   Folders[];
};
```

## <a name="members"></a><span data-ttu-id="a8c51-109">Члены</span><span class="sxs-lookup"><span data-stu-id="a8c51-109">Members</span></span>

<span data-ttu-id="a8c51-110">Класс **Win32 \_ рдцентралпублишедремотеаппликатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a8c51-110">The **Win32\_RDCentralPublishedRemoteApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="a8c51-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a8c51-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8c51-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="a8c51-112">Properties</span></span>

<span data-ttu-id="a8c51-113">Класс **Win32 \_ рдцентралпублишедремотеаппликатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a8c51-113">The **Win32\_RDCentralPublishedRemoteApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8c51-114">**Псевдоним**</span><span class="sxs-lookup"><span data-stu-id="a8c51-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c51-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a8c51-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-116">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8c51-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-117">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a8c51-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a8c51-118">Псевдоним приложения.</span><span class="sxs-lookup"><span data-stu-id="a8c51-118">Alias of the application.</span></span>

</dd> <dt>

<span data-ttu-id="a8c51-119">**AppID**</span><span class="sxs-lookup"><span data-stu-id="a8c51-119">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c51-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a8c51-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8c51-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a8c51-122">AppID используется для закрепления на клиентах.</span><span class="sxs-lookup"><span data-stu-id="a8c51-122">AppID is used for pinning on the clients.</span></span>

</dd> <dt>

<span data-ttu-id="a8c51-123">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="a8c51-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c51-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a8c51-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8c51-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-126">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a8c51-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a8c51-127">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="a8c51-127">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="a8c51-128">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8c51-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8c51-129">**коммандлинесеттинг**</span><span class="sxs-lookup"><span data-stu-id="a8c51-129">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c51-130">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a8c51-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-131">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8c51-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a8c51-132">Требуются ли аргументы командной строки для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="a8c51-132">Whether command-line arguments are required for this application.</span></span>

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span data-ttu-id="a8c51-133"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**Доноталлов** (0)</span><span class="sxs-lookup"><span data-stu-id="a8c51-133"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a8c51-134">Запретить</span><span class="sxs-lookup"><span data-stu-id="a8c51-134">Do not allow</span></span>

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="a8c51-135"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Разрешить** (1)</span><span class="sxs-lookup"><span data-stu-id="a8c51-135"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span data-ttu-id="a8c51-136"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Требовать** (2)</span><span class="sxs-lookup"><span data-stu-id="a8c51-136"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Require** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a8c51-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a8c51-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c51-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a8c51-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8c51-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8c51-140">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a8c51-140">Description of the object.</span></span>

<span data-ttu-id="a8c51-141">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8c51-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8c51-142">**Папки**</span><span class="sxs-lookup"><span data-stu-id="a8c51-142">**Folders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c51-143">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="a8c51-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8c51-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a8c51-145">Список папок, в которых должен отображаться этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="a8c51-145">List of the folders where this resource should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="a8c51-146">**иконконтентс**</span><span class="sxs-lookup"><span data-stu-id="a8c51-146">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c51-147">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a8c51-147">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8c51-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-149">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a8c51-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a8c51-150">Содержимое значка, соответствующего приложению.</span><span class="sxs-lookup"><span data-stu-id="a8c51-150">Contents of the icon corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="a8c51-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a8c51-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c51-152">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a8c51-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8c51-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-154">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="a8c51-154">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="a8c51-155">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="a8c51-155">The date the object was installed.</span></span> <span data-ttu-id="a8c51-156">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="a8c51-156">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a8c51-157">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8c51-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8c51-158">**Name**</span><span class="sxs-lookup"><span data-stu-id="a8c51-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c51-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a8c51-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8c51-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8c51-161">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="a8c51-161">The name of the object.</span></span>

<span data-ttu-id="a8c51-162">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8c51-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8c51-163">**Путь**</span><span class="sxs-lookup"><span data-stu-id="a8c51-163">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c51-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a8c51-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8c51-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a8c51-166">Путь к приложению</span><span class="sxs-lookup"><span data-stu-id="a8c51-166">Path to the application</span></span>

</dd> <dt>

<span data-ttu-id="a8c51-167">**публишингфарм**</span><span class="sxs-lookup"><span data-stu-id="a8c51-167">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c51-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a8c51-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8c51-169">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-170">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a8c51-170">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a8c51-171">Псевдоним фермы, опубликовавшего приложение</span><span class="sxs-lookup"><span data-stu-id="a8c51-171">Alias of the farm that published the Application</span></span>

</dd> <dt>

<span data-ttu-id="a8c51-172">**рдпфилеконтентс**</span><span class="sxs-lookup"><span data-stu-id="a8c51-172">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c51-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a8c51-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8c51-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8c51-175">Содержимое RDP-файла, соответствующего приложению.</span><span class="sxs-lookup"><span data-stu-id="a8c51-175">Contents of the RDP file corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="a8c51-176">**рекуиредкоммандлине**</span><span class="sxs-lookup"><span data-stu-id="a8c51-176">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c51-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a8c51-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8c51-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a8c51-179">Аргументы командной строки, необходимые для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="a8c51-179">Command-line arguments required for this application.</span></span>

</dd> <dt>

<span data-ttu-id="a8c51-180">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a8c51-180">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c51-181">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a8c51-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-182">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8c51-182">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-183">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a8c51-183">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a8c51-184">Дескриптор безопасности, управляющий доступом к приложению, в формате SDDL.</span><span class="sxs-lookup"><span data-stu-id="a8c51-184">Security Descriptor controlling access to the application, in SDDL Format.</span></span> <span data-ttu-id="a8c51-185">Пустая строка подразумевает разрешение любой доступ.</span><span class="sxs-lookup"><span data-stu-id="a8c51-185">Empty string implies allow all access.</span></span>

</dd> <dt>

<span data-ttu-id="a8c51-186">**шовинпортал**</span><span class="sxs-lookup"><span data-stu-id="a8c51-186">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c51-187">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a8c51-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-188">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8c51-188">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a8c51-189">**значение true** , если это приложение должно отображаться на веб-доступ TS; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a8c51-189">**true** if this application should be shown in the TS Web Access; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="a8c51-190">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="a8c51-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c51-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a8c51-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8c51-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-193">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="a8c51-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="a8c51-194">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="a8c51-194">Current status of the object.</span></span> <span data-ttu-id="a8c51-195">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="a8c51-195">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a8c51-196">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="a8c51-196">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a8c51-197">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="a8c51-197">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a8c51-198">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="a8c51-198">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a8c51-199">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="a8c51-199">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a8c51-200">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8c51-200">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="a8c51-201">("ОК")</span><span class="sxs-lookup"><span data-stu-id="a8c51-201">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a8c51-202">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="a8c51-202">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a8c51-203">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="a8c51-203">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a8c51-204">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="a8c51-204">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a8c51-205">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="a8c51-205">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a8c51-206">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="a8c51-206">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a8c51-207">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="a8c51-207">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a8c51-208">("Служба")</span><span class="sxs-lookup"><span data-stu-id="a8c51-208">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a8c51-209">**впас**</span><span class="sxs-lookup"><span data-stu-id="a8c51-209">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8c51-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a8c51-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8c51-211">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8c51-211">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a8c51-212">Виртуальный путь к приложению.</span><span class="sxs-lookup"><span data-stu-id="a8c51-212">Virtual Path to the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8c51-213">Требования</span><span class="sxs-lookup"><span data-stu-id="a8c51-213">Requirements</span></span>



| <span data-ttu-id="a8c51-214">Требование</span><span class="sxs-lookup"><span data-stu-id="a8c51-214">Requirement</span></span> | <span data-ttu-id="a8c51-215">Значение</span><span class="sxs-lookup"><span data-stu-id="a8c51-215">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8c51-216">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8c51-216">Minimum supported client</span></span><br/> | <span data-ttu-id="a8c51-217">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a8c51-217">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a8c51-218">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8c51-218">Minimum supported server</span></span><br/> | <span data-ttu-id="a8c51-219">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a8c51-219">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="a8c51-220">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a8c51-220">Namespace</span></span><br/>                | <span data-ttu-id="a8c51-221">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="a8c51-221">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a8c51-222">MOF</span><span class="sxs-lookup"><span data-stu-id="a8c51-222">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8c51-223"><dt>Тскпуб. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8c51-223"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="a8c51-224">DLL</span><span class="sxs-lookup"><span data-stu-id="a8c51-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8c51-225"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8c51-225"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

