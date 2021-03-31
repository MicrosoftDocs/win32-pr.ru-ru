---
title: Паттернмап (Паттернмаплисттипе), элемент
description: Определяет сопоставление между двумя регулярными выражениями. Одно выражение используется для поиска соответствующей строки в строке сообщения, а другая — для изменения строки перед тем, как служба снова поместит ее в строку сообщения.
ms.assetid: 5cf28d38-4cc3-4a7b-a64b-3ad1cb42ebef
keywords:
- Журнал событий элемента Паттернмап
topic_type:
- apiref
api_name:
- patternMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ae29d60e39515a7c4b4db334f947abc44df5ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071052"
---
# <a name="patternmap-patternmaplisttype-element"></a><span data-ttu-id="240bd-105">Паттернмап (Паттернмаплисттипе), элемент</span><span class="sxs-lookup"><span data-stu-id="240bd-105">patternMap (PatternMapListType) Element</span></span>

<span data-ttu-id="240bd-106">Определяет сопоставление между двумя регулярными выражениями.</span><span class="sxs-lookup"><span data-stu-id="240bd-106">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="240bd-107">Одно выражение используется для поиска соответствующей строки в строке сообщения, а другая — для изменения строки перед тем, как служба снова поместит ее в строку сообщения.</span><span class="sxs-lookup"><span data-stu-id="240bd-107">One expression is used to find a matching string in the message string, and the other is used to alter the string before the service places it back in the message string.</span></span>

``` syntax
<xs:element name="patternMap"
    type="PatternMapType"
 />
```

<span data-ttu-id="240bd-108">Элемент **паттернмап** определяется сложным типом [**паттернмаплисттипе**](eventmanifestschema-patternmaplisttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="240bd-108">The **patternMap** element is defined by the [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="240bd-109">Требования</span><span class="sxs-lookup"><span data-stu-id="240bd-109">Requirements</span></span>



| <span data-ttu-id="240bd-110">Требование</span><span class="sxs-lookup"><span data-stu-id="240bd-110">Requirement</span></span> | <span data-ttu-id="240bd-111">Значение</span><span class="sxs-lookup"><span data-stu-id="240bd-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="240bd-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="240bd-112">Minimum supported client</span></span><br/> | <span data-ttu-id="240bd-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="240bd-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="240bd-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="240bd-114">Minimum supported server</span></span><br/> | <span data-ttu-id="240bd-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="240bd-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="240bd-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="240bd-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="240bd-117">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="240bd-117">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="240bd-118">**Паттернмапс (Намедкуеритипе)**</span><span class="sxs-lookup"><span data-stu-id="240bd-118">**patternMaps (NamedQueryType)**</span></span>](eventmanifestschema-patternmaps-namedquerytype-element.md)
</dt> </dl>

 

 





