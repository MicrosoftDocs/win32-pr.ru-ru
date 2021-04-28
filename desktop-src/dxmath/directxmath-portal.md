---
description: DirectXMath
ms.assetid: 719954bf-0d7d-f647-2d3f-a77d87df204e
title: DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd35f1faf004bc55a6802da204a6c2fe4e7869b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113012"
---
# <a name="directxmath"></a><span data-ttu-id="113c0-103">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="113c0-103">DirectXMath</span></span>

## <a name="purpose"></a><span data-ttu-id="113c0-104">Цель</span><span class="sxs-lookup"><span data-stu-id="113c0-104">Purpose</span></span>

<span data-ttu-id="113c0-105">API Директксмас предоставляет SIMD-удобные типы и функции C++ для обычных линейных и графических математических операций, общих для приложений DirectX.</span><span class="sxs-lookup"><span data-stu-id="113c0-105">The DirectXMath API provides SIMD-friendly C++ types and functions for common linear algebra and graphics math operations common to DirectX applications.</span></span> <span data-ttu-id="113c0-106">Библиотека предоставляет оптимизированные версии для Windows 32 (x86), Windows 64-bit (x64) и Windows в ARM/ARM64 с поддержкой функций SSE, AVX и ARM-NEON в компиляторе Visual C++.</span><span class="sxs-lookup"><span data-stu-id="113c0-106">The library provides optimized versions for Windows 32-bit (x86), Windows 64-bit (x64), and Windows on ARM/ARM64 through SSE, AVX, and ARM-NEON intrinsics support in the Visual C++ compiler.</span></span>

<span data-ttu-id="113c0-107">Для разработчиков, начинающихся с директксмас, можно использовать оболочку симплемас в *наборе средств DirectX* для [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929)  /  [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) в качестве отправной точки.</span><span class="sxs-lookup"><span data-stu-id="113c0-107">For developers new to DirectXMath, you may want to consider using the SimpleMath wrapper in the *DirectX Tool Kit* for [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929) / [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) as a starting point.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="113c0-108">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="113c0-108">In this section</span></span>



| <span data-ttu-id="113c0-109">Раздел</span><span class="sxs-lookup"><span data-stu-id="113c0-109">Topic</span></span>                                                                     | <span data-ttu-id="113c0-110">Описание</span><span class="sxs-lookup"><span data-stu-id="113c0-110">Description</span></span>                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="113c0-111">Директксмас по программированию</span><span class="sxs-lookup"><span data-stu-id="113c0-111">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)<br/>     | <span data-ttu-id="113c0-112">Директксмас предоставляет математическое решение, оптимизированное для Windows.</span><span class="sxs-lookup"><span data-stu-id="113c0-112">DirectXMath provides a math solution optimized for Windows.</span></span><br/>           |
| [<span data-ttu-id="113c0-113">Справочник по программированию Директксмас</span><span class="sxs-lookup"><span data-stu-id="113c0-113">DirectXMath Programming Reference</span></span>](ovw-xnamath-reference.md)<br/> | <span data-ttu-id="113c0-114">Этот раздел содержит справочные материалы по библиотеке Директксмас.</span><span class="sxs-lookup"><span data-stu-id="113c0-114">This section contains reference material for the DirectXMath Library.</span></span><br/> |



 

## <a name="developer-audience"></a><span data-ttu-id="113c0-115">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="113c0-115">Developer audience</span></span>

<span data-ttu-id="113c0-116">Библиотека Директксмас разработана для разработчиков на C++, работающих в играх и графиках DirectX в приложениях для Магазина Windows, в играх Xbox и традиционных настольных приложениях для Windows.</span><span class="sxs-lookup"><span data-stu-id="113c0-116">The DirectXMath library is designed for C++ developers working on games and DirectX graphics in Windows Store apps, Xbox games, and traditional desktop apps for Windows.</span></span>

## <a name="obtaining-directxmath"></a><span data-ttu-id="113c0-117">Получение Директксмас</span><span class="sxs-lookup"><span data-stu-id="113c0-117">Obtaining DirectXMath</span></span>
 
<span data-ttu-id="113c0-118">Заголовки Директксмас поставляются в Windows SDK, поставляемом с Visual Studio 2012 или более поздней версии, и во всех встроенных заголовках нет библиотеки DLL или статической библиотеки для связи.</span><span class="sxs-lookup"><span data-stu-id="113c0-118">The DirectXMath headers ship in the Windows SDK that comes with Visual Studio 2012 or later, and as an all inline header there is no DLL or static library to link against.</span></span> <span data-ttu-id="113c0-119">Он также доступен в виде пакета в [NuGet](https://www.nuget.org/packages/directxmath/).</span><span class="sxs-lookup"><span data-stu-id="113c0-119">It is also available as a package on [NuGet](https://www.nuget.org/packages/directxmath/).</span></span>

<span data-ttu-id="113c0-120">Директксмас — это открытый исходный код с [лицензией MIT](https://opensource.org/licenses/MIT) , размещенной на [GitHub](https://github.com/Microsoft/DirectXMath).</span><span class="sxs-lookup"><span data-stu-id="113c0-120">DirectXMath is open source under the [MIT license](https://opensource.org/licenses/MIT) hosted on [GitHub](https://github.com/Microsoft/DirectXMath).</span></span>




