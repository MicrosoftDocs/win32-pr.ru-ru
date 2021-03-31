---
title: Сведения об объектах CDROM и Кдромколлектион
description: Сведения об объектах CDROM и Кдромколлектион
ms.assetid: b764806b-d9e1-4c36-b86b-24613501c926
keywords:
- Проигрыватель Windows Media, объект CDROM
- Объектная модель проигрывателя Windows Media, объект CDROM
- Объектная модель, объект CDROM
- Элемент управления ActiveX проигрывателя Windows Media, объект CDROM
- Элемент управления ActiveX, объект CDROM
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, объект CDROM
- Проигрыватель Windows Media Mobile, объект CDROM
- Объект CDROM
- Проигрыватель Windows Media, объект Кдромколлектион
- Объектная модель проигрывателя Windows Media, объект Кдромколлектион
- Объектная модель, объект Кдромколлектион
- Элемент управления ActiveX проигрывателя Windows Media, объект Кдромколлектион
- Элемент управления ActiveX, объект Кдромколлектион
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, объект Кдромколлектион
- Проигрыватель Windows Media Mobile, объект Кдромколлектион
- Объект Кдромколлектион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8fca9f7097f67226e31173670ca2935969704a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776937"
---
# <a name="about-the-cdrom-and-cdromcollection-objects"></a><span data-ttu-id="3ec13-119">Сведения об объектах CDROM и Кдромколлектион</span><span class="sxs-lookup"><span data-stu-id="3ec13-119">About the Cdrom and CdromCollection Objects</span></span>

<span data-ttu-id="3ec13-120">Объекты **CDROM** и **кдромколлектион** управляют интерфейсом для дисководов компакт-дисков на компьютере в целях чтения и воспроизведения CD.</span><span class="sxs-lookup"><span data-stu-id="3ec13-120">The **Cdrom** and **CdromCollection** objects govern the interface to the CD drives in your computer for purposes of reading and playing CDs.</span></span>

<span data-ttu-id="3ec13-121">Доступ к объекту **кдромколлектион** осуществляется только через свойство **кдромколлектион** объекта **Player** .</span><span class="sxs-lookup"><span data-stu-id="3ec13-121">The **CdromCollection** object is accessed only through the **cdromCollection** property of the **Player** object.</span></span> <span data-ttu-id="3ec13-122">Свойство **кдромколлектион** возвращает объект **кдромколлектион** .</span><span class="sxs-lookup"><span data-stu-id="3ec13-122">The **cdromCollection** property returns the **CdromCollection** object.</span></span> <span data-ttu-id="3ec13-123">Доступ к свойствам объекта **кдромколлектион** можно получить только после его создания.</span><span class="sxs-lookup"><span data-stu-id="3ec13-123">You can only access the properties of the **CdromCollection** object after you have created it.</span></span> <span data-ttu-id="3ec13-124">Например, чтобы использовать свойство **Count** , необходимо использовать следующий код:</span><span class="sxs-lookup"><span data-stu-id="3ec13-124">For example, to use the **count** property, you must use the following code:</span></span>


```C++
mycount = player.cdromcollection.count;
```



<span data-ttu-id="3ec13-125">Доступ к объекту **CDROM** можно получить только через объект **кдромколлектион** .</span><span class="sxs-lookup"><span data-stu-id="3ec13-125">You can only access the **Cdrom** object through the **CdromCollection** object.</span></span> <span data-ttu-id="3ec13-126">Например, чтобы извлечь компакт-диск с помощью метода **Eject** , необходимо сначала создать объект коллекции, а затем элемент в объекте.</span><span class="sxs-lookup"><span data-stu-id="3ec13-126">For example, to eject the CD by using the **Eject** method, you must first create the collection object and then an item in the object.</span></span> <span data-ttu-id="3ec13-127">Чтобы извлечь компакт-диск, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="3ec13-127">To eject the CD, use the following code:</span></span>


```C++
player.cdromcollection.item(0).eject();
```



<span data-ttu-id="3ec13-128">В обоих случаях сначала создается объект коллекции (**кдромколлектион**), а затем получается конкретный объект этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="3ec13-128">In both cases, you are first creating the collection object (**CdromCollection**) and then getting a specific object of that collection.</span></span> <span data-ttu-id="3ec13-129">Объект является первым элементом в коллекции, **элементом**(0), который соответствует первому компакт-диску.</span><span class="sxs-lookup"><span data-stu-id="3ec13-129">The object is the first item in the collection, **Item**(0), which corresponds to the first CD drive.</span></span> <span data-ttu-id="3ec13-130">Затем в этом элементе вызывается метод, который можно **извлечь**.</span><span class="sxs-lookup"><span data-stu-id="3ec13-130">You then call a method, **Eject**, on that item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ec13-131">См. также</span><span class="sxs-lookup"><span data-stu-id="3ec13-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ec13-132">**Объект CDROM**</span><span class="sxs-lookup"><span data-stu-id="3ec13-132">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="3ec13-133">**Объект Кдромколлектион**</span><span class="sxs-lookup"><span data-stu-id="3ec13-133">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="3ec13-134">**Объектная модель проигрывателя для языков сценариев**</span><span class="sxs-lookup"><span data-stu-id="3ec13-134">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




