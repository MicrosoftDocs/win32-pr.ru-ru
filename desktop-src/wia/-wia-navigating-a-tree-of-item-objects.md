---
description: 'Дополнительные сведения: Навигация по дереву объектов элементов'
ms.assetid: e91f72c8-3ad6-49e8-88cc-aa99c13cd4c2
title: Навигация по дереву объектов элементов
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04e87444c2b9c473268c5e97dd9c26d04d95b93b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711093"
---
# <a name="navigating-a-tree-of-item-objects"></a><span data-ttu-id="2ff68-103">Навигация по дереву объектов элементов</span><span class="sxs-lookup"><span data-stu-id="2ff68-103">Navigating a Tree of Item Objects</span></span>

> [!Note]  
> <span data-ttu-id="2ff68-104">Эта система сценариев была заменена на уровень автоматизации службы "получение образа Windows" (WIA).</span><span class="sxs-lookup"><span data-stu-id="2ff68-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="2ff68-105">См. раздел [уровень службы "получение образа Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)".</span><span class="sxs-lookup"><span data-stu-id="2ff68-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="2ff68-106">Приложение или сценарий выполняет навигацию по дереву элементов устройства для получения изображений (WIA), чтобы найти и выбрать образы на этом устройстве.</span><span class="sxs-lookup"><span data-stu-id="2ff68-106">An application or script navigates a Windows Image Acquisition (WIA) device's item tree to find and select images on that device.</span></span> <span data-ttu-id="2ff68-107">С помощью этого метода приложение выбирает и получает образ без использования диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="2ff68-107">Using this technique, an application selects and acquires an image without the use of a dialog box.</span></span>

<span data-ttu-id="2ff68-108">Устройство WIA представляется как корневой элемент в дереве объектов [**элементов**](-wia-item.md) .</span><span class="sxs-lookup"><span data-stu-id="2ff68-108">A WIA device is represented as the root item in a tree of [**Item**](-wia-item.md) objects.</span></span> <span data-ttu-id="2ff68-109">Дочерние элементы в дереве представляют собой папки и изображения для камеры или сканирования кроватях для сканера.</span><span class="sxs-lookup"><span data-stu-id="2ff68-109">The child items in the tree represent folders and images for a camera or scan beds for a scanner.</span></span>

<span data-ttu-id="2ff68-110">После подключения к устройству вызовите свойство [**Children**](-wia-iwiadispatchitem-children.md) объекта [**Item**](-wia-item.md) , представляющего устройство (корневой элемент дерева), чтобы получить коллекцию дочерних элементов (изображений или сканирования кроватях) устройства.</span><span class="sxs-lookup"><span data-stu-id="2ff68-110">After connecting to a device, call the [**Children**](-wia-iwiadispatchitem-children.md) property of the [**Item**](-wia-item.md) object that represents the device (the root item of the tree) to obtain a collection of the child items (the images or scan beds) of the device.</span></span>

<span data-ttu-id="2ff68-111">Перечислите эту коллекцию (при необходимости) для навигации по дереву элементов.</span><span class="sxs-lookup"><span data-stu-id="2ff68-111">Enumerate this collection (recursively, if necessary) to navigate item tree.</span></span>

 

 
