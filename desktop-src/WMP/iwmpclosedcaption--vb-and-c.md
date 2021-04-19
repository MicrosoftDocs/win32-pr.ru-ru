---
title: Интерфейс Ивмпклоседкаптион (VB и C) (WMP. h)
description: Предоставляет возможность включать субтитры с цифровым файлом мультимедиа. Текст субтитров находится в синхронизированном доступном файле обмена мультимедиа (SAMI).
ms.assetid: 927f6fe4-5847-439e-9df0-19cc910d887d
keywords:
- Ивмпклоседкаптион (VB и C) интерфейс проигрывателя Windows Media
- Ивмпклоседкаптион (VB и C) интерфейс проигрывателя Windows Media, описание
topic_type:
- apiref
api_name:
- IWMPClosedCaption (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce3f697fc5c651a47f257a61bd9841987f54478
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688851"
---
# <a name="iwmpclosedcaption-vb-and-c-interface"></a><span data-ttu-id="55e01-106">Интерфейс Ивмпклоседкаптион (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="55e01-106">IWMPClosedCaption (VB and C#) interface</span></span>

<span data-ttu-id="55e01-107">Предоставляет возможность включать субтитры с цифровым файлом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="55e01-107">Provides a way to include captions with a digital media file.</span></span> <span data-ttu-id="55e01-108">Текст субтитров находится в синхронизированном доступном файле обмена мультимедиа (SAMI).</span><span class="sxs-lookup"><span data-stu-id="55e01-108">The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.</span></span>

## <a name="members"></a><span data-ttu-id="55e01-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="55e01-109">Members</span></span>

<span data-ttu-id="55e01-110">Интерфейс **ивмпклоседкаптион (VB и C#)** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="55e01-110">The **IWMPClosedCaption (VB and C#)** interface does not define any members.</span></span>

<span data-ttu-id="55e01-111">Интерфейс **ивмпклоседкаптион** предоставляет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="55e01-111">The **IWMPClosedCaption** interface exposes the following properties.</span></span>



| <span data-ttu-id="55e01-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="55e01-112">Property</span></span>                                                                             | <span data-ttu-id="55e01-113">Описание</span><span class="sxs-lookup"><span data-stu-id="55e01-113">Description</span></span>                                                                                |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55e01-114">каптионингид</span><span class="sxs-lookup"><span data-stu-id="55e01-114">captioningId</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md) | <span data-ttu-id="55e01-115">Возвращает или задает имя HTML-элемента, отображающего субтитры.</span><span class="sxs-lookup"><span data-stu-id="55e01-115">Gets or sets the name of the HTML element displaying the captioning.</span></span>                       |
| [<span data-ttu-id="55e01-116">самифиленаме</span><span class="sxs-lookup"><span data-stu-id="55e01-116">SAMIFileName</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samifilename--vb-and-c.md) | <span data-ttu-id="55e01-117">Возвращает или задает имя файла, содержащего сведения, необходимые для закрытого субтитров.</span><span class="sxs-lookup"><span data-stu-id="55e01-117">Gets or sets the name of the file containing the information needed for closed captioning.</span></span> |
| [<span data-ttu-id="55e01-118">самиланг</span><span class="sxs-lookup"><span data-stu-id="55e01-118">SAMILang</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)         | <span data-ttu-id="55e01-119">Возвращает или задает язык, отображаемый для скрытых титров.</span><span class="sxs-lookup"><span data-stu-id="55e01-119">Gets or sets the language displayed for closed captioning.</span></span>                                 |
| [<span data-ttu-id="55e01-120">самистиле</span><span class="sxs-lookup"><span data-stu-id="55e01-120">SAMIStyle</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)       | <span data-ttu-id="55e01-121">Возвращает или задает стиль закрытых субтитров.</span><span class="sxs-lookup"><span data-stu-id="55e01-121">Gets or sets the closed captioning style.</span></span>                                                  |



 

<span data-ttu-id="55e01-122">Получите интерфейс **ивмпклоседкаптион** с помощью следующего свойства.</span><span class="sxs-lookup"><span data-stu-id="55e01-122">Get an **IWMPClosedCaption** interface by using the following property.</span></span>



| <span data-ttu-id="55e01-123">Объект</span><span class="sxs-lookup"><span data-stu-id="55e01-123">Object</span></span>                                                            | <span data-ttu-id="55e01-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="55e01-124">Property</span></span>                                                                   |
|-------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="55e01-125">аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="55e01-125">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="55e01-126">клоседкаптион</span><span class="sxs-lookup"><span data-stu-id="55e01-126">closedCaption</span></span>](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="55e01-127">Требования</span><span class="sxs-lookup"><span data-stu-id="55e01-127">Requirements</span></span>



| <span data-ttu-id="55e01-128">Требование</span><span class="sxs-lookup"><span data-stu-id="55e01-128">Requirement</span></span> | <span data-ttu-id="55e01-129">Значение</span><span class="sxs-lookup"><span data-stu-id="55e01-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="55e01-130">Header</span><span class="sxs-lookup"><span data-stu-id="55e01-130">Header</span></span><br/> | <dl> <span data-ttu-id="55e01-131"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="55e01-131"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55e01-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55e01-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55e01-133">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="55e01-133">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="55e01-134">**Интерфейсы для Visual Basic .NET и C #**</span><span class="sxs-lookup"><span data-stu-id="55e01-134">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="55e01-135">**Интерфейс IWMPClosedCaption2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="55e01-135">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





