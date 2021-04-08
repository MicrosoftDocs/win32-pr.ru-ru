---
title: Схема сообщений
description: Схема сообщений
ms.assetid: 4640b0f5-625e-4a9e-86f5-3e75d0afb40d
keywords:
- Подключаемые модули проигрывателя Windows Media, схема сообщений
- подключаемые модули, схема сообщений
- подключаемые модули пользовательского интерфейса, схема сообщений
- Подключаемые модули пользовательского интерфейса, схема сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea7fc04caf752383368ab6e51ae19c82e8c3515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068084"
---
# <a name="the-message-map"></a><span data-ttu-id="92055-107">Схема сообщений</span><span class="sxs-lookup"><span data-stu-id="92055-107">The Message Map</span></span>

<span data-ttu-id="92055-108">Окно подключаемого модуля реагирует на различные события, вызывая методы, сопоставленные с соответствующими сообщениями о событиях.</span><span class="sxs-lookup"><span data-stu-id="92055-108">The plug-in window responds to various events by calling methods that are mapped to corresponding event messages.</span></span> <span data-ttu-id="92055-109">Мастер обеспечивает сопоставление таким образом, что onpain и Онерасебаккграунд будут вызываться в нужное время.</span><span class="sxs-lookup"><span data-stu-id="92055-109">The wizard provides a mapping so that OnPaint and OnEraseBackground will be called at the appropriate times.</span></span> <span data-ttu-id="92055-110">Чтобы создать кнопку **поиска** и ответить на ее щелчки, раздел схемы сообщений изменяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="92055-110">To create the **Search** button and to respond to clicks from it, the message map section is modified as follows:</span></span>


```C++
BEGIN_MSG_MAP(CPluginWindow)
    MESSAGE_HANDLER(WM_PAINT, OnPaint)
    MESSAGE_HANDLER(WM_ERASEBKGND, OnEraseBackground)
    MESSAGE_HANDLER(WM_CREATE, OnCreate)
    COMMAND_ID_HANDLER(IDC_SEARCH, OnSearch)
END_MSG_MAP()

```



## <a name="related-topics"></a><span data-ttu-id="92055-111">См. также</span><span class="sxs-lookup"><span data-stu-id="92055-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92055-112">**Реализация Кплугинвиндов**</span><span class="sxs-lookup"><span data-stu-id="92055-112">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




