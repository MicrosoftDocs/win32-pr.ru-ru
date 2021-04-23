---
description: Расширения Intel Advanced VML (AVX) — это 256-разрядное расширение вектора с плавающей точкой на основе архитектуры Intel. Он включает расширения для наборов инструкций и регистров.
ms.assetid: 76357e08-a53c-4490-b08d-1c26900a3826
title: Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 454c8bd5090463cefa1b0ff3a27ef7a04787db0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423182"
---
# <a name="intel-avx"></a><span data-ttu-id="dfc02-104">Intel AVX</span><span class="sxs-lookup"><span data-stu-id="dfc02-104">Intel AVX</span></span>

## <a name="purpose"></a><span data-ttu-id="dfc02-105">Назначение</span><span class="sxs-lookup"><span data-stu-id="dfc02-105">Purpose</span></span>

<span data-ttu-id="dfc02-106">Расширения Intel Advanced VML (AVX) — это 256-разрядное расширение вектора с плавающей точкой на основе архитектуры Intel.</span><span class="sxs-lookup"><span data-stu-id="dfc02-106">Intel Advanced Vector Extensions (AVX) is a 256-bit SIMD floating point vector extension of Intel architecture.</span></span> <span data-ttu-id="dfc02-107">Он включает расширения для наборов инструкций и регистров.</span><span class="sxs-lookup"><span data-stu-id="dfc02-107">It includes extensions to both instruction and register sets.</span></span>

<span data-ttu-id="dfc02-108">Корпорация Майкрософт разработала некоторые улучшения API, такие как функции Ксстате, которые позволяют приложениям получать доступ к информации и состоянию расширенных функций процессора, включая Intel AVX, и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="dfc02-108">Microsoft has developed some API enhancements, such as XState functions, that enable applications to access and manipulate extended processor feature information and state, including Intel AVX.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dfc02-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="dfc02-109">In this section</span></span>



| <span data-ttu-id="dfc02-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="dfc02-110">Topic</span></span>                                                                     | <span data-ttu-id="dfc02-111">Описание</span><span class="sxs-lookup"><span data-stu-id="dfc02-111">Description</span></span>                                                                                                                                               |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dfc02-112">Работа с контекстом Ксстате</span><span class="sxs-lookup"><span data-stu-id="dfc02-112">Working with XState Context</span></span>](working-with-xstate-context.md)<br/> | <span data-ttu-id="dfc02-113">Этот документ содержит пример, демонстрирующий использование функций контекста Ксстате для получения и задания расширенных функций в потоке.</span><span class="sxs-lookup"><span data-stu-id="dfc02-113">This document contains an example that demonstrates how to use the XState context functions to retrieve and set extended features on a thread.</span></span><br/> |
| [<span data-ttu-id="dfc02-114">Функции AVX</span><span class="sxs-lookup"><span data-stu-id="dfc02-114">AVX Functions</span></span>](avx-functions.md)<br/>                             | <span data-ttu-id="dfc02-115">Функции Intel AVX</span><span class="sxs-lookup"><span data-stu-id="dfc02-115">Intel AVX functions</span></span><br/>                                                                                                                            |



 

## <a name="developer-audience"></a><span data-ttu-id="dfc02-116">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="dfc02-116">Developer audience</span></span>

<span data-ttu-id="dfc02-117">Intel AVX предназначен для использования приложениями, которые имеют большие объемы вычислений с плавающей точкой и могут быть векторными.</span><span class="sxs-lookup"><span data-stu-id="dfc02-117">Intel AVX is designed for use by applications that are strongly floating point compute intensive and can be vectorized.</span></span> <span data-ttu-id="dfc02-118">Примерами приложений могут служить аудио и аудиокодеки, приложения для редактирования изображений и видео, средства анализа финансовых служб и программное обеспечение для моделирования, а затем производственное и инженерное программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="dfc02-118">Example applications include audio processing and audio codecs, image and video editing applications, financial services analysis and modeling software, and manufacturing and engineering software.</span></span>

 

 




