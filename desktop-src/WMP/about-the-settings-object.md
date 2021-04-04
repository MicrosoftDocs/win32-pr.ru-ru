---
title: Сведения об объекте Settings
description: Сведения об объекте Settings
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Проигрыватель Windows Media, объект параметров
- Объектная модель проигрывателя Windows Media, объект параметров
- Объектная модель, объект Settings
- Элемент управления ActiveX проигрывателя Windows Media, объект Settings
- Элемент управления ActiveX, объект Settings
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, объект Settings
- Проигрыватель Windows Media Mobile, объект параметров
- Объект параметров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20dae51d42e6c67a59ddc23dca19bc7f4180001
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887804"
---
# <a name="about-the-settings-object"></a><span data-ttu-id="f905c-111">Сведения об объекте Settings</span><span class="sxs-lookup"><span data-stu-id="f905c-111">About the Settings Object</span></span>

<span data-ttu-id="f905c-112">Объект **параметров** управляет параметрами таких элементов управления, как громкость, число воспроизведения, звук и т. д.</span><span class="sxs-lookup"><span data-stu-id="f905c-112">The **Settings** object governs the settings of the control such as volume, play count, mute, and so on.</span></span> <span data-ttu-id="f905c-113">Доступ к нему осуществляется только через свойство **Settings** объекта **Player** .</span><span class="sxs-lookup"><span data-stu-id="f905c-113">It is accessed only through the **Settings** property of the **Player** object.</span></span> <span data-ttu-id="f905c-114">Свойство **Settings** возвращает объект **Settings** .</span><span class="sxs-lookup"><span data-stu-id="f905c-114">The **Settings** property returns the **Settings** object.</span></span> <span data-ttu-id="f905c-115">Доступ к свойствам объекта **параметров** можно получить только после его создания.</span><span class="sxs-lookup"><span data-stu-id="f905c-115">You can only access the properties of the **Settings** object after you have created it.</span></span> <span data-ttu-id="f905c-116">Например, чтобы получить значение свойства **Volume** , необходимо использовать следующий код:</span><span class="sxs-lookup"><span data-stu-id="f905c-116">For example, to get the value of the **Volume** property, you must use the following code:</span></span>


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a><span data-ttu-id="f905c-117">См. также</span><span class="sxs-lookup"><span data-stu-id="f905c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f905c-118">**Объектная модель проигрывателя для языков сценариев**</span><span class="sxs-lookup"><span data-stu-id="f905c-118">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="f905c-119">**Объект параметров**</span><span class="sxs-lookup"><span data-stu-id="f905c-119">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 




