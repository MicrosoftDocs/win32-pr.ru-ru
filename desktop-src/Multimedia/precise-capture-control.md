---
title: Точный контроль захвата
description: Точный контроль захвата
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- Функции обратного вызова Авикап, точный контроль записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0749d420d7a1999d074546a0cf577fdaceb72483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532084"
---
# <a name="precise-capture-control"></a><span data-ttu-id="8c995-104">Точный контроль захвата</span><span class="sxs-lookup"><span data-stu-id="8c995-104">Precise Capture Control</span></span>

<span data-ttu-id="8c995-105">Окно записи может предоставлять функцию обратного вызова с контролем захвата, точно контролируя время начала и окончания сбора потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="8c995-105">A capture window can provide the capture-control callback function with precise control over the moments that streaming capture begin and end.</span></span> <span data-ttu-id="8c995-106">Первое сообщение, отправленное из драйвера записи в процедуру обратного вызова, задает для параметра *nсведения* значение контролкаллбакк First \_ после выделения всех буферов и завершения всех остальных подготовительных процедур записи.</span><span class="sxs-lookup"><span data-stu-id="8c995-106">The first message sent from the capture driver to the callback procedure sets the *nState* parameter to CONTROLCALLBACK\_PREROLL after allocating all buffers and all other capture preparations are complete.</span></span> <span data-ttu-id="8c995-107">Это сообщение дает приложению возможность выполнить предпрезентацию источников видео.</span><span class="sxs-lookup"><span data-stu-id="8c995-107">This message gives the application the ability to preroll the video sources.</span></span> <span data-ttu-id="8c995-108">(Функция обратного вызова указывает *nсведения* в качестве второго параметра.) Затем функция обратного вызова возвращается в момент, когда начинается запись.</span><span class="sxs-lookup"><span data-stu-id="8c995-108">(The callback function specifies *nState* as its second parameter.) The callback function then returns at the exact moment recording is to begin.</span></span> <span data-ttu-id="8c995-109">Возвращаемое значение **true** из функции обратного вызова продолжит запись.</span><span class="sxs-lookup"><span data-stu-id="8c995-109">A return value of **TRUE** from the callback function continues capture.</span></span> <span data-ttu-id="8c995-110">Возвращаемое значение **false** прерывает захват.</span><span class="sxs-lookup"><span data-stu-id="8c995-110">A return value of **FALSE** aborts capture.</span></span> <span data-ttu-id="8c995-111">После начала записи функция обратного вызова вызывается часто с параметром *nсведения* , равным контролкаллбакк \_ Capture, чтобы разрешить приложению завершать захват, возвращая **значение false**.</span><span class="sxs-lookup"><span data-stu-id="8c995-111">Once capture begins, the callback function is called frequently with *nState* set to CONTROLCALLBACK\_CAPTURING to allow the application to end capture by returning **FALSE**.</span></span>

 

 




