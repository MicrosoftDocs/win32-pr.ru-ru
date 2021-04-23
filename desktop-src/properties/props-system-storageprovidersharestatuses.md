---
description: Это свойство представляет список состояний общего ресурса для файла или папки, указанной поставщиком хранилища. Каждое состояние общей папки должно быть одним из известных значений, указанных в перечислениях Беловсторажепровидершарестатусес, является свойством только для чтения, оно должно обновляться только поставщиком хранилища.
ms.assetid: 131bf48a-0ab9-4b1f-9625-6fca5d15219f
title: System. Сторажепровидершарестатусес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92340e4afb1005146a32d2505292a5e60dec971
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693256"
---
# <a name="systemstorageprovidersharestatuses"></a><span data-ttu-id="f6489-103">System. Сторажепровидершарестатусес</span><span class="sxs-lookup"><span data-stu-id="f6489-103">System.StorageProviderShareStatuses</span></span>

<span data-ttu-id="f6489-104">Это свойство представляет список состояний общего ресурса для файла или папки, указанной поставщиком хранилища. Каждое состояние общей папки должно быть одним из известных значений, указанных в перечислениях Беловсторажепровидершарестатусес, является свойством только для чтения, оно должно обновляться только поставщиком хранилища.</span><span class="sxs-lookup"><span data-stu-id="f6489-104">This property represents a list of share statuses for the file/folder specified by the storage provider.Each share status must be one of the known value specified by the enumerations belowStorageProviderShareStatuses is a readonly property, it should only be updated by the storage provider.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="f6489-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f6489-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.StorageProviderShareStatuses
   shellPKey = PKEY_StorageProviderShareStatuses
   formatID = FCEFF153-E839-4CF3-A9E7-EA22832094B8
   propID = 111
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Multivalue String
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Private
            value = Private
            text = Private
            defineToken = STORAGE_PROVIDER_SHARE_STATUS_PRIVATE
            mnemonics = private
         enum
            name = Shared
            value = Shared
            text = Shared
            defineToken = STORAGE_PROVIDER_SHARE_STATUS_SHARED
            mnemonics = shared
         enum
            name = Public
            value = Public
            text = Public
            defineToken = STORAGE_PROVIDER_SHARE_STATUS_PUBLIC
            mnemonics = public
         enum
            name = Group
            value = Group
            text = Group
            defineToken = STORAGE_PROVIDER_SHARE_STATUS_GROUP
            mnemonics = group
         enum
            name = Owner
            value = Owner
            text = Owner
            defineToken = STORAGE_PROVIDER_SHARE_STATUS_OWNER
            mnemonics = owner
```

## <a name="remarks"></a><span data-ttu-id="f6489-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6489-106">Remarks</span></span>

<span data-ttu-id="f6489-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="f6489-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6489-108">См. также</span><span class="sxs-lookup"><span data-stu-id="f6489-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6489-109">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="f6489-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="f6489-110">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="f6489-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="f6489-111">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="f6489-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="f6489-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="f6489-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="f6489-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="f6489-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="f6489-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="f6489-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="f6489-115">булеанформат</span><span class="sxs-lookup"><span data-stu-id="f6489-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="f6489-116">numberFormat</span><span class="sxs-lookup"><span data-stu-id="f6489-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="f6489-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="f6489-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="f6489-118">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="f6489-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="f6489-119">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="f6489-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="f6489-120">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="f6489-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="f6489-121">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="f6489-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="f6489-122">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="f6489-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
