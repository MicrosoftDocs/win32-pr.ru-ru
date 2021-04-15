---
title: TEXT. Скроллингделай
description: Атрибут Скроллингделай указывает или получает временную задержку между перемещениями с прокруткой.
ms.assetid: b965fe8f-c809-431f-b8fe-f7c3060068ac
keywords:
- Проигрыватель Windows Media TEXT. Скроллингделай
topic_type:
- apiref
api_name:
- TEXT.scrollingDelay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e81259ca84c62327bea67ae70d3f9ec3363450fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675607"
---
# <a name="textscrollingdelay"></a><span data-ttu-id="c5ace-104">TEXT. Скроллингделай</span><span class="sxs-lookup"><span data-stu-id="c5ace-104">TEXT.scrollingDelay</span></span>

<span data-ttu-id="c5ace-105">Атрибут **скроллингделай** указывает или получает временную задержку между перемещениями с прокруткой.</span><span class="sxs-lookup"><span data-stu-id="c5ace-105">The **scrollingDelay** attribute specifies or retrieves the time delay between scrolling movements.</span></span>

``` syntax
        elementID.scrollingDelay
```

## <a name="possible-values"></a><span data-ttu-id="c5ace-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="c5ace-106">Possible Values</span></span>

<span data-ttu-id="c5ace-107">Этот атрибут является **числом** для чтения и записи (**int**), задающим задержку в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="c5ace-107">This attribute is a read/write **Number** (**int**) specifying the delay in milliseconds.</span></span> <span data-ttu-id="c5ace-108">Он имеет минимальное значение 30, а значение по умолчанию — 85.</span><span class="sxs-lookup"><span data-stu-id="c5ace-108">It has a minimum value of 30, and a default value of 85.</span></span> <span data-ttu-id="c5ace-109">Если указано значение, меньшее минимального значения, используется значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c5ace-109">If a value less than the minimum is specified, the default is used.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5ace-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5ace-110">Remarks</span></span>

<span data-ttu-id="c5ace-111">Если для **прокрутки** задано значение false, **скроллингделай** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="c5ace-111">If **scrolling** is set to false, **scrollingDelay** is ignored.</span></span>

<span data-ttu-id="c5ace-112">См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.</span><span class="sxs-lookup"><span data-stu-id="c5ace-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ace-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c5ace-113">Requirements</span></span>



| <span data-ttu-id="c5ace-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c5ace-114">Requirement</span></span> | <span data-ttu-id="c5ace-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c5ace-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c5ace-116">Версия</span><span class="sxs-lookup"><span data-stu-id="c5ace-116">Version</span></span><br/> | <span data-ttu-id="c5ace-117">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="c5ace-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5ace-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5ace-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ace-119">**TEXT, элемент**</span><span class="sxs-lookup"><span data-stu-id="c5ace-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="c5ace-120">**TEXT. Scroll**</span><span class="sxs-lookup"><span data-stu-id="c5ace-120">**TEXT.scrolling**</span></span>](text-scrolling.md)
</dt> </dl>

 

 





