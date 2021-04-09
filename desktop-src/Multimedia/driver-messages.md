---
title: Сообщения драйвера
description: Сообщения драйвера
ms.assetid: ed3748ac-08e6-418e-b345-30c796fa38f3
keywords:
- устанавливаемые драйверы, сообщения
- устанавливаемые драйверы, пользовательские сообщения
- сообщения драйвера
- пользовательские сообщения драйверов
- устанавливаемые драйверы, функция Дриверпрок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25e03f9d68254752655be8abe9040a17d44dc0ff
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069868"
---
# <a name="driver-messages"></a><span data-ttu-id="12bce-108">Сообщения драйвера</span><span class="sxs-lookup"><span data-stu-id="12bce-108">Driver Messages</span></span>

<span data-ttu-id="12bce-109">Каждое сообщение драйвера состоит из идентификатора сообщения и 2 32-разрядных параметров.</span><span class="sxs-lookup"><span data-stu-id="12bce-109">Each driver message consists of a message identifier and two 32-bit parameters.</span></span> <span data-ttu-id="12bce-110">Идентификатор сообщения — это уникальное значение, которое проверяется функцией [дриверпрок](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) , чтобы определить, какое действие следует выполнить. Значение параметров сообщения зависит от сообщения.</span><span class="sxs-lookup"><span data-stu-id="12bce-110">The message identifier is a unique value that the [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function checks to determine which action to carry out. The meaning of the message parameters depends on the message.</span></span> <span data-ttu-id="12bce-111">Параметры могут представлять значения или адреса.</span><span class="sxs-lookup"><span data-stu-id="12bce-111">The parameters may represent values or addresses.</span></span> <span data-ttu-id="12bce-112">Во многих случаях параметры не используются и имеют значение 0.</span><span class="sxs-lookup"><span data-stu-id="12bce-112">In many cases, the parameters are not used and are set to zero.</span></span>

<span data-ttu-id="12bce-113">Сообщения драйвера могут быть стандартными или пользовательскими.</span><span class="sxs-lookup"><span data-stu-id="12bce-113">Driver messages can be standard or custom.</span></span> <span data-ttu-id="12bce-114">Windows отправляет стандартные сообщения драйвера, такие как [**DRV \_ Open**](drv-open.md), [**DRV \_ Close**](drv-close.md)и [**DRV \_ Configure**](drv-configure.md), на устанавливаемый драйвер в ответ на запрос на открытие, закрытие или настройку драйвера.</span><span class="sxs-lookup"><span data-stu-id="12bce-114">Windows sends standard driver messages, such as [**DRV\_OPEN**](drv-open.md), [**DRV\_CLOSE**](drv-close.md), and [**DRV\_CONFIGURE**](drv-configure.md), to an installable driver in response to a request to open, close, or configure the driver.</span></span> <span data-ttu-id="12bce-115">Стандартные сообщения направляют устанавливаемый драйвер для загрузки или выгрузки ресурсов, включения или отключения его работы, открытия или закрытия экземпляра драйвера и вывода диалогового окна конфигурации.</span><span class="sxs-lookup"><span data-stu-id="12bce-115">The standard messages direct the installable driver to load or unload its resources, enable or disable its operation, open or close a driver instance, and display a configuration dialog box.</span></span> <span data-ttu-id="12bce-116">Некоторые стандартные сообщения, такие как [**DRV \_ Power**](drv-power.md) и [**DRV \_ екситсессион**](drv-exitsession.md), уведомляют драйвер о системных событиях, влияющих на работу драйвера или любого связанного оборудования.</span><span class="sxs-lookup"><span data-stu-id="12bce-116">Some standard messages, such as [**DRV\_POWER**](drv-power.md) and [**DRV\_EXITSESSION**](drv-exitsession.md), notify the driver of system-wide events that affect the operation of the driver or any related hardware.</span></span>

<span data-ttu-id="12bce-117">Приложения и библиотеки DLL отправляют пользовательские сообщения драйвера для направления устанавливаемого драйвера для выполнения действий, связанных с драйвером.</span><span class="sxs-lookup"><span data-stu-id="12bce-117">Applications and DLLs send custom driver messages to direct an installable driver to carry out driver-specific actions.</span></span> <span data-ttu-id="12bce-118">Устанавливаемые драйверы, поддерживающие пользовательские сообщения, должны содержать соответствующую обработку в функции **дриверпрок** .</span><span class="sxs-lookup"><span data-stu-id="12bce-118">Installable drivers that support custom messages must include appropriate processing in the **DriverProc** function.</span></span> <span data-ttu-id="12bce-119">Чтобы предотвратить конфликт между пользовательскими и стандартными сообщениями драйверов, идентификаторы настраиваемых сообщений должны иметь значения от DRV, \_ зарезервированные для \_ пользователя DRV.</span><span class="sxs-lookup"><span data-stu-id="12bce-119">To prevent conflict between custom and standard driver messages, custom message identifiers must have values ranging from DRV\_RESERVED to DRV\_USER.</span></span> <span data-ttu-id="12bce-120">Пользовательские сообщения, передаваемые в функцию [дефдриверпрок](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) , игнорируются.</span><span class="sxs-lookup"><span data-stu-id="12bce-120">Custom messages passed to the [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) function are ignored.</span></span>

 

 