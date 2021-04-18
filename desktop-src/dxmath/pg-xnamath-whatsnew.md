---
description: Библиотека Директксмас основана на библиотеке XNA Math C++ SIMD Library версии 2. x. Здесь описывается отличие Директксмас от XNA Math и отличия версий Директксмас.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Новые возможности (Директксмас)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb9fa8c7ee0600ce0b0fa5eade3a3e111e5edbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692617"
---
# <a name="whats-new-directxmath"></a><span data-ttu-id="e9c02-104">Новые возможности (Директксмас)</span><span class="sxs-lookup"><span data-stu-id="e9c02-104">What's New (DirectXMath)</span></span>

<span data-ttu-id="e9c02-105">Библиотека Директксмас основана на [библиотеке XNA Math C++ SIMD версии 2,04](https://walbourn.github.io/).</span><span class="sxs-lookup"><span data-stu-id="e9c02-105">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/).</span></span> <span data-ttu-id="e9c02-106">Здесь описывается отличие Директксмас от XNA Math и отличия версий Директксмас.</span><span class="sxs-lookup"><span data-stu-id="e9c02-106">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span>

-   [<span data-ttu-id="e9c02-107">Журнал рлеасе</span><span class="sxs-lookup"><span data-stu-id="e9c02-107">Rlease history</span></span>](#release-history)
-   [<span data-ttu-id="e9c02-108">Директксмас различия от XNA Math</span><span class="sxs-lookup"><span data-stu-id="e9c02-108">DirectXMath differences from XNA Math</span></span>](#directxmath-differences-from-xna-math)
-   [<span data-ttu-id="e9c02-109">См. также</span><span class="sxs-lookup"><span data-stu-id="e9c02-109">Related topics</span></span>](#related-topics)

## <a name="release-history"></a><span data-ttu-id="e9c02-110">История выпусков</span><span class="sxs-lookup"><span data-stu-id="e9c02-110">Release history</span></span>

<table>
 <tr>
  <td><span data-ttu-id="e9c02-111">Windows 10 Май 2020 обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="e9c02-111">Windows 10 May 2020 Update SDK</span></span></td><td><span data-ttu-id="e9c02-112">Директксмас 3,14</span><span class="sxs-lookup"><span data-stu-id="e9c02-112">DirectXMath 3.14</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="e9c02-113">Пакет SDK для Windows 10 Октябрь 2018 с обновлением</span><span class="sxs-lookup"><span data-stu-id="e9c02-113">Windows 10 October 2018 Update SDK</span></span></td><td><span data-ttu-id="e9c02-114">Директксмас 3,13</span><span class="sxs-lookup"><span data-stu-id="e9c02-114">DirectXMath 3.13</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="e9c02-115">Пакет SDK для Windows 10 от апреля 2018 с обновлением</span><span class="sxs-lookup"><span data-stu-id="e9c02-115">Windows 10 April 2018 Update SDK</span></span><br /><span data-ttu-id="e9c02-116">Пакет SDK обновления Windows 10 для дизайнеров</span><span class="sxs-lookup"><span data-stu-id="e9c02-116">Windows 10 Fall Creators Update SDK</span></span></td><td><span data-ttu-id="e9c02-117">Директксмас 3,11</span><span class="sxs-lookup"><span data-stu-id="e9c02-117">DirectXMath 3.11</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="e9c02-118">Пакет SDK для Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="e9c02-118">Windows 10 Creators Update SDK</span></span></td><td><span data-ttu-id="e9c02-119">Директксмас 3,10</span><span class="sxs-lookup"><span data-stu-id="e9c02-119">DirectXMath 3.10</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="e9c02-120">Windows 10 для юбилея SDK</span><span class="sxs-lookup"><span data-stu-id="e9c02-120">Windows 10 Anniversary SDK</span></span></td><td><span data-ttu-id="e9c02-121">Директксмас 3,09</span><span class="sxs-lookup"><span data-stu-id="e9c02-121">DirectXMath 3.09</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="e9c02-122">Пакет SDK для Windows 10 (Ноябрь 2015)</span><span class="sxs-lookup"><span data-stu-id="e9c02-122">Windows 10 SDK (November 2015)</span></span></td><td><span data-ttu-id="e9c02-123">Директксмас 3,08</span><span class="sxs-lookup"><span data-stu-id="e9c02-123">DirectXMath 3.08</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="e9c02-124">Windows SDK для Windows 8.1 (пружинный 2015)</span><span class="sxs-lookup"><span data-stu-id="e9c02-124">Windows SDK for Windows 8.1 (Spring 2015)</span></span></td><td><span data-ttu-id="e9c02-125">Директксмас 3,07</span><span class="sxs-lookup"><span data-stu-id="e9c02-125">DirectXMath 3.07</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="e9c02-126">Windows SDK для Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e9c02-126">Windows SDK for Windows 8.1</span></span></td><td><span data-ttu-id="e9c02-127">Директксмас 3,06</span><span class="sxs-lookup"><span data-stu-id="e9c02-127">DirectXMath 3.06</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="e9c02-128">Windows SDK для Windows 8</span><span class="sxs-lookup"><span data-stu-id="e9c02-128">Windows SDK for Windows 8</span></span></td><td><span data-ttu-id="e9c02-129">Директксмас 3,03</span><span class="sxs-lookup"><span data-stu-id="e9c02-129">DirectXMath 3.03</span></span></td>
 </tr>
</table>

<span data-ttu-id="e9c02-130">Дополнительные сведения см. в разделе [директксмас releases](https://github.com/Microsoft/DirectXMath/releases) .</span><span class="sxs-lookup"><span data-stu-id="e9c02-130">See [DirectXMath releases](https://github.com/Microsoft/DirectXMath/releases) for more information.</span></span>

## <a name="directxmath-differences-from-xna-math"></a><span data-ttu-id="e9c02-131">Директксмас различия от XNA Math</span><span class="sxs-lookup"><span data-stu-id="e9c02-131">DirectXMath differences from XNA Math</span></span>

<span data-ttu-id="e9c02-132">Вот как библиотека Директксмас в основном отличается от библиотеки XNA Math:</span><span class="sxs-lookup"><span data-stu-id="e9c02-132">Here is how the DirectXMath library primarily differs from the XNA Math library:</span></span>

-   <span data-ttu-id="e9c02-133">Директксмас имеет только C++ (пространства имен, перегрузки, новые шаблоны и т. д.).</span><span class="sxs-lookup"><span data-stu-id="e9c02-133">DirectXMath is C++ only (namespaces, overloads, new templates, and so on).</span></span>
-   <span data-ttu-id="e9c02-134">Требуется поддержка стандартной библиотеки C++ 11 (т. е. stdint. h и т. д.).</span><span class="sxs-lookup"><span data-stu-id="e9c02-134">Requires C++11 standard library support (that is, stdint.h, and so on).</span></span>
-   <span data-ttu-id="e9c02-135">Поддержка встроенных функций ARM-NEON для платформы Windows RT.</span><span class="sxs-lookup"><span data-stu-id="e9c02-135">ARM-NEON intrinsics support for the Windows RT platform.</span></span>
-   <span data-ttu-id="e9c02-136">Новые функции цвета (преобразования цветового пространства, константы цвета .NET).</span><span class="sxs-lookup"><span data-stu-id="e9c02-136">New color functionality (color space conversions, .NET color constants).</span></span>
-   <span data-ttu-id="e9c02-137">Ограничивающие типы томов (версия, которая ранее была в заголовке Кснаколлисион в примере конфликта SDK DirectX).</span><span class="sxs-lookup"><span data-stu-id="e9c02-137">Bounding volume types (a version of which was previously in the XNACollision header in the DirectX SDK Collision sample).</span></span>
-   <span data-ttu-id="e9c02-138">Версия Xbox 360 недоступна.</span><span class="sxs-lookup"><span data-stu-id="e9c02-138">No Xbox 360 version is available.</span></span> <span data-ttu-id="e9c02-139">XDK Xbox 360 переходит на Кснамас v2. x; Удаление конкретных типов данных и вариантов функций Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="e9c02-139">The Xbox 360 XDK continues to ship XNAMath v2.x; removal of Xbox 360 specific data types and function variants.</span></span>
-   <span data-ttu-id="e9c02-140">Переработано [**ксмвекторпермуте**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) для улучшения оптимизации SSE и встроенных функций ARM-Neon.</span><span class="sxs-lookup"><span data-stu-id="e9c02-140">Reworked [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) for improved optimization for SSE and ARM-NEON intrinsics.</span></span>
-   <span data-ttu-id="e9c02-141">Тип [**ксмматрикс**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) является полностью непрозрачным.</span><span class="sxs-lookup"><span data-stu-id="e9c02-141">The [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) type is fully opaque.</span></span> <span data-ttu-id="e9c02-142">Для доступа к отдельным элементам **ксмматрикс** используйте другие типы, например [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span><span class="sxs-lookup"><span data-stu-id="e9c02-142">To access individual elements of **XMMATRIX**, use other types such as [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9c02-143">См. также</span><span class="sxs-lookup"><span data-stu-id="e9c02-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9c02-144">Директксмас по программированию</span><span class="sxs-lookup"><span data-stu-id="e9c02-144">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> <dt>

[<span data-ttu-id="e9c02-145">Выпуски Директксмас</span><span class="sxs-lookup"><span data-stu-id="e9c02-145">DirectXMath releases</span></span>](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
