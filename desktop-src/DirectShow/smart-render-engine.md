---
description: Модуль интеллектуального просмотра
ms.assetid: 279be879-9728-4fa1-bdf7-6b48485fc75f
title: Модуль интеллектуального просмотра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa727397f21aeba754cfe41f2dc4f9c1da1c91b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682272"
---
# <a name="smart-render-engine"></a><span data-ttu-id="033e1-103">Модуль интеллектуального просмотра</span><span class="sxs-lookup"><span data-stu-id="033e1-103">Smart Render Engine</span></span>

> [!Note]  
> <span data-ttu-id="033e1-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="033e1-104">\[Deprecated.</span></span> <span data-ttu-id="033e1-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="033e1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="033e1-106">Объект интеллектуального модуля отрисовки визуализирует выходные данные из временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="033e1-106">The Smart Render Engine object renders compressed output from a timeline.</span></span> <span data-ttu-id="033e1-107">Чтобы создать этот объект, вызовите **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="033e1-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="033e1-108">Для несжатых выходных данных используйте базовый механизм визуализации.</span><span class="sxs-lookup"><span data-stu-id="033e1-108">For uncompressed output, use the Basic Render Engine.</span></span> <span data-ttu-id="033e1-109">Идентификатор класса — CLSID \_ смартрендеренгине.</span><span class="sxs-lookup"><span data-stu-id="033e1-109">The class identifier is CLSID\_SmartRenderEngine.</span></span>

<span data-ttu-id="033e1-110">Модуль интеллектуального просмотра предоставляет следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="033e1-110">The Smart Render Engine exposes the following interfaces:</span></span>

-   [<span data-ttu-id="033e1-111">**иамсетеррорлог**</span><span class="sxs-lookup"><span data-stu-id="033e1-111">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   <span data-ttu-id="033e1-112">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="033e1-112">**IObjectWithSite**</span></span>
-   [<span data-ttu-id="033e1-113">**ирендеренгине**</span><span class="sxs-lookup"><span data-stu-id="033e1-113">**IRenderEngine**</span></span>](irenderengine.md)
-   [<span data-ttu-id="033e1-114">**IRenderEngine2**</span><span class="sxs-lookup"><span data-stu-id="033e1-114">**IRenderEngine2**</span></span>](irenderengine2.md)
-   [<span data-ttu-id="033e1-115">**исмартрендеренгине**</span><span class="sxs-lookup"><span data-stu-id="033e1-115">**ISmartRenderEngine**</span></span>](ismartrenderengine.md)

## <a name="related-topics"></a><span data-ttu-id="033e1-116">См. также</span><span class="sxs-lookup"><span data-stu-id="033e1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="033e1-117">Подготовка проекта</span><span class="sxs-lookup"><span data-stu-id="033e1-117">Rendering a Project</span></span>](rendering-a-project.md)
</dt> <dt>

[<span data-ttu-id="033e1-118">Базовый механизм визуализации</span><span class="sxs-lookup"><span data-stu-id="033e1-118">Basic Render Engine</span></span>](basic-render-engine.md)
</dt> </dl>

 

 



