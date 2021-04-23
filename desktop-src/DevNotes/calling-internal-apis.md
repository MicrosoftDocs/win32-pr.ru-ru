---
description: Файл заголовка Винтернл. h предоставляет прототипы внутренних интерфейсов API Windows. Нет связанной библиотеки импорта, поэтому разработчики должны использовать динамическую компоновку во время выполнения для вызова функций, описанных в этом файле заголовка.
ms.assetid: 11f09479-e04b-4e5e-bc46-a2d0daf13785
title: Вызов внутренних API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a8ad3533db411d6143d64ca0f4c559334ccaaa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990517"
---
# <a name="calling-internal-apis"></a><span data-ttu-id="c7619-104">Вызов внутренних API</span><span class="sxs-lookup"><span data-stu-id="c7619-104">Calling Internal APIs</span></span>

<span data-ttu-id="c7619-105">Файл заголовка Винтернл. h предоставляет прототипы внутренних интерфейсов API Windows.</span><span class="sxs-lookup"><span data-stu-id="c7619-105">The Winternl.h header file exposes prototypes of internal Windows APIs.</span></span> <span data-ttu-id="c7619-106">Нет связанной библиотеки импорта, поэтому разработчики должны использовать динамическую компоновку во время выполнения для вызова функций, описанных в этом файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="c7619-106">There is no associated import library, so developers must use run-time dynamic linking to call the functions described in this header file.</span></span>

<span data-ttu-id="c7619-107">Функции и структуры в Винтернл. h являются внутренними по отношению к операционной системе и могут изменяться от одного выпуска Windows к другому и, возможно, даже между пакетами обновления для каждого выпуска.</span><span class="sxs-lookup"><span data-stu-id="c7619-107">The functions and structures in Winternl.h are internal to the operating system and subject to change from one release of Windows to the next, and possibly even between service packs for each release.</span></span> <span data-ttu-id="c7619-108">Чтобы обеспечить совместимость приложения, вместо этого следует использовать эквивалентные открытые функции.</span><span class="sxs-lookup"><span data-stu-id="c7619-108">To maintain the compatibility of your application, you should use the equivalent public functions instead.</span></span> <span data-ttu-id="c7619-109">Дополнительные сведения можно найти в файле заголовка Винтернл. h, а также в документации по каждой функции.</span><span class="sxs-lookup"><span data-stu-id="c7619-109">Further information is available in the header file, Winternl.h, and the documentation for each function.</span></span>

<span data-ttu-id="c7619-110">Если вы используете эти функции, вы можете обращаться к ним через динамическую компоновку во время выполнения с помощью [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="c7619-110">If you do use these functions, you can access them through run-time dynamic linking using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="c7619-111">Это дает коду возможность корректно реагировать, если функция была изменена или удалена из операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c7619-111">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="c7619-112">Однако изменения сигнатуры могут быть недоступны для обнаружения.</span><span class="sxs-lookup"><span data-stu-id="c7619-112">Signature changes, however, may not be detectable.</span></span>

 

 
