---
description: Дополнительные сведения о подключении к устройству
ms.assetid: 16ff280d-818b-4a4e-b5a6-16e81f5b35c6
title: Подключение к устройству
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fc7d8c78f77854a9adbedad7c0870721b3b037ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693084"
---
# <a name="connecting-to-a-device"></a><span data-ttu-id="c3be5-103">Подключение к устройству</span><span class="sxs-lookup"><span data-stu-id="c3be5-103">Connecting to a Device</span></span>

> [!Note]  
> <span data-ttu-id="c3be5-104">Эта система сценариев была заменена на уровень автоматизации службы "получение образа Windows" (WIA).</span><span class="sxs-lookup"><span data-stu-id="c3be5-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="c3be5-105">См. раздел [уровень службы "получение образа Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)".</span><span class="sxs-lookup"><span data-stu-id="c3be5-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="c3be5-106">Первым шагом в любом приложении или скрипте, использующем модель сценариев получения изображений Windows (WIA), является создание объекта [**WIA**](-wia-wia.md) .</span><span class="sxs-lookup"><span data-stu-id="c3be5-106">The first step in any application or script that uses the Windows Image Acquisition (WIA) scripting model is creating the [**Wia**](-wia-wia.md) object.</span></span> <span data-ttu-id="c3be5-107">Этот объект предоставляет методы для получения коллекции объектов [**DeviceInfo**](-wia-deviceinfo.md) и подключения этих объектов к устройствам.</span><span class="sxs-lookup"><span data-stu-id="c3be5-107">This object provides methods for to obtain a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects and connect these objects to devices.</span></span> <span data-ttu-id="c3be5-108">Он также обеспечивает возможность прослушивания аппаратных событий WIA.</span><span class="sxs-lookup"><span data-stu-id="c3be5-108">It also provides the ability to listen for WIA hardware events.</span></span>

<span data-ttu-id="c3be5-109">В следующей строке кода Microsoft Visual Basic Scripting Edition (VBScript) создается объект [**WIA**](-wia-wia.md) :</span><span class="sxs-lookup"><span data-stu-id="c3be5-109">The following line of Microsoft Visual Basic Scripting Edition (VBScript) code creates the [**Wia**](-wia-wia.md) object:</span></span>


```
objWia = CreateObject("Wia.Script")
```



<span data-ttu-id="c3be5-110">После создания объекта [**WIA**](-wia-wia.md) используйте его метод [**CREATE**](-wia-iwia-create.md) для подключения к аппаратному устройству WIA.</span><span class="sxs-lookup"><span data-stu-id="c3be5-110">After creating the [**Wia**](-wia-wia.md) object, use its [**Create**](-wia-iwia-create.md) method to connect to a WIA hardware device.</span></span>

<span data-ttu-id="c3be5-111">Для получения коллекции объектов [**DeviceInfo**](-wia-deviceinfo.md) можно также использовать свойство [**Devices**](-wia-iwia-devices.md) объекта [**WIA**](-wia-wia.md) .</span><span class="sxs-lookup"><span data-stu-id="c3be5-111">You can also use the [**Wia**](-wia-wia.md) object's [**Devices**](-wia-iwia-devices.md) property to obtain a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects.</span></span> <span data-ttu-id="c3be5-112">Перечисление этой коллекции и использование метода [**CREATE**](-wia-iwiadeviceinfo-create.md) для подключения к устройству.</span><span class="sxs-lookup"><span data-stu-id="c3be5-112">Enumerate this collection and use the [**Create**](-wia-iwiadeviceinfo-create.md) method to connect to a device.</span></span>

 

 
