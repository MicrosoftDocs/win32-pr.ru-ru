---
title: VIEW. backgroundColor
description: Атрибут backgroundColor указывает или получает цвет фона для представления или подпредставления.
ms.assetid: 02804e03-3518-4825-8ad0-bf91f74b5f74
keywords:
- Просмотреть. backgroundColor проигрыватель Windows Media
topic_type:
- apiref
api_name:
- VIEW.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73bbee10c6f442c9c03f46baa26251a7f6f85c22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648055"
---
# <a name="viewbackgroundcolor"></a><span data-ttu-id="a9870-104">VIEW. backgroundColor</span><span class="sxs-lookup"><span data-stu-id="a9870-104">VIEW.backgroundColor</span></span>

<span data-ttu-id="a9870-105">Атрибут **backgroundColor** указывает или получает цвет фона для **представления** или **подпредставления**.</span><span class="sxs-lookup"><span data-stu-id="a9870-105">The **backgroundColor** attribute specifies or retrieves the background color of the **VIEW** or **SUBVIEW**.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="a9870-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="a9870-106">Possible Values</span></span>

<span data-ttu-id="a9870-107">Этот атрибут является **строкой** для чтения и записи, содержащей любое значение цвета Microsoft Internet Explorer, или значение None.</span><span class="sxs-lookup"><span data-stu-id="a9870-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value or the value "none".</span></span> <span data-ttu-id="a9870-108">Он имеет значение по умолчанию "белый" для элементов **представления** или "нет" для элементов вложенного **представления** .</span><span class="sxs-lookup"><span data-stu-id="a9870-108">It has a default value of "white" for **VIEW** elements or "none" for **SUBVIEW** elements.</span></span>

<span data-ttu-id="a9870-109">Если в пакете загрузки Windows Media задан атрибут backgroundImage для элемента **View** , необходимо также указать атрибут **backgroundColor** для этого элемента.</span><span class="sxs-lookup"><span data-stu-id="a9870-109">In a Windows Media Download package, if you specify the backgroundImage attribute for a **VIEW** element, then you must also specify the **backgroundColor** attribute for that element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9870-110">Требования</span><span class="sxs-lookup"><span data-stu-id="a9870-110">Requirements</span></span>



| <span data-ttu-id="a9870-111">Требование</span><span class="sxs-lookup"><span data-stu-id="a9870-111">Requirement</span></span> | <span data-ttu-id="a9870-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a9870-112">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a9870-113">Версия</span><span class="sxs-lookup"><span data-stu-id="a9870-113">Version</span></span><br/> | <span data-ttu-id="a9870-114">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="a9870-114">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a9870-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9870-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9870-116">**Ссылка на цвет**</span><span class="sxs-lookup"><span data-stu-id="a9870-116">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="a9870-117">**VIEW, элемент**</span><span class="sxs-lookup"><span data-stu-id="a9870-117">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





