---
title: Обработка ошибок серверного приложения
description: Если серверное приложение успешно обрабатывает переданный файл, приложение должно вернуть 200.
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6019f296cb3b960369efc2c3ca8f25eb7738e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773391"
---
# <a name="handling-server-application-errors"></a><span data-ttu-id="5370d-103">Обработка ошибок серверного приложения</span><span class="sxs-lookup"><span data-stu-id="5370d-103">Handling Server Application Errors</span></span>

<span data-ttu-id="5370d-104">Если серверное приложение успешно обрабатывает переданный файл, приложение должно вернуть 200.</span><span class="sxs-lookup"><span data-stu-id="5370d-104">If the server application successfully processes the uploaded file, the application should return 200.</span></span> <span data-ttu-id="5370d-105">Если приложение не возвращает 200, клиент BITS использует код ошибки, чтобы определить, является ли ошибка временной или неустранимой ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5370d-105">If the application does not return 200, the BITS client uses the error code to determine if the error is a transient error or fatal error.</span></span>

<span data-ttu-id="5370d-106">Все коды ошибок 3xx являются временными ошибками, за исключением 300-305 и 307, которые являются неустранимыми ошибками.</span><span class="sxs-lookup"><span data-stu-id="5370d-106">All 3xx error codes are transient errors except 300 - 305 and 307, which are fatal errors.</span></span> <span data-ttu-id="5370d-107">Все коды ошибок 4xx являются неустранимыми ошибками, за исключением 408 и 409, которые являются временными ошибками.</span><span class="sxs-lookup"><span data-stu-id="5370d-107">All 4xx error codes are fatal errors except for 408 and 409, which are transient errors.</span></span> <span data-ttu-id="5370d-108">Все коды ошибок 5xx являются временными ошибками, за исключением 501 и 505, которые являются неустранимыми ошибками.</span><span class="sxs-lookup"><span data-stu-id="5370d-108">All 5xx error codes are transient errors except 501 and 505, which are fatal errors.</span></span> <span data-ttu-id="5370d-109">Все остальные коды HTTP считаются временными ошибками.</span><span class="sxs-lookup"><span data-stu-id="5370d-109">All other HTTP codes are considered transient errors.</span></span> <span data-ttu-id="5370d-110">Обратите внимание, что код ошибки 403 — это единственный код ошибки, который не позволяет BITS отправлять файл отправки в серверное приложение.</span><span class="sxs-lookup"><span data-stu-id="5370d-110">Note that a 403 error code is the only error code that prevents BITS from posting the upload file to the server application again.</span></span>

<span data-ttu-id="5370d-111">Чтобы получить ошибку, вызовите метод [**ибаккграундкоперрор:: OnError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) .</span><span class="sxs-lookup"><span data-stu-id="5370d-111">To retrieve the error, call the [**IBackgroundCopyError::GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) method.</span></span> <span data-ttu-id="5370d-112">Контекст ошибки будет \_ \_ удаленным приложением с контекстом ошибки BG \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5370d-112">The error context will be BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION.</span></span>

 

 




