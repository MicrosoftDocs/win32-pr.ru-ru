---
title: Требования к протоколу HTTP для загрузки BITS
description: Служба BITS поддерживает загрузку и загрузку по протоколу HTTP и HTTPS, а также требует, чтобы сервер поддерживал протокол HTTP/1.1.
ms.assetid: 35af422b-62e4-41fd-8890-579ccf016c83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d130ab3e527b62f34f48e6df4695bf75f63dcd2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486645"
---
# <a name="http-requirements-for-bits-downloads"></a><span data-ttu-id="c44fa-103">Требования к протоколу HTTP для загрузки BITS</span><span class="sxs-lookup"><span data-stu-id="c44fa-103">HTTP Requirements for BITS Downloads</span></span>

<span data-ttu-id="c44fa-104">Служба BITS поддерживает загрузку и загрузку по протоколу HTTP и HTTPS, а также требует, чтобы сервер поддерживал протокол HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="c44fa-104">BITS supports HTTP and HTTPS downloads and uploads and requires that the server supports the HTTP/1.1 protocol.</span></span> <span data-ttu-id="c44fa-105">Для загрузки метод **head** HTTP-сервера должен возвращать размер файла, а его метод **Get** должен поддерживать заголовки Content-Range и Content-Length.</span><span class="sxs-lookup"><span data-stu-id="c44fa-105">For downloads, the HTTP server's **Head** method must return the file size and its **Get** method must support the Content-Range and Content-Length headers.</span></span> <span data-ttu-id="c44fa-106">В результате BITS передает только статическое содержимое файла и выдает ошибку при попытке передачи динамического содержимого, если только скрипты ASP, ISAPI или CGI не поддерживают заголовки Content-Range и Content-Length.</span><span class="sxs-lookup"><span data-stu-id="c44fa-106">As a result, BITS only transfers static file content and generates an error if you try to transfer dynamic content, unless the ASP, ISAPI, or CGI script supports the Content-Range and Content-Length headers.</span></span>

<span data-ttu-id="c44fa-107">BITS может использовать сервер HTTP/1.0, если он соответствует требованиям к методам **head** и **Get** .</span><span class="sxs-lookup"><span data-stu-id="c44fa-107">BITS can use an HTTP/1.0 server as long as it meets the **Head** and **Get** method requirements.</span></span>

<span data-ttu-id="c44fa-108">Для поддержки загрузки диапазонов файла сервер должен поддерживать следующие требования:</span><span class="sxs-lookup"><span data-stu-id="c44fa-108">To support downloading ranges of a file, the server must support the following requirements:</span></span>

-   <span data-ttu-id="c44fa-109">Разрешает заголовкам MIME включать заголовки стандартного содержимого и типа содержимого, а также не более 180 байт других заголовков.</span><span class="sxs-lookup"><span data-stu-id="c44fa-109">Allow MIME headers to include the standard Content-Range and Content-Type headers, plus a maximum of 180 bytes of other headers.</span></span>
-   <span data-ttu-id="c44fa-110">Разрешить не более двух символов CR/LFs между заголовками HTTP и первой строкой границы.</span><span class="sxs-lookup"><span data-stu-id="c44fa-110">Allow a maximum of two CR/LFs between the HTTP headers and the first boundary string.</span></span>

 

 




