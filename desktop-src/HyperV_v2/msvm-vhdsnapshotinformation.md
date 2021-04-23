---
description: Предоставляет сведения о моментальном снимке в файле набора виртуальных жестких дисков.
ms.assetid: 922bf0b8-523d-488e-9a41-1a27594e2e44
title: Класс Msvm_VHDSnapshotInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSnapshotInformation
- Msvm_VHDSnapshotInformation.FilePath
- Msvm_VHDSnapshotInformation.SnapshotId
- Msvm_VHDSnapshotInformation.SnapshotPath
- Msvm_VHDSnapshotInformation.ParentPathsList
- Msvm_VHDSnapshotInformation.CreationTime
- Msvm_VHDSnapshotInformation.ResilientChangeTrackingId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1e2a573546d62d79170f15abddd8d5c17e30f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898054"
---
# <a name="msvm_vhdsnapshotinformation-class"></a><span data-ttu-id="27e02-103">\_Класс мсвм вхдснапшотинформатион</span><span class="sxs-lookup"><span data-stu-id="27e02-103">Msvm\_VHDSnapshotInformation class</span></span>

<span data-ttu-id="27e02-104">Предоставляет сведения о моментальном снимке в файле набора виртуальных жестких дисков</span><span class="sxs-lookup"><span data-stu-id="27e02-104">Provides information about a snapshot within a VHD Set file</span></span>

<span data-ttu-id="27e02-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="27e02-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="27e02-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27e02-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VHDSnapshotInformation
{
  string   FilePath;
  string   SnapshotId;
  string   SnapshotPath;
  string   ParentPathsList[];
  DATETIME CreationTime;
  string   ResilientChangeTrackingId;
};
```

## <a name="members"></a><span data-ttu-id="27e02-107">Члены</span><span class="sxs-lookup"><span data-stu-id="27e02-107">Members</span></span>

<span data-ttu-id="27e02-108">Класс **мсвм \_ вхдснапшотинформатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="27e02-108">The **Msvm\_VHDSnapshotInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="27e02-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="27e02-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="27e02-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="27e02-110">Properties</span></span>

<span data-ttu-id="27e02-111">Класс **мсвм \_ вхдснапшотинформатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="27e02-111">The **Msvm\_VHDSnapshotInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="27e02-112">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="27e02-112">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e02-113">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="27e02-113">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="27e02-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e02-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27e02-115">Дата и время создания моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="27e02-115">The date and time of this snapshot's creation.</span></span>

</dd> <dt>

<span data-ttu-id="27e02-116">**Равно**</span><span class="sxs-lookup"><span data-stu-id="27e02-116">**FilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e02-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="27e02-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e02-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e02-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27e02-119">Путь к файлу набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="27e02-119">The path of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="27e02-120">**парентпасслист**</span><span class="sxs-lookup"><span data-stu-id="27e02-120">**ParentPathsList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e02-121">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="27e02-121">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="27e02-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e02-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27e02-123">Список путей к файлам, представляющих все файлы, от которых зависит этот моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="27e02-123">A list of file paths representing all of the files on which this snapshot depends.</span></span> <span data-ttu-id="27e02-124">Это поле будет пустым, если не запрашивается специально.</span><span class="sxs-lookup"><span data-stu-id="27e02-124">This field will be empty unless specifically requested.</span></span> <span data-ttu-id="27e02-125">Первая запись — это непосредственный родительский элемент файла с последней записью корня.</span><span class="sxs-lookup"><span data-stu-id="27e02-125">The first entry is the file's immediate parent, with the last entry being the root.</span></span>

</dd> <dt>

<span data-ttu-id="27e02-126">**ресилиентчанжетраккингид**</span><span class="sxs-lookup"><span data-stu-id="27e02-126">**ResilientChangeTrackingId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e02-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="27e02-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e02-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e02-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27e02-129">Идентификатор отказоустойчивого отслеживания изменений (при наличии), связанный с этим моментальным снимком.</span><span class="sxs-lookup"><span data-stu-id="27e02-129">The resilient change tracking ID, if any, associated with this snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="27e02-130">**SnapshotId**</span><span class="sxs-lookup"><span data-stu-id="27e02-130">**SnapshotId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e02-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="27e02-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e02-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e02-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27e02-133">Идентификатор GUID, который однозначно определяет этот моментальный снимок в файле набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="27e02-133">A GUID that uniquely identifies this snapshot within the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="27e02-134">**снапшотпас**</span><span class="sxs-lookup"><span data-stu-id="27e02-134">**SnapshotPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e02-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="27e02-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e02-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e02-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27e02-137">Путь к файлу, представленному этим снимком.</span><span class="sxs-lookup"><span data-stu-id="27e02-137">The path of the file represented by this snapshot.</span></span> <span data-ttu-id="27e02-138">Это поле может быть пустым, если с этим моментальным снимком не связан ни один файл.</span><span class="sxs-lookup"><span data-stu-id="27e02-138">This field may be empty if there is no file associated with this snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27e02-139">Требования</span><span class="sxs-lookup"><span data-stu-id="27e02-139">Requirements</span></span>



| <span data-ttu-id="27e02-140">Требование</span><span class="sxs-lookup"><span data-stu-id="27e02-140">Requirement</span></span> | <span data-ttu-id="27e02-141">Значение</span><span class="sxs-lookup"><span data-stu-id="27e02-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27e02-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27e02-142">Minimum supported client</span></span><br/> | <span data-ttu-id="27e02-143">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="27e02-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="27e02-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27e02-144">Minimum supported server</span></span><br/> | <span data-ttu-id="27e02-145">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="27e02-145">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="27e02-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="27e02-146">Namespace</span></span><br/>                | <span data-ttu-id="27e02-147">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="27e02-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="27e02-148">MOF</span><span class="sxs-lookup"><span data-stu-id="27e02-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27e02-149"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27e02-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="27e02-150">DLL</span><span class="sxs-lookup"><span data-stu-id="27e02-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27e02-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="27e02-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




