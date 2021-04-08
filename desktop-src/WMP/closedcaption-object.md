---
title: Объект Клоседкаптион
description: Объект Клоседкаптион предоставляет возможность включения субтитров с помощью клипа мультимедиа. Текст субтитров находится в синхронизированном доступном файле обмена мультимедиа (SAMI).
ms.assetid: 5e192aa4-0ecd-4bda-8dad-1750039c7898
keywords:
- Проигрыватель Windows Media Object Клоседкаптион
topic_type:
- apiref
api_name:
- ClosedCaption Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85e53468e8d5cc2694555b9a05d8b207d1660618
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "104069219"
---
# <a name="closedcaption-object"></a><span data-ttu-id="832f2-105">Объект Клоседкаптион</span><span class="sxs-lookup"><span data-stu-id="832f2-105">ClosedCaption Object</span></span>

<span data-ttu-id="832f2-106">Объект **клоседкаптион** предоставляет возможность включения субтитров с помощью клипа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="832f2-106">The **ClosedCaption** object provides a way to include captions with a media clip.</span></span> <span data-ttu-id="832f2-107">Текст субтитров находится в синхронизированном доступном файле обмена мультимедиа (SAMI).</span><span class="sxs-lookup"><span data-stu-id="832f2-107">The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.</span></span>

<span data-ttu-id="832f2-108">Объект **клоседкаптион** поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="832f2-108">The **ClosedCaption** object supports the following properties.</span></span>



| <span data-ttu-id="832f2-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="832f2-109">Property</span></span>                                           | <span data-ttu-id="832f2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="832f2-110">Description</span></span>                                                                                          |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="832f2-111">каптионингид</span><span class="sxs-lookup"><span data-stu-id="832f2-111">captioningID</span></span>](closedcaption-captioningid.md)     | <span data-ttu-id="832f2-112">Указывает или получает имя фрейма или элемента управления, отображающего субтитры.</span><span class="sxs-lookup"><span data-stu-id="832f2-112">Specifies or retrieves the name of the frame or control displaying the captioning.</span></span>                   |
| [<span data-ttu-id="832f2-113">самифиленаме</span><span class="sxs-lookup"><span data-stu-id="832f2-113">SAMIFileName</span></span>](closedcaption-samifilename.md)     | <span data-ttu-id="832f2-114">Указывает или получает имя файла, содержащего сведения, необходимые для субтитров.</span><span class="sxs-lookup"><span data-stu-id="832f2-114">Specifies or retrieves the name of the file containing the information needed for closed captioning.</span></span> |
| [<span data-ttu-id="832f2-115">самиланг</span><span class="sxs-lookup"><span data-stu-id="832f2-115">SAMILang</span></span>](closedcaption-samilang.md)             | <span data-ttu-id="832f2-116">Указывает или получает язык, отображаемый для субтитров.</span><span class="sxs-lookup"><span data-stu-id="832f2-116">Specifies or retrieves the language displayed for closed captioning.</span></span>                                 |
| [<span data-ttu-id="832f2-117">самилангкаунт</span><span class="sxs-lookup"><span data-stu-id="832f2-117">SAMILangCount</span></span>](closedcaption-samilangcount.md)   | <span data-ttu-id="832f2-118">Возвращает число языков, поддерживаемых текущим файлом SAMI.</span><span class="sxs-lookup"><span data-stu-id="832f2-118">Retrieves the number of languages supported by the current SAMI file.</span></span>                                |
| [<span data-ttu-id="832f2-119">самистиле</span><span class="sxs-lookup"><span data-stu-id="832f2-119">SAMIStyle</span></span>](closedcaption-samistyle.md)           | <span data-ttu-id="832f2-120">Указывает или получает стиль закрытых субтитров.</span><span class="sxs-lookup"><span data-stu-id="832f2-120">Specifies or retrieves the closed captioning style.</span></span>                                                  |
| [<span data-ttu-id="832f2-121">самистилекаунт</span><span class="sxs-lookup"><span data-stu-id="832f2-121">SAMIStyleCount</span></span>](closedcaption-samistylecount.md) | <span data-ttu-id="832f2-122">Возвращает количество стилей, поддерживаемое текущим файлом SAMI.</span><span class="sxs-lookup"><span data-stu-id="832f2-122">Retrieves the number of styles supported by the current SAMI file.</span></span>                                   |



 

<span data-ttu-id="832f2-123">Объект **клоседкаптион** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="832f2-123">The **ClosedCaption** object supports the following methods.</span></span>



| <span data-ttu-id="832f2-124">Метод</span><span class="sxs-lookup"><span data-stu-id="832f2-124">Method</span></span>                                                 | <span data-ttu-id="832f2-125">Описание</span><span class="sxs-lookup"><span data-stu-id="832f2-125">Description</span></span>                                                                              |
|--------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="832f2-126">жетсамилангид</span><span class="sxs-lookup"><span data-stu-id="832f2-126">getSAMILangID</span></span>](closedcaption-getsamilangid.md)       | <span data-ttu-id="832f2-127">Извлекает код локали (LCID) языка, поддерживаемого текущим файлом SAMI.</span><span class="sxs-lookup"><span data-stu-id="832f2-127">Retrieves the locale identifier (LCID) of a language supported by the current SAMI file.</span></span> |
| [<span data-ttu-id="832f2-128">жетсамилангнаме</span><span class="sxs-lookup"><span data-stu-id="832f2-128">getSAMILangName</span></span>](closedcaption-getsamilangname.md)   | <span data-ttu-id="832f2-129">Извлекает имя языка, поддерживаемого текущим файлом SAMI.</span><span class="sxs-lookup"><span data-stu-id="832f2-129">Retrieves the name of a language supported by the current SAMI file.</span></span>                     |
| [<span data-ttu-id="832f2-130">жетсамистиленаме</span><span class="sxs-lookup"><span data-stu-id="832f2-130">getSAMIStyleName</span></span>](closedcaption-getsamistylename.md) | <span data-ttu-id="832f2-131">Извлекает имя стиля, поддерживаемого текущим файлом SAMI.</span><span class="sxs-lookup"><span data-stu-id="832f2-131">Retrieves the name of a style supported by the current SAMI file.</span></span>                        |



 

<span data-ttu-id="832f2-132">Доступ к объекту **клоседкаптион** осуществляется через следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="832f2-132">The **ClosedCaption** object is accessed through the following property.</span></span>



| <span data-ttu-id="832f2-133">Объект</span><span class="sxs-lookup"><span data-stu-id="832f2-133">Object</span></span>                      | <span data-ttu-id="832f2-134">Свойство</span><span class="sxs-lookup"><span data-stu-id="832f2-134">Property</span></span>                                  |
|-----------------------------|-------------------------------------------|
| [<span data-ttu-id="832f2-135">Игрок</span><span class="sxs-lookup"><span data-stu-id="832f2-135">Player</span></span>](player-object.md) | [<span data-ttu-id="832f2-136">клоседкаптион</span><span class="sxs-lookup"><span data-stu-id="832f2-136">closedCaption</span></span>](player-closedcaption.md) |



 

## <a name="see-also"></a><span data-ttu-id="832f2-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="832f2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="832f2-138">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="832f2-138">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="832f2-139">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="832f2-139">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




