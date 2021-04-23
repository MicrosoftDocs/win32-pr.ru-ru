---
title: attribute_onchange
description: Когда атрибут обложки изменяет значение, возникает событие, которое может быть обработано обработчиком событий. Имя обработчика событий — это имя атрибута, за которым следует символ подчеркивания и \ 0034; OnChange \ 0034;, например \ 0034; значение \_ onChange \ 0034;.
ms.assetid: 783b686c-d56c-4036-9af4-97b9b246ef7e
keywords:
- attribute_onchange проигрыватель Windows Media
topic_type:
- apiref
api_name:
- attribute_onchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c4955193507e258d055a3399fc565c569fd291
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698838"
---
# <a name="attribute_onchange"></a><span data-ttu-id="b22cf-105">атрибут \_ onChange</span><span class="sxs-lookup"><span data-stu-id="b22cf-105">attribute\_onchange</span></span>

<span data-ttu-id="b22cf-106">Когда атрибут обложки изменяет значение, возникает событие, которое может быть обработано обработчиком событий.</span><span class="sxs-lookup"><span data-stu-id="b22cf-106">When a skin attribute changes value, an event occurs that can be handled by an event handler.</span></span> <span data-ttu-id="b22cf-107">Имя обработчика событий — это имя атрибута, за которым следует символ подчеркивания и "OnChange", например "значение \_ onChange".</span><span class="sxs-lookup"><span data-stu-id="b22cf-107">The name of the event handler is the name of the attribute followed by an underscore and "onchange", such as "value\_onchange".</span></span>

``` syntax
        attribute_onchange
```

## <a name="examples"></a><span data-ttu-id="b22cf-108">Примеры</span><span class="sxs-lookup"><span data-stu-id="b22cf-108">Examples</span></span>


```JScript
<SLIDER 
  thumbImage = "thumb.gif"
  value_onchange = "JScript: if (value == 100) backgroundColor = 'green';"
/>

```



## <a name="requirements"></a><span data-ttu-id="b22cf-109">Требования</span><span class="sxs-lookup"><span data-stu-id="b22cf-109">Requirements</span></span>



| <span data-ttu-id="b22cf-110">Требование</span><span class="sxs-lookup"><span data-stu-id="b22cf-110">Requirement</span></span> | <span data-ttu-id="b22cf-111">Значение</span><span class="sxs-lookup"><span data-stu-id="b22cf-111">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="b22cf-112">Версия</span><span class="sxs-lookup"><span data-stu-id="b22cf-112">Version</span></span><br/> | <span data-ttu-id="b22cf-113">Проигрыватель Windows Media версии 70 или более поздней</span><span class="sxs-lookup"><span data-stu-id="b22cf-113">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b22cf-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b22cf-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b22cf-115">**Обработчики событий окружения**</span><span class="sxs-lookup"><span data-stu-id="b22cf-115">**Ambient Event Handlers**</span></span>](ambient-event-handlers.md)
</dt> </dl>

 

 





