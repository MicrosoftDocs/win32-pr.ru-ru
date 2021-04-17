---
description: В Windows Vista счетчики производительности реализовали новую архитектуру (версия 2,0) для предоставления данных счетчиков.
ms.assetid: c17eda2f-3cf8-40d6-8be6-c1ce190d1a26
title: Предоставление данных счетчиков
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: ed5aa4cc505baab9e15d3f69c3fb466712eddbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663160"
---
# <a name="providing-counter-data"></a><span data-ttu-id="14097-103">Предоставление данных счетчиков</span><span class="sxs-lookup"><span data-stu-id="14097-103">Providing Counter Data</span></span>

<span data-ttu-id="14097-104">Программные компоненты, которые публикуют данные с помощью счетчиков производительности Windows, называются поставщиками данных производительности.</span><span class="sxs-lookup"><span data-stu-id="14097-104">Software components that publish data via Windows Performance Counters are called performance data providers.</span></span>

<span data-ttu-id="14097-105">Windows поддерживает два типа поставщиков данных о производительности.</span><span class="sxs-lookup"><span data-stu-id="14097-105">Windows supports two kinds of performance data providers.</span></span> <span data-ttu-id="14097-106">Устаревшие поставщики данных о производительности (**v1**) реализуются с помощью. INI-файл и DLL производительности.</span><span class="sxs-lookup"><span data-stu-id="14097-106">Legacy performance data providers (**V1 providers**) are implemented using an .INI file and a performance DLL.</span></span> <span data-ttu-id="14097-107">Современные поставщики данных производительности (**поставщики v2**) используют. MAN (XML manifest) и API поставщика счетчика производительности.</span><span class="sxs-lookup"><span data-stu-id="14097-107">Modern performance data providers (**V2 providers**) use a .MAN (XML manifest) and the performance counter provider APIs.</span></span>

## <a name="manifests"></a><span data-ttu-id="14097-108">Манифесты</span><span class="sxs-lookup"><span data-stu-id="14097-108">Manifests</span></span>

<span data-ttu-id="14097-109">Современные поставщики данных производительности используют. MAN (XML manifest) для определения данных счетчика и использования API поставщика счетчиков производительности для управления данными в контексте поставщика.</span><span class="sxs-lookup"><span data-stu-id="14097-109">Modern performance data providers use a .MAN (XML manifest) to define the counter data and use performance counter provider APIs to manage data within the context of the provider.</span></span>

<span data-ttu-id="14097-110">Поставщики, реализованные с использованием манифеста и API поставщика счетчиков производительности, часто называются **поставщиками версии 2**.</span><span class="sxs-lookup"><span data-stu-id="14097-110">Providers implemented using a manifest and performance counter provider APIs are often called **V2 providers**.</span></span>

<span data-ttu-id="14097-111">Windows поддерживает поставщики пользовательского режима v2 в Windows Vista или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="14097-111">Windows supports user-mode V2 providers on Windows Vista or later.</span></span> <span data-ttu-id="14097-112">Сведения о пользовательском режиме см. в разделе [предоставление данных счетчиков с помощью версии 2,0](providing-counter-data-using-version-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="14097-112">For user-mode details, see [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>

<span data-ttu-id="14097-113">Windows поддерживает поставщики в режиме ядра v2 в Windows 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="14097-113">Windows supports kernel-mode V2 providers on Windows 7 or later.</span></span> <span data-ttu-id="14097-114">Сведения о режиме ядра см. в разделе [мониторинг производительности в режиме ядра](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).</span><span class="sxs-lookup"><span data-stu-id="14097-114">For kernel-mode details, see [Kernel Mode Performance Monitoring](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).</span></span>

## <a name="performance-dll-deprecated"></a><span data-ttu-id="14097-115">Библиотека DLL производительности (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="14097-115">Performance DLL (deprecated)</span></span>

<span data-ttu-id="14097-116">В архитектуре устаревших счетчиков производительности поставщики реализовали библиотеку DLL производительности, которая выполнялась в процессе потребителя для получения и предоставления данных счетчиков, когда потребитель запросил его.</span><span class="sxs-lookup"><span data-stu-id="14097-116">In the legacy performance counter architecture, providers implemented a performance DLL to that ran in the consumer's process to collect and provide the counter data when a consumer requested it.</span></span> <span data-ttu-id="14097-117">Поставщик использовал инициализацию (. INI) и записи реестра для определения счетчиков и настройки библиотеки производительности.</span><span class="sxs-lookup"><span data-stu-id="14097-117">The provider used an initialization (.INI) file and registry entries to define the counters and to configure the performance DLL.</span></span>

<span data-ttu-id="14097-118">Поставщики, реализованные с помощью. INI-файл и библиотека производительности часто называются **поставщиками v1**.</span><span class="sxs-lookup"><span data-stu-id="14097-118">Providers implemented using an .INI file and a performance DLL are often called **V1 providers**.</span></span>

> [!CAUTION]
> <span data-ttu-id="14097-119">Хотя вы по-прежнему можете использовать библиотеку DLL производительности для предоставления данных счетчиков, эта архитектура устарела из-за существенных ограничений производительности и надежности.</span><span class="sxs-lookup"><span data-stu-id="14097-119">Although you can still use a performance DLL to provide counter data, this architecture is deprecated due to significant performance and reliability limitations.</span></span> <span data-ttu-id="14097-120">Кроме того, поставщики v1 часто сложнее реализовать, поскольку им требуется доставка отдельной библиотеки DLL, которая должна выполняться в процессе потребителя.</span><span class="sxs-lookup"><span data-stu-id="14097-120">In addition, V1 providers are often harder to implement since they require shipping a separate DLL that must run in the consumer's process.</span></span>

<span data-ttu-id="14097-121">Дополнительные сведения см. [в разделе Предоставление данных счетчика с помощью библиотеки DLL производительности](providing-counter-data-using-a-performance-dll.md).</span><span class="sxs-lookup"><span data-stu-id="14097-121">For details, see [Providing Counter Data Using a Performance DLL](providing-counter-data-using-a-performance-dll.md).</span></span>
