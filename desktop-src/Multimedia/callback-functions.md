---
title: Функции обратного вызова
description: Функции обратного вызова
ms.assetid: d96e93e5-ebc9-4ad4-aaec-dcc4197a3fc5
keywords:
- устанавливаемые драйверы, функции обратного вызова
- устанавливаемые драйверы, функция Дриверкаллбакк
- устанавливаемые драйверы, события
- Функция Дриверкаллбакк
- Сообщение DRV_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e23f933567d125dd07f81047ea8868c12f41ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890604"
---
# <a name="callback-functions"></a><span data-ttu-id="755dc-108">Функции обратного вызова</span><span class="sxs-lookup"><span data-stu-id="755dc-108">Callback Functions</span></span>

<span data-ttu-id="755dc-109">Устанавливаемые драйверы могут уведомлять приложение, окно или задачу, которые открыли данный экземпляр о событиях с помощью функции [дриверкаллбакк](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback) .</span><span class="sxs-lookup"><span data-stu-id="755dc-109">Installable drivers can notify the application, window, or task that opened the given instance about events by using the [DriverCallback](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback) function.</span></span> <span data-ttu-id="755dc-110">Эта функция предоставляет драйверу средства для возврата сведений в приложение или библиотеку DLL при продолжении обработки запроса.</span><span class="sxs-lookup"><span data-stu-id="755dc-110">This function gives the driver the means to return information to an application or DLL while continuing to process a request.</span></span>

<span data-ttu-id="755dc-111">Если драйвер поддерживает функции обратного вызова, то приложение или библиотека DLL, которые открывают экземпляр, должны предоставить значение, которое является адресом функции обратного вызова, обработчиком окна или обработчиком задачи.</span><span class="sxs-lookup"><span data-stu-id="755dc-111">If a driver supports callback functions, the application or DLL that opens the instance must supply a value this is either the address of a callback function, a window handle, or a task handle.</span></span> <span data-ttu-id="755dc-112">Это значение и флаг, идентифицирующий тип значения, обычно передаются в структуру, на которую указывает второй параметр [**\_ открытого сообщения DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="755dc-112">This value and a flag identifying the type of the value are typically passed in a structure pointed to by the second parameter of the [**DRV\_OPEN**](drv-open.md) message.</span></span>

 

 