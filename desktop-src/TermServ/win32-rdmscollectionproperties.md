---
title: Класс Win32_RDMSCollectionProperties
description: Управляет свойствами коллекции виртуальных рабочих столов.
ms.assetid: 8c533284-aa7b-4c47-b0a3-33307c4c805b
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSCollectionProperties службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSCollectionProperties, описание
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties
- Win32_RDMSCollectionProperties.Alias
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopMachineName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopHost
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopGuid
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopOsversion
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRamsizeMB
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopArchitecture
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRemoteFX
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopAdapters
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7397ccc1afd350689ac1eeb984a62177140f50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415324"
---
# <a name="win32_rdmscollectionproperties-class"></a><span data-ttu-id="c4244-105">\_Класс Win32 рдмсколлектионпропертиес</span><span class="sxs-lookup"><span data-stu-id="c4244-105">Win32\_RDMSCollectionProperties class</span></span>

<span data-ttu-id="c4244-106">Управляет свойствами коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c4244-106">Manages the properties of a virtual desktop collection.</span></span>

<span data-ttu-id="c4244-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c4244-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4244-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4244-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSCollectionProperties
{
  string  Alias;
  string  ReferenceVirtualDesktopName;
  string  ReferenceVirtualDesktopMachineName;
  string  ReferenceVirtualDesktopHost;
  string  ReferenceVirtualDesktopGuid;
  string  ReferenceVirtualDesktopOsversion;
  uint32  ReferenceVirtualDesktopRamsizeMB;
  string  ReferenceVirtualDesktopArchitecture;
  boolean ReferenceVirtualDesktopRemoteFX = false;
  string  ReferenceVirtualDesktopAdapters[];
};
```

## <a name="members"></a><span data-ttu-id="c4244-109">Члены</span><span class="sxs-lookup"><span data-stu-id="c4244-109">Members</span></span>

<span data-ttu-id="c4244-110">Класс **Win32 \_ рдмсколлектионпропертиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c4244-110">The **Win32\_RDMSCollectionProperties** class has these types of members:</span></span>

-   [<span data-ttu-id="c4244-111">Методы</span><span class="sxs-lookup"><span data-stu-id="c4244-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c4244-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="c4244-112">Properties</span></span>](/windows)

### <a name="methods"></a><span data-ttu-id="c4244-113">Методы</span><span class="sxs-lookup"><span data-stu-id="c4244-113">Methods</span></span>

<span data-ttu-id="c4244-114">Класс **Win32 \_ рдмсколлектионпропертиес** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c4244-114">The **Win32\_RDMSCollectionProperties** class has these methods.</span></span>



| <span data-ttu-id="c4244-115">Метод</span><span class="sxs-lookup"><span data-stu-id="c4244-115">Method</span></span>                                                                                        | <span data-ttu-id="c4244-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c4244-116">Description</span></span>                                                                         |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4244-117">**жетпровисионингпропертиес**</span><span class="sxs-lookup"><span data-stu-id="c4244-117">**GetProvisioningProperties**</span></span>](getprovisioningproperties-win32-rdmscollectionproperties.md) | <span data-ttu-id="c4244-118">Извлекает свойства подготовки коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c4244-118">Retrieves the provisioning properties of the virtual desktop collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c4244-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="c4244-119">Properties</span></span>

<span data-ttu-id="c4244-120">Класс **Win32 \_ рдмсколлектионпропертиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c4244-120">The **Win32\_RDMSCollectionProperties** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4244-121">**Псевдоним**</span><span class="sxs-lookup"><span data-stu-id="c4244-121">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4244-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4244-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4244-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4244-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4244-124">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c4244-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c4244-125">Возвращает псевдоним коллекции.</span><span class="sxs-lookup"><span data-stu-id="c4244-125">Gets the alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="c4244-126">**референцевиртуалдесктопадаптерс**</span><span class="sxs-lookup"><span data-stu-id="c4244-126">**ReferenceVirtualDesktopAdapters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4244-127">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c4244-127">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c4244-128">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c4244-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4244-129">Возвращает и задает имена виртуальных сетевых адаптеров главной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c4244-129">Gets and sets the names of the virtual network adapters of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="c4244-130">**референцевиртуалдесктопарчитектуре**</span><span class="sxs-lookup"><span data-stu-id="c4244-130">**ReferenceVirtualDesktopArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4244-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4244-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4244-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c4244-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4244-133">Возвращает и задает архитектуру процессора для главной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c4244-133">Gets and sets the processor architecture of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="c4244-134">**референцевиртуалдесктопгуид**</span><span class="sxs-lookup"><span data-stu-id="c4244-134">**ReferenceVirtualDesktopGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4244-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4244-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4244-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c4244-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4244-137">Возвращает и задает идентификатор GUID главной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c4244-137">Gets and sets the GUID of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="c4244-138">**референцевиртуалдесктофост**</span><span class="sxs-lookup"><span data-stu-id="c4244-138">**ReferenceVirtualDesktopHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4244-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4244-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4244-140">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c4244-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4244-141">Возвращает и задает имя главного сервера для главной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c4244-141">Gets and sets the host server name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="c4244-142">**референцевиртуалдесктопмачиненаме**</span><span class="sxs-lookup"><span data-stu-id="c4244-142">**ReferenceVirtualDesktopMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4244-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4244-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4244-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c4244-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4244-145">Возвращает и задает имя компьютера для главной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c4244-145">Gets and sets the machine name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="c4244-146">**референцевиртуалдесктопнаме**</span><span class="sxs-lookup"><span data-stu-id="c4244-146">**ReferenceVirtualDesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4244-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4244-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4244-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c4244-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4244-149">Возвращает и задает имя главной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c4244-149">Gets and sets the name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="c4244-150">**референцевиртуалдесктопосверсион**</span><span class="sxs-lookup"><span data-stu-id="c4244-150">**ReferenceVirtualDesktopOsversion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4244-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4244-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4244-152">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c4244-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4244-153">Возвращает и задает версию ОС главной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c4244-153">Gets and sets the OS version of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="c4244-154">**референцевиртуалдесктопрамсиземб**</span><span class="sxs-lookup"><span data-stu-id="c4244-154">**ReferenceVirtualDesktopRamsizeMB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4244-155">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c4244-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4244-156">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c4244-156">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4244-157">Возвращает и задает объем памяти для главной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c4244-157">Gets and sets the memory size of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="c4244-158">**референцевиртуалдесктопремотефкс**</span><span class="sxs-lookup"><span data-stu-id="c4244-158">**ReferenceVirtualDesktopRemoteFX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4244-159">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c4244-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4244-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c4244-160">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4244-161">Возвращает и задает значение, указывающее, включено ли RemoteFX для главной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c4244-161">Gets and sets a value that indicates whether RemoteFX is enabled for the master VM.</span></span> <span data-ttu-id="c4244-162">**Значение true** , если RemoteFX включен. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c4244-162">**TRUE** if RemoteFX is enabled; otherwise, **FALSE**.</span></span> <span data-ttu-id="c4244-163">Значение этого свойства по умолчанию равно **false**.</span><span class="sxs-lookup"><span data-stu-id="c4244-163">The default value for this property is **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4244-164">Требования</span><span class="sxs-lookup"><span data-stu-id="c4244-164">Requirements</span></span>



| <span data-ttu-id="c4244-165">Требование</span><span class="sxs-lookup"><span data-stu-id="c4244-165">Requirement</span></span> | <span data-ttu-id="c4244-166">Значение</span><span class="sxs-lookup"><span data-stu-id="c4244-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4244-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4244-167">Minimum supported client</span></span><br/> | <span data-ttu-id="c4244-168">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c4244-168">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c4244-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4244-169">Minimum supported server</span></span><br/> | <span data-ttu-id="c4244-170">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c4244-170">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c4244-171">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c4244-171">Namespace</span></span><br/>                | <span data-ttu-id="c4244-172">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="c4244-172">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c4244-173">MOF</span><span class="sxs-lookup"><span data-stu-id="c4244-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4244-174"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4244-174"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4244-175">DLL</span><span class="sxs-lookup"><span data-stu-id="c4244-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4244-176"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4244-176"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c4244-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4244-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4244-178">Поставщик служб удаленный рабочий стол Management Services</span><span class="sxs-lookup"><span data-stu-id="c4244-178">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

