---
title: Элемент Metadata (Инструментатионманифест)
description: Содержит глобальные значения, на которые можно ссылаться в других манифестах.
ms.assetid: 5bf3bb1e-47c9-4d6e-86e3-3316e21b76b3
keywords:
- Журнал событий элемента метаданных
topic_type:
- apiref
api_name:
- metadata
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14dc8772dee66fcce9ff07e9918c11b463aa414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135166"
---
# <a name="metadata-instrumentationmanifest-element"></a><span data-ttu-id="01ed0-104">Элемент Metadata (Инструментатионманифест)</span><span class="sxs-lookup"><span data-stu-id="01ed0-104">metadata (instrumentationManifest) Element</span></span>

<span data-ttu-id="01ed0-105">Содержит глобальные значения, на которые можно ссылаться в других манифестах.</span><span class="sxs-lookup"><span data-stu-id="01ed0-105">Contains global values that you can reference in other manifests.</span></span> <span data-ttu-id="01ed0-106">Пример см. в файле Winmeta.xml, включенном в \\ папку Include Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="01ed0-106">For an example, see the Winmeta.xml file included in the \\Include folder of the Windows SDK.</span></span>

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

<span data-ttu-id="01ed0-107">Элемент **метаданных** определяется элементом [**инструментатионманифест**](eventmanifestschema-instrumentationmanifest-element.md) .</span><span class="sxs-lookup"><span data-stu-id="01ed0-107">The **metadata** element is defined by the [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="01ed0-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01ed0-108">Remarks</span></span>

<span data-ttu-id="01ed0-109">Несмотря на то, что можно создать манифест, содержащий раздел метаданных, служба не будет использовать ее. единственными метаданными, распознаваемыми службой, являются метаданные, найденные в файле Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="01ed0-109">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="requirements"></a><span data-ttu-id="01ed0-110">Требования</span><span class="sxs-lookup"><span data-stu-id="01ed0-110">Requirements</span></span>



| <span data-ttu-id="01ed0-111">Требование</span><span class="sxs-lookup"><span data-stu-id="01ed0-111">Requirement</span></span> | <span data-ttu-id="01ed0-112">Значение</span><span class="sxs-lookup"><span data-stu-id="01ed0-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="01ed0-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01ed0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="01ed0-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01ed0-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="01ed0-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01ed0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="01ed0-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="01ed0-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01ed0-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01ed0-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="01ed0-118">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="01ed0-118">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="01ed0-119">**инструментатионманифест**</span><span class="sxs-lookup"><span data-stu-id="01ed0-119">**instrumentationManifest**</span></span>](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 





