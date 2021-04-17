---
title: Событие Player. Медиаколлектионаттрибутестрингаддед
description: Событие Медиаколлектионаттрибутестрингаддед возникает при добавлении значения атрибута в библиотеку. | Событие Player. Медиаколлектионаттрибутестрингаддед
ms.assetid: 0a7fd61f-0429-4c1c-8790-d2f0e7f41d44
keywords:
- Проигрыватель Windows Media Event Медиаколлектионаттрибутестрингаддед
- Проигрыватель Windows Media Event Медиаколлектионаттрибутестрингаддед, класс Player
- Класс проигрывателя Windows Media Player, событие Медиаколлектионаттрибутестрингаддед
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ec30cf22b36fe97902d6eb6d6949daeb751f8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708486"
---
# <a name="playermediacollectionattributestringadded-event"></a><span data-ttu-id="93d3f-107">Событие Player. Медиаколлектионаттрибутестрингаддед</span><span class="sxs-lookup"><span data-stu-id="93d3f-107">Player.MediaCollectionAttributeStringAdded event</span></span>

<span data-ttu-id="93d3f-108">Событие **медиаколлектионаттрибутестрингаддед** возникает при добавлении значения атрибута в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="93d3f-108">The **MediaCollectionAttributeStringAdded** event occurs when an attribute value is added to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="93d3f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93d3f-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringAdded(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="93d3f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="93d3f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93d3f-111">*бстраттрибнаме*</span><span class="sxs-lookup"><span data-stu-id="93d3f-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="93d3f-112">**Строка** , указывающая имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="93d3f-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="93d3f-113">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="93d3f-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="93d3f-114">*бстраттрибвал*</span><span class="sxs-lookup"><span data-stu-id="93d3f-114">*bstrAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="93d3f-115">**Строка** , указывающая значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="93d3f-115">**String** specifying the value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93d3f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93d3f-116">Return value</span></span>

<span data-ttu-id="93d3f-117">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="93d3f-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="93d3f-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93d3f-118">Remarks</span></span>

<span data-ttu-id="93d3f-119">При добавлении элемента мультимедиа в библиотеку его метаданные добавляются в объект **медиаколлектион** , и это событие срабатывает для каждого добавленного атрибута.</span><span class="sxs-lookup"><span data-stu-id="93d3f-119">When a media item is added to the library its metadata is added to the **MediaCollection** object and this event is fired for each attribute added.</span></span>

<span data-ttu-id="93d3f-120">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="93d3f-120">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="93d3f-121">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="93d3f-121">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="93d3f-122">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="93d3f-122">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="93d3f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="93d3f-123">Requirements</span></span>



| <span data-ttu-id="93d3f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="93d3f-124">Requirement</span></span> | <span data-ttu-id="93d3f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="93d3f-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="93d3f-126">Версия</span><span class="sxs-lookup"><span data-stu-id="93d3f-126">Version</span></span><br/> | <span data-ttu-id="93d3f-127">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="93d3f-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="93d3f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="93d3f-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="93d3f-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93d3f-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93d3f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93d3f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93d3f-131">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="93d3f-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="93d3f-132">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="93d3f-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="93d3f-133">**Player. Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="93d3f-133">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





