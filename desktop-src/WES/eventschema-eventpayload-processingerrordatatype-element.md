---
title: Евентпайлоад (Процессинжеррордататипе), элемент
description: Содержит двоичные данные событий для события, которое привело к ошибке при обработке данных события.
ms.assetid: 0ba72d72-8f43-40ca-b3ee-89fe27a4dd07
keywords:
- Журнал событий элемента Евентпайлоад
topic_type:
- apiref
api_name:
- EventPayload
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4dd20f95924282ae8cb0f1b0604c0e77d07766ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691786"
---
# <a name="eventpayload-processingerrordatatype-element"></a><span data-ttu-id="c91fb-104">Евентпайлоад (Процессинжеррордататипе), элемент</span><span class="sxs-lookup"><span data-stu-id="c91fb-104">EventPayload (ProcessingErrorDataType) Element</span></span>

<span data-ttu-id="c91fb-105">Содержит двоичные данные событий для события, которое привело к ошибке при обработке данных события.</span><span class="sxs-lookup"><span data-stu-id="c91fb-105">Contains binary event data for the event that caused an error when the event data was processed.</span></span>

``` syntax
<xs:element name="EventPayload"
    type="hexBinary"
 />
```

<span data-ttu-id="c91fb-106">Элемент **евентпайлоад** определяется сложным типом [**процессинжеррордататипе**](eventschema-processingerrordatatype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c91fb-106">The **EventPayload** element is defined by the [**ProcessingErrorDataType**](eventschema-processingerrordatatype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c91fb-107">Требования</span><span class="sxs-lookup"><span data-stu-id="c91fb-107">Requirements</span></span>



| <span data-ttu-id="c91fb-108">Требование</span><span class="sxs-lookup"><span data-stu-id="c91fb-108">Requirement</span></span> | <span data-ttu-id="c91fb-109">Значение</span><span class="sxs-lookup"><span data-stu-id="c91fb-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c91fb-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c91fb-110">Minimum supported client</span></span><br/> | <span data-ttu-id="c91fb-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c91fb-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c91fb-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c91fb-112">Minimum supported server</span></span><br/> | <span data-ttu-id="c91fb-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c91fb-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c91fb-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c91fb-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="c91fb-115">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="c91fb-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="c91fb-116">**Процессинжеррордата (EventType)**</span><span class="sxs-lookup"><span data-stu-id="c91fb-116">**ProcessingErrorData (EventType)**</span></span>](eventschema-processingerrordata-eventtype-element.md)
</dt> </dl>

 

 





