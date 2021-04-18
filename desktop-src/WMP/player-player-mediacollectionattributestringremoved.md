---
title: Событие Player. Медиаколлектионаттрибутестрингремовед
description: Событие Медиаколлектионаттрибутестрингремовед возникает при удалении значения атрибута из библиотеки. | Событие Player. Медиаколлектионаттрибутестрингремовед
ms.assetid: f1253996-10d1-42fa-89f9-1e52ca830aea
keywords:
- Проигрыватель Windows Media Event Медиаколлектионаттрибутестрингремовед
- Проигрыватель Windows Media Event Медиаколлектионаттрибутестрингремовед, класс Player
- Класс проигрывателя Windows Media Player, событие Медиаколлектионаттрибутестрингремовед
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1b85dfd566c507f6ae5557134ac95544e42d688
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704070"
---
# <a name="playermediacollectionattributestringremoved-event"></a><span data-ttu-id="d3e5f-107">Событие Player. Медиаколлектионаттрибутестрингремовед</span><span class="sxs-lookup"><span data-stu-id="d3e5f-107">Player.MediaCollectionAttributeStringRemoved event</span></span>

<span data-ttu-id="d3e5f-108">Событие **медиаколлектионаттрибутестрингремовед** возникает при удалении значения атрибута из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="d3e5f-108">The **MediaCollectionAttributeStringRemoved** event occurs when an attribute value is removed from the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3e5f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3e5f-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringRemoved(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="d3e5f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3e5f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3e5f-111">*бстраттрибнаме*</span><span class="sxs-lookup"><span data-stu-id="d3e5f-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="d3e5f-112">**Строка** , указывающая имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="d3e5f-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="d3e5f-113">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d3e5f-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3e5f-114">*бстраттрибвал*</span><span class="sxs-lookup"><span data-stu-id="d3e5f-114">*bstrAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="d3e5f-115">**Строка** , указывающая значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="d3e5f-115">**String** specifying the value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3e5f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3e5f-116">Return value</span></span>

<span data-ttu-id="d3e5f-117">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d3e5f-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3e5f-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3e5f-118">Remarks</span></span>

<span data-ttu-id="d3e5f-119">При удалении элемента мультимедиа из библиотеки его метаданные удаляются из объекта **медиаколлектион** , и это событие срабатывает для каждого удаляемого атрибута.</span><span class="sxs-lookup"><span data-stu-id="d3e5f-119">When a media item is removed from the library, its metadata is removed from the **MediaCollection** object and this event is fired for each attribute removed.</span></span>

<span data-ttu-id="d3e5f-120">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="d3e5f-120">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="d3e5f-121">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="d3e5f-121">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="d3e5f-122">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d3e5f-122">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3e5f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d3e5f-123">Requirements</span></span>



| <span data-ttu-id="d3e5f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d3e5f-124">Requirement</span></span> | <span data-ttu-id="d3e5f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d3e5f-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e5f-126">Версия</span><span class="sxs-lookup"><span data-stu-id="d3e5f-126">Version</span></span><br/> | <span data-ttu-id="d3e5f-127">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="d3e5f-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d3e5f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d3e5f-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="d3e5f-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3e5f-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3e5f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3e5f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3e5f-131">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="d3e5f-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="d3e5f-132">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="d3e5f-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="d3e5f-133">**Player. Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="d3e5f-133">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





