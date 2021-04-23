---
title: Различия между объектными моделями
description: Различия между объектными моделями
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Проигрыватель Windows Media, объектная модель
- Объектная модель проигрывателя Windows Media, отличия версий
- Объектная модель, различия версий
- Элемент управления ActiveX проигрывателя Windows Media, различия версий
- Элемент управления ActiveX, различия версий
- Элемент управления ActiveX мобильных устройств проигрывателя Windows Media, различия версий
- Проигрыватель Windows Media Mobile, объектная модель
- рекомендации по миграции, отличия версий
- версии проигрывателя Windows Media, объектная модель
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5341067e2daad0f44fbdd7075f0f543bac2fd4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691304"
---
# <a name="differences-between-the-object-models"></a><span data-ttu-id="7033a-112">Различия между объектными моделями</span><span class="sxs-lookup"><span data-stu-id="7033a-112">Differences Between the Object Models</span></span>

<span data-ttu-id="7033a-113">Существует два основных различия между объектной моделью проигрывателя Windows Media 6,4 и объектной моделью проигрывателя Windows Media 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="7033a-113">There are two primary differences between the Windows Media Player 6.4 object model and the Windows Media Player 7 or later object model.</span></span>

-   <span data-ttu-id="7033a-114">**Идентификатор CLSID** Объектная модель проигрывателя Windows Media 7 или более поздней версии — это законченная версия объектной модели версии 6,4.</span><span class="sxs-lookup"><span data-stu-id="7033a-114">**CLSID** The Windows Media Player 7 or later object model is a complete departure from the version 6.4 object model.</span></span> <span data-ttu-id="7033a-115">Спецификация модели COM требует, чтобы все существующие интерфейсы продолжали функционировать в новых версиях COM-компонента.</span><span class="sxs-lookup"><span data-stu-id="7033a-115">The Component Object Model (COM) specification requires that all existing interfaces must continue to function in new versions of a COM component.</span></span> <span data-ttu-id="7033a-116">Это означает, что новые интерфейсы можно добавить в COM-компонент, но существующие интерфейсы никогда не должны изменяться, гарантируя, что более старый код клиента будет всегда работать с конкретным компонентом, который он должен использовать.</span><span class="sxs-lookup"><span data-stu-id="7033a-116">This means that new interfaces can be added to a COM component, but existing interfaces must never be altered, ensuring older client code will always work with the particular component it was designed to use.</span></span> <span data-ttu-id="7033a-117">Поэтому в проигрывателе Windows Media 7 или более поздней версии элемент управления ActiveX имеет новый идентификатор класса: 6BF52A52-394A-11D3-B153-00C04F79FAA6.</span><span class="sxs-lookup"><span data-stu-id="7033a-117">Therefore, the Windows Media Player 7 or later ActiveX control has a new class ID: 6BF52A52-394A-11D3-B153-00C04F79FAA6.</span></span> <span data-ttu-id="7033a-118">Если вы хотите воспользоваться преимуществами новых функций элемента управления для этой версии, необходимо изменить идентификатор CLSID.</span><span class="sxs-lookup"><span data-stu-id="7033a-118">If you want to take advantage of the new functionality of the control for this version, you must change your CLSID.</span></span>
-   <span data-ttu-id="7033a-119">**Иерархическая объектная модель** Если вы использовали элемент управления ActiveX проигрывателя Windows Media 6,4, вы могли заметить, что доступ ко всем свойствам, методам и событиям осуществляется через один и тот же объект: объект **Player** .</span><span class="sxs-lookup"><span data-stu-id="7033a-119">**Hierarchical Object Model** If you've been using the Windows Media Player 6.4 ActiveX control, you may have noticed that all the properties, methods, and events are accessed through the same object: the **Player** object.</span></span> <span data-ttu-id="7033a-120">В отличие от этого, объектная модель проигрывателя Windows Media 7 или более поздней версии организована как иерархия объектов.</span><span class="sxs-lookup"><span data-stu-id="7033a-120">By contrast, the Windows Media Player 7 or later object model is organized as a hierarchy of objects.</span></span> <span data-ttu-id="7033a-121">Объект **Player** по-прежнему является корневым объектом, но доступ к функциям теперь осуществляется через разнообразные дочерние объекты.</span><span class="sxs-lookup"><span data-stu-id="7033a-121">The **Player** object is still the root object, but functions are now accessed through a variety of child objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7033a-122">См. также</span><span class="sxs-lookup"><span data-stu-id="7033a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7033a-123">**Руководством по миграции объектной модели**</span><span class="sxs-lookup"><span data-stu-id="7033a-123">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




