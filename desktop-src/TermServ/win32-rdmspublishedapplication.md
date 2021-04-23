---
title: Класс Win32_RDMSPublishedApplication
description: Управляет опубликованным приложением.
ms.assetid: 7a529f1d-1aaf-42fb-8469-92d38a7b0ffc
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSPublishedApplication службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSPublishedApplication, описание
topic_type:
- apiref
api_name:
- Win32_RDMSPublishedApplication
- Win32_RDMSPublishedApplication.AppAlias
- Win32_RDMSPublishedApplication.PoolName
- Win32_RDMSPublishedApplication.DisplayName
- Win32_RDMSPublishedApplication.ShowInPortal
- Win32_RDMSPublishedApplication.SecurityDescriptor
- Win32_RDMSPublishedApplication.AppPath
- Win32_RDMSPublishedApplication.VirtualPath
- Win32_RDMSPublishedApplication.CommandLineSetting
- Win32_RDMSPublishedApplication.RequiredCommandLine
- Win32_RDMSPublishedApplication.Folder
- Win32_RDMSPublishedApplication.IconPath
- Win32_RDMSPublishedApplication.IconIndex
- Win32_RDMSPublishedApplication.IconContents
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb003faf5e51c9da1f46f23c5f8d6b5ae977987c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341125"
---
# <a name="win32_rdmspublishedapplication-class"></a><span data-ttu-id="07d9d-105">\_Класс Win32 рдмспублишедаппликатион</span><span class="sxs-lookup"><span data-stu-id="07d9d-105">Win32\_RDMSPublishedApplication class</span></span>

<span data-ttu-id="07d9d-106">Управляет опубликованным приложением.</span><span class="sxs-lookup"><span data-stu-id="07d9d-106">Manages a published application.</span></span>

