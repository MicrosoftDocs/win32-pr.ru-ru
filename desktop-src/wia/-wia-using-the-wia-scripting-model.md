---
description: С помощью модели сценариев WIA функциональные возможности получения изображений (WIA) становятся доступными для языков сценариев, таких как Microsoft JScript Development Software и Microsoft Visual Basic Scripting Edition (VBScript), и высокоуровневых языков, таких как система разработки Microsoft Visual Basic.
ms.assetid: eec5dc91-7b32-4f38-bdfe-c11bddc17ba2
title: Использование модели скриптов WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: affa2c4368a83b2d67c1c6219b76040ba043a1f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692411"
---
# <a name="using-the-wia-scripting-model"></a><span data-ttu-id="a86f5-103">Использование модели скриптов WIA</span><span class="sxs-lookup"><span data-stu-id="a86f5-103">Using the WIA Scripting Model</span></span>

<span data-ttu-id="a86f5-104">С помощью [модели сценариев WIA](-wia-wia-scripting-model.md)функциональные возможности получения изображений (WIA) становятся доступными для языков сценариев, таких как Microsoft JScript Development Software и Microsoft Visual Basic Scripting Edition (VBScript), и высокоуровневых языков, таких как система разработки Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a86f5-104">Through the [WIA Scripting Model](-wia-wia-scripting-model.md), Windows Image Acquisition (WIA) functionality is made available to scripting languages such as Microsoft JScript development software and Microsoft Visual Basic Scripting Edition (VBScript), and high-level languages such as Microsoft Visual Basic development system.</span></span>

> [!Note]  
> <span data-ttu-id="a86f5-105">Эта система сценариев была заменена на уровень автоматизации службы "получение образа Windows" (WIA).</span><span class="sxs-lookup"><span data-stu-id="a86f5-105">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="a86f5-106">См. раздел [уровень службы "получение образа Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)".</span><span class="sxs-lookup"><span data-stu-id="a86f5-106">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="a86f5-107">Модель скриптов WIA предоставляет объекты, наследующие интерфейс [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="a86f5-107">The WIA scripting model exposes objects that inherit the [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) interface.</span></span>

<span data-ttu-id="a86f5-108">Модель скриптов предлагает упрощенную версию ВИААПИ.</span><span class="sxs-lookup"><span data-stu-id="a86f5-108">The scripting model offers a simplified version of the WIAAPI.</span></span>

<span data-ttu-id="a86f5-109">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="a86f5-109">For more information, see the following:</span></span>

-   [<span data-ttu-id="a86f5-110">Настройка среды разработки модели сценариев</span><span class="sxs-lookup"><span data-stu-id="a86f5-110">Setting up the Scripting Model Development Environment</span></span>](-wia-setting-up-the-scripting-model.md)
-   [<span data-ttu-id="a86f5-111">Подключение к устройству</span><span class="sxs-lookup"><span data-stu-id="a86f5-111">Connecting to a Device</span></span>](-wia-connecting-to-a-device.md)
-   [<span data-ttu-id="a86f5-112">Навигация по дереву объектов элементов</span><span class="sxs-lookup"><span data-stu-id="a86f5-112">Navigating a Tree of Item Objects</span></span>](-wia-navigating-a-tree-of-item-objects.md)
-   [<span data-ttu-id="a86f5-113">Передача данных</span><span class="sxs-lookup"><span data-stu-id="a86f5-113">Transferring Data</span></span>](-wia-transferring-data.md)
-   [<span data-ttu-id="a86f5-114">Ограничения модели скриптов</span><span class="sxs-lookup"><span data-stu-id="a86f5-114">Limitations of the Scripting Model</span></span>](-wia-limitations-of-the-scripting-model.md)

 

 
