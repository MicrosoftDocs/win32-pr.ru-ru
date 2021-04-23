---
description: Приложение переходит к дереву элементов устройства для получения изображений (WIA), чтобы найти и выбрать образы на этом устройстве. С помощью этого метода приложение выбирает и получает изображение, не выполняя показ пользователю диалогового окна.
ms.assetid: 1f124b4a-45fb-4181-b45a-e810a61ac37d
title: Навигация по дереву элементов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787ff3b53690ae7db4ff69fd5de2f4f4186f8e43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541935"
---
# <a name="navigating-an-item-tree"></a><span data-ttu-id="18bbe-104">Навигация по дереву элементов</span><span class="sxs-lookup"><span data-stu-id="18bbe-104">Navigating an Item Tree</span></span>

<span data-ttu-id="18bbe-105">Приложение переходит к дереву элементов устройства для получения изображений (WIA), чтобы найти и выбрать образы на этом устройстве.</span><span class="sxs-lookup"><span data-stu-id="18bbe-105">An application navigates a Windows Image Acquisition (WIA) device's item tree to find and select images on that device.</span></span> <span data-ttu-id="18bbe-106">С помощью этого метода приложение выбирает и получает изображение, не выполняя показ пользователю диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="18bbe-106">Using this technique, an application selects and acquires an image without presenting a dialog box to the user.</span></span>

<span data-ttu-id="18bbe-107">Устройство WIA представляется как корневой элемент в дереве объектов [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) или [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="18bbe-107">A WIA device is represented as the root item in a tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="18bbe-108">Дочерние элементы в дереве представляют изображения для камеры или сканирования кроватях для сканера.</span><span class="sxs-lookup"><span data-stu-id="18bbe-108">The child items in the tree represent images for a camera or scan beds for a scanner.</span></span>

<span data-ttu-id="18bbe-109">После выбора устройства WIA приложение вызывает метод [**ивиаитем:: енумчилдитемс**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) интерфейса [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) или [**IWiaItem2**](-wia-iwiaitem2.md) устройства, чтобы перечислить дочерние элементы (Images или Scan кроватях) устройства.</span><span class="sxs-lookup"><span data-stu-id="18bbe-109">After a WIA device is selected, an application calls the [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) method of the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) interface of the device to enumerate the child items (the images or scan beds) of the device.</span></span> <span data-ttu-id="18bbe-110">Инструкции см. [в разделе Выбор устройства](-wia-selecting-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="18bbe-110">For instructions, see [Selecting a Device](-wia-selecting-a-device.md).</span></span>

<span data-ttu-id="18bbe-111">Метод [**ивиаитем:: енумчилдитемс**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) создает объект перечисления для дочерних элементов устройства и возвращает указатель на интерфейс [**иенумвиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) этого объекта.</span><span class="sxs-lookup"><span data-stu-id="18bbe-111">The [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) method creates an enumeration object for the child items of the device, and returns a pointer to that object's [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) interface.</span></span> <span data-ttu-id="18bbe-112">Затем приложение может использовать методы интерфейса **иенумвиаитем** для получения указателей на элементы в дереве элементов устройства.</span><span class="sxs-lookup"><span data-stu-id="18bbe-112">The application can then use the methods of the **IEnumWiaItem** interface to obtain pointers to the items in the device's item tree.</span></span>

 

 



