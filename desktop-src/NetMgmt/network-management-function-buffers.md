---
title: Буферы функций управления сетью
description: Библиотека времени выполнения RPC обрабатывает буферы, необходимые для функций управления сетью получения данных 32-bit, следующим образом.
ms.assetid: f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385382d12aa5b5c8c7c93b9a833f684d913c5783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258557"
---
# <a name="network-management-function-buffers"></a><span data-ttu-id="f4aa6-103">Буферы функций управления сетью</span><span class="sxs-lookup"><span data-stu-id="f4aa6-103">Network Management Function Buffers</span></span>

<span data-ttu-id="f4aa6-104">Библиотека времени выполнения RPC обрабатывает буферы, необходимые для функций управления сетью получения данных 32-bit, следующим образом.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-104">The RPC run-time library handles the buffers required by the 32-bit data retrieval network management functions as follows:</span></span>

-   <span data-ttu-id="f4aa6-105">**Отправка данных на сервер** (данные, указанные \[ в \] параметре in).</span><span class="sxs-lookup"><span data-stu-id="f4aa6-105">**Sending data to the server** (data specified by \[in\] parameters).</span></span>

    <span data-ttu-id="f4aa6-106">Вызывающий объект должен выделить буфер и освободить его для соответствующей структуры информации (или структур) и передать в функцию переменную указателя.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-106">The caller must allocate and deallocate the buffer for the relevant information structure (or structures) and pass a pointer variable to the function.</span></span> <span data-ttu-id="f4aa6-107">Вызывающему объекту не нужно указывать длину буфера.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-107">The caller does not need to specify the buffer length.</span></span>

    <span data-ttu-id="f4aa6-108">Пример: [ **нетграупадд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)</span><span class="sxs-lookup"><span data-stu-id="f4aa6-108">Example: [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)</span></span>

-   <span data-ttu-id="f4aa6-109">**Получение данных с сервера** (данные, указанные в \[ \] параметрах out).</span><span class="sxs-lookup"><span data-stu-id="f4aa6-109">**Retrieving data from the server** (data specified by \[out\] parameters).</span></span>

    <span data-ttu-id="f4aa6-110">Система выделяет буфер для возвращаемых сведений.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-110">The system allocates the buffer for the returned information.</span></span> <span data-ttu-id="f4aa6-111">Вызывающая сторона должна передать переменную указателя в функцию на входе.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-111">The caller must pass a pointer variable to the function on input.</span></span> <span data-ttu-id="f4aa6-112">При успешном возвращении указатель получает адрес выделенного системой буфера, который содержит возвращенные сведения.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-112">On successful return, the pointer receives the address of the system-allocated buffer that contains the returned information.</span></span> <span data-ttu-id="f4aa6-113">Это упрощает вызывающий код, поскольку вызывающему объекту не нужно оценивать размер буфера или изменять размер буфера и повторно выдавать функцию.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-113">This simplifies the calling code, because the caller does not need to estimate the size of the buffer, or resize the buffer and reissue the function.</span></span>

    <span data-ttu-id="f4aa6-114">Когда вызывающий объект завершил обработку возвращенных данных, он должен освободить память, выделенную системой, вызвав функцию [**нетапибуфферфри**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) .</span><span class="sxs-lookup"><span data-stu-id="f4aa6-114">When the caller has finished processing the returned information, it must free the system-allocated memory by calling the [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) function.</span></span> <span data-ttu-id="f4aa6-115">Дополнительные сведения об указании размеров буфера см. в разделе [Длина буфера функции управления сетью](network-management-function-buffer-lengths.md).</span><span class="sxs-lookup"><span data-stu-id="f4aa6-115">For more information about specifying buffer sizes, see [Network Management Function Buffer Lengths](network-management-function-buffer-lengths.md).</span></span>

    <span data-ttu-id="f4aa6-116">Пример: [ **нетграупенум**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)</span><span class="sxs-lookup"><span data-stu-id="f4aa6-116">Example: [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)</span></span>

 

 




