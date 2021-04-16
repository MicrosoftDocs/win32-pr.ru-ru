---
description: Интерфейс управления «подсветкой» — это стандартизированный интерфейс IOCTL для управления яркостью ЖК-подсветки.
ms.assetid: edf2b7ed-2676-483a-80ba-f148951e0e58
title: Интерфейс управления подсветкой
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecbcc3d635d120c1049f8ec586d7296a953dfac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663137"
---
# <a name="backlight-control-interface"></a><span data-ttu-id="59f3e-103">Интерфейс управления подсветкой</span><span class="sxs-lookup"><span data-stu-id="59f3e-103">Backlight Control Interface</span></span>

<span data-ttu-id="59f3e-104">Интерфейс управления «подсветкой» — это стандартизированный интерфейс IOCTL для управления яркостью ЖК-подсветки.</span><span class="sxs-lookup"><span data-stu-id="59f3e-104">The backlight control interface is a standardized IOCTL interface for controlling the brightness of the LCD backlight.</span></span>

<span data-ttu-id="59f3e-105">Приложения, которым требуется программное управление яркостью подсветки или предоставлением пользователям элементов управления, следует использовать этот интерфейс, а не собственный интерфейс. в противном случае система не сможет запросить текущую аппаратную яркость и может стать несинхронизированной.</span><span class="sxs-lookup"><span data-stu-id="59f3e-105">Applications that require programmatic control of the backlight brightness or provide controls for the user to do so should use this interface rather than a proprietary interface; otherwise, the system cannot query the current hardware brightness and may become unsynchronized.</span></span>

<span data-ttu-id="59f3e-106">Первым шагом является запрос устройства для поддержки яркости с помощью [**\_ \_ Видеозапроса ioctl \_ поддерживаемого \_**](ioctl-video-query-supported-brightness.md) управляющего кода.</span><span class="sxs-lookup"><span data-stu-id="59f3e-106">The first step is to query the device for the supported brightness using the [**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**](ioctl-video-query-supported-brightness.md) control code.</span></span> <span data-ttu-id="59f3e-107">Эта операция возвращает буфер, указывающий доступные уровни яркости.</span><span class="sxs-lookup"><span data-stu-id="59f3e-107">This operation returns a buffer that specifies the available brightness levels.</span></span> <span data-ttu-id="59f3e-108">Затем можно запросить устройство для использования текущей яркости экрана с помощью управляющего кода, определяющего [**\_ \_ \_ \_ яркость экрана запроса видео ioctl**](ioctl-video-query-display-brightness.md) .</span><span class="sxs-lookup"><span data-stu-id="59f3e-108">Next, you can query the device for the current display brightness using the [**IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS**](ioctl-video-query-display-brightness.md) control code.</span></span> <span data-ttu-id="59f3e-109">Эта операция возвращает текущие параметры для чередования текущей (AC) яркости, прямого тока (DC) и состояния электропитания.</span><span class="sxs-lookup"><span data-stu-id="59f3e-109">This operation returns the current settings for alternating current (AC) brightness, direct current (DC) brightness, and the power state.</span></span>

<span data-ttu-id="59f3e-110">Чтобы изменить яркость экрана, используйте управляющий код для [**\_ \_ настройки \_ \_ яркости экрана**](ioctl-video-set-display-brightness.md) с помощью ioctl.</span><span class="sxs-lookup"><span data-stu-id="59f3e-110">To change the display brightness, use the [**IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS**](ioctl-video-set-display-brightness.md) control code.</span></span> <span data-ttu-id="59f3e-111">Можно задать яркость AC, яркость контроллера домена или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="59f3e-111">You can set the AC brightness, the DC brightness, or both.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59f3e-112">См. также</span><span class="sxs-lookup"><span data-stu-id="59f3e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59f3e-113">Сведения об управлении питанием</span><span class="sxs-lookup"><span data-stu-id="59f3e-113">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



