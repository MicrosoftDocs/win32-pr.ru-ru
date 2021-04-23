---
title: Сведения об объекте Player
description: Сведения об объекте Player
ms.assetid: db995e75-d4e3-4f50-a34a-cc1b2f2c5db5
keywords:
- Проигрыватель Windows Media Player, объект Player
- Объектная модель проигрывателя Windows Media, объект Player
- Объектная модель, объект Player
- Элемент управления ActiveX проигрывателя Windows Media, объект Player
- Элемент управления ActiveX, объект Player
- Элемент управления ActiveX проигрывателя Windows Media Mobile, объект Player
- Проигрыватель Windows Media Mobile, объект Player
- Объект Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c030d42cd6fd65811c41af7401ec3e60c8c7801
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104133026"
---
# <a name="about-the-player-object"></a><span data-ttu-id="56434-111">Сведения об объекте Player</span><span class="sxs-lookup"><span data-stu-id="56434-111">About the Player Object</span></span>

<span data-ttu-id="56434-112">Объект **Player** — это основной объект для элемента управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="56434-112">The **Player** object is the core object for the Windows Media Player control.</span></span> <span data-ttu-id="56434-113">Все прочие связанные объекты подключаются к этому объекту через определенные свойства, которые возвращают объект.</span><span class="sxs-lookup"><span data-stu-id="56434-113">All other related objects are connected to this object through specific properties that return the object.</span></span> <span data-ttu-id="56434-114">Например, доступ к объекту **параметров** осуществляется через свойство **Settings** .</span><span class="sxs-lookup"><span data-stu-id="56434-114">For example, the **Settings** object is accessed through the **settings** property.</span></span> <span data-ttu-id="56434-115">Объект **Player** предоставляет методы, свойства и события, относящиеся к основным функциям проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="56434-115">The **Player** object provides methods, properties, and events that relate to the core functionality of Windows Media Player.</span></span>

<span data-ttu-id="56434-116">Так как эта ссылка также используется для программирования обложек, идентификатор объекта **проигрывателя** будет "Player" для примеров синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="56434-116">Because this reference is also to be used for skins programming, the ID of the **Player** object will be "player" for syntax examples.</span></span>

<span data-ttu-id="56434-117">Использование глобального атрибута **Player** в файле определения обложки предоставляет доступ к объекту **Player** для использования в сценариях.</span><span class="sxs-lookup"><span data-stu-id="56434-117">Using the **player** global attribute within a skin definition file gives access to the **Player** object for use in scripting.</span></span> <span data-ttu-id="56434-118">С помощью объекта **Player** все остальные объекты в элементе управления проигрывателя Windows Media также становятся доступными для сценариев.</span><span class="sxs-lookup"><span data-stu-id="56434-118">Through the **Player** object, all other objects in the Windows Media Player control become accessible to scripts as well.</span></span> <span data-ttu-id="56434-119">События объекта **Player** и свойства **URL-адреса** можно также указать во время разработки с помощью элемента Skin [проигрывателя](player-element.md) .</span><span class="sxs-lookup"><span data-stu-id="56434-119">The events of the **Player** object and the **URL** property can also be specified at design time using the [PLAYER](player-element.md) skin element.</span></span> <span data-ttu-id="56434-120">Дополнительные сведения см. в разделе [обложки проигрывателя Windows Media](windows-media-player-skins.md).</span><span class="sxs-lookup"><span data-stu-id="56434-120">For more information, see [Windows Media Player Skins](windows-media-player-skins.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56434-121">См. также</span><span class="sxs-lookup"><span data-stu-id="56434-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56434-122">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="56434-122">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="56434-123">**Объектная модель проигрывателя для языков сценариев**</span><span class="sxs-lookup"><span data-stu-id="56434-123">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