<span data-ttu-id="07d9d-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="07d9d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d9d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07d9d-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSPublishedApplication
{
  string  AppAlias;
  string  PoolName;
  string  DisplayName;
  boolean ShowInPortal;
  string  SecurityDescriptor;
  string  AppPath;
  string  VirtualPath;
  uint32  CommandLineSetting;
  string  RequiredCommandLine;
  string  Folder;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
};
```

## <a name="members"></a><span data-ttu-id="07d9d-109">Члены</span><span class="sxs-lookup"><span data-stu-id="07d9d-109">Members</span></span>

<span data-ttu-id="07d9d-110">Класс **Win32 \_ рдмспублишедаппликатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="07d9d-110">The **Win32\_RDMSPublishedApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="07d9d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="07d9d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="07d9d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="07d9d-112">Properties</span></span>

<span data-ttu-id="07d9d-113">Класс **Win32 \_ рдмспублишедаппликатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="07d9d-113">The **Win32\_RDMSPublishedApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="07d9d-114">**аппалиас**</span><span class="sxs-lookup"><span data-stu-id="07d9d-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d9d-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d9d-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d9d-116">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07d9d-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="07d9d-117">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="07d9d-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="07d9d-118">Возвращает и задает псевдоним приложения.</span><span class="sxs-lookup"><span data-stu-id="07d9d-118">Gets and sets the alias of the application.</span></span>

</dd> <dt>

<span data-ttu-id="07d9d-119">**AppPath**</span><span class="sxs-lookup"><span data-stu-id="07d9d-119">**AppPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d9d-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d9d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d9d-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07d9d-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="07d9d-122">Возвращает и задает путь к приложению.</span><span class="sxs-lookup"><span data-stu-id="07d9d-122">Gets and sets the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="07d9d-123">**коммандлинесеттинг**</span><span class="sxs-lookup"><span data-stu-id="07d9d-123">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d9d-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07d9d-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07d9d-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07d9d-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="07d9d-126">Возвращает и задает параметр командной строки для приложения.</span><span class="sxs-lookup"><span data-stu-id="07d9d-126">Gets and sets the command line setting for the application.</span></span>

<span data-ttu-id="07d9d-127">Это свойство может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="07d9d-127">This property can be set to one of the following values:</span></span>

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span data-ttu-id="07d9d-128"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**Доноталлов** (0)</span><span class="sxs-lookup"><span data-stu-id="07d9d-128"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span></span>


</dt> <dd>

<span data-ttu-id="07d9d-129">Не разрешать аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="07d9d-129">Do not allow command line arguments.</span></span>

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="07d9d-130"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Разрешить** (1)</span><span class="sxs-lookup"><span data-stu-id="07d9d-130"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow** (1)</span></span>


</dt> <dd>

<span data-ttu-id="07d9d-131">Разрешить аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="07d9d-131">Allow command line arguments.</span></span>

</dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span data-ttu-id="07d9d-132"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Требовать** (2)</span><span class="sxs-lookup"><span data-stu-id="07d9d-132"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Require** (2)</span></span>


</dt> <dd>

<span data-ttu-id="07d9d-133">Требовать аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="07d9d-133">Require command line arguments.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="07d9d-134">**Отображаемое имя**</span><span class="sxs-lookup"><span data-stu-id="07d9d-134">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d9d-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d9d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d9d-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07d9d-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="07d9d-137">Возвращает и задает отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="07d9d-137">Gets and sets the display name of the application.</span></span>

</dd> <dt>

<span data-ttu-id="07d9d-138">**Папка**</span><span class="sxs-lookup"><span data-stu-id="07d9d-138">**Folder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d9d-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d9d-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d9d-140">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07d9d-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="07d9d-141">Возвращает и задает путь к приложению.</span><span class="sxs-lookup"><span data-stu-id="07d9d-141">Gets and sets the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="07d9d-142">**иконконтентс**</span><span class="sxs-lookup"><span data-stu-id="07d9d-142">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d9d-143">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="07d9d-143">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="07d9d-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07d9d-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="07d9d-145">Возвращает и задает массив, содержащий значок приложения.</span><span class="sxs-lookup"><span data-stu-id="07d9d-145">Gets and sets an array that contains the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="07d9d-146">**икониндекс**</span><span class="sxs-lookup"><span data-stu-id="07d9d-146">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d9d-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="07d9d-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="07d9d-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07d9d-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="07d9d-149">Возвращает и задает индекс для значка приложения.</span><span class="sxs-lookup"><span data-stu-id="07d9d-149">Gets and sets the index for the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="07d9d-150">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="07d9d-150">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d9d-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d9d-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d9d-152">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07d9d-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="07d9d-153">Возвращает и задает путь к значку для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="07d9d-153">Gets and sets the path to the icon for this application.</span></span>

</dd> <dt>

<span data-ttu-id="07d9d-154">**PoolName**</span><span class="sxs-lookup"><span data-stu-id="07d9d-154">**PoolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d9d-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d9d-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d9d-156">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07d9d-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="07d9d-157">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="07d9d-157">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="07d9d-158">Возвращает и задает имя пула приложений приложения.</span><span class="sxs-lookup"><span data-stu-id="07d9d-158">Gets and sets the name of the application pool of the application.</span></span>

</dd> <dt>

<span data-ttu-id="07d9d-159">**рекуиредкоммандлине**</span><span class="sxs-lookup"><span data-stu-id="07d9d-159">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d9d-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d9d-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d9d-161">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07d9d-161">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="07d9d-162">Возвращает и задает аргументы командной строки, необходимые для приложения.</span><span class="sxs-lookup"><span data-stu-id="07d9d-162">Gets and sets the command line arguments that are required for the application</span></span>

</dd> <dt>

<span data-ttu-id="07d9d-163">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="07d9d-163">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d9d-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d9d-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d9d-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07d9d-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="07d9d-166">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="07d9d-166">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="07d9d-167">Возвращает и задает дескриптор безопасности, управляющий доступом к приложению, в формате языка определения дескрипторов безопасности (SDDL).</span><span class="sxs-lookup"><span data-stu-id="07d9d-167">Gets and sets the security descriptor that controls access to the application, in security descriptor definition language (SDDL) format.</span></span>

</dd> <dt>

<span data-ttu-id="07d9d-168">**шовинпортал**</span><span class="sxs-lookup"><span data-stu-id="07d9d-168">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d9d-169">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="07d9d-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="07d9d-170">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07d9d-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="07d9d-171">Указывает, следует ли отображать приложение в службах терминалов Веб-доступ (TS Веб-доступ).</span><span class="sxs-lookup"><span data-stu-id="07d9d-171">Indicates whether to display the application in Terminal Services Web Access (TS Web Access).</span></span> <span data-ttu-id="07d9d-172">**Значение true** , чтобы отобразить приложение в службах терминалов веб-доступ; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="07d9d-172">**TRUE** to display the application in TS Web Access; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="07d9d-173">**VirtualPath**</span><span class="sxs-lookup"><span data-stu-id="07d9d-173">**VirtualPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d9d-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d9d-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d9d-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07d9d-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="07d9d-176">Возвращает и задает виртуальный путь к приложению.</span><span class="sxs-lookup"><span data-stu-id="07d9d-176">Gets and sets the virtual path to the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07d9d-177">Требования</span><span class="sxs-lookup"><span data-stu-id="07d9d-177">Requirements</span></span>



| <span data-ttu-id="07d9d-178">Требование</span><span class="sxs-lookup"><span data-stu-id="07d9d-178">Requirement</span></span> | <span data-ttu-id="07d9d-179">Значение</span><span class="sxs-lookup"><span data-stu-id="07d9d-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="07d9d-180">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07d9d-180">Minimum supported client</span></span><br/> | <span data-ttu-id="07d9d-181">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="07d9d-181">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="07d9d-182">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07d9d-182">Minimum supported server</span></span><br/> | <span data-ttu-id="07d9d-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="07d9d-183">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="07d9d-184">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="07d9d-184">Namespace</span></span><br/>                | <span data-ttu-id="07d9d-185">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="07d9d-185">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="07d9d-186">MOF</span><span class="sxs-lookup"><span data-stu-id="07d9d-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07d9d-187"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07d9d-187"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="07d9d-188">DLL</span><span class="sxs-lookup"><span data-stu-id="07d9d-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07d9d-189"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07d9d-189"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="07d9d-190">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07d9d-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d9d-191">Поставщик служб удаленный рабочий стол Management Services</span><span class="sxs-lookup"><span data-stu-id="07d9d-191">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

