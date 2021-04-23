---
description: Элемент Effect определяет объект аудио или видео. Результат применяется к одному потоку (например, композиции, дорожке или источнику).
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: Элемент Effect (Гдиплусеффектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4c925e61578857415bb22248a9ad2b1df27cdac
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908662"
---
# <a name="effect-element"></a><span data-ttu-id="89761-104">Элемент Effect</span><span class="sxs-lookup"><span data-stu-id="89761-104">effect Element</span></span>

> [!Note]  
> <span data-ttu-id="89761-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="89761-105">\[Deprecated.</span></span> <span data-ttu-id="89761-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="89761-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="89761-107">`effect`Элемент определяет объект аудио или видео.</span><span class="sxs-lookup"><span data-stu-id="89761-107">The `effect` element defines an audio or video effect object.</span></span> <span data-ttu-id="89761-108">Результат применяется к одному потоку (например, композиции, дорожке или источнику).</span><span class="sxs-lookup"><span data-stu-id="89761-108">An effect is applied to a single stream (such as a composition, track, or source).</span></span>

## <a name="attributes"></a><span data-ttu-id="89761-109">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="89761-109">Attributes</span></span>

<span data-ttu-id="89761-110">[**CLSID**](clsid-attribute.md), [**Lock**](lock-attribute.md), [**выкл**](mute-attribute.md)., [**Запуск**](start-attribute.md), [**Завершение**](stop-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**имя пользователя**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="89761-110">[**clsid**](clsid-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="89761-111">Сведения о родителе и дочернем элементе</span><span class="sxs-lookup"><span data-stu-id="89761-111">Parent/Child Information</span></span>



| <span data-ttu-id="89761-112">Метка</span><span class="sxs-lookup"><span data-stu-id="89761-112">Label</span></span> | <span data-ttu-id="89761-113">Значение</span><span class="sxs-lookup"><span data-stu-id="89761-113">Value</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89761-114">Parent</span><span class="sxs-lookup"><span data-stu-id="89761-114">Parent</span></span>   | <span data-ttu-id="89761-115">[**составной**](composite-element.md), [**Группа**](group-element.md), [**Обрезка**](clip-element.md), [**запись**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="89761-115">[**composite**](composite-element.md), [**group**](group-element.md), [**clip**](clip-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="89761-116">Дети</span><span class="sxs-lookup"><span data-stu-id="89761-116">Children</span></span> | [<span data-ttu-id="89761-117">**param**</span><span class="sxs-lookup"><span data-stu-id="89761-117">**param**</span></span>](param-element.md)                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="89761-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89761-118">Remarks</span></span>

<span data-ttu-id="89761-119">Атрибут **CLSID** задает подобъект, который создает результат.</span><span class="sxs-lookup"><span data-stu-id="89761-119">The **clsid** attribute specifies the subobject that creates the effect.</span></span>

## <a name="examples"></a><span data-ttu-id="89761-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="89761-120">Examples</span></span>


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a><span data-ttu-id="89761-121">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="89761-121">Requirements</span></span>



| <span data-ttu-id="89761-122">Требование</span><span class="sxs-lookup"><span data-stu-id="89761-122">Requirement</span></span> | <span data-ttu-id="89761-123">Значение</span><span class="sxs-lookup"><span data-stu-id="89761-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="89761-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="89761-124">Header</span></span><br/> | <dl> <span data-ttu-id="89761-125"><dt>Гдиплусеффектс. h</dt></span><span class="sxs-lookup"><span data-stu-id="89761-125"><dt>Gdipluseffects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89761-126">См. также</span><span class="sxs-lookup"><span data-stu-id="89761-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89761-127">Элементы КСТЛ</span><span class="sxs-lookup"><span data-stu-id="89761-127">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




