---
title: Просмотреть. заголовок
description: Атрибут заголовка строки получает значение, указывающее, отображается ли заголовок окна.
ms.assetid: 996aa2e0-0313-4a48-adcb-b82f76f38b6a
keywords:
- Просмотр. строка проигрывателя Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.titleBar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea225103913e3906cf6cd3b129943fbf9b9f165
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717883"
---
# <a name="viewtitlebar"></a><span data-ttu-id="e6c1c-104">Просмотреть. заголовок</span><span class="sxs-lookup"><span data-stu-id="e6c1c-104">VIEW.titleBar</span></span>

<span data-ttu-id="e6c1c-105">Атрибут **заголовка** строки получает значение, указывающее, отображается ли заголовок окна.</span><span class="sxs-lookup"><span data-stu-id="e6c1c-105">The **titleBar** attribute retrieves a value indicating whether the window title bar is shown.</span></span>

``` syntax
        elementID.titleBar
```

## <a name="possible-values"></a><span data-ttu-id="e6c1c-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="e6c1c-106">Possible Values</span></span>

<span data-ttu-id="e6c1c-107">Этот атрибут является **логическим значением**, доступным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e6c1c-107">This attribute is a read-only **Boolean**.</span></span>



| <span data-ttu-id="e6c1c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e6c1c-108">Value</span></span> | <span data-ttu-id="e6c1c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e6c1c-109">Description</span></span>                             |
|-------|-----------------------------------------|
| <span data-ttu-id="e6c1c-110">true</span><span class="sxs-lookup"><span data-stu-id="e6c1c-110">true</span></span>  | <span data-ttu-id="e6c1c-111">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e6c1c-111">Default.</span></span> <span data-ttu-id="e6c1c-112">Отобразится заголовок окна.</span><span class="sxs-lookup"><span data-stu-id="e6c1c-112">The window title bar is shown.</span></span> |
| <span data-ttu-id="e6c1c-113">false</span><span class="sxs-lookup"><span data-stu-id="e6c1c-113">false</span></span> | <span data-ttu-id="e6c1c-114">Заголовок окна не отображается.</span><span class="sxs-lookup"><span data-stu-id="e6c1c-114">The window title bar is not shown.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="e6c1c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6c1c-115">Remarks</span></span>

<span data-ttu-id="e6c1c-116">Если строка заголовка отображается, отобразятся поля элемента управления, сворачивания и закрытия.</span><span class="sxs-lookup"><span data-stu-id="e6c1c-116">If the title bar is shown, the control box, minimize, and close buttons will be shown.</span></span> <span data-ttu-id="e6c1c-117">Заголовок окна будет заголовком элемента **View** .</span><span class="sxs-lookup"><span data-stu-id="e6c1c-117">The title of the window will be the title of the **VIEW** element.</span></span>

<span data-ttu-id="e6c1c-118">Если параметру « **заголовок** окна» присвоено значение true и пользователь пытается изменить значение **видео. Zoom**, изменение не будет выполнено, если только Обложка не наблюдает за **масштабом** и не примет необходимые меры для изменения размера.</span><span class="sxs-lookup"><span data-stu-id="e6c1c-118">If **titleBar** is set to true and the user attempts to change the value of **Video.zoom**, the change will not take place unless the skin monitors **zoom** and takes appropriate action to resize itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6c1c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e6c1c-119">Requirements</span></span>



| <span data-ttu-id="e6c1c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e6c1c-120">Requirement</span></span> | <span data-ttu-id="e6c1c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e6c1c-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e6c1c-122">Версия</span><span class="sxs-lookup"><span data-stu-id="e6c1c-122">Version</span></span><br/> | <span data-ttu-id="e6c1c-123">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="e6c1c-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6c1c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6c1c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6c1c-125">**VIEW, элемент**</span><span class="sxs-lookup"><span data-stu-id="e6c1c-125">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="e6c1c-126">**Просмотреть. заголовок**</span><span class="sxs-lookup"><span data-stu-id="e6c1c-126">**VIEW.title**</span></span>](view-title.md)
</dt> <dt>

[<span data-ttu-id="e6c1c-127">**ВИДЕО. Zoom**</span><span class="sxs-lookup"><span data-stu-id="e6c1c-127">**VIDEO.zoom**</span></span>](video-zoom.md)
</dt> </dl>

 

 





