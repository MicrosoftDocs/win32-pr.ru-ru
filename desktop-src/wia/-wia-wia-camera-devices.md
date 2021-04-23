---
description: WIA представляет устройство камеры в виде иерархического дерева объектов Ивиаитем.
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: Устройства камеры WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002a14d8e047019b1af2d2f86c1fd4a2e00d7808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263122"
---
# <a name="wia-camera-devices"></a><span data-ttu-id="ee988-103">Устройства камеры WIA</span><span class="sxs-lookup"><span data-stu-id="ee988-103">WIA Camera Devices</span></span>

<span data-ttu-id="ee988-104">WIA представляет устройство камеры в виде иерархического дерева объектов [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="ee988-104">WIA represents a camera device as a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) objects.</span></span> <span data-ttu-id="ee988-105">Корневой элемент, возвращенный из вызова метода [**ивиадевмгр:: креатедевице**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) диспетчера устройств Windows Image (WIA), используется для получения и задания сведений об устройстве, управления устройством и для начала перечисления элементов устройства.</span><span class="sxs-lookup"><span data-stu-id="ee988-105">The root item, returned from a call to the Windows Image Acquisition (WIA) device manager [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) method, is used to get and set device information, to control the device, and to begin device item enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="ee988-106">WIA не поддерживает камеры в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="ee988-106">WIA does not support cameras in Windows Vista or later.</span></span> <span data-ttu-id="ee988-107">Для этих версий Windows используйте API переносных устройств Windows (WPD), описанный в пакете средств разработки драйверов Windows (DDK), для получения изображений из камер.</span><span class="sxs-lookup"><span data-stu-id="ee988-107">For those versions of the Windows, use the Windows Portable Device (WPD) API described in the Windows Driver Development Kit (DDK) to acquire images from cameras.</span></span>

 

<span data-ttu-id="ee988-108">На следующей схеме показан пример реализации камеры.</span><span class="sxs-lookup"><span data-stu-id="ee988-108">The following diagram illustrates a sample camera implementation.</span></span> <span data-ttu-id="ee988-109">Корневой элемент камеры имеет три дочерних элемента: два изображения и одна папка.</span><span class="sxs-lookup"><span data-stu-id="ee988-109">The camera root item has three child items, two pictures and one folder.</span></span> <span data-ttu-id="ee988-110">В папке есть два дочерних элемента, оба рисунка.</span><span class="sxs-lookup"><span data-stu-id="ee988-110">The folder has two child items, both pictures.</span></span>

![Реализация образца камеры](images/wihierar.gif)

 

 



