---
title: VIEW. Ресизебаккграундимаже
description: Атрибут Ресизебаккграундимаже указывает или получает значение, указывающее, можно ли изменить размер фонового изображения.
ms.assetid: d18f3def-777f-4a71-961e-73bae98a4c64
keywords:
- Просмотреть. Ресизебаккграундимаже проигрыватель Windows Media
topic_type:
- apiref
api_name:
- VIEW.resizeBackgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397929d69cc6ac6ad51c29883898c153218afdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105714088"
---
# <a name="viewresizebackgroundimage"></a><span data-ttu-id="527b0-104">VIEW. Ресизебаккграундимаже</span><span class="sxs-lookup"><span data-stu-id="527b0-104">VIEW.resizeBackgroundImage</span></span>

<span data-ttu-id="527b0-105">Атрибут **ресизебаккграундимаже** указывает или получает значение, указывающее, можно ли изменить размер фонового изображения.</span><span class="sxs-lookup"><span data-stu-id="527b0-105">The **resizeBackgroundImage** attribute specifies or retrieves a value indicating whether the background image can be resized.</span></span>

``` syntax
        elementID.resizeBackgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="527b0-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="527b0-106">Possible Values</span></span>

<span data-ttu-id="527b0-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="527b0-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="527b0-108">Значения</span><span class="sxs-lookup"><span data-stu-id="527b0-108">Values</span></span> | <span data-ttu-id="527b0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="527b0-109">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="527b0-110">true</span><span class="sxs-lookup"><span data-stu-id="527b0-110">true</span></span>   | <span data-ttu-id="527b0-111">Размер фонового изображения можно изменить.</span><span class="sxs-lookup"><span data-stu-id="527b0-111">The background image can be resized.</span></span>             |
| <span data-ttu-id="527b0-112">false</span><span class="sxs-lookup"><span data-stu-id="527b0-112">false</span></span>  | <span data-ttu-id="527b0-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="527b0-113">Default.</span></span> <span data-ttu-id="527b0-114">Размер фонового изображения не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="527b0-114">The background image cannot be resized.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="527b0-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="527b0-115">Remarks</span></span>

<span data-ttu-id="527b0-116">Если задать для этого атрибута значение true, размер фонового изображения изменится в соответствии с текущими значениями атрибутов **Width** и **Height** .</span><span class="sxs-lookup"><span data-stu-id="527b0-116">If you set this attribute to true, the background image will resize to fit the current values of the **width** and **height** attributes.</span></span>

## <a name="requirements"></a><span data-ttu-id="527b0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="527b0-117">Requirements</span></span>



| <span data-ttu-id="527b0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="527b0-118">Requirement</span></span> | <span data-ttu-id="527b0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="527b0-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="527b0-120">Версия</span><span class="sxs-lookup"><span data-stu-id="527b0-120">Version</span></span><br/> | <span data-ttu-id="527b0-121">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="527b0-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="527b0-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="527b0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="527b0-123">**VIEW, элемент**</span><span class="sxs-lookup"><span data-stu-id="527b0-123">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="527b0-124">**Просмотр. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="527b0-124">**VIEW.backgroundImage**</span></span>](view-backgroundimage.md)
</dt> </dl>

 

 





