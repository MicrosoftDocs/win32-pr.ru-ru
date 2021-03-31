---
description: Устройство сканера для получения изображений (WIA) реализуется в виде иерархического дерева объектов Ивиаитем.
ms.assetid: d716faec-9ace-422d-b6eb-ad4d86c1b0fd
title: Устройства сканера WIA в WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443277b0b580a481b523739cd5bc21642d827252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809970"
---
# <a name="wia-scanner-devices-in-wia-10"></a><span data-ttu-id="fa941-103">Устройства сканера WIA в WIA 1,0</span><span class="sxs-lookup"><span data-stu-id="fa941-103">WIA Scanner Devices in WIA 1.0</span></span>

> [!Note]  
> <span data-ttu-id="fa941-104">В этом разделе рассматривается дерево устройств сканера для приложений, использующих службу загрузки изображений Windows (WIA) 1,0 (которая поддерживается в Windows XP или более ранней версии).</span><span class="sxs-lookup"><span data-stu-id="fa941-104">This topic discusses the scanner device tree for applications that use the Windows Image Acquisition (WIA) 1.0 service (which is supported on Windows XP or earlier).</span></span> <span data-ttu-id="fa941-105">Сведения о дереве устройств (WIA) 2,0 элементов (которые поддерживаются в Windows Vista и более поздних версиях) см. в разделе [о дереве элементов IWiaItem2](-wia-about-item-tree.md).</span><span class="sxs-lookup"><span data-stu-id="fa941-105">For information on the device tree of Windows Image Acquisition (WIA) 2.0 items (which are supported on Windows Vista or later), see [About the IWiaItem2 Item Tree](-wia-about-item-tree.md).</span></span>

 

<span data-ttu-id="fa941-106">Устройство сканера для получения изображений (WIA) реализуется в виде иерархического дерева объектов [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="fa941-106">The Windows Image Acquisition (WIA) scanner device is implemented as a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) objects.</span></span> <span data-ttu-id="fa941-107">Из корневого элемента приложение может:</span><span class="sxs-lookup"><span data-stu-id="fa941-107">From the root item an application may:</span></span>

-   <span data-ttu-id="fa941-108">Запрос возможностей сканера</span><span class="sxs-lookup"><span data-stu-id="fa941-108">Query scanner capabilities</span></span>
-   <span data-ttu-id="fa941-109">Настройка свойств устройства сканера</span><span class="sxs-lookup"><span data-stu-id="fa941-109">Set scanner device properties</span></span>
-   <span data-ttu-id="fa941-110">Управление устройством подачи документов</span><span class="sxs-lookup"><span data-stu-id="fa941-110">Control the document feeder</span></span>

<span data-ttu-id="fa941-111">Устройство сканера WIA отличается от устройства камеры WIA, поскольку в целом оно не хранит несколько образов в памяти.</span><span class="sxs-lookup"><span data-stu-id="fa941-111">A WIA scanner device is different from a WIA camera device because, in general, it does not store multiple images in memory.</span></span>

<span data-ttu-id="fa941-112">Под корневым элементом обычный объект сканера имеет один объект [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) , представляющий функции сбора данных устройства, элемента Scan.</span><span class="sxs-lookup"><span data-stu-id="fa941-112">Underneath the root item, a typical scanner object has a single [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object that represents the data collecting functionality of the device, the Scan Item.</span></span> <span data-ttu-id="fa941-113">Для этого элемента установлен флаг [**виаитемтипефиле**](-wia-wia-item-type-flags.md) , указывающий, что передача данных в этом элементе возможна.</span><span class="sxs-lookup"><span data-stu-id="fa941-113">This item has the [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) flag set to indicate that data transfers on this item are possible.</span></span> <span data-ttu-id="fa941-114">Приложение настраивает проверку, задавая свойства элемента Scan, затем выполняет проверку и передает данные с помощью интерфейса передачи данных.</span><span class="sxs-lookup"><span data-stu-id="fa941-114">An application sets up a scan by setting the properties of the scan item, then performs the scan and transfers the data using a data transfer interface.</span></span>

<span data-ttu-id="fa941-115">На следующей схеме показана реализация WIA для типичного сканера:</span><span class="sxs-lookup"><span data-stu-id="fa941-115">The following diagram illustrates the WIA implementation for a typical scanner:</span></span>

![реализация стандартного сканера WIA](images/wiscantr.gif)

<span data-ttu-id="fa941-117">Обычный дуплексный сканер представлен в WIA с помощью одного объекта [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="fa941-117">A typical duplex scanner is represented in WIA by having one [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object.</span></span> <span data-ttu-id="fa941-118">Доступ к данным внешнего и фонового страниц осуществляется последовательно по одному передаче данных на страницу.</span><span class="sxs-lookup"><span data-stu-id="fa941-118">Front- and back-page data is accessed sequentially one data transfer per page.</span></span> <span data-ttu-id="fa941-119">Поэтому представление дуплексного сканера идентично представлению обычного сканера.</span><span class="sxs-lookup"><span data-stu-id="fa941-119">Therefore, the representation of a duplex scanner is identical to the representation of a typical scanner.</span></span>

<span data-ttu-id="fa941-120">Сканер слайдов, способный сканировать несколько слайдов в одной операции сканирования, представляет каждый отдельный образ как отдельный объект [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="fa941-120">A slide scanner capable of scanning multiple slides in a single scan operation represents each separate image as a separate [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object.</span></span>

<span data-ttu-id="fa941-121">На следующей схеме показано WIA-представление сканера слайдов.</span><span class="sxs-lookup"><span data-stu-id="fa941-121">The following diagram illustrates the WIA representation of a slide scanner:</span></span>

![сканер слайдов](images/wislscan.gif)

 

 



