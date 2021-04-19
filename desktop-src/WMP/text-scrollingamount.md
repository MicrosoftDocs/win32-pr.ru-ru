---
title: TEXT. Скроллингамаунт
description: Атрибут Скроллингамаунт указывает или получает количество пикселей, на которое текст перемещается при каждом перемещении прокрутки.
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- Проигрыватель Windows Media TEXT. Скроллингамаунт
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66de7bfc6001f10c429d05c480dc315edfe72f76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675608"
---
# <a name="textscrollingamount"></a><span data-ttu-id="8f8d7-104">TEXT. Скроллингамаунт</span><span class="sxs-lookup"><span data-stu-id="8f8d7-104">TEXT.scrollingAmount</span></span>

<span data-ttu-id="8f8d7-105">Атрибут **скроллингамаунт** указывает или получает количество пикселей, на которое текст перемещается при каждом перемещении прокрутки.</span><span class="sxs-lookup"><span data-stu-id="8f8d7-105">The **scrollingAmount** attribute specifies or retrieves the number of pixels that the text moves during each scrolling movement.</span></span>

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a><span data-ttu-id="8f8d7-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="8f8d7-106">Possible Values</span></span>

<span data-ttu-id="8f8d7-107">Этот атрибут является положительным **числом** для чтения и записи (**int**) со значением по умолчанию 6.</span><span class="sxs-lookup"><span data-stu-id="8f8d7-107">This attribute is a positive read/write **Number** (**int**) with a default value of 6.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f8d7-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f8d7-108">Remarks</span></span>

<span data-ttu-id="8f8d7-109">Для плавной прокрутки **скроллингамаунт** должны быть небольшими.</span><span class="sxs-lookup"><span data-stu-id="8f8d7-109">For smooth scrolling, **scrollingAmount** should be small.</span></span> <span data-ttu-id="8f8d7-110">Для быстрого рисования с большими промежутками **скроллингамаунт** должно быть больше.</span><span class="sxs-lookup"><span data-stu-id="8f8d7-110">For fast drawing with big gaps, the **scrollingAmount** should be larger.</span></span> <span data-ttu-id="8f8d7-111">Если **Scroll** = "false", **скроллингамаунт** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8f8d7-111">If **scrolling** ="false", **scrollingAmount** is ignored.</span></span>

<span data-ttu-id="8f8d7-112">См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.</span><span class="sxs-lookup"><span data-stu-id="8f8d7-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f8d7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8f8d7-113">Requirements</span></span>



| <span data-ttu-id="8f8d7-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8f8d7-114">Requirement</span></span> | <span data-ttu-id="8f8d7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8f8d7-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8f8d7-116">Версия</span><span class="sxs-lookup"><span data-stu-id="8f8d7-116">Version</span></span><br/> | <span data-ttu-id="8f8d7-117">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="8f8d7-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8f8d7-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f8d7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f8d7-119">**TEXT, элемент**</span><span class="sxs-lookup"><span data-stu-id="8f8d7-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="8f8d7-120">**TEXT. Scroll**</span><span class="sxs-lookup"><span data-stu-id="8f8d7-120">**TEXT.scrolling**</span></span>](text-scrolling.md)
</dt> </dl>

 

 





