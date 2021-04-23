---
title: Ивмпклоседкаптион Каптионингид, свойство
description: Свойство Ивмпклоседкаптион Возвращает или задает имя HTML-элемента, отображающего субтитры.
ms.assetid: b09bb7c7-c3b6-4e0d-962f-24b06a04f6d1
keywords:
- Проигрыватель Windows Media для свойства Каптионингид
- Каптионингид свойство проигрывателя Windows Media Player, интерфейс Ивмпклоседкаптион
- Интерфейс Ивмпклоседкаптион Windows Media Player, свойство Каптионингид
topic_type:
- apiref
api_name:
- IWMPClosedCaption.captioningId
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343234fce2b93ac02255731a38025f6d7b9fac6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648824"
---
# <a name="iwmpclosedcaptioncaptioningid-property"></a><span data-ttu-id="70687-106">Свойство Ивмпклоседкаптион:: Каптионингид</span><span class="sxs-lookup"><span data-stu-id="70687-106">IWMPClosedCaption::captioningId property</span></span>

<span data-ttu-id="70687-107">Свойство **ивмпклоседкаптион** Возвращает или задает имя HTML-элемента, отображающего субтитры.</span><span class="sxs-lookup"><span data-stu-id="70687-107">The **IWMPClosedCaption** property gets or sets the name of the HTML element displaying the captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="70687-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70687-108">Syntax</span></span>


```CSharp
public System.String captioningId {get; set;}
```


```VB

Public Property captioningId As System.String
```





## <a name="property-value"></a><span data-ttu-id="70687-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="70687-109">Property value</span></span>

<span data-ttu-id="70687-110">**Строка System. String** , которая является идентификатором HTML-элемента.</span><span class="sxs-lookup"><span data-stu-id="70687-110">The **System.String** that is the ID of the HTML element.</span></span>

## <a name="remarks"></a><span data-ttu-id="70687-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70687-111">Remarks</span></span>

<span data-ttu-id="70687-112">Указанное имя элемента может быть любым HTML-элементом на веб-странице, если он поддерживает атрибут **InnerHtml** .</span><span class="sxs-lookup"><span data-stu-id="70687-112">The element name specified can be any HTML element in the webpage as long as it supports the **innerHTML** attribute.</span></span> <span data-ttu-id="70687-113">Если веб-страница содержит несколько кадров, имя элемента может ссылаться только на элемент в том же кадре, что и элемент управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="70687-113">If the webpage contains multiple frames, the element name can only refer to an element in the same frame as the Windows Media Player control.</span></span>

## <a name="requirements"></a><span data-ttu-id="70687-114">Требования</span><span class="sxs-lookup"><span data-stu-id="70687-114">Requirements</span></span>



| <span data-ttu-id="70687-115">Требование</span><span class="sxs-lookup"><span data-stu-id="70687-115">Requirement</span></span> | <span data-ttu-id="70687-116">Значение</span><span class="sxs-lookup"><span data-stu-id="70687-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70687-117">Версия</span><span class="sxs-lookup"><span data-stu-id="70687-117">Version</span></span><br/>   | <span data-ttu-id="70687-118">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="70687-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="70687-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="70687-119">Namespace</span></span><br/> | <span data-ttu-id="70687-120">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="70687-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="70687-121">Сборка</span><span class="sxs-lookup"><span data-stu-id="70687-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="70687-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="70687-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70687-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70687-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70687-124">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="70687-124">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="70687-125">**Интерфейс Ивмпклоседкаптион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="70687-125">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="70687-126">**Интерфейс IWMPClosedCaption2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="70687-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





