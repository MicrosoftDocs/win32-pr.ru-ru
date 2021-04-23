---
title: Архитектура ВКМ
description: Архитектура ВКМ
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- Видео для Windows (VFW), архитектура ВКМ
- VFW (видео для Windows), архитектура ВКМ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b672c86053086f63127aae586517fac4906326
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331056"
---
# <a name="vcm-architecture"></a><span data-ttu-id="9e44c-105">Архитектура ВКМ</span><span class="sxs-lookup"><span data-stu-id="9e44c-105">VCM Architecture</span></span>

<span data-ttu-id="9e44c-106">ВКМ является посредником между приложением и сжатием и распаковкой драйверов.</span><span class="sxs-lookup"><span data-stu-id="9e44c-106">VCM is an intermediary between an application and compression and decompression drivers.</span></span> <span data-ttu-id="9e44c-107">Драйверы сжатия и распаковки сжимают и рассжимают отдельные кадры данных.</span><span class="sxs-lookup"><span data-stu-id="9e44c-107">The compression and decompression drivers compress and decompress individual frames of data.</span></span>

<span data-ttu-id="9e44c-108">Когда приложение выполняет вызов ВКМ, ВКМ преобразует вызов в сообщение.</span><span class="sxs-lookup"><span data-stu-id="9e44c-108">When an application makes a call to VCM, VCM translates the call into a message.</span></span> <span data-ttu-id="9e44c-109">Сообщение отправляется с помощью функции [**иксендмессаже**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) в соответствующий компрессор или декомпрессор, который сжимает или Распаковывает данные.</span><span class="sxs-lookup"><span data-stu-id="9e44c-109">The message is sent by using the [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) function to the appropriate compressor or decompressor, which compresses or decompresses the data.</span></span> <span data-ttu-id="9e44c-110">ВКМ получает возвращаемое значение из драйвера сжатия или распаковки, а затем возвращает управление приложению.</span><span class="sxs-lookup"><span data-stu-id="9e44c-110">VCM receives the return value from the compression or decompression driver and then returns control to the application.</span></span>

<span data-ttu-id="9e44c-111">Если макрос определен для сообщения, макрос разворачивается в вызове функции **иксендмессаже** , предоставляющей соответствующие параметры для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e44c-111">If a macro is defined for a message, the macro expands to an **ICSendMessage** function call supplying appropriate parameters for that message.</span></span> <span data-ttu-id="9e44c-112">Если макрос определен для сообщения, приложение должно использовать его, а не сообщение.</span><span class="sxs-lookup"><span data-stu-id="9e44c-112">If a macro is defined for a message, your application should use it rather than the message.</span></span> <span data-ttu-id="9e44c-113">В этом обзоре эти макросы следуют сообщениям в круглых скобках.</span><span class="sxs-lookup"><span data-stu-id="9e44c-113">In this overview, these macros follow messages in parentheses.</span></span>

 

 




