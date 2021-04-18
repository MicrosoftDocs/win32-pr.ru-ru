---
title: ПОЛЗУНок. Усефореграундпрогресс
description: Атрибут Усефореграундпрогресс указывает или получает значение, указывающее, будет ли использоваться основной индикатор выполнения.
ms.assetid: 10f3b4d9-ba82-4e30-affa-50c15a809ed6
keywords:
- ПОЛЗУНок. Усефореграундпрогресс Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.useForegroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b572933549417713158acea1a24fa9e1434c9dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657011"
---
# <a name="slideruseforegroundprogress"></a><span data-ttu-id="717c5-104">ПОЛЗУНок. Усефореграундпрогресс</span><span class="sxs-lookup"><span data-stu-id="717c5-104">SLIDER.useForegroundProgress</span></span>

<span data-ttu-id="717c5-105">Атрибут **усефореграундпрогресс** указывает или получает значение, указывающее, будет ли использоваться основной индикатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="717c5-105">The **useForegroundProgress** attribute specifies or retrieves a value indicating whether the foreground progress bar will be used.</span></span>

``` syntax
        elementID.useForegroundProgress
```

## <a name="possible-values"></a><span data-ttu-id="717c5-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="717c5-106">Possible Values</span></span>

<span data-ttu-id="717c5-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="717c5-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="717c5-108">Значение</span><span class="sxs-lookup"><span data-stu-id="717c5-108">Value</span></span> | <span data-ttu-id="717c5-109">Описание</span><span class="sxs-lookup"><span data-stu-id="717c5-109">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="717c5-110">true</span><span class="sxs-lookup"><span data-stu-id="717c5-110">true</span></span>  | <span data-ttu-id="717c5-111">Использовать основной ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="717c5-111">Use foreground progress.</span></span>                 |
| <span data-ttu-id="717c5-112">false</span><span class="sxs-lookup"><span data-stu-id="717c5-112">false</span></span> | <span data-ttu-id="717c5-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="717c5-113">Default.</span></span> <span data-ttu-id="717c5-114">Не используйте основной ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="717c5-114">Do not use foreground progress.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="717c5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="717c5-115">Remarks</span></span>

<span data-ttu-id="717c5-116">Этот атрибут позволяет использовать атрибут **фореграундпрогресс** , который в основном используется для отслеживания хода загрузки файла мультимедиа при одновременной отслеживании текущей позицией воспроизведения файла с помощью атрибута **value** .</span><span class="sxs-lookup"><span data-stu-id="717c5-116">This attribute allows the use of the **foregroundProgress** attribute, which is used primarily to track the download progress of a media file while simultaneously tracking the current play position of the file using the **value** attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="717c5-117">Требования</span><span class="sxs-lookup"><span data-stu-id="717c5-117">Requirements</span></span>



| <span data-ttu-id="717c5-118">Требование</span><span class="sxs-lookup"><span data-stu-id="717c5-118">Requirement</span></span> | <span data-ttu-id="717c5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="717c5-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="717c5-120">Версия</span><span class="sxs-lookup"><span data-stu-id="717c5-120">Version</span></span><br/> | <span data-ttu-id="717c5-121">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="717c5-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="717c5-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="717c5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="717c5-123">**Элемент SLIDER**</span><span class="sxs-lookup"><span data-stu-id="717c5-123">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="717c5-124">**ПОЛЗУНок. Фореграундпрогресс**</span><span class="sxs-lookup"><span data-stu-id="717c5-124">**SLIDER.foregroundProgress**</span></span>](slider-foregroundprogress.md)
</dt> <dt>

[<span data-ttu-id="717c5-125">**ПОЛЗУНок. Value**</span><span class="sxs-lookup"><span data-stu-id="717c5-125">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





