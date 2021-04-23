---
description: Директксмас предоставляет математическое решение, оптимизированное для Windows.
ms.assetid: c2a64435-b2fb-3638-2eea-3ed52f4c7cd5
title: Директксмас по программированию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df406787776f9fa5d1786e6ed6c5998e27a1c059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683084"
---
# <a name="directxmath-programming-guide"></a><span data-ttu-id="3288c-103">Директксмас по программированию</span><span class="sxs-lookup"><span data-stu-id="3288c-103">DirectXMath programming guide</span></span>

<span data-ttu-id="3288c-104">Директксмас предоставляет математическое решение, оптимизированное для Windows.</span><span class="sxs-lookup"><span data-stu-id="3288c-104">DirectXMath provides a math solution optimized for Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3288c-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="3288c-105">In this section</span></span>



| <span data-ttu-id="3288c-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="3288c-106">Topic</span></span>                                                             | <span data-ttu-id="3288c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3288c-107">Description</span></span>                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3288c-108">Начало работы</span><span class="sxs-lookup"><span data-stu-id="3288c-108">Getting Started</span></span>](pg-xnamath-getting-started.md)<br/>      | <span data-ttu-id="3288c-109">Библиотека Директксмас реализует оптимальный и переносимый интерфейс для арифметических и линейных операций с векторами с плавающей запятой одиночной точности (двумерные, трехмерные и 4D) или матрицы (3 × 3 и 4 × 4).</span><span class="sxs-lookup"><span data-stu-id="3288c-109">The DirectXMath Library implements an optimal and portable interface for arithmetic and linear algebra operations on single-precision floating-point vectors (2D, 3D, and 4D) or matrices (3×3 and 4×4).</span></span> <br/>                                                    |
| [<span data-ttu-id="3288c-110">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="3288c-110">What's New</span></span>](pg-xnamath-whatsnew.md)<br/>                  | <span data-ttu-id="3288c-111">Библиотека Директксмас основана на [библиотеке XNA Math C++ SIMD версии 2,04](https://walbourn.github.io/).</span><span class="sxs-lookup"><span data-stu-id="3288c-111">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/).</span></span> <span data-ttu-id="3288c-112">Здесь описывается отличие Директксмас от XNA Math и отличия версий Директксмас.</span><span class="sxs-lookup"><span data-stu-id="3288c-112">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span> <br/> |
| [<span data-ttu-id="3288c-113">Перенос кода</span><span class="sxs-lookup"><span data-stu-id="3288c-113">Code Migration</span></span>](pg-xnamath-migration.md)<br/>             | <span data-ttu-id="3288c-114">В этом обзоре описываются изменения, необходимые для переноса существующего кода с помощью библиотеки XNA Math в библиотеку Директксмас.</span><span class="sxs-lookup"><span data-stu-id="3288c-114">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="3288c-115">Работа с D3DXMath</span><span class="sxs-lookup"><span data-stu-id="3288c-115">Working with D3DXMath</span></span>](pg-xnamath-migration-d3dx.md)<br/> | <span data-ttu-id="3288c-116">D3DXMath — это математическая вспомогательная библиотека для приложений Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3288c-116">D3DXMath is a math helper library for Direct3D applications.</span></span> <br/>                                                                                                                                                                                                |
| [<span data-ttu-id="3288c-117">Оптимизация кода</span><span class="sxs-lookup"><span data-stu-id="3288c-117">Code Optimization</span></span>](pg-xnamath-optimizing.md)<br/>         | <span data-ttu-id="3288c-118">В этом разделе описываются рекомендации по оптимизации и стратегии использования библиотеки Директксмас.</span><span class="sxs-lookup"><span data-stu-id="3288c-118">This topic describes optimization considerations and strategies with the DirectXMath Library.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="3288c-119">Внутренние библиотеки</span><span class="sxs-lookup"><span data-stu-id="3288c-119">Library Internals</span></span>](pg-xnamath-internals.md)<br/>          | <span data-ttu-id="3288c-120">В этом разделе описывается внутренняя структура библиотеки Директксмас.</span><span class="sxs-lookup"><span data-stu-id="3288c-120">This topic describes the internal design of the DirectXMath library.</span></span><br/>                                                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="3288c-121">См. также</span><span class="sxs-lookup"><span data-stu-id="3288c-121">Related Topics</span></span>

<dl> <dt>

<span data-ttu-id="3288c-122"><span id="DirectXMath_Programming_Reference"></span><span id="directxmath_programming_reference"></span><span id="DIRECTXMATH_PROGRAMMING_REFERENCE"></span>[Справочник по программированию Директксмас](ovw-xnamath-reference.md)</span><span class="sxs-lookup"><span data-stu-id="3288c-122"><span id="DirectXMath_Programming_Reference"></span><span id="directxmath_programming_reference"></span><span id="DIRECTXMATH_PROGRAMMING_REFERENCE"></span>[DirectXMath Programming Reference](ovw-xnamath-reference.md)</span></span>
<span data-ttu-id="3288c-123"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3288c-123"></dt> <dd></dd> </dl></span></span>

## <a name="related-topics"></a><span data-ttu-id="3288c-124">См. также</span><span class="sxs-lookup"><span data-stu-id="3288c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3288c-125">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="3288c-125">DirectXMath</span></span>](directxmath-portal.md)
</dt> </dl>

 

 




