---
title: Событие Player. Медиаколлектионаттрибутестрингчанжед
description: Событие Медиаколлектионаттрибутестрингчанжед возникает при изменении значения атрибута в библиотеке. | Событие Player. Медиаколлектионаттрибутестрингчанжед
ms.assetid: 9bc81cf2-50a9-41cf-8eff-25c9395dfdac
keywords:
- Проигрыватель Windows Media Event Медиаколлектионаттрибутестрингчанжед
- Проигрыватель Windows Media Event Медиаколлектионаттрибутестрингчанжед, класс Player
- Класс проигрывателя Windows Media Player, событие Медиаколлектионаттрибутестрингчанжед
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringChanged
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92eba7f0f585b9bbff7a8eb52ab13ec0d74aaa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704210"
---
# <a name="playermediacollectionattributestringchanged-event"></a><span data-ttu-id="fc177-107">Событие Player. Медиаколлектионаттрибутестрингчанжед</span><span class="sxs-lookup"><span data-stu-id="fc177-107">Player.MediaCollectionAttributeStringChanged event</span></span>

<span data-ttu-id="fc177-108">Событие **медиаколлектионаттрибутестрингчанжед** возникает при изменении значения атрибута в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="fc177-108">The **MediaCollectionAttributeStringChanged** event occurs when an attribute value in the library is changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc177-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc177-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringChanged(
  bstrAttribName,
  bstrOldAttribVal,
  bstrNewAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="fc177-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc177-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc177-111">*бстраттрибнаме*</span><span class="sxs-lookup"><span data-stu-id="fc177-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="fc177-112">**Строка** , указывающая имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="fc177-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="fc177-113">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fc177-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc177-114">*бстролдаттрибвал*</span><span class="sxs-lookup"><span data-stu-id="fc177-114">*bstrOldAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="fc177-115">**Строка** , указывающая старое значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="fc177-115">**String** specifying the old value of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="fc177-116">*бстрневаттрибвал*</span><span class="sxs-lookup"><span data-stu-id="fc177-116">*bstrNewAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="fc177-117">**Строка** , указывающая новое значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="fc177-117">**String** specifying the new value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc177-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc177-118">Return value</span></span>

<span data-ttu-id="fc177-119">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="fc177-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc177-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc177-120">Remarks</span></span>

<span data-ttu-id="fc177-121">Когда пользователь изменяет метаданные библиотеки, объект **медиаколлектион** обновляется, и это событие срабатывает для каждого измененного атрибута.</span><span class="sxs-lookup"><span data-stu-id="fc177-121">When a user modifies library metadata, the **MediaCollection** object is updated and this event fires for each attribute changed.</span></span>

<span data-ttu-id="fc177-122">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="fc177-122">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="fc177-123">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="fc177-123">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="fc177-124">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc177-124">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc177-125">Требования</span><span class="sxs-lookup"><span data-stu-id="fc177-125">Requirements</span></span>



| <span data-ttu-id="fc177-126">Требование</span><span class="sxs-lookup"><span data-stu-id="fc177-126">Requirement</span></span> | <span data-ttu-id="fc177-127">Значение</span><span class="sxs-lookup"><span data-stu-id="fc177-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc177-128">Версия</span><span class="sxs-lookup"><span data-stu-id="fc177-128">Version</span></span><br/> | <span data-ttu-id="fc177-129">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="fc177-129">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="fc177-130">DLL</span><span class="sxs-lookup"><span data-stu-id="fc177-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="fc177-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc177-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc177-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc177-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc177-133">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="fc177-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="fc177-134">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="fc177-134">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="fc177-135">**Player. Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="fc177-135">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





