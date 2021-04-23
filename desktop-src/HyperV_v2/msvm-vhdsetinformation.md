---
description: Предоставляет сведения о файле набора виртуальных жестких дисков.
ms.assetid: a975c131-d3f3-4be3-bc69-e277e3ce4d28
title: Класс Msvm_VHDSetInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSetInformation
- Msvm_VHDSetInformation.Path
- Msvm_VHDSetInformation.SnapshotIdList
- Msvm_VHDSetInformation.AllPaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 51f1371baea902627160c2c7a1fb31d156be8951
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683018"
---
# <a name="msvm_vhdsetinformation-class"></a><span data-ttu-id="6ae2d-103">\_Класс мсвм вхдсетинформатион</span><span class="sxs-lookup"><span data-stu-id="6ae2d-103">Msvm\_VHDSetInformation class</span></span>

<span data-ttu-id="6ae2d-104">Предоставляет сведения о файле набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="6ae2d-104">Provides information about a VHD Set file.</span></span>

<span data-ttu-id="6ae2d-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6ae2d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ae2d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ae2d-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VHDSetInformation
{
  string Path;
  string SnapshotIdList[];
  string AllPaths[];
};
```

## <a name="members"></a><span data-ttu-id="6ae2d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="6ae2d-107">Members</span></span>

<span data-ttu-id="6ae2d-108">Класс **мсвм \_ вхдсетинформатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6ae2d-108">The **Msvm\_VHDSetInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="6ae2d-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="6ae2d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ae2d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="6ae2d-110">Properties</span></span>

<span data-ttu-id="6ae2d-111">Класс **мсвм \_ вхдсетинформатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6ae2d-111">The **Msvm\_VHDSetInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ae2d-112">**аллпасс**</span><span class="sxs-lookup"><span data-stu-id="6ae2d-112">**AllPaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae2d-113">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="6ae2d-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6ae2d-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae2d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae2d-115">Список всех файлов, входящих в файл набора виртуальных жестких дисков, включая любые файлы, на которые нет ссылок, и все родительские элементы корневого виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="6ae2d-115">A list of all files encompassed by the VHD Set file, including any unreferenced files and any parents of the root virtual hard disk.</span></span> <span data-ttu-id="6ae2d-116">Этот файл набора ВИРТУАЛЬНЫХ жестких дисков не управляет всеми файлами, перечисленными после корневого виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="6ae2d-116">All files listed after the root virtual hard disk are unmanaged by this VHD Set file.</span></span> <span data-ttu-id="6ae2d-117">Это поле может быть пустым, если эти сведения не были специально запрошены.</span><span class="sxs-lookup"><span data-stu-id="6ae2d-117">This field may be empty if this information was not specifically requested.</span></span>

</dd> <dt>

<span data-ttu-id="6ae2d-118">**Путь**</span><span class="sxs-lookup"><span data-stu-id="6ae2d-118">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae2d-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6ae2d-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ae2d-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae2d-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae2d-121">Путь к файлу набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="6ae2d-121">The path of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="6ae2d-122">**снапшотидлист**</span><span class="sxs-lookup"><span data-stu-id="6ae2d-122">**SnapshotIdList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae2d-123">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="6ae2d-123">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6ae2d-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae2d-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae2d-125">Список идентификаторов GUID, представляющих все моментальные снимки, содержащиеся в этом файле набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="6ae2d-125">A list of GUIDs representing all of the snapshots contained by this VHD Set file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ae2d-126">Требования</span><span class="sxs-lookup"><span data-stu-id="6ae2d-126">Requirements</span></span>



| <span data-ttu-id="6ae2d-127">Требование</span><span class="sxs-lookup"><span data-stu-id="6ae2d-127">Requirement</span></span> | <span data-ttu-id="6ae2d-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6ae2d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae2d-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ae2d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6ae2d-130">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6ae2d-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6ae2d-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ae2d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6ae2d-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6ae2d-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6ae2d-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6ae2d-133">Namespace</span></span><br/>                | <span data-ttu-id="6ae2d-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6ae2d-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6ae2d-135">MOF</span><span class="sxs-lookup"><span data-stu-id="6ae2d-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ae2d-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ae2d-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ae2d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6ae2d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ae2d-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ae2d-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




