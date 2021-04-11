---
title: Использование контекстов устройств
description: Использование контекстов устройств
ms.assetid: 2e8de313-6218-4401-a578-73140e7fdae1
keywords:
- визуализации, контекст устройства
- Пользовательские визуализации, контекст устройства
- визуализации, функция Render
- Пользовательские визуализации, функция Render
- Функция Render, контекст устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c315d5004565644750f4adcd099fc165e81575
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330536"
---
# <a name="using-device-contexts"></a><span data-ttu-id="8a465-108">Использование контекстов устройств</span><span class="sxs-lookup"><span data-stu-id="8a465-108">Using Device Contexts</span></span>

<span data-ttu-id="8a465-109">Контекст устройства является стандартным обработчиком для контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="8a465-109">The device context is a standard handle to a device context.</span></span> <span data-ttu-id="8a465-110">Это необходимо для многих функций рисования, чтобы система Microsoft Windows знала, в каком окне нужно рисовать.</span><span class="sxs-lookup"><span data-stu-id="8a465-110">You need this for many drawing functions so that Microsoft Windows knows which window to draw in.</span></span> <span data-ttu-id="8a465-111">Например, чтобы нарисовать прямоугольник, необходимо указать контекст устройства.</span><span class="sxs-lookup"><span data-stu-id="8a465-111">For example, to draw a rectangle, you need to specify the device context.</span></span>


```C++
HDC hdc;
::Rectangle( hdc, 1, 1, 100, 100 );

```



<span data-ttu-id="8a465-112">Контекст устройства указывается проигрывателем Windows Media с помощью функции **Render** .</span><span class="sxs-lookup"><span data-stu-id="8a465-112">The device context is specified by Windows Media Player through the **Render** function.</span></span> <span data-ttu-id="8a465-113">Если подключаемый модуль визуализируется с помощью окна, необходимо использовать контекст устройства этого окна.</span><span class="sxs-lookup"><span data-stu-id="8a465-113">If your plug-in renders using a window, you'll need to use the device context of that window.</span></span> <span data-ttu-id="8a465-114">Используйте этот контекст устройства для любого инструмента рисования, для которого требуется контекст устройства.</span><span class="sxs-lookup"><span data-stu-id="8a465-114">Use this device context for any drawing tool that requires a device context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a465-115">См. также</span><span class="sxs-lookup"><span data-stu-id="8a465-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a465-116">**Реализация отрисовки**</span><span class="sxs-lookup"><span data-stu-id="8a465-116">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




