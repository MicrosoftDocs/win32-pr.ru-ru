---
title: Об ошибках и объектах Ерроритем
description: Об ошибках и объектах Ерроритем
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Проигрыватель Windows Media, объект Error
- Объектная модель проигрывателя Windows Media, объект Error
- Объектная модель, объект Error
- Элемент управления ActiveX проигрывателя Windows Media, объект Error
- Элемент управления ActiveX, объект Error
- Элемент управления ActiveX мобильных устройств проигрывателя Windows Media, объект Error
- Проигрыватель Windows Media Mobile, объект Error
- Объект ошибки
- Проигрыватель Windows Media, объект Ерроритем
- Объектная модель проигрывателя Windows Media, объект Ерроритем
- Объектная модель, объект Ерроритем
- Элемент управления ActiveX проигрывателя Windows Media, объект Ерроритем
- Элемент управления ActiveX, объект Ерроритем
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, объект Ерроритем
- Проигрыватель Windows Media Mobile, объект Ерроритем
- Объект Ерроритем
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23064670f13229aca84ae6dc86cf27cf34abbc56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330440"
---
# <a name="about-the-error-and-erroritem-objects"></a><span data-ttu-id="6201b-119">Об ошибках и объектах Ерроритем</span><span class="sxs-lookup"><span data-stu-id="6201b-119">About the Error and ErrorItem Objects</span></span>

<span data-ttu-id="6201b-120">Объекты **Error** и **ерроритем** управляют функциями обработки ошибок проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6201b-120">The **Error** and **ErrorItem** objects govern the error-handling capabilities of Windows Media Player.</span></span> <span data-ttu-id="6201b-121">Объект **Error** извлекается из объекта **Player** через свойство **Error** .</span><span class="sxs-lookup"><span data-stu-id="6201b-121">The **Error** object is obtained from the **Player** object through the **error** property.</span></span> <span data-ttu-id="6201b-122">Вы можете получить конкретный код из объекта **Error** , используя свойство **Item** объекта **Error** для создания объекта **ерроритем** .</span><span class="sxs-lookup"><span data-stu-id="6201b-122">You can get a specific code from the **Error** object by using the **item** property of the **Error** object to create the **ErrorItem** object.</span></span> <span data-ttu-id="6201b-123">Например, чтобы получить код ошибки первого элемента ошибки, введите:</span><span class="sxs-lookup"><span data-stu-id="6201b-123">For example, to get the error code of the first error item, type:</span></span>


```C++
myerrorcode = player.error.item(0).errorCode;

```



<span data-ttu-id="6201b-124">Также можно вызвать веб-справку с объектом **Error** , используя следующий код:</span><span class="sxs-lookup"><span data-stu-id="6201b-124">You can also invoke Web Help with the **Error** object by using the following code:</span></span>


```C++
player.error.webHelp();

```



## <a name="related-topics"></a><span data-ttu-id="6201b-125">См. также</span><span class="sxs-lookup"><span data-stu-id="6201b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6201b-126">**Объект Error**</span><span class="sxs-lookup"><span data-stu-id="6201b-126">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="6201b-127">**Объект Ерроритем**</span><span class="sxs-lookup"><span data-stu-id="6201b-127">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="6201b-128">**Объектная модель проигрывателя для языков сценариев**</span><span class="sxs-lookup"><span data-stu-id="6201b-128">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




