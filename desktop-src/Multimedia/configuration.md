---
title: Конфигурация (мультимедиа Windows)
description: Сведения о том, как драйвер Windows мультимедиа может позволить пользователям выбирать параметры конфигурации, отображая диалоговое окно "Конфигурация".
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- устанавливаемые драйверы, конфигурация
- устанавливаемые драйверы, DRV_CONFIGURE сообщение
- Сообщение DRV_CONFIGURE
- Сообщение DRV_QUERYCONFIGURE
- Сообщение ДРВКОНФИГИНФО
- Настройка устанавливаемых драйверов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804e4d92d30d666d4d28c253a1a44572a707daa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403927"
---
# <a name="configuration-windows-multimedia"></a><span data-ttu-id="153b3-109">Конфигурация (мультимедиа Windows)</span><span class="sxs-lookup"><span data-stu-id="153b3-109">Configuration (Windows Multimedia)</span></span>

<span data-ttu-id="153b3-110">Устанавливаемый драйвер может позволить пользователям выбирать параметры конфигурации для драйвера и связанного оборудования, отображая диалоговое окно настройки при обработке сообщения конфигурации [**DRV. \_**](drv-configure.md)</span><span class="sxs-lookup"><span data-stu-id="153b3-110">An installable driver can let users choose configuration settings for the driver and associated hardware by displaying a configuration dialog box when processing the [**DRV\_CONFIGURE**](drv-configure.md) message.</span></span> <span data-ttu-id="153b3-111">Драйвер отвечает за создание и управление диалоговым окном, обработку любых вводимых пользователем данных из диалогового окна и изменение конфигурации драйвера или оборудования согласно запросу пользователя.</span><span class="sxs-lookup"><span data-stu-id="153b3-111">The driver is responsible for creating and managing the dialog box, processing any user input from the dialog box, and changing the configuration of the driver or hardware as requested by the user.</span></span> <span data-ttu-id="153b3-112">Драйвер должен предоставить отдельную процедуру диалогового окна для обработки сообщений окна для диалогового окна и шаблон диалогового окна для определения внешнего вида и содержимого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="153b3-112">The driver must provide a separate dialog box procedure to process window messages for the dialog box and a dialog box template to define the appearance and content of the dialog box.</span></span>

<span data-ttu-id="153b3-113">Перед получением \_ сообщения конфигурации DRV драйвер получает сообщение [**DRV \_ куериконфигуре**](drv-queryconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="153b3-113">Before receiving the DRV\_CONFIGURE message, a driver receives the [**DRV\_QUERYCONFIGURE**](drv-queryconfigure.md) message.</span></span> <span data-ttu-id="153b3-114">Драйвер должен возвращать в запрос ненулевое значение, чтобы обеспечить получение последующего \_ сообщения конфигурации DRV.</span><span class="sxs-lookup"><span data-stu-id="153b3-114">The driver must return a nonzero value to the query to ensure receipt of the subsequent DRV\_CONFIGURE message.</span></span>

<span data-ttu-id="153b3-115">При инициализации диалогового окна настройки драйвер обычно извлекает сведения о конфигурации из реестра.</span><span class="sxs-lookup"><span data-stu-id="153b3-115">When initializing the configuration dialog box, the driver typically retrieves configuration information from the registry.</span></span> <span data-ttu-id="153b3-116">Для облегчения размещения этих сведений сообщение о \_ настройке DRV обычно включает адрес структуры [**дрвконфигинфо**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) , содержащей имена раздела реестра и значения, связанные с драйвером.</span><span class="sxs-lookup"><span data-stu-id="153b3-116">To help locate this information, the DRV\_CONFIGURE message usually includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver.</span></span> <span data-ttu-id="153b3-117">Если пользователь запрашивает изменения в конфигурации, драйвер должен обновить сведения о конфигурации в реестре.</span><span class="sxs-lookup"><span data-stu-id="153b3-117">If the user requests changes to the configuration, the driver should update the configuration information in the registry.</span></span>

 

 
