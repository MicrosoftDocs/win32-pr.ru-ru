---
title: Амбиентаттрибутес. Клиппингколор
description: Атрибут Клиппингколор указывает или получает цвет для отсечения из точечного рисунка Клиппингимаже.
ms.assetid: d6ea43d3-c118-43d3-bfdc-29ddd6ea4978
keywords:
- Проигрыватель Windows Media Амбиентаттрибутес. Клиппингколор
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad526eb0f705d1fce95f3813a666420b29db9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698929"
---
# <a name="ambientattributesclippingcolor"></a><span data-ttu-id="8b548-104">Амбиентаттрибутес. Клиппингколор</span><span class="sxs-lookup"><span data-stu-id="8b548-104">AmbientAttributes.clippingColor</span></span>

<span data-ttu-id="8b548-105">Атрибут **клиппингколор** указывает или получает цвет для отсечения из точечного рисунка **клиппингимаже** .</span><span class="sxs-lookup"><span data-stu-id="8b548-105">The **clippingColor** attribute specifies or retrieves the color to clip out from the **clippingImage** bitmap.</span></span>

``` syntax
        elementID.clippingColor
```

## <a name="possible-values"></a><span data-ttu-id="8b548-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="8b548-106">Possible Values</span></span>

<span data-ttu-id="8b548-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8b548-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="8b548-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8b548-108">Value</span></span>                                       | <span data-ttu-id="8b548-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8b548-109">Description</span></span>                                       |
|---------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="8b548-110">Auto (Автоматически)</span><span class="sxs-lookup"><span data-stu-id="8b548-110">Auto</span></span>                                        | <span data-ttu-id="8b548-111">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8b548-111">Default.</span></span> <span data-ttu-id="8b548-112">Используется цвет в пиксельном расположении 0, 0.</span><span class="sxs-lookup"><span data-stu-id="8b548-112">The color at pixel location 0,0 is used.</span></span> |
| <span data-ttu-id="8b548-113">любое значение цвета Microsoft Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="8b548-113">any Microsoft Internet Explorer color value</span></span> | <span data-ttu-id="8b548-114">Используется указанный цвет Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="8b548-114">The specified Internet Explorer color is used.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="8b548-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b548-115">Remarks</span></span>

<span data-ttu-id="8b548-116">Цвет обрезки указывает области **клиппингимаже** (или **фонового** изображения для **представления** или **подпредставления**), которые соответствуют прозрачным нещелчкам части элемента управления.</span><span class="sxs-lookup"><span data-stu-id="8b548-116">The clipping color indicates the regions of the **clippingImage** (or **backgroundImage** for **VIEW** or **SUBVIEW**) that correspond to transparent, non-clickable portions of the control.</span></span> <span data-ttu-id="8b548-117">Отсеченный цвет может указывать на несколько областей для обрезки. Предупреждение выдается, если **клиппингимаже** является JPG, чтобы предупредить потери цвета в жпгс.</span><span class="sxs-lookup"><span data-stu-id="8b548-117">The clipping color can indicate multiple regions to be clipped out. A warning is issued if the **clippingImage** is a JPG to warn of loss of color in JPGs.</span></span>

<span data-ttu-id="8b548-118">Атрибут **клиппингколор** не поддерживается элементом **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="8b548-118">The **clippingColor** attribute is not supported by the **PLAYLIST** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b548-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8b548-119">Requirements</span></span>



| <span data-ttu-id="8b548-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8b548-120">Requirement</span></span> | <span data-ttu-id="8b548-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8b548-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8b548-122">Версия</span><span class="sxs-lookup"><span data-stu-id="8b548-122">Version</span></span><br/> | <span data-ttu-id="8b548-123">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="8b548-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8b548-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b548-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b548-125">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="8b548-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b548-126">**Амбиентаттрибутес. Клиппингимаже**</span><span class="sxs-lookup"><span data-stu-id="8b548-126">**AmbientAttributes.clippingImage**</span></span>](ambientattributes-clippingimage.md)
</dt> <dt>

[<span data-ttu-id="8b548-127">**Ссылка на цвет**</span><span class="sxs-lookup"><span data-stu-id="8b548-127">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





