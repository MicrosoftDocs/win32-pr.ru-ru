---
title: Об объекте Controls
description: Об объекте Controls
ms.assetid: 1678c931-af47-42c9-a8a5-b6b775aebda8
keywords:
- Проигрыватель Windows Media, объект Controls
- Объектная модель проигрывателя Windows Media, объект Controls
- Объектная модель, объект Controls
- Элемент управления ActiveX проигрывателя Windows Media, объект Controls
- Элемент управления ActiveX, объект Controls
- Элемент управления ActiveX проигрывателя Windows Media Mobile, объект Controls
- Проигрыватель Windows Media Mobile, объект Controls
- Объект Controls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f064ef65401876dedb4181ba788788f5e5d9676c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410630"
---
# <a name="about-the-controls-object"></a><span data-ttu-id="9c8df-111">Об объекте Controls</span><span class="sxs-lookup"><span data-stu-id="9c8df-111">About the Controls Object</span></span>

<span data-ttu-id="9c8df-112">Объект **Controls** управляет передачей цифрового мультимедийного содержимого через элемент управления с помощью таких методов, как **Play** и **останавливаться**.</span><span class="sxs-lookup"><span data-stu-id="9c8df-112">The **Controls** object governs the transport of digital media content through the control by using methods such as **Play** and **Stop**.</span></span> <span data-ttu-id="9c8df-113">Доступ к нему осуществляется только через свойство **Controls** объекта **Player** .</span><span class="sxs-lookup"><span data-stu-id="9c8df-113">It is accessed only through the **Controls** property of the **Player** object.</span></span> <span data-ttu-id="9c8df-114">Свойство **Controls** возвращает объект **Controls** .</span><span class="sxs-lookup"><span data-stu-id="9c8df-114">The **Controls** property returns the **Controls** object.</span></span> <span data-ttu-id="9c8df-115">Доступ к свойствам объекта **элементов управления** можно получить только после его создания.</span><span class="sxs-lookup"><span data-stu-id="9c8df-115">You can only access the properties of the **Controls** object after you have created it.</span></span> <span data-ttu-id="9c8df-116">Например, чтобы использовать метод **Play** , необходимо использовать следующий код:</span><span class="sxs-lookup"><span data-stu-id="9c8df-116">For example, to use the **Play** method, you must use the following code:</span></span>


```C++
player.controls.play();

```



## <a name="related-topics"></a><span data-ttu-id="9c8df-117">См. также</span><span class="sxs-lookup"><span data-stu-id="9c8df-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c8df-118">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="9c8df-118">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="9c8df-119">**Объектная модель проигрывателя для языков сценариев**</span><span class="sxs-lookup"><span data-stu-id="9c8df-119">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




