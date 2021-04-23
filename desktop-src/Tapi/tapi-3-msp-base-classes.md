---
description: В этом документе описывается проектирование и использование базовых классов MSP. Использование этих классов не является обязательным, но большинство разработчиков найдут, что они упрощают задачу создания MSP-файла на основе DirectShow для TAPI 3S New МСПИ.
ms.assetid: 97597dcf-eb18-47aa-b0ed-a43286d5d134
title: Базовые классы MSP TAPI 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb7c7958847ef7bf699cfe4810f7133ef0b4bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674264"
---
# <a name="tapi-3-msp-base-classes"></a><span data-ttu-id="b5c56-104">Базовые классы MSP TAPI 3</span><span class="sxs-lookup"><span data-stu-id="b5c56-104">TAPI 3 MSP Base Classes</span></span>

<span data-ttu-id="b5c56-105">В этом документе описывается проектирование и использование базовых классов MSP.</span><span class="sxs-lookup"><span data-stu-id="b5c56-105">This document describes the design and use of the MSP Base Classes.</span></span> <span data-ttu-id="b5c56-106">Использование этих классов не является обязательным, но большинство разработчиков найдут, что они упрощают задачу создания MSP-файла на основе DirectShow для новых МСПИов TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="b5c56-106">Use of these classes is not required, but most developers will find they simplify the task of building a DirectShow-based MSP for TAPI 3's new MSPI.</span></span>

<span data-ttu-id="b5c56-107">Исходный код для базовых классов MSP можно найти в каталоге Samples платформы Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="b5c56-107">Source code for the MSP base classes can be found in the Samples directory of the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="b5c56-108">Предполагается знание модели COM, ATL, DirectShow и C++.</span><span class="sxs-lookup"><span data-stu-id="b5c56-108">Familiarity with COM, ATL, DirectShow, and C++ is assumed.</span></span> <span data-ttu-id="b5c56-109">Читатель должен также узнать общий материал [о поставщике службы мультимедиа (MSP)](about-the-media-service-provider-msp-.md) и в [интерфейсе поставщика услуг мультимедиа (мспи)](media-service-provider-interface-mspi-.md).</span><span class="sxs-lookup"><span data-stu-id="b5c56-109">The reader must also know the general material in [About the Media Service Provider (MSP)](about-the-media-service-provider-msp-.md) and in [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md).</span></span>

<span data-ttu-id="b5c56-110">Для Windows 2000 требуется ATL 2,1.</span><span class="sxs-lookup"><span data-stu-id="b5c56-110">ATL 2.1 is required for Windows 2000.</span></span> <span data-ttu-id="b5c56-111">Начиная с Windows XP, будут компилироваться и ATL 2,1, и 3,0.</span><span class="sxs-lookup"><span data-stu-id="b5c56-111">Starting with Windows XP, both ATL 2.1 and 3.0 will compile.</span></span>

<span data-ttu-id="b5c56-112">Библиотеки базовых классов MSP (доступны в пакете SDK):</span><span class="sxs-lookup"><span data-stu-id="b5c56-112">MSP Base Class Libraries (available in the SDK):</span></span>

-   <span data-ttu-id="b5c56-113">Мспбасе. lib</span><span class="sxs-lookup"><span data-stu-id="b5c56-113">Mspbase.lib</span></span>
-   <span data-ttu-id="b5c56-114">Мспид. lib</span><span class="sxs-lookup"><span data-stu-id="b5c56-114">Mspid.lib</span></span>
-   <span data-ttu-id="b5c56-115">Стрмбасе. lib</span><span class="sxs-lookup"><span data-stu-id="b5c56-115">Strmbase.lib</span></span>
-   <span data-ttu-id="b5c56-116">Тмуид. lib</span><span class="sxs-lookup"><span data-stu-id="b5c56-116">Tmuid.lib</span></span>
    > [!Note]  
    > <span data-ttu-id="b5c56-117">Следует использовать динамическое, а не статическое связывание.</span><span class="sxs-lookup"><span data-stu-id="b5c56-117">Dynamic rather than static linking should be used.</span></span>

     

<span data-ttu-id="b5c56-118">Файлы заголовков базового класса MSP (доступны в пакете SDK):</span><span class="sxs-lookup"><span data-stu-id="b5c56-118">MSP Base Class Header Files (available in the SDK):</span></span>

