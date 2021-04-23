---
title: Работа с проигрывателем
description: Работа с проигрывателем
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Обложки проигрывателя Windows Media, атрибут Player в JScript
- обложки, атрибут Player в JScript
- атрибуты, проигрыватель
- атрибут Player
- Файлы JScript для обложек, атрибут Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d47ea74b4c91f92ef33106e40e9896b98de6a34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411398"
---
# <a name="working-with-the-player"></a><span data-ttu-id="46813-108">Работа с проигрывателем</span><span class="sxs-lookup"><span data-stu-id="46813-108">Working with the Player</span></span>

<span data-ttu-id="46813-109">При использовании Microsoft JScript для доступа к методам и свойствам проигрывателя Windows Media необходимо использовать имя "Player" в качестве имени элемента управления.</span><span class="sxs-lookup"><span data-stu-id="46813-109">When using Microsoft JScript to access methods and properties of Windows Media Player, you must use the name "player" for the name of the control.</span></span> <span data-ttu-id="46813-110">Например, для ссылки на метод останавливаться необходимо ввести:</span><span class="sxs-lookup"><span data-stu-id="46813-110">For example, to reference the Stop method, you must type:</span></span>


```C++
player.Controls.Stop()

```



<span data-ttu-id="46813-111">Глобальный атрибут **игрока** — это ключ к доступу к элементу управления проигрывателя Windows Media через скрипты обложек.</span><span class="sxs-lookup"><span data-stu-id="46813-111">The **player** global attribute is the key to accessing the Windows Media Player control through skin scripting.</span></span> <span data-ttu-id="46813-112">С помощью этого атрибута все объекты элемента управления проигрывателя Windows Media становятся доступными для изменения во время выполнения с помощью их свойств и методов.</span><span class="sxs-lookup"><span data-stu-id="46813-112">Through this attribute, all the objects of the Windows Media Player control become accessible for run-time modification through their properties and methods.</span></span> <span data-ttu-id="46813-113">Кроме того, доступен элемент **Player** , позволяющий задавать обработчики событий и атрибут **URL-адреса** во время разработки.</span><span class="sxs-lookup"><span data-stu-id="46813-113">Additionally, the **PLAYER** element is available so that you can specify event handlers and the **url** attribute at design time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46813-114">См. также</span><span class="sxs-lookup"><span data-stu-id="46813-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46813-115">**Использование JScript**</span><span class="sxs-lookup"><span data-stu-id="46813-115">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




