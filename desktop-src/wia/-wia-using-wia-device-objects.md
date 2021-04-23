---
description: Устройство обработки изображений представляется в виде иерархического дерева объектов элементов WIA (интерфейсов Ивиаитем).
ms.assetid: 5f3e56aa-8616-4574-882c-619caf54ca04
title: Использование объектов устройств WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1af755b243d322feac746620cb9dd9bd9965d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145358"
---
# <a name="using-wia-device-objects"></a><span data-ttu-id="35dcd-103">Использование объектов устройств WIA</span><span class="sxs-lookup"><span data-stu-id="35dcd-103">Using WIA Device Objects</span></span>

<span data-ttu-id="35dcd-104">Устройство обработки изображений представляется в виде иерархического дерева объектов элементов WIA (интерфейсов [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ).</span><span class="sxs-lookup"><span data-stu-id="35dcd-104">An imaging device is represented in Windows Image Acquisition (WIA) as a hierarchical tree of WIA item objects ([**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interfaces).</span></span> <span data-ttu-id="35dcd-105">Как правило, корень этого дерева элементов представляет само устройство, а другие элементы в дереве представляют изображения, для камеры или для сканирования регионов для сканера.</span><span class="sxs-lookup"><span data-stu-id="35dcd-105">Typically, the root of this item tree represents the device itself, while the other items on the tree represent images, for a camera, or scanning regions, for a scanner.</span></span>

<span data-ttu-id="35dcd-106">Приложения используют диспетчер устройств WIA для создания и перечисления устройств WIA.</span><span class="sxs-lookup"><span data-stu-id="35dcd-106">Applications use the WIA device manager to create and enumerate WIA devices.</span></span> <span data-ttu-id="35dcd-107">В следующих разделах объясняется, как создавать и использовать устройства WIA:</span><span class="sxs-lookup"><span data-stu-id="35dcd-107">The following sections explain how to create and use WIA devices:</span></span>

-   [<span data-ttu-id="35dcd-108">Выбор устройства</span><span class="sxs-lookup"><span data-stu-id="35dcd-108">Selecting a Device</span></span>](-wia-selecting-a-device.md)
-   [<span data-ttu-id="35dcd-109">Устройства камеры WIA</span><span class="sxs-lookup"><span data-stu-id="35dcd-109">WIA Camera Devices</span></span>](-wia-wia-camera-devices.md)
-   [<span data-ttu-id="35dcd-110">Устройства сканера WIA</span><span class="sxs-lookup"><span data-stu-id="35dcd-110">WIA Scanner Devices</span></span>](-wia-wia-scanner-devices.md)

 

 



