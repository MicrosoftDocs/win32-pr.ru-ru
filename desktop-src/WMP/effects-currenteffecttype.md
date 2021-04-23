---
title: EFFECTs. Куррентеффекттипе
description: Атрибут Куррентеффекттипе указывает или получает имя реестра текущей визуализации. Это имя является уникальным ИДЕНТИФИКАТОРом, определенным автором визуализации.
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- Effect. Куррентеффекттипе Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7c7671c4a5dce9df81cf8f9d770d71eba3325e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694708"
---
# <a name="effectscurrenteffecttype"></a><span data-ttu-id="127eb-105">EFFECTs. Куррентеффекттипе</span><span class="sxs-lookup"><span data-stu-id="127eb-105">EFFECTS.currentEffectType</span></span>

<span data-ttu-id="127eb-106">Атрибут **куррентеффекттипе** указывает или получает имя реестра текущей визуализации.</span><span class="sxs-lookup"><span data-stu-id="127eb-106">The **currentEffectType** attribute specifies or retrieves the registry name of the current visualization.</span></span> <span data-ttu-id="127eb-107">Это имя является уникальным ИДЕНТИФИКАТОРом, определенным автором визуализации.</span><span class="sxs-lookup"><span data-stu-id="127eb-107">This name is a unique ID defined by the visualization author.</span></span>

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a><span data-ttu-id="127eb-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="127eb-108">Possible Values</span></span>

<span data-ttu-id="127eb-109">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="127eb-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="127eb-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="127eb-110">Remarks</span></span>

<span data-ttu-id="127eb-111">Этот атрибут можно использовать во время выполнения, чтобы изменить отображаемый в данный момент результат.</span><span class="sxs-lookup"><span data-stu-id="127eb-111">You can use this attribute at run time to change the currently displayed effect.</span></span> <span data-ttu-id="127eb-112">Для этого выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="127eb-112">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="127eb-113">Используйте **еффекткаунт** для получения числа зарегистрированных эффектов.</span><span class="sxs-lookup"><span data-stu-id="127eb-113">Use **effectCount** to retrieve the count of registered effects.</span></span>
2.  <span data-ttu-id="127eb-114">В цикле извлеките имя каждого зарегистрированного результата с помощью **еффекттипе**.</span><span class="sxs-lookup"><span data-stu-id="127eb-114">In a loop, retrieve the name of each registered effect by using **effectType**.</span></span>
3.  <span data-ttu-id="127eb-115">Укажите одно из имен, полученных для **куррентеффекттипе** , чтобы установить текущий результат.</span><span class="sxs-lookup"><span data-stu-id="127eb-115">Specify one of the names you retrieved for **currentEffectType** to set the current effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="127eb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="127eb-116">Requirements</span></span>



| <span data-ttu-id="127eb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="127eb-117">Requirement</span></span> | <span data-ttu-id="127eb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="127eb-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="127eb-119">Версия</span><span class="sxs-lookup"><span data-stu-id="127eb-119">Version</span></span><br/> | <span data-ttu-id="127eb-120">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="127eb-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="127eb-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="127eb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="127eb-122">**EFFECTs, элемент**</span><span class="sxs-lookup"><span data-stu-id="127eb-122">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="127eb-123">**EFFECTs. Куррентеффект**</span><span class="sxs-lookup"><span data-stu-id="127eb-123">**EFFECTS.currentEffect**</span></span>](effects-currenteffect.md)
</dt> <dt>

[<span data-ttu-id="127eb-124">**EFFECTs. Еффекткаунт**</span><span class="sxs-lookup"><span data-stu-id="127eb-124">**EFFECTS.effectCount**</span></span>](effects-effectcount.md)
</dt> <dt>

[<span data-ttu-id="127eb-125">**EFFECTs. Еффекттипе**</span><span class="sxs-lookup"><span data-stu-id="127eb-125">**EFFECTS.effectType**</span></span>](effects-effecttype.md)
</dt> </dl>

 

 





