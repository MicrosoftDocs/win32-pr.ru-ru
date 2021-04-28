---
description: API сжатия
ms.assetid: 3ef35cd0-3742-4fc2-9c06-e0485d3538f2
title: API сжатия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e088b37bbe2ba652379a2d90e6e1e21f87a2e68
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087992"
---
# <a name="compression-api"></a><span data-ttu-id="ad069-103">API сжатия</span><span class="sxs-lookup"><span data-stu-id="ad069-103">Compression API</span></span>

## <a name="purpose"></a><span data-ttu-id="ad069-104">Цель</span><span class="sxs-lookup"><span data-stu-id="ad069-104">Purpose</span></span>

<span data-ttu-id="ad069-105">API сжатия предоставляет алгоритмы сжатия Windows MSZIP, XPRESS, XPRESS \_ Хаффа и лзмс.</span><span class="sxs-lookup"><span data-stu-id="ad069-105">The Compression API exposes the Windows MSZIP, XPRESS, XPRESS\_HUFF, and LZMS compression algorithms.</span></span> <span data-ttu-id="ad069-106">Это позволяет разработчикам приложений Windows управлять версиями, службами и расширять предоставляемые алгоритмы сжатия.</span><span class="sxs-lookup"><span data-stu-id="ad069-106">This enables developers of Windows applications to manage versions, service, and extend the exposed compression algorithms.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="ad069-107">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="ad069-107">Developer audience</span></span>

<span data-ttu-id="ad069-108">API сжатия предназначен для использования профессиональными разработчиками C/C++ приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="ad069-108">The Compression API is designed for use by professional C/C++ developers of Windows applications.</span></span> <span data-ttu-id="ad069-109">API сжатия предоставляет алгоритмы сжатия без потерь, используемые Windows при использовании общедоступного интерфейса и API пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="ad069-109">The Compression API exposes the lossless compression algorithms used by Windows though a public interface and user-mode API.</span></span> <span data-ttu-id="ad069-110">API сжатия — это рекомендуемый способ управления алгоритмами сжатия для разработчиков Windows.</span><span class="sxs-lookup"><span data-stu-id="ad069-110">The Compression API is the recommended method for Windows developers to control the compression algorithms.</span></span> <span data-ttu-id="ad069-111">Эта функция 64-бит на 64-разрядной версии Windows и 32-bit в 32-bit Windows.</span><span class="sxs-lookup"><span data-stu-id="ad069-111">This feature is 64-bit on 64-bit Windows and 32-bit on 32-bit Windows.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ad069-112">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="ad069-112">Run-time requirements</span></span>

<span data-ttu-id="ad069-113">API сжатия доступен, начиная с Windows 8 или Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ad069-113">The Compression API is available beginning with the Windows 8 or Windows Server 2012.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ad069-114">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="ad069-114">In this section</span></span>

-   [<span data-ttu-id="ad069-115">Использование API сжатия</span><span class="sxs-lookup"><span data-stu-id="ad069-115">Using the Compression API</span></span>](using-the-compression-api.md)
-   [<span data-ttu-id="ad069-116">Функции API сжатия</span><span class="sxs-lookup"><span data-stu-id="ad069-116">Compression API Functions</span></span>](compression-api-functions.md)
-   [<span data-ttu-id="ad069-117">Структуры API сжатия</span><span class="sxs-lookup"><span data-stu-id="ad069-117">Compression API Structures</span></span>](compression-api-structures.md)
-   [<span data-ttu-id="ad069-118">Перечисления API сжатия</span><span class="sxs-lookup"><span data-stu-id="ad069-118">Compression API Enumerations</span></span>](compression-api-enumerations.md)

 

 



