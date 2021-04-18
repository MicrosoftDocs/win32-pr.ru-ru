---
title: Амбиентаттрибутес. zIndex
description: Атрибут zIndex указывает или получает порядок, в котором отображается элемент управления.
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- Проигрыватель Windows Media Амбиентаттрибутес. zIndex
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52480cc387c0a9e5e45c4b8e8fd2dae4199dbd16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698953"
---
# <a name="ambientattributeszindex"></a><span data-ttu-id="cf305-104">Амбиентаттрибутес. zIndex</span><span class="sxs-lookup"><span data-stu-id="cf305-104">AmbientAttributes.zIndex</span></span>

<span data-ttu-id="cf305-105">Атрибут **zIndex** указывает или получает порядок, в котором отображается элемент управления.</span><span class="sxs-lookup"><span data-stu-id="cf305-105">The **zIndex** attribute specifies or retrieves the order in which the control is rendered.</span></span>

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a><span data-ttu-id="cf305-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="cf305-106">Possible Values</span></span>

<span data-ttu-id="cf305-107">Этот атрибут имеет **номер** для чтения и записи (**длинный**) со значением по умолчанию 0.</span><span class="sxs-lookup"><span data-stu-id="cf305-107">This attribute is a read/write **Number** (**long**) with a default value of zero.</span></span> <span data-ttu-id="cf305-108">Диапазон состоит из длинного целого числа со знаком.</span><span class="sxs-lookup"><span data-stu-id="cf305-108">The range is that of a signed long integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf305-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf305-109">Remarks</span></span>

<span data-ttu-id="cf305-110">Фоновый рисунок **представления** или **подпредставления** имеет фиксированный нулевой индекс, равный нулю.</span><span class="sxs-lookup"><span data-stu-id="cf305-110">The background bitmap of a **VIEW** or **SUBVIEW** has a fixed z index of zero.</span></span> <span data-ttu-id="cf305-111">Если требуется, чтобы элемент управления находящийся за фоном, **zIndex** должен иметь отрицательное значение.</span><span class="sxs-lookup"><span data-stu-id="cf305-111">If you want a control to be behind the background, the **zIndex** must be set to a negative number.</span></span>

<span data-ttu-id="cf305-112">Z-индекс **представления** или **подпредставления** является абсолютным индексом, а z-индексом элемента управления относительно индекса по оси z **представления** или **подпредставления** , содержащего его.</span><span class="sxs-lookup"><span data-stu-id="cf305-112">The z index of a **VIEW** or **SUBVIEW** is an absolute index, while the z index of a control is relative to the z index of the **VIEW** or **SUBVIEW** that contains it.</span></span>

<span data-ttu-id="cf305-113">Атрибут **zIndex** не поддерживается элементами **браузера** и **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="cf305-113">The **zIndex** attribute is not supported by the **BROWSER** and **PLAYLIST** elements.</span></span> <span data-ttu-id="cf305-114">Он не будет работать с элементом **Video** , если *видео*. **окно без окон** имеет значение false или элемент **Effects** , если он имеет **эффект**. для **окон** задано значение true.</span><span class="sxs-lookup"><span data-stu-id="cf305-114">It will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if **EFFECTS**.**windowed** is set to true.</span></span>

<span data-ttu-id="cf305-115">Элементы **буттонелемент** используют **zIndex** **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="cf305-115">**BUTTONELEMENT** elements use the **zIndex** of their **BUTTONGROUP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf305-116">Требования</span><span class="sxs-lookup"><span data-stu-id="cf305-116">Requirements</span></span>



| <span data-ttu-id="cf305-117">Требование</span><span class="sxs-lookup"><span data-stu-id="cf305-117">Requirement</span></span> | <span data-ttu-id="cf305-118">Значение</span><span class="sxs-lookup"><span data-stu-id="cf305-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="cf305-119">Версия</span><span class="sxs-lookup"><span data-stu-id="cf305-119">Version</span></span><br/> | <span data-ttu-id="cf305-120">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="cf305-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf305-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf305-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf305-122">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="cf305-122">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





