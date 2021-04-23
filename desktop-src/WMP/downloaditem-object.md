---
title: Объект Довнлоадитем
description: Объект Довнлоадитем
ms.assetid: 668ee632-0a3d-426b-baab-08e88b9fc607
keywords:
- Интернет-магазины проигрывателя Windows Media, объект Довнлоадитем
- Интернет-магазины, объект Довнлоадитем
- Тип 2 Интернет-магазинов, объект Довнлоадитем
- довнлоадитем
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c367eee37f2f4d8329d71f3d42a3c78771a50a6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691378"
---
# <a name="downloaditem-object"></a><span data-ttu-id="217ab-107">Объект Довнлоадитем</span><span class="sxs-lookup"><span data-stu-id="217ab-107">DownloadItem Object</span></span>

> [!Note]  
> <span data-ttu-id="217ab-108">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="217ab-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="217ab-109">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="217ab-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="217ab-110">Объект **довнлоадитем** представляет запрос на скачивание файла.</span><span class="sxs-lookup"><span data-stu-id="217ab-110">The **DownloadItem** object represents a file download request.</span></span> <span data-ttu-id="217ab-111">Она может использоваться веб-страницами, размещенными в проигрывателе Windows Media в полном режиме и имеющими доступ к **внешнему** объекту, например службам Premium.</span><span class="sxs-lookup"><span data-stu-id="217ab-111">It can be used by webpages that are hosted in the full mode Windows Media Player and that have access to the **External** object, such as premium services.</span></span>

<span data-ttu-id="217ab-112">Объект **довнлоадитем** поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="217ab-112">The **DownloadItem** object supports the following properties.</span></span>



| <span data-ttu-id="217ab-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="217ab-113">Property</span></span>                                        | <span data-ttu-id="217ab-114">Описание</span><span class="sxs-lookup"><span data-stu-id="217ab-114">Description</span></span>                                      |
|-------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="217ab-115">довнлоадстате</span><span class="sxs-lookup"><span data-stu-id="217ab-115">downloadState</span></span>](downloaditem-downloadstate.md) | <span data-ttu-id="217ab-116">Получает состояние загрузки.</span><span class="sxs-lookup"><span data-stu-id="217ab-116">Retrieves the state of the download.</span></span>             |
| [<span data-ttu-id="217ab-117">двигается</span><span class="sxs-lookup"><span data-stu-id="217ab-117">progress</span></span>](downloaditem-progress.md)           | <span data-ttu-id="217ab-118">Получает сведения о ходе загрузки в байтах.</span><span class="sxs-lookup"><span data-stu-id="217ab-118">Retrieves the progress of the download in bytes.</span></span> |
| [<span data-ttu-id="217ab-119">size</span><span class="sxs-lookup"><span data-stu-id="217ab-119">size</span></span>](downloaditem-size.md)                   | <span data-ttu-id="217ab-120">Возвращает размер загружаемого файла.</span><span class="sxs-lookup"><span data-stu-id="217ab-120">Retrieves the size of the download.</span></span>              |
| [<span data-ttu-id="217ab-121">саурцеурл</span><span class="sxs-lookup"><span data-stu-id="217ab-121">sourceURL</span></span>](downloaditem-sourceurl.md)         | <span data-ttu-id="217ab-122">Извлекает исходный URL-адрес для скачивания.</span><span class="sxs-lookup"><span data-stu-id="217ab-122">Retrieves the source URL of the download.</span></span>        |
| [<span data-ttu-id="217ab-123">type</span><span class="sxs-lookup"><span data-stu-id="217ab-123">type</span></span>](downloaditem-type.md)                   | <span data-ttu-id="217ab-124">Возвращает тип загрузки.</span><span class="sxs-lookup"><span data-stu-id="217ab-124">Retrieves the type of the download.</span></span>              |



 

<span data-ttu-id="217ab-125">Объект **довнлоадитем** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="217ab-125">The **DownloadItem** object supports the following methods.</span></span>



| <span data-ttu-id="217ab-126">Метод</span><span class="sxs-lookup"><span data-stu-id="217ab-126">Method</span></span>                                      | <span data-ttu-id="217ab-127">Описание</span><span class="sxs-lookup"><span data-stu-id="217ab-127">Description</span></span>                                                |
|---------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="217ab-128">cancel</span><span class="sxs-lookup"><span data-stu-id="217ab-128">cancel</span></span>](downloaditem-cancel.md)           | <span data-ttu-id="217ab-129">Отменяет скачивание.</span><span class="sxs-lookup"><span data-stu-id="217ab-129">Cancels the download.</span></span>                                      |
| [<span data-ttu-id="217ab-130">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="217ab-130">getItemInfo</span></span>](downloaditem-getiteminfo.md) | <span data-ttu-id="217ab-131">Возвращает значение атрибута для элемента загрузки.</span><span class="sxs-lookup"><span data-stu-id="217ab-131">Retrieves the value of an attribute for the download item.</span></span> |
| [<span data-ttu-id="217ab-132">pause</span><span class="sxs-lookup"><span data-stu-id="217ab-132">pause</span></span>](downloaditem-pause.md)             | <span data-ttu-id="217ab-133">Приостанавливает скачивание.</span><span class="sxs-lookup"><span data-stu-id="217ab-133">Pauses the download.</span></span>                                       |
| [<span data-ttu-id="217ab-134">выход</span><span class="sxs-lookup"><span data-stu-id="217ab-134">resume</span></span>](downloaditem-resume.md)           | <span data-ttu-id="217ab-135">Возобновляет скачивание.</span><span class="sxs-lookup"><span data-stu-id="217ab-135">Resumes the download.</span></span>                                      |



 

<span data-ttu-id="217ab-136">Доступ к объекту **довнлоадитем** осуществляется через следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="217ab-136">The **DownloadItem** object is accessed through the following property.</span></span>



| <span data-ttu-id="217ab-137">Объект</span><span class="sxs-lookup"><span data-stu-id="217ab-137">Object</span></span>                                              | <span data-ttu-id="217ab-138">Свойство</span><span class="sxs-lookup"><span data-stu-id="217ab-138">Property</span></span>                            |
|-----------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="217ab-139">довнлоадколлектион</span><span class="sxs-lookup"><span data-stu-id="217ab-139">DownloadCollection</span></span>](downloadcollection-object.md) | [<span data-ttu-id="217ab-140">Item</span><span class="sxs-lookup"><span data-stu-id="217ab-140">item</span></span>](downloadcollection-item.md) |



 

<span data-ttu-id="217ab-141">В целях иллюстрации **довнлоадманажер**. **жетдовнлоадколлектион**(*CollectionID*). **элемент**(*ItemId*) используется в разделах синтаксиса Reference.</span><span class="sxs-lookup"><span data-stu-id="217ab-141">For purposes of illustration, **DownloadManager**.**getDownloadCollection**(*collectionId*).**item**(*itemId*) is used in the reference syntax sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="217ab-142">См. также</span><span class="sxs-lookup"><span data-stu-id="217ab-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="217ab-143">**Справочные материалы по интернет-магазинам типа 2**</span><span class="sxs-lookup"><span data-stu-id="217ab-143">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




