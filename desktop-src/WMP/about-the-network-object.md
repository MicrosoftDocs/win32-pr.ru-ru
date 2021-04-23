---
title: О сетевом объекте
description: О сетевом объекте
ms.assetid: 367a51d4-2db8-4c9e-82b7-85b2b631c721
keywords:
- Проигрыватель Windows Media, объект "сеть"
- Объектная модель проигрывателя Windows Media, сетевой объект
- Объектная модель, сетевой объект
- Элемент управления ActiveX проигрывателя Windows Media, сетевой объект
- Элемент управления ActiveX, сетевой объект
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, сетевой объект
- Проигрыватель Windows Media Mobile, сетевой объект
- Сетевой объект
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1f3ff892a4d5b078956c9d126d0efaa844031d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773337"
---
# <a name="about-the-network-object"></a><span data-ttu-id="c5496-111">О сетевом объекте</span><span class="sxs-lookup"><span data-stu-id="c5496-111">About the Network Object</span></span>

<span data-ttu-id="c5496-112">Объект **Network** управляет свойствами, позволяющими определить, насколько хорошо содержимое потоковой передачи через сеть.</span><span class="sxs-lookup"><span data-stu-id="c5496-112">The **Network** object governs the properties that allow you to determine how well the content is streaming through the network.</span></span> <span data-ttu-id="c5496-113">Например, можно узнать, теряются ли пакеты, и выполнить соответствующие действия.</span><span class="sxs-lookup"><span data-stu-id="c5496-113">For example, you can find out whether packets are being lost and take appropriate action.</span></span> <span data-ttu-id="c5496-114">Доступ к **сетевому** объекту осуществляется только через свойство **Network** объекта **Player** .</span><span class="sxs-lookup"><span data-stu-id="c5496-114">The **Network** object is accessed only through the **network** property of the **Player** object.</span></span> <span data-ttu-id="c5496-115">Свойство **Network** возвращает объект **Network** .</span><span class="sxs-lookup"><span data-stu-id="c5496-115">The **network** property returns the **Network** object.</span></span> <span data-ttu-id="c5496-116">Доступ к свойствам **сетевого** объекта можно получить только после его создания.</span><span class="sxs-lookup"><span data-stu-id="c5496-116">You can only access the properties of the **Network** object after you have created it.</span></span> <span data-ttu-id="c5496-117">Например, чтобы использовать свойство **пропускной способности** , необходимо использовать следующий код:</span><span class="sxs-lookup"><span data-stu-id="c5496-117">For example, to use the **Bandwidth** property, you must use the following code:</span></span>


```C++
mybandwidth = player.network.bandwidth;

```



## <a name="related-topics"></a><span data-ttu-id="c5496-118">См. также</span><span class="sxs-lookup"><span data-stu-id="c5496-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5496-119">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="c5496-119">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="c5496-120">**Объектная модель проигрывателя для языков сценариев**</span><span class="sxs-lookup"><span data-stu-id="c5496-120">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




