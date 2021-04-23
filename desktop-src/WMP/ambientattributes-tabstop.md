---
title: Амбиентаттрибутес. tabStop
description: Атрибут tabStop указывает или получает значение, указывающее, находится ли элемент управления в порядке перехода. Порядок табуляции задается путем размещения элемента управления в общем сценарии до или после других управляющих тегов.
ms.assetid: 3d4b7fe4-1032-44e1-bae5-f253d00881bf
keywords:
- Проигрыватель Windows Media Амбиентаттрибутес. tabStop
topic_type:
- apiref
api_name:
- AmbientAttributes.tabStop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4005fc26a2bc5f928cde0f5ed67ec2098cf3e6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699059"
---
# <a name="ambientattributestabstop"></a><span data-ttu-id="23d71-105">Амбиентаттрибутес. tabStop</span><span class="sxs-lookup"><span data-stu-id="23d71-105">AmbientAttributes.tabStop</span></span>

<span data-ttu-id="23d71-106">Атрибут **tabStop** указывает или получает значение, указывающее, находится ли элемент управления в порядке перехода.</span><span class="sxs-lookup"><span data-stu-id="23d71-106">The **tabStop** attribute specifies or retrieves a value indicating whether the control is in the tabbing order.</span></span> <span data-ttu-id="23d71-107">Порядок табуляции задается путем размещения элемента управления в общем сценарии до или после других управляющих тегов.</span><span class="sxs-lookup"><span data-stu-id="23d71-107">You set the tabbing order by placing the control in the overall script before or after other control tags.</span></span>

``` syntax
        elementID.tabStop
```

## <a name="possible-values"></a><span data-ttu-id="23d71-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="23d71-108">Possible Values</span></span>

<span data-ttu-id="23d71-109">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="23d71-109">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="23d71-110">Значение</span><span class="sxs-lookup"><span data-stu-id="23d71-110">Value</span></span> | <span data-ttu-id="23d71-111">Описание</span><span class="sxs-lookup"><span data-stu-id="23d71-111">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="23d71-112">true</span><span class="sxs-lookup"><span data-stu-id="23d71-112">true</span></span>  | <span data-ttu-id="23d71-113">Элемент управления находится в порядке перехода (элемент управления будет иметь позицию табуляции: требование специальных возможностей).</span><span class="sxs-lookup"><span data-stu-id="23d71-113">Control is in the tabbing order (control will have a tab stop: accessibility requirement).</span></span> |
| <span data-ttu-id="23d71-114">false</span><span class="sxs-lookup"><span data-stu-id="23d71-114">false</span></span> | <span data-ttu-id="23d71-115">Элемент управления не находится в порядке перехода.</span><span class="sxs-lookup"><span data-stu-id="23d71-115">Control is not in the tabbing order.</span></span>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="23d71-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23d71-116">Remarks</span></span>

<span data-ttu-id="23d71-117">Атрибут **tabStop** неприменим к элементу **Effects** .</span><span class="sxs-lookup"><span data-stu-id="23d71-117">The **tabStop** attribute is not applicable to the **EFFECTS** element.</span></span>

<span data-ttu-id="23d71-118">Значение по умолчанию для этого атрибута равно true для всех элементов, кроме **АВТОМЕНЮ** и **текста**, которые имеют значение по умолчанию false.</span><span class="sxs-lookup"><span data-stu-id="23d71-118">The default value for this attribute is true for all elements except **AUTOMENU** and **TEXT**, which have a default value of false.</span></span>

## <a name="requirements"></a><span data-ttu-id="23d71-119">Требования</span><span class="sxs-lookup"><span data-stu-id="23d71-119">Requirements</span></span>



| <span data-ttu-id="23d71-120">Требование</span><span class="sxs-lookup"><span data-stu-id="23d71-120">Requirement</span></span> | <span data-ttu-id="23d71-121">Значение</span><span class="sxs-lookup"><span data-stu-id="23d71-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="23d71-122">Версия</span><span class="sxs-lookup"><span data-stu-id="23d71-122">Version</span></span><br/> | <span data-ttu-id="23d71-123">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="23d71-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="23d71-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23d71-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23d71-125">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="23d71-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





