---
description: Базовый механизм визуализации
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: Базовый механизм визуализации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9b51240b43c58de99b7d6fe1f7ad61f754c7ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537817"
---
# <a name="basic-render-engine"></a><span data-ttu-id="ccde6-103">Базовый механизм визуализации</span><span class="sxs-lookup"><span data-stu-id="ccde6-103">Basic Render Engine</span></span>

> [!Note]  
> <span data-ttu-id="ccde6-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ccde6-104">\[Deprecated.</span></span> <span data-ttu-id="ccde6-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ccde6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ccde6-106">Базовый объект модуля рендеринга отображает несжатые выходные данные из временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="ccde6-106">The Basic Render Engine object renders uncompressed output from a timeline.</span></span> <span data-ttu-id="ccde6-107">Чтобы создать этот объект, вызовите **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="ccde6-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="ccde6-108">Для сжатых выходных данных используйте интеллектуальный механизм визуализации.</span><span class="sxs-lookup"><span data-stu-id="ccde6-108">For compressed output, use the Smart Render Engine.</span></span> <span data-ttu-id="ccde6-109">Идентификатор класса — CLSID \_ рендеренгине.</span><span class="sxs-lookup"><span data-stu-id="ccde6-109">The class identifier is CLSID\_RenderEngine.</span></span>

<span data-ttu-id="ccde6-110">Базовый механизм визуализации предоставляет следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="ccde6-110">The Basic Render Engine exposes the following interfaces:</span></span>

-   [<span data-ttu-id="ccde6-111">**иамсетеррорлог**</span><span class="sxs-lookup"><span data-stu-id="ccde6-111">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   <span data-ttu-id="ccde6-112">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="ccde6-112">IObjectWithSite</span></span>
-   [<span data-ttu-id="ccde6-113">**ирендеренгине**</span><span class="sxs-lookup"><span data-stu-id="ccde6-113">**IRenderEngine**</span></span>](irenderengine.md)
-   [<span data-ttu-id="ccde6-114">**IRenderEngine2**</span><span class="sxs-lookup"><span data-stu-id="ccde6-114">**IRenderEngine2**</span></span>](irenderengine2.md)

## <a name="related-topics"></a><span data-ttu-id="ccde6-115">См. также</span><span class="sxs-lookup"><span data-stu-id="ccde6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccde6-116">Подготовка проекта</span><span class="sxs-lookup"><span data-stu-id="ccde6-116">Rendering a Project</span></span>](rendering-a-project.md)
</dt> <dt>

[<span data-ttu-id="ccde6-117">Модуль интеллектуального просмотра</span><span class="sxs-lookup"><span data-stu-id="ccde6-117">Smart Render Engine</span></span>](smart-render-engine.md)
</dt> </dl>

 

 



