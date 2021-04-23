---
title: Функции и сообщения, устанавливаемые драйвером
description: Функции и сообщения, устанавливаемые драйвером
ms.assetid: f487705a-ae8e-4ea8-bfd5-9b0f6087ddbb
keywords:
- устанавливаемые драйверы, функции
- устанавливаемые драйверы, сообщения
- устанавливаемые драйверы, функция Опендривер
- Функция Опендривер
- устанавливаемые драйверы, пользовательские сообщения
- сообщения драйвера
- пользовательские сообщения драйверов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66e6ebaac73bf8eb779119750cb390481152c3f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987470"
---
# <a name="installable-driver-functions-and-messages"></a><span data-ttu-id="82b54-110">Функции и сообщения, устанавливаемые драйвером</span><span class="sxs-lookup"><span data-stu-id="82b54-110">Installable Driver Functions and Messages</span></span>

<span data-ttu-id="82b54-111">Можно открыть устанавливаемый драйвер из приложения с помощью функции [**опендривер**](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) .</span><span class="sxs-lookup"><span data-stu-id="82b54-111">You can open an installable driver from an application by using the [**OpenDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) function.</span></span> <span data-ttu-id="82b54-112">Эта функция создает экземпляр драйвера, загружает драйвер в память, если другой экземпляр не существует, и возвращает маркер нового экземпляра.</span><span class="sxs-lookup"><span data-stu-id="82b54-112">This function creates an instance of the driver, loading the driver into memory if no other instance exists, and returns the handle of the new instance.</span></span> <span data-ttu-id="82b54-113">При открытии устанавливаемого драйвера необходимо указать либо полный путь к драйверу, либо имена раздела реестра и значения, связанные с драйвером.</span><span class="sxs-lookup"><span data-stu-id="82b54-113">When opening an installable driver, you must supply either the full path of the driver or the names of the registry key and value associated with the driver.</span></span>

<span data-ttu-id="82b54-114">После открытия драйвера можно направить его для выполнения задач с помощью функции [**сенддривермессаже**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) , которая отправляет драйверу сообщения драйвера.</span><span class="sxs-lookup"><span data-stu-id="82b54-114">Once a driver is open, you can direct it to carry out tasks by using the [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) function to send driver messages to the driver.</span></span> <span data-ttu-id="82b54-115">Например, можно настроить драйвер для показа диалогового окна конфигурации, отправив сообщение [**\_ Настройка DRV**](drv-configure.md) .</span><span class="sxs-lookup"><span data-stu-id="82b54-115">For example, you can direct the driver to display its configuration dialog box by sending the [**DRV\_CONFIGURE**](drv-configure.md) message.</span></span> <span data-ttu-id="82b54-116">Перед отправкой этого сообщения необходимо определить, есть ли у драйвера диалоговое окно конфигурации, отправив сообщение [**DRV \_ куериконфигуре**](drv-queryconfigure.md) и проверив наличие ненулевого возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="82b54-116">Before sending this message, you must determine whether the driver has a configuration dialog box by sending the [**DRV\_QUERYCONFIGURE**](drv-queryconfigure.md) message and checking for a nonzero return value.</span></span> <span data-ttu-id="82b54-117">Многие драйверы предоставляют набор настраиваемых сообщений, которые можно отправить для направления операций драйвера.</span><span class="sxs-lookup"><span data-stu-id="82b54-117">Many drivers provide a set of custom messages that you can send to direct the operations of the driver.</span></span>

<span data-ttu-id="82b54-118">Если вам нужен специальный доступ к устанавливаемому драйверу, например к его ресурсам, можно получить обработчик модуля драйвера с помощью функции [**жетдривермодулехандле**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) .</span><span class="sxs-lookup"><span data-stu-id="82b54-118">If you need special access to an installable driver, such as access to its resources, you can retrieve the module handle of the driver by using the [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) function.</span></span>

<span data-ttu-id="82b54-119">Если устанавливаемый драйвер больше не нужен, его можно закрыть с помощью функции [**клоседривер**](/windows/win32/api/mmiscapi/nf-mmiscapi-closedriver) .</span><span class="sxs-lookup"><span data-stu-id="82b54-119">When you no longer need the installable driver, you can close it by using the [**CloseDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-closedriver) function.</span></span>

<span data-ttu-id="82b54-120">Можно использовать функции и сообщения устанавливаемого драйвера, чтобы открыть любой устанавливаемый драйвер и управлять им.</span><span class="sxs-lookup"><span data-stu-id="82b54-120">You can use the installable driver functions and messages to open and manage any installable driver.</span></span> <span data-ttu-id="82b54-121">Однако для открытия и управления устройствами мультимедиа рекомендуется сначала использовать стандартные службы (например, [**вавеаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen), [**вавеаутмессаже**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)и [**вавеаутклосе**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) для устройств вывода аудио), если они существуют.</span><span class="sxs-lookup"><span data-stu-id="82b54-121">However, the recommended course of action for opening and managing multimedia devices is to first use standard services (such as [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen), [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage), and [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) for waveform output devices), if they exist.</span></span> <span data-ttu-id="82b54-122">Если стандартные службы не существуют для драйвера мультимедиа, откройте драйвер и управляйте им с помощью функций и сообщений, устанавливаемых драйвером.</span><span class="sxs-lookup"><span data-stu-id="82b54-122">If standard services do not exist for a multimedia driver, then open and manage the driver using the installable driver functions and messages.</span></span>

> [!Note]  
> <span data-ttu-id="82b54-123">Функции [**сенддривермессаже**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) и [**жетдривермодулехандле**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) являются предпочтительными функциями, которые используются для отправки сообщений драйверу и для получения маркера к экземпляру модуля.</span><span class="sxs-lookup"><span data-stu-id="82b54-123">The [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) and [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) functions are the preferred functions to use to send messages to a driver and to obtain a handle to a module instance.</span></span> <span data-ttu-id="82b54-124">Однако для обеспечения совместимости с предыдущими версиями операционной системы Windows включена старая функция [**дрвжетмодулехандле**](/windows/win32/api/mmiscapi/nf-mmiscapi-drvgetmodulehandle) .</span><span class="sxs-lookup"><span data-stu-id="82b54-124">The older [**DrvGetModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-drvgetmodulehandle) function, however, has been included to maintain compatibility with previous versions of the Windows operating system.</span></span>

 

 

 