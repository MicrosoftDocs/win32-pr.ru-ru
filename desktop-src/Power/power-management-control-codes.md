---
description: С батареями используются следующие управляющие коды.
ms.assetid: 027fffdb-62a1-47d8-b69f-c2fcf7f9ac97
title: Управляющие коды управления питанием
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef980bdcd3aa4c1ace9ee0b0cd92265d3dd9dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663107"
---
# <a name="power-management-control-codes"></a><span data-ttu-id="cc975-103">Управляющие коды управления питанием</span><span class="sxs-lookup"><span data-stu-id="cc975-103">Power Management Control Codes</span></span>

<span data-ttu-id="cc975-104">С [батареями](battery-information.md)используются следующие управляющие коды.</span><span class="sxs-lookup"><span data-stu-id="cc975-104">The following control codes are used with [batteries](battery-information.md).</span></span>



| <span data-ttu-id="cc975-105">Контрольный код</span><span class="sxs-lookup"><span data-stu-id="cc975-105">Control Code</span></span>                                                                  | <span data-ttu-id="cc975-106">Описание</span><span class="sxs-lookup"><span data-stu-id="cc975-106">Description</span></span>                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="cc975-107">**\_ \_ сведения о запросе от аккумулятора ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="cc975-107">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md) | <span data-ttu-id="cc975-108">Получает разнообразные сведения о батарее</span><span class="sxs-lookup"><span data-stu-id="cc975-108">Retrieves a variety of information for the battery</span></span> |
| [<span data-ttu-id="cc975-109">**\_ \_ состояние запроса аккумулятора \_ ioctl**</span><span class="sxs-lookup"><span data-stu-id="cc975-109">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)           | <span data-ttu-id="cc975-110">Извлекает текущее состояние аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="cc975-110">Retrieves the current status for the battery.</span></span>      |
| [<span data-ttu-id="cc975-111">**\_тег запроса на батарею ioctl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cc975-111">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)                 | <span data-ttu-id="cc975-112">Извлекает текущий тег батареи.</span><span class="sxs-lookup"><span data-stu-id="cc975-112">Retrieves the battery's current tag.</span></span>               |
| [<span data-ttu-id="cc975-113">**\_ \_ сведения о настройке аккумулятора ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="cc975-113">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)     | <span data-ttu-id="cc975-114">Задает различные сведения о батарее.</span><span class="sxs-lookup"><span data-stu-id="cc975-114">Sets various battery information.</span></span>                  |



 

<span data-ttu-id="cc975-115">Следующие управляющие коды являются частью [интерфейса элемента управления "подсветка](backlight-control-interface.md)".</span><span class="sxs-lookup"><span data-stu-id="cc975-115">The following control codes are part of the [backlight control interface](backlight-control-interface.md).</span></span>



| <span data-ttu-id="cc975-116">Контрольный код</span><span class="sxs-lookup"><span data-stu-id="cc975-116">Control Code</span></span>                                                                                 | <span data-ttu-id="cc975-117">Описание</span><span class="sxs-lookup"><span data-stu-id="cc975-117">Description</span></span>                                                                   |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="cc975-118">**\_ \_ \_ яркость экрана запроса видео \_ ioctl**</span><span class="sxs-lookup"><span data-stu-id="cc975-118">**IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS**</span></span>](ioctl-video-query-display-brightness.md)     | <span data-ttu-id="cc975-119">Извлекает текущие уровни подсветки AC и DC и текущее состояние электропитания.</span><span class="sxs-lookup"><span data-stu-id="cc975-119">Retrieves the current AC and DC backlight levels and the current power state.</span></span> |
| [<span data-ttu-id="cc975-120">**видеозапрос IOCTL — \_ \_ \_ поддерживаемая \_ яркость**</span><span class="sxs-lookup"><span data-stu-id="cc975-120">**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**</span></span>](ioctl-video-query-supported-brightness.md) | <span data-ttu-id="cc975-121">Извлекает Поддерживаемые уровни подсветки.</span><span class="sxs-lookup"><span data-stu-id="cc975-121">Retrieves the supported backlight levels.</span></span>                                     |
| [<span data-ttu-id="cc975-122">**\_ \_ Настройка \_ яркости экрана для видео ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="cc975-122">**IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS**</span></span>](ioctl-video-set-display-brightness.md)         | <span data-ttu-id="cc975-123">Задает текущие уровни подсветки AC и DC</span><span class="sxs-lookup"><span data-stu-id="cc975-123">Sets the current AC and DC backlight levels</span></span>                                   |



 

 

 



