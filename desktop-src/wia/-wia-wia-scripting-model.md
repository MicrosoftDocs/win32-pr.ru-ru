---
description: Программа получения изображений (WIA) предоставляет объекты автоматизации для использования в языках сценариев, таких как Microsoft JScript Visual Basic и программное обеспечение разработки сценариев VBScript, а также высокоуровневые языки программирования, такие как система разработки Visual Basic Microsoft.
ms.assetid: 3d294db3-3349-4b26-aae1-1e3f588a0f0e
title: Модель скриптов WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e70863e60e0d7aa6172bd9c93240f38cac27c6be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711079"
---
# <a name="wia-scripting-model"></a><span data-ttu-id="57709-103">Модель скриптов WIA</span><span class="sxs-lookup"><span data-stu-id="57709-103">WIA Scripting Model</span></span>

<span data-ttu-id="57709-104">Программа получения изображений (WIA) предоставляет объекты автоматизации для использования в языках сценариев, таких как Microsoft JScript Visual Basic и программное обеспечение разработки сценариев VBScript, а также высокоуровневые языки программирования, такие как система разработки Visual Basic Microsoft.</span><span class="sxs-lookup"><span data-stu-id="57709-104">Windows Image Acquisition (WIA) provides automation objects for use in scripting languages, such as Microsoft JScript and Microsoft Visual Basic Scripting Edition (VBScript) development software, and high-level programming languages such as Microsoft Visual Basic development system.</span></span>

> [!Note]  
> <span data-ttu-id="57709-105">Эта система сценариев была заменена на уровень автоматизации службы "получение образа Windows" (WIA).</span><span class="sxs-lookup"><span data-stu-id="57709-105">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="57709-106">См. раздел [уровень службы "получение образа Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)".</span><span class="sxs-lookup"><span data-stu-id="57709-106">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="57709-107">В следующей таблице описываются объекты сценариев WIA и их использование.</span><span class="sxs-lookup"><span data-stu-id="57709-107">The following table describes WIA scripting objects and how they are used.</span></span> 

| <span data-ttu-id="57709-108">Объект</span><span class="sxs-lookup"><span data-stu-id="57709-108">Object</span></span>                                | <span data-ttu-id="57709-109">Описание</span><span class="sxs-lookup"><span data-stu-id="57709-109">Description</span></span>                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57709-110">**Одно**</span><span class="sxs-lookup"><span data-stu-id="57709-110">**Wia**</span></span>](-wia-wia.md)               | <span data-ttu-id="57709-111">Объект скрипта WIA верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="57709-111">The top-level WIA scripting object.</span></span> <span data-ttu-id="57709-112">Используйте объект [**WIA**](-wia-wia.md) для перечисления и подключения к устройствам, а также для управления событиями устройств.</span><span class="sxs-lookup"><span data-stu-id="57709-112">Use the [**Wia**](-wia-wia.md) object to enumerate and connect to devices, and to handle hardware device events.</span></span>                                        |
| [<span data-ttu-id="57709-113">**DeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="57709-113">**DeviceInfo**</span></span>](-wia-deviceinfo.md) | <span data-ttu-id="57709-114">Объект [**DeviceInfo**](-wia-deviceinfo.md) предоставляет доступ к сведениям о свойствах устройства.</span><span class="sxs-lookup"><span data-stu-id="57709-114">The [**DeviceInfo**](-wia-deviceinfo.md) object provides access to information about device properties.</span></span>                                                                                     |
| [<span data-ttu-id="57709-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="57709-115">**Item**</span></span>](-wia-item.md)             | <span data-ttu-id="57709-116">Этот объект представляет элементы устройства WIA, файлов и папок.</span><span class="sxs-lookup"><span data-stu-id="57709-116">This object represents WIA device, file, and folder items.</span></span> <span data-ttu-id="57709-117">Аппаратное устройство WIA и его образы или сканирование кроватях представляются в виде иерархического дерева объектов [**элементов**](-wia-item.md) .</span><span class="sxs-lookup"><span data-stu-id="57709-117">A WIA hardware device and its images or scanning beds is represented as a hierarchical tree of [**Item**](-wia-item.md) objects.</span></span> |



 

<span data-ttu-id="57709-118">Объект [**DeviceInfo**](-wia-deviceinfo.md) и объект [**Item**](-wia-item.md) связаны с объектами коллекции.</span><span class="sxs-lookup"><span data-stu-id="57709-118">Both the [**DeviceInfo**](-wia-deviceinfo.md) object and the [**Item**](-wia-item.md) object are associated with collection objects.</span></span> <span data-ttu-id="57709-119">Сведения об использовании объектов коллекции см. в разделе Использование объектов коллекции WIA.</span><span class="sxs-lookup"><span data-stu-id="57709-119">For information about using collection objects, see Using WIA Collection Objects.</span></span>

<span data-ttu-id="57709-120">В следующих разделах рассматриваются общие сведения об использовании модели скриптов WIA.</span><span class="sxs-lookup"><span data-stu-id="57709-120">The following topics cover general information about using the WIA scripting model:</span></span>

-   [<span data-ttu-id="57709-121">Синтаксические обозначения</span><span class="sxs-lookup"><span data-stu-id="57709-121">Syntax Conventions</span></span>](-wia-syntax-conventions.md)
-   [<span data-ttu-id="57709-122">Использование объектов коллекции WIA</span><span class="sxs-lookup"><span data-stu-id="57709-122">Using WIA Collection Objects</span></span>](-wia-using-wia-collection-objects.md)
-   [<span data-ttu-id="57709-123">Определения констант свойств WIA</span><span class="sxs-lookup"><span data-stu-id="57709-123">WIA Property Constant Definitions</span></span>](-wia-wia-property-constant-definitions.md)

 

 
