---
title: Формат устанавливаемого драйвера
description: Формат устанавливаемого драйвера
ms.assetid: 4573567e-237d-47f9-9510-31d01326205f
keywords:
- устанавливаемые драйверы, форматы
- устанавливаемые драйверы, функция Дриверпрок
- устанавливаемые драйверы, сообщения
- сообщения драйвера
- форматы драйверов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fbbdcb8a49184dee6e9cf13c9f434506b1b48f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337236"
---
# <a name="installable-driver-format"></a><span data-ttu-id="1670a-108">Формат устанавливаемого драйвера</span><span class="sxs-lookup"><span data-stu-id="1670a-108">Installable Driver Format</span></span>

<span data-ttu-id="1670a-109">Каждый устанавливаемый драйвер экспортирует функцию [дриверпрок](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) .</span><span class="sxs-lookup"><span data-stu-id="1670a-109">Every installable driver exports a [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function.</span></span> <span data-ttu-id="1670a-110">Эта общая функция точки входа получает от системы *сообщения драйвера* , которые направляют драйвер для выполнения действий или предоставления информации.</span><span class="sxs-lookup"><span data-stu-id="1670a-110">This common entry-point function receives *driver messages* from the system that direct the driver to carry out actions or provide information.</span></span> <span data-ttu-id="1670a-111">Система отправляет сообщения драйвера в функцию **дриверпрок** , когда приложение или библиотека DLL открывает или закрывает драйвер или запрашивает отправку сообщения драйверу.</span><span class="sxs-lookup"><span data-stu-id="1670a-111">The system sends driver messages to the **DriverProc** function when an application or DLL opens or closes the driver or requests that a message be sent to the driver.</span></span> <span data-ttu-id="1670a-112">Функция **дриверпрок** обрабатывает сообщение или передает сообщение в обработчик сообщений по умолчанию, функцию [дефдриверпрок](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) .</span><span class="sxs-lookup"><span data-stu-id="1670a-112">The **DriverProc** function either processes the message or passes the message to the default message handler, the [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) function.</span></span> <span data-ttu-id="1670a-113">В любом случае **дриверпрок** должен возвращать значение, указывающее, было ли запрошенное действие успешным.</span><span class="sxs-lookup"><span data-stu-id="1670a-113">In either case, **DriverProc** must return a value indicating whether the requested action was successful.</span></span>

 

 