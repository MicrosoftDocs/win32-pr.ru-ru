---
title: Объект Довнлоадколлектион
description: Объект Довнлоадколлектион
ms.assetid: e943b391-386e-43c5-a314-55ea31b2eefa
keywords:
- Интернет-магазины проигрывателя Windows Media, объект Довнлоадколлектион
- Интернет-магазины, объект Довнлоадколлектион
- Тип 2 Интернет-магазинов, объект Довнлоадколлектион
- довнлоадколлектион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8275cbd2661bdce9c428800206c14b9c55942c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691294"
---
# <a name="downloadcollection-object"></a><span data-ttu-id="db7ae-107">Объект Довнлоадколлектион</span><span class="sxs-lookup"><span data-stu-id="db7ae-107">DownloadCollection Object</span></span>

> [!Note]  
> <span data-ttu-id="db7ae-108">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="db7ae-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="db7ae-109">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="db7ae-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="db7ae-110">Объект **довнлоадколлектион** содержит свойства и методы для управления коллекциями элементов загрузки.</span><span class="sxs-lookup"><span data-stu-id="db7ae-110">The **DownloadCollection** object contains properties and methods to handle collections of download items.</span></span> <span data-ttu-id="db7ae-111">Она может использоваться веб-страницами, размещенными в проигрывателе Windows Media в полном режиме и имеющими доступ к **внешнему** объекту, например Интернет-магазинам.</span><span class="sxs-lookup"><span data-stu-id="db7ae-111">It can be used by webpages that are hosted in the full mode Windows Media Player and that have access to the **External** object, such as online stores.</span></span>

<span data-ttu-id="db7ae-112">Объект **довнлоадколлектион** поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="db7ae-112">The **DownloadCollection** object supports the following properties.</span></span>



| <span data-ttu-id="db7ae-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="db7ae-113">Property</span></span>                              | <span data-ttu-id="db7ae-114">Описание</span><span class="sxs-lookup"><span data-stu-id="db7ae-114">Description</span></span>                                  |
|---------------------------------------|----------------------------------------------|
| [<span data-ttu-id="db7ae-115">count</span><span class="sxs-lookup"><span data-stu-id="db7ae-115">count</span></span>](downloadcollection-count.md) | <span data-ttu-id="db7ae-116">Возвращает число незавершенных Скачиваний.</span><span class="sxs-lookup"><span data-stu-id="db7ae-116">Retrieves the number of pending downloads.</span></span>   |
| [<span data-ttu-id="db7ae-117">id</span><span class="sxs-lookup"><span data-stu-id="db7ae-117">id</span></span>](downloadcollection-id.md)       | <span data-ttu-id="db7ae-118">Возвращает идентификатор коллекции загрузки.</span><span class="sxs-lookup"><span data-stu-id="db7ae-118">Retrieves the ID of the download collection.</span></span> |



 

<span data-ttu-id="db7ae-119">Объект **довнлоадколлектион** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="db7ae-119">The **DownloadCollection** object supports the following methods.</span></span>



| <span data-ttu-id="db7ae-120">Метод</span><span class="sxs-lookup"><span data-stu-id="db7ae-120">Method</span></span>                                                | <span data-ttu-id="db7ae-121">Описание</span><span class="sxs-lookup"><span data-stu-id="db7ae-121">Description</span></span>                                   |
|-------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="db7ae-122">Очистить</span><span class="sxs-lookup"><span data-stu-id="db7ae-122">Clear</span></span>](downloadcollection-clear.md)                 | <span data-ttu-id="db7ae-123">Удаляет все элементы из коллекции загрузки.</span><span class="sxs-lookup"><span data-stu-id="db7ae-123">Removes all items from a download collection.</span></span> |
| [<span data-ttu-id="db7ae-124">Item</span><span class="sxs-lookup"><span data-stu-id="db7ae-124">item</span></span>](downloadcollection-item.md)                   | <span data-ttu-id="db7ae-125">Извлекает объект, ожидающий загрузки.</span><span class="sxs-lookup"><span data-stu-id="db7ae-125">Retrieves a pending download object.</span></span>          |
| [<span data-ttu-id="db7ae-126">removeItem</span><span class="sxs-lookup"><span data-stu-id="db7ae-126">removeItem</span></span>](downloadcollection-removeitem.md)       | <span data-ttu-id="db7ae-127">Удаляет элемент загрузки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="db7ae-127">Removes a download item from a collection.</span></span>    |
| [<span data-ttu-id="db7ae-128">стартдовнлоад</span><span class="sxs-lookup"><span data-stu-id="db7ae-128">startDownload</span></span>](downloadcollection-startdownload.md) | <span data-ttu-id="db7ae-129">Загружает в очередь.</span><span class="sxs-lookup"><span data-stu-id="db7ae-129">Queues a download.</span></span>                            |



 

<span data-ttu-id="db7ae-130">Доступ к объекту **довнлоадколлектион** осуществляется с помощью следующих методов.</span><span class="sxs-lookup"><span data-stu-id="db7ae-130">The **DownloadCollection** object is accessed through the following methods.</span></span>



| <span data-ttu-id="db7ae-131">Объект</span><span class="sxs-lookup"><span data-stu-id="db7ae-131">Object</span></span>                                        | <span data-ttu-id="db7ae-132">Метод</span><span class="sxs-lookup"><span data-stu-id="db7ae-132">Method</span></span>                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="db7ae-133">довнлоадманажер</span><span class="sxs-lookup"><span data-stu-id="db7ae-133">DownloadManager</span></span>](downloadmanager-object.md) | [<span data-ttu-id="db7ae-134">креатедовнлоадколлектион</span><span class="sxs-lookup"><span data-stu-id="db7ae-134">createDownloadCollection</span></span>](downloadmanager-createdownloadcollection.md) |
| [<span data-ttu-id="db7ae-135">довнлоадманажер</span><span class="sxs-lookup"><span data-stu-id="db7ae-135">DownloadManager</span></span>](downloadmanager-object.md) | [<span data-ttu-id="db7ae-136">жетдовнлоадколлектион</span><span class="sxs-lookup"><span data-stu-id="db7ae-136">getDownloadCollection</span></span>](downloadmanager-getdownloadcollection.md)       |



 

<span data-ttu-id="db7ae-137">В целях иллюстрации **довнлоадманажер**. **жетдовнлоадколлектион**(*CollectionID*) используется в разделах синтаксиса Reference.</span><span class="sxs-lookup"><span data-stu-id="db7ae-137">For purposes of illustration, **DownloadManager**.**getDownloadCollection**(*collectionId*) is used in the reference syntax sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db7ae-138">См. также</span><span class="sxs-lookup"><span data-stu-id="db7ae-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db7ae-139">**Справочные материалы по интернет-магазинам типа 2**</span><span class="sxs-lookup"><span data-stu-id="db7ae-139">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




