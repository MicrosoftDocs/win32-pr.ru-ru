---
description: Библиотека Директксмас основана на библиотеке XNA Math C++ SIMD Library версии 2. x. Здесь описывается отличие Директксмас от XNA Math и отличия версий Директксмас.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Новые возможности (Директксмас)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df1e7f25789ca6f58205ce9f45482e0a49540d1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827630"
---
# <a name="whats-new-directxmath"></a><span data-ttu-id="4908e-104">Новые возможности (Директксмас)</span><span class="sxs-lookup"><span data-stu-id="4908e-104">What's New (DirectXMath)</span></span>

<span data-ttu-id="4908e-105">Библиотека Директксмас основана на [библиотеке XNA Math C++ SIMD версии 2,04](https://walbourn.github.io/xna-math-version-2-04/).</span><span class="sxs-lookup"><span data-stu-id="4908e-105">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/xna-math-version-2-04/).</span></span> <span data-ttu-id="4908e-106">Здесь описывается отличие Директксмас от XNA Math и отличия версий Директксмас.</span><span class="sxs-lookup"><span data-stu-id="4908e-106">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span>

-   [<span data-ttu-id="4908e-107">Журнал рлеасе</span><span class="sxs-lookup"><span data-stu-id="4908e-107">Rlease history</span></span>](#release-history)
-   [<span data-ttu-id="4908e-108">Директксмас различия от XNA Math</span><span class="sxs-lookup"><span data-stu-id="4908e-108">DirectXMath differences from XNA Math</span></span>](#directxmath-differences-from-xna-math)
-   [<span data-ttu-id="4908e-109">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="4908e-109">Related topics</span></span>](#related-topics)

## <a name="release-history"></a><span data-ttu-id="4908e-110">История выпусков</span><span class="sxs-lookup"><span data-stu-id="4908e-110">Release history</span></span>

<table>
 <tr>
  <td><span data-ttu-id="4908e-111">Пакет SDK для Windows 10 (20348), версия 2104</span><span class="sxs-lookup"><span data-stu-id="4908e-111">Windows 10 SDK (20348), version 2104</span></span></td><td><span data-ttu-id="4908e-112">Директксмас 3,16</span><span class="sxs-lookup"><span data-stu-id="4908e-112">DirectXMath 3.16</span></span></td>
 </td>
 <tr>
  <td><span data-ttu-id="4908e-113">Windows 10 Май 2020 обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="4908e-113">Windows 10 May 2020 Update SDK</span></span></td><td><span data-ttu-id="4908e-114">Директксмас 3,14</span><span class="sxs-lookup"><span data-stu-id="4908e-114">DirectXMath 3.14</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4908e-115">Пакет SDK для Windows 10 Октябрь 2018 с обновлением</span><span class="sxs-lookup"><span data-stu-id="4908e-115">Windows 10 October 2018 Update SDK</span></span></td><td><span data-ttu-id="4908e-116">Директксмас 3,13</span><span class="sxs-lookup"><span data-stu-id="4908e-116">DirectXMath 3.13</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4908e-117">Пакет SDK для Windows 10 от апреля 2018 с обновлением</span><span class="sxs-lookup"><span data-stu-id="4908e-117">Windows 10 April 2018 Update SDK</span></span><br /><span data-ttu-id="4908e-118">Пакет SDK обновления Windows 10 для дизайнеров</span><span class="sxs-lookup"><span data-stu-id="4908e-118">Windows 10 Fall Creators Update SDK</span></span></td><td><span data-ttu-id="4908e-119">Директксмас 3,11</span><span class="sxs-lookup"><span data-stu-id="4908e-119">DirectXMath 3.11</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4908e-120">Пакет SDK для Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="4908e-120">Windows 10 Creators Update SDK</span></span></td><td><span data-ttu-id="4908e-121">Директксмас 3,10</span><span class="sxs-lookup"><span data-stu-id="4908e-121">DirectXMath 3.10</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4908e-122">Windows 10 для юбилея SDK</span><span class="sxs-lookup"><span data-stu-id="4908e-122">Windows 10 Anniversary SDK</span></span></td><td><span data-ttu-id="4908e-123">Директксмас 3,09</span><span class="sxs-lookup"><span data-stu-id="4908e-123">DirectXMath 3.09</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4908e-124">Пакет SDK для Windows 10 (Ноябрь 2015)</span><span class="sxs-lookup"><span data-stu-id="4908e-124">Windows 10 SDK (November 2015)</span></span></td><td><span data-ttu-id="4908e-125">Директксмас 3,08</span><span class="sxs-lookup"><span data-stu-id="4908e-125">DirectXMath 3.08</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4908e-126">Windows SDK для Windows 8.1 (пружинный 2015)</span><span class="sxs-lookup"><span data-stu-id="4908e-126">Windows SDK for Windows 8.1 (Spring 2015)</span></span></td><td><span data-ttu-id="4908e-127">Директксмас 3,07</span><span class="sxs-lookup"><span data-stu-id="4908e-127">DirectXMath 3.07</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4908e-128">Windows SDK для Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4908e-128">Windows SDK for Windows 8.1</span></span></td><td><span data-ttu-id="4908e-129">Директксмас 3,06</span><span class="sxs-lookup"><span data-stu-id="4908e-129">DirectXMath 3.06</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4908e-130">Windows SDK для Windows 8</span><span class="sxs-lookup"><span data-stu-id="4908e-130">Windows SDK for Windows 8</span></span></td><td><span data-ttu-id="4908e-131">Директксмас 3,03</span><span class="sxs-lookup"><span data-stu-id="4908e-131">DirectXMath 3.03</span></span></td>
 </tr>
</table>

<span data-ttu-id="4908e-132">Дополнительные сведения см. в разделе [директксмас releases](https://github.com/Microsoft/DirectXMath/releases) .</span><span class="sxs-lookup"><span data-stu-id="4908e-132">See [DirectXMath releases](https://github.com/Microsoft/DirectXMath/releases) for more information.</span></span>

## <a name="directxmath-differences-from-xna-math"></a><span data-ttu-id="4908e-133">Директксмас различия от XNA Math</span><span class="sxs-lookup"><span data-stu-id="4908e-133">DirectXMath differences from XNA Math</span></span>

<span data-ttu-id="4908e-134">Вот как библиотека Директксмас в основном отличается от библиотеки XNA Math:</span><span class="sxs-lookup"><span data-stu-id="4908e-134">Here is how the DirectXMath library primarily differs from the XNA Math library:</span></span>

-   <span data-ttu-id="4908e-135">Директксмас имеет только C++ (пространства имен, перегрузки, новые шаблоны и т. д.).</span><span class="sxs-lookup"><span data-stu-id="4908e-135">DirectXMath is C++ only (namespaces, overloads, new templates, and so on).</span></span>
-   <span data-ttu-id="4908e-136">Требуется поддержка стандартной библиотеки C++ 11 (т. е. stdint. h и т. д.).</span><span class="sxs-lookup"><span data-stu-id="4908e-136">Requires C++11 standard library support (that is, stdint.h, and so on).</span></span>
-   <span data-ttu-id="4908e-137">Поддержка встроенных функций ARM-NEON для платформы Windows RT.</span><span class="sxs-lookup"><span data-stu-id="4908e-137">ARM-NEON intrinsics support for the Windows RT platform.</span></span>
-   <span data-ttu-id="4908e-138">Новые функции цвета (преобразования цветового пространства, константы цвета .NET).</span><span class="sxs-lookup"><span data-stu-id="4908e-138">New color functionality (color space conversions, .NET color constants).</span></span>
-   <span data-ttu-id="4908e-139">Ограничивающие типы томов (версия, которая ранее была в заголовке Кснаколлисион в примере конфликта SDK DirectX).</span><span class="sxs-lookup"><span data-stu-id="4908e-139">Bounding volume types (a version of which was previously in the XNACollision header in the DirectX SDK Collision sample).</span></span>
-   <span data-ttu-id="4908e-140">Версия Xbox 360 недоступна.</span><span class="sxs-lookup"><span data-stu-id="4908e-140">No Xbox 360 version is available.</span></span> <span data-ttu-id="4908e-141">XDK Xbox 360 переходит на Кснамас v2. x; Удаление конкретных типов данных и вариантов функций Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="4908e-141">The Xbox 360 XDK continues to ship XNAMath v2.x; removal of Xbox 360 specific data types and function variants.</span></span>
-   <span data-ttu-id="4908e-142">Переработано [**ксмвекторпермуте**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) для улучшения оптимизации SSE и встроенных функций ARM-Neon.</span><span class="sxs-lookup"><span data-stu-id="4908e-142">Reworked [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) for improved optimization for SSE and ARM-NEON intrinsics.</span></span>
-   <span data-ttu-id="4908e-143">Тип [**ксмматрикс**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) является полностью непрозрачным.</span><span class="sxs-lookup"><span data-stu-id="4908e-143">The [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) type is fully opaque.</span></span> <span data-ttu-id="4908e-144">Для доступа к отдельным элементам **ксмматрикс** используйте другие типы, например [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span><span class="sxs-lookup"><span data-stu-id="4908e-144">To access individual elements of **XMMATRIX**, use other types such as [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4908e-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="4908e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4908e-146">Директксмас по программированию</span><span class="sxs-lookup"><span data-stu-id="4908e-146">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> <dt>

[<span data-ttu-id="4908e-147">Выпуски Директксмас</span><span class="sxs-lookup"><span data-stu-id="4908e-147">DirectXMath releases</span></span>](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
