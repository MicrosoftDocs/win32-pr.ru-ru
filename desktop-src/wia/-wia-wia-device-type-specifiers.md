---
description: Описатели типов устройств для получения изображений (WIA) — это константы, указывающие тип устройства, подключенного к компьютеру пользователя.
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: Описатели типа устройства WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc18b000d84bec5e5be37a5a5c52f28f6f8325d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711085"
---
# <a name="wia-device-type-specifiers"></a><span data-ttu-id="8877a-103">Описатели типа устройства WIA</span><span class="sxs-lookup"><span data-stu-id="8877a-103">WIA Device Type Specifiers</span></span>

<span data-ttu-id="8877a-104">Описатели типов устройств для получения изображений (WIA) — это константы, указывающие тип устройства, подключенного к компьютеру пользователя.</span><span class="sxs-lookup"><span data-stu-id="8877a-104">Windows Image Acquisition (WIA) Device Type Specifiers are constants that indicate the type of device attached to a user's computer.</span></span> <span data-ttu-id="8877a-105">Используйте макрос GET \_ стидевице \_ Type для получения этих значений из свойства типа устройства WIA.</span><span class="sxs-lookup"><span data-stu-id="8877a-105">Use the GET\_STIDEVICE\_TYPE macro to obtain these values from the WIA device type property.</span></span> <span data-ttu-id="8877a-106">Ниже приведены допустимые спецификаторы типа устройства WIA.</span><span class="sxs-lookup"><span data-stu-id="8877a-106">The following are valid WIA Device Type Specifiers:</span></span> 

| <span data-ttu-id="8877a-107">Тип устройства</span><span class="sxs-lookup"><span data-stu-id="8877a-107">Device Type</span></span>                 | <span data-ttu-id="8877a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8877a-108">Meaning</span></span>                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8877a-109">стидевицетипедефаулт</span><span class="sxs-lookup"><span data-stu-id="8877a-109">StiDeviceTypeDefault</span></span>        | <span data-ttu-id="8877a-110">Универсальное устройство WIA.</span><span class="sxs-lookup"><span data-stu-id="8877a-110">Generic WIA device.</span></span> <span data-ttu-id="8877a-111">Во время перечислений устройств Эта константа используется для перечисления всех устройств WIA.</span><span class="sxs-lookup"><span data-stu-id="8877a-111">During device enumerations, this constant is used to enumerate all WIA devices.</span></span>                         |
| <span data-ttu-id="8877a-112">стидевицетипедигиталкамера</span><span class="sxs-lookup"><span data-stu-id="8877a-112">StiDeviceTypeDigitalCamera</span></span>  | <span data-ttu-id="8877a-113">Устройство является камерой.</span><span class="sxs-lookup"><span data-stu-id="8877a-113">The device is a camera.</span></span> <span data-ttu-id="8877a-114">*Этот описатель не поддерживается* Windows Vista *и более поздние версии.*</span><span class="sxs-lookup"><span data-stu-id="8877a-114">*This specifier is not supported by* Windows Vista *and later.*</span></span>                                     |
| <span data-ttu-id="8877a-115">стидевицетипесканнер</span><span class="sxs-lookup"><span data-stu-id="8877a-115">StiDeviceTypeScanner</span></span>        | <span data-ttu-id="8877a-116">Устройство является сканером.</span><span class="sxs-lookup"><span data-stu-id="8877a-116">The device is a scanner.</span></span>                                                                                                    |
| <span data-ttu-id="8877a-117">стидевицетипестреамингвидео</span><span class="sxs-lookup"><span data-stu-id="8877a-117">StiDeviceTypeStreamingVideo</span></span> | <span data-ttu-id="8877a-118">Устройство содержит потоковую передачу видео.</span><span class="sxs-lookup"><span data-stu-id="8877a-118">The device contains streaming video.</span></span> <span data-ttu-id="8877a-119">*Этот описатель не поддерживается* Windows Server 2003 *,* Windows Vista *или более поздней версии.*</span><span class="sxs-lookup"><span data-stu-id="8877a-119">*This specifier is not supported by* Windows Server 2003 *,* Windows Vista, *or later.*</span></span> |



 

 

 



