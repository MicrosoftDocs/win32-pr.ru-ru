---
description: 'Приложения могут использовать следующие функции для получения данных устройства с помощью контекста устройства: Жетдевицекапс и Девицекапабилитиес.'
ms.assetid: eed6a323-b7eb-41a2-adb9-592f3f912884
title: Получение данных устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28fa4054170f9b66d73e3494928db312eb8aa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984813"
---
# <a name="retrieving-device-data"></a><span data-ttu-id="7f1e9-103">Получение данных устройства</span><span class="sxs-lookup"><span data-stu-id="7f1e9-103">Retrieving Device Data</span></span>

<span data-ttu-id="7f1e9-104">Приложения могут использовать следующие функции для получения данных устройства с помощью контекста устройства: [**жетдевицекапс**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) и [**девицекапабилитиес**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa).</span><span class="sxs-lookup"><span data-stu-id="7f1e9-104">Applications can use the following functions to retrieve device data using a device context: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) and [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa).</span></span>

<span data-ttu-id="7f1e9-105">[**Жетдевицекапс**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) получает общие данные об устройстве для следующих устройств:</span><span class="sxs-lookup"><span data-stu-id="7f1e9-105">[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) retrieves general device data for the following devices:</span></span>

-   <span data-ttu-id="7f1e9-106">Растровое отображение</span><span class="sxs-lookup"><span data-stu-id="7f1e9-106">Raster displays</span></span>
-   <span data-ttu-id="7f1e9-107">Матричные принтеры</span><span class="sxs-lookup"><span data-stu-id="7f1e9-107">Dot-matrix printers</span></span>
-   <span data-ttu-id="7f1e9-108">Струйные принтеры</span><span class="sxs-lookup"><span data-stu-id="7f1e9-108">Ink-jet printers</span></span>
-   <span data-ttu-id="7f1e9-109">Лазерные принтеры</span><span class="sxs-lookup"><span data-stu-id="7f1e9-109">Laser printers</span></span>
-   <span data-ttu-id="7f1e9-110">Векторные плоттеры</span><span class="sxs-lookup"><span data-stu-id="7f1e9-110">Vector plotters</span></span>
-   <span data-ttu-id="7f1e9-111">Растровые камеры</span><span class="sxs-lookup"><span data-stu-id="7f1e9-111">Raster cameras</span></span>

<span data-ttu-id="7f1e9-112">Эти данные включают в себя поддерживаемые возможности устройства, включая разрешение устройства (для видеоэкранов), цветовой формат (для видеомониторов и цветовых принтеров), число графических объектов, растровые возможности, рисование кривой, Рисование линий, Рисование многоугольников и Рисование текста.</span><span class="sxs-lookup"><span data-stu-id="7f1e9-112">The data includes the supported capabilities of the device, including device resolution (for video displays), color format (for video displays and color printers), number of graphic objects, raster capabilities, curve drawing, line drawing, polygon drawing, and text drawing.</span></span> <span data-ttu-id="7f1e9-113">Приложение получает эти данные, предоставляя маркер, идентифицирующий соответствующий контекст устройства, а также индекс, указывающий тип данных, которые должна получить функция.</span><span class="sxs-lookup"><span data-stu-id="7f1e9-113">An application retrieves this data by supplying a handle identifying the appropriate device context, as well as an index specifying the type of data the function is to retrieve.</span></span>

<span data-ttu-id="7f1e9-114">Функция [**девицекапабилитиес**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) извлекает данные, характерные для принтеров, включая количество доступных лотков бумаги, возможности дуплекса принтера, разрешения, поддерживаемые принтером, максимальный и минимальный поддерживаемый размер бумаги и т. д.</span><span class="sxs-lookup"><span data-stu-id="7f1e9-114">The [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) function retrieves data specific to printers, including the number of available paper bins, the duplex capabilities of the printer, the resolutions supported by the printer, the maximum and minimum supported paper size, and so on.</span></span> <span data-ttu-id="7f1e9-115">Приложение получает эти данные, предоставляя строки, указывающие устройство принтера и порт, а также индекс, указывающий тип данных, извлекаемых функцией.</span><span class="sxs-lookup"><span data-stu-id="7f1e9-115">An application retrieves this data by supplying strings specifying a printer device and port, as well as an index specifying the type of data that the function is to retrieve.</span></span>

 

 