-   <span data-ttu-id="b5c56-119">Мспаддр. h</span><span class="sxs-lookup"><span data-stu-id="b5c56-119">Mspaddr.h</span></span>
-   <span data-ttu-id="b5c56-120">Мспбасе. h</span><span class="sxs-lookup"><span data-stu-id="b5c56-120">Mspbase.h</span></span>
-   <span data-ttu-id="b5c56-121">Мспкалл. h</span><span class="sxs-lookup"><span data-stu-id="b5c56-121">Mspcall.h</span></span>
-   <span data-ttu-id="b5c56-122">Мсплог. h</span><span class="sxs-lookup"><span data-stu-id="b5c56-122">Msplog.h</span></span>
-   <span data-ttu-id="b5c56-123">Мспстрм. h</span><span class="sxs-lookup"><span data-stu-id="b5c56-123">Mspstrm.h</span></span>
-   <span data-ttu-id="b5c56-124">Мсптерм. h</span><span class="sxs-lookup"><span data-stu-id="b5c56-124">Mspterm.h</span></span>
-   <span data-ttu-id="b5c56-125">Мспсрд. h</span><span class="sxs-lookup"><span data-stu-id="b5c56-125">Mspthrd.h</span></span>
-   <span data-ttu-id="b5c56-126">Мсптмак. h</span><span class="sxs-lookup"><span data-stu-id="b5c56-126">Msptmac.h</span></span>
-   <span data-ttu-id="b5c56-127">Мсптмвк. h</span><span class="sxs-lookup"><span data-stu-id="b5c56-127">Msptmvc.h</span></span>
-   <span data-ttu-id="b5c56-128">Мсптрмвк. h</span><span class="sxs-lookup"><span data-stu-id="b5c56-128">Msptrmvc.h</span></span>
-   <span data-ttu-id="b5c56-129">Мсптрмак. h</span><span class="sxs-lookup"><span data-stu-id="b5c56-129">Msptrmac.h</span></span>
-   <span data-ttu-id="b5c56-130">Мсптрмар. h</span><span class="sxs-lookup"><span data-stu-id="b5c56-130">Msptrmar.h</span></span>
-   <span data-ttu-id="b5c56-131">Мспутилс. h</span><span class="sxs-lookup"><span data-stu-id="b5c56-131">Msputils.h</span></span>

<span data-ttu-id="b5c56-132">Исходные файлы для базового класса MSP (доступны в примерах пакета SDK):</span><span class="sxs-lookup"><span data-stu-id="b5c56-132">MSP Base Class Source Files (available in the SDK Samples):</span></span>

-   <span data-ttu-id="b5c56-133">Мспаддр. cpp</span><span class="sxs-lookup"><span data-stu-id="b5c56-133">Mspaddr.cpp</span></span>
-   <span data-ttu-id="b5c56-134">Мспкалл. cpp</span><span class="sxs-lookup"><span data-stu-id="b5c56-134">Mspcall.cpp</span></span>
-   <span data-ttu-id="b5c56-135">Мсплог. cpp</span><span class="sxs-lookup"><span data-stu-id="b5c56-135">Msplog.cpp</span></span>
-   <span data-ttu-id="b5c56-136">Мспстрм. cpp</span><span class="sxs-lookup"><span data-stu-id="b5c56-136">Mspstrm.cpp</span></span>
-   <span data-ttu-id="b5c56-137">Мсптерм. cpp</span><span class="sxs-lookup"><span data-stu-id="b5c56-137">Mspterm.cpp</span></span>
-   <span data-ttu-id="b5c56-138">Мспсрд. cpp</span><span class="sxs-lookup"><span data-stu-id="b5c56-138">Mspthrd.cpp</span></span>
-   <span data-ttu-id="b5c56-139">Мсптрмак. cpp</span><span class="sxs-lookup"><span data-stu-id="b5c56-139">Msptrmac.cpp</span></span>
-   <span data-ttu-id="b5c56-140">Мсптрмар. cpp</span><span class="sxs-lookup"><span data-stu-id="b5c56-140">Msptrmar.cpp</span></span>
-   <span data-ttu-id="b5c56-141">Мсптрмвк. cpp</span><span class="sxs-lookup"><span data-stu-id="b5c56-141">Msptrmvc.cpp</span></span>
-   <span data-ttu-id="b5c56-142">Мспутилс. cpp</span><span class="sxs-lookup"><span data-stu-id="b5c56-142">Msputils.cpp</span></span>

 

 



