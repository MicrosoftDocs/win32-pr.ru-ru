---
title: Усовершенствования средства синтаксического анализа
description: Усовершенствования средства синтаксического анализа
ms.assetid: b520aebe-9182-4e60-9111-49af09cdbd79
keywords:
- Усовершенствования средства синтаксического анализа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a22f4b4dced29e25662a6fc521057a055b56f70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411133"
---
# <a name="parser-enhancements"></a><span data-ttu-id="7cc5f-104">Усовершенствования средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="7cc5f-104">Parser Enhancements</span></span>

<span data-ttu-id="7cc5f-105">В Windows Server 2003 с пакетом обновления 1 (SP1) API сервера HTTP позволяет выполнять следующие запросы от HTTP-клиентов.</span><span class="sxs-lookup"><span data-stu-id="7cc5f-105">In Windows Server 2003 with Service Pack 1 (SP1), the HTTP Server API allows the following requests from HTTP clients.</span></span>

-   <span data-ttu-id="7cc5f-106">Запросы, использующие символ перевода строки (LF) в качестве признака конца строки.</span><span class="sxs-lookup"><span data-stu-id="7cc5f-106">Requests that use a single Line Feed (LF) as line terminators.</span></span>
-   <span data-ttu-id="7cc5f-107">Запросы, содержащие линейный пробел (LWS) между строкой запроса HTTP и началом заголовков.</span><span class="sxs-lookup"><span data-stu-id="7cc5f-107">Requests that contain linear white space (LWS) between the HTTP request line and start of headers.</span></span>

<span data-ttu-id="7cc5f-108">Эти поведения включены по умолчанию и не контролируются параметрами реестра.</span><span class="sxs-lookup"><span data-stu-id="7cc5f-108">These behaviors are enabled by default and are not controlled by registry settings.</span></span>

 

 




