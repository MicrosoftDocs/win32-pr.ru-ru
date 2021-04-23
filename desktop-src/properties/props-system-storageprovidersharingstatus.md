---
description: Это свойство представляет собой наиболее разрешающее состояние общего ресурса для файла или папки, указанной поставщиком хранилища. Общий ресурс имеет состояние от большинства до наименьших разрешений принадлежит > совместного доступа > Public > Shared > Private. Сторажепровидершарингстатус является свойством только для чтения.
ms.assetid: c3b93159-4279-4b27-b006-ab73e0beee9c
title: System. Сторажепровидершарингстатус
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b5b6b23b3a541037511eee3ae7201252e4ec3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693290"
---
# <a name="systemstorageprovidersharingstatus"></a><span data-ttu-id="32fac-103">System. Сторажепровидершарингстатус</span><span class="sxs-lookup"><span data-stu-id="32fac-103">System.StorageProviderSharingStatus</span></span>

<span data-ttu-id="32fac-104">Это свойство представляет собой наиболее разрешающее состояние общего ресурса для файла или папки, указанной поставщиком хранилища. Общий ресурс имеет состояние от большинства до наименьших разрешений принадлежит > совместного доступа > Public > Shared > Private. Сторажепровидершарингстатус является свойством только для чтения.</span><span class="sxs-lookup"><span data-stu-id="32fac-104">This property represents a the most permissive share status for the file/folder specified by the storage provider.The share statuses from most to least permissive are Owned > Co-owned > Public > Shared > Private.StorageProviderSharingStatus is a readonly property.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="32fac-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="32fac-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.StorageProviderSharingStatus
   shellPKey = PKEY_StorageProviderSharingStatus
   formatID = FCEFF153-E839-4CF3-A9E7-EA22832094B8
   propID = 117
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotShared
            value = 0
            text
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_NOTSHARED
         enum
            name = Shared
            value = 1
            text = Shared
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_SHARED
         enum
            name = Private
            value = 2
            text
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_PRIVATE
         enum
            name = Public
            value = 3
            text = Public
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_PUBLIC
         enum
            name = SharedOwned
            value = 4
            text = Shared (co-owned, owner)
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_SHARED_OWNED
         enum
            name = SharedCoOwned
            value = 5
            text = Shared (co-owned)
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_SHARED_COOWNED
         enum
            name = PublicOwned
            value = 6
            text = Public (co-owned, owner)
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_PUBLIC_OWNED
         enum
            name = PublicCoOwned
            value = 7
            text = Public (co-owned)
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_PUBLIC_COOWNED
```

## <a name="remarks"></a><span data-ttu-id="32fac-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32fac-106">Remarks</span></span>

<span data-ttu-id="32fac-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="32fac-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32fac-108">См. также</span><span class="sxs-lookup"><span data-stu-id="32fac-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32fac-109">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="32fac-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="32fac-110">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="32fac-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="32fac-111">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="32fac-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="32fac-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="32fac-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="32fac-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="32fac-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="32fac-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="32fac-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="32fac-115">булеанформат</span><span class="sxs-lookup"><span data-stu-id="32fac-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="32fac-116">numberFormat</span><span class="sxs-lookup"><span data-stu-id="32fac-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="32fac-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="32fac-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="32fac-118">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="32fac-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="32fac-119">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="32fac-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="32fac-120">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="32fac-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="32fac-121">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="32fac-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="32fac-122">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="32fac-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
