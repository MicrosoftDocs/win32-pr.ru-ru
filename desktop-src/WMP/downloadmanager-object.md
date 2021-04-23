---
title: Объект Довнлоадманажер
description: Объект Довнлоадманажер
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Интернет-магазины проигрывателя Windows Media, объект Довнлоадманажер
- Интернет-магазины, объект Довнлоадманажер
- Тип 2 Интернет-магазинов, объект Довнлоадманажер
- довнлоадманажер
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3555ee7b99c97e85ce856766bd9f670aac4229b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888583"
---
# <a name="downloadmanager-object"></a><span data-ttu-id="8663e-107">Объект Довнлоадманажер</span><span class="sxs-lookup"><span data-stu-id="8663e-107">DownloadManager Object</span></span>

> [!Note]  
> <span data-ttu-id="8663e-108">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="8663e-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="8663e-109">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8663e-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="8663e-110">Объект **довнлоадманажер** является корневым объектом для диспетчера загрузки проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8663e-110">The **DownloadManager** object is the root object for the Windows Media Player Download Manager.</span></span> <span data-ttu-id="8663e-111">Она может использоваться веб-страницами, размещенными в панелях задач службы "Интернет-магазин".</span><span class="sxs-lookup"><span data-stu-id="8663e-111">It can be used by webpages that are hosted in online store service task panes.</span></span>

<span data-ttu-id="8663e-112">Объект **довнлоадманажер** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8663e-112">The **DownloadManager** object supports the following methods.</span></span>



| <span data-ttu-id="8663e-113">Метод</span><span class="sxs-lookup"><span data-stu-id="8663e-113">Method</span></span>                                                                   | <span data-ttu-id="8663e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="8663e-114">Description</span></span>                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="8663e-115">креатедовнлоадколлектион</span><span class="sxs-lookup"><span data-stu-id="8663e-115">createDownloadCollection</span></span>](downloadmanager-createdownloadcollection.md) | <span data-ttu-id="8663e-116">Создает пустую коллекцию загрузки.</span><span class="sxs-lookup"><span data-stu-id="8663e-116">Creates an empty download collection.</span></span>        |
| [<span data-ttu-id="8663e-117">жетдовнлоадколлектион</span><span class="sxs-lookup"><span data-stu-id="8663e-117">getDownloadCollection</span></span>](downloadmanager-getdownloadcollection.md)       | <span data-ttu-id="8663e-118">Извлекает указанную коллекцию загрузки.</span><span class="sxs-lookup"><span data-stu-id="8663e-118">Retrieves the specified download collection.</span></span> |



 

<span data-ttu-id="8663e-119">Доступ к объекту **довнлоадманажер** осуществляется с помощью **внешнего объекта. Довнлоадманажер**.</span><span class="sxs-lookup"><span data-stu-id="8663e-119">The **DownloadManager** object is accessed by using **external.DownloadManager**.</span></span> <span data-ttu-id="8663e-120">В целях иллюстрации предполагается, что это значение было присвоено переменной с именем «Довнлоадманажер», которая будет использоваться для идентификации этого объекта в разделах синтаксиса Reference.</span><span class="sxs-lookup"><span data-stu-id="8663e-120">For illustration purposes, it is assumed that this value has been assigned to a variable named "DownloadManager", which will be used to identify this object in the reference syntax sections.</span></span>

<span data-ttu-id="8663e-121">В проигрывателе Windows Media 10 или более поздней версии свойство **довнлоадманажер** и объект доступны только из областей задач службы "Интернет-магазин".</span><span class="sxs-lookup"><span data-stu-id="8663e-121">In Windows Media Player 10 or later, the **DownloadManager** property and object are accessible only from online store service task panes.</span></span> <span data-ttu-id="8663e-122">Нельзя использовать **довнлоадманажер** из других функций, где доступен **внешний** объект, например Хтмлвиев, представление информационной центра и сведения о диске.</span><span class="sxs-lookup"><span data-stu-id="8663e-122">You cannot use the **DownloadManager** from other features where the **External** object is available, such as HTMLView, Info Center View, and album information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8663e-123">См. также</span><span class="sxs-lookup"><span data-stu-id="8663e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8663e-124">**Справочные материалы по интернет-магазинам типа 2**</span><span class="sxs-lookup"><span data-stu-id="8663e-124">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




