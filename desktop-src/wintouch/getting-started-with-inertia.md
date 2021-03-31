---
title: Инерция
description: В этом разделе описывается инерция для Windows Touch.
ms.assetid: c33dda89-c715-4da0-a7af-aa0010dfd88b
keywords:
- Касание Windows, инерция
- инерция, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b69ad31ec4a61f8723c9e52f87883dc4af3772
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067459"
---
# <a name="inertia"></a><span data-ttu-id="3d7e5-105">Инерция</span><span class="sxs-lookup"><span data-stu-id="3d7e5-105">Inertia</span></span>

<span data-ttu-id="3d7e5-106">В этом разделе описывается инерция для Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="3d7e5-106">This section explains inertia for Windows Touch.</span></span>

<span data-ttu-id="3d7e5-107">API инерции, входящий в Windows 7, обеспечивает единообразное поведение объектов в приложениях Windows Touch, предоставляя простую модель.</span><span class="sxs-lookup"><span data-stu-id="3d7e5-107">The inertia API included in Windows 7 enables consistent object behavior in Windows Touch applications by providing a simple physics model.</span></span> <span data-ttu-id="3d7e5-108">Инерция включается с помощью обработчика инерции — класса, который инкапсулирует функциональность.</span><span class="sxs-lookup"><span data-stu-id="3d7e5-108">Inertia is enabled by using the inertia processor, a class that encapsulates functionality.</span></span> <span data-ttu-id="3d7e5-109">Обработчик инерции работает путем обработки событий, которые передаются в него при завершении манипуляций с объектом и обработки траекторий объектов способом, согласованным с другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="3d7e5-109">The inertia processor works by processing events that are passed to it when object manipulations finish and by handling object trajectories in a way that is consistent with other applications.</span></span> <span data-ttu-id="3d7e5-110">Обратите внимание, что обработчик инерции тесно связан с обработчиком манипуляций, что упрощает добавление поддержки инерции в приложения, использующие манипуляции.</span><span class="sxs-lookup"><span data-stu-id="3d7e5-110">Note that the inertia processor is tightly coupled to the manipulation processor to simplify adding inertia support to applications that use manipulations.</span></span> <span data-ttu-id="3d7e5-111">На самом деле обработчик инерции вызывает те же события, что и обработчик манипуляции.</span><span class="sxs-lookup"><span data-stu-id="3d7e5-111">In fact, the inertia processor raises the same events that the manipulation processor does.</span></span> <span data-ttu-id="3d7e5-112">В следующем разделе объясняется, как приступить к работе с инерцией.</span><span class="sxs-lookup"><span data-stu-id="3d7e5-112">The following section explains how to get started with inertia.</span></span>



| <span data-ttu-id="3d7e5-113">Section</span><span class="sxs-lookup"><span data-stu-id="3d7e5-113">Section</span></span>                                                                      | <span data-ttu-id="3d7e5-114">Описание</span><span class="sxs-lookup"><span data-stu-id="3d7e5-114">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d7e5-115">Механика инерции</span><span class="sxs-lookup"><span data-stu-id="3d7e5-115">Inertia Mechanics</span></span>](inertia-mechanics.md)                                   | <span data-ttu-id="3d7e5-116">Поясняются основы вычислений инерции.</span><span class="sxs-lookup"><span data-stu-id="3d7e5-116">Explains the basics of inertia calculations.</span></span>                                                                             |
| [<span data-ttu-id="3d7e5-117">Обработка инерции в неуправляемом коде</span><span class="sxs-lookup"><span data-stu-id="3d7e5-117">Handling Inertia in Unmanaged Code</span></span>](handling-inertia-in-unmanaged-code.md) | <span data-ttu-id="3d7e5-118">Объясняет, как использовать интерфейс [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) для обработки инерции в неуправляемом коде.</span><span class="sxs-lookup"><span data-stu-id="3d7e5-118">Explains how to use the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface for handling inertia in unmanaged code.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3d7e5-119">См. также</span><span class="sxs-lookup"><span data-stu-id="3d7e5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d7e5-120">Манипуляции и инерция</span><span class="sxs-lookup"><span data-stu-id="3d7e5-120">Manipulations and Inertia</span></span>](manipulation-and-inertia.md)
</dt> </dl>

 

 




