---
title: Архитектура WFP
description: В этом разделе содержится краткий обзор архитектуры платформы фильтрации Windows.
ms.assetid: 17a90f5c-ef82-4b14-b7f1-dd025d5f7303
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8740fed254aca97ab77566e2a7f0ace9a6679d56
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104260834"
---
# <a name="wfp-architecture"></a><span data-ttu-id="ba576-103">Архитектура WFP</span><span class="sxs-lookup"><span data-stu-id="ba576-103">WFP Architecture</span></span>

<span data-ttu-id="ba576-104">На следующем рисунке показана базовая архитектура платформы фильтрации Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="ba576-104">The following figure shows the basic architecture of the Windows Filtering Platform (WFP).</span></span>

![Базовая архитектура схемы платформы фильтрации Windows](images/wfp-architecture.png)

## <a name="filter-engine"></a><span data-ttu-id="ba576-106">Обработчик фильтров</span><span class="sxs-lookup"><span data-stu-id="ba576-106">Filter Engine</span></span>

<span data-ttu-id="ba576-107">Обработчик фильтров содержит компонент пользовательского режима и компонент режима ядра, которые вместе выполняют все операции фильтрации сетевых данных.</span><span class="sxs-lookup"><span data-stu-id="ba576-107">The filter engine contains a user-mode component and a kernel-mode component, which together perform all of the filtering operations on network data.</span></span> <span data-ttu-id="ba576-108">Механизм фильтрации содержит несколько слоев фильтрации, которые неплотно сопоставляются с уровнями стека сети операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ba576-108">The filter engine contains multiple filtering layers that map loosely to the operating system's networking stack layers.</span></span> <span data-ttu-id="ba576-109">Уровни механизма фильтрации делятся на слои пользовательского режима и уровни ядра на основе компонента механизма фильтрации, который их владеет.</span><span class="sxs-lookup"><span data-stu-id="ba576-109">The filter engine layers are divided into user-mode layers and kernel-mode layers based on the filter engine component that owns them.</span></span>

<span data-ttu-id="ba576-110">Компонент пользовательского режима выполняет фильтрацию RPC и IPsec.</span><span class="sxs-lookup"><span data-stu-id="ba576-110">The user-mode component performs RPC and IPsec filtering.</span></span> <span data-ttu-id="ba576-111">Механизм фильтрации содержит около 10 слоев фильтрации в пользовательском режиме.</span><span class="sxs-lookup"><span data-stu-id="ba576-111">The filter engine contains approximately 10 user-mode filtering layers.</span></span>

<span data-ttu-id="ba576-112">Компонент режима ядра выполняет фильтрацию по сети и транспортным слоям в стеке TC/IP.</span><span class="sxs-lookup"><span data-stu-id="ba576-112">The kernel-mode component performs filtering at the network and transport layers of the TC/IP stack.</span></span> <span data-ttu-id="ba576-113">Этот компонент также вызывает доступные функции выноски во время процесса [классификации](basic-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ba576-113">This component also calls the available callout functions during the [classification](basic-operation.md) process.</span></span> <span data-ttu-id="ba576-114">Обработчик фильтров содержит приблизительно 50 уровней фильтрации в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="ba576-114">The filter engine contains approximately 50 kernel-mode filtering layers.</span></span>

<span data-ttu-id="ba576-115">Описание каждого уровня механизма фильтрации см. в разделе [**Фильтрация идентификаторов слоев**](management-filtering-layer-identifiers-.md) .</span><span class="sxs-lookup"><span data-stu-id="ba576-115">See [**Filtering Layer Identifiers**](management-filtering-layer-identifiers-.md) for a description of each of the filter engine layers.</span></span>

## <a name="base-filtering-engine"></a><span data-ttu-id="ba576-116">Базовый модуль фильтрации</span><span class="sxs-lookup"><span data-stu-id="ba576-116">Base Filtering Engine</span></span>

<span data-ttu-id="ba576-117">Модуль базовой фильтрации (BFE) — это служба пользовательского режима (bfe.dll выполняется в процессе svchost.exe), которая координирует компоненты WFP.</span><span class="sxs-lookup"><span data-stu-id="ba576-117">The Base Filtering Engine (BFE) is a user-mode service (bfe.dll running in a svchost.exe process) that coordinates the WFP components.</span></span> <span data-ttu-id="ba576-118">Основные задачи, выполняемые BFE, — это добавление и удаление фильтров из системы, Хранение конфигурации фильтра и обеспечение безопасности конфигурации WFP.</span><span class="sxs-lookup"><span data-stu-id="ba576-118">The principal tasks performed by BFE are adding and removing filters from the system, storing filter configuration, and enforcing WFP configuration security.</span></span> <span data-ttu-id="ba576-119">Приложения взаимодействуют с BFE с помощью [функций управления WFP](fwp-mgmt-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ba576-119">Applications communicate with BFE through the [WFP management functions](fwp-mgmt-functions.md).</span></span>

## <a name="callout-drivers"></a><span data-ttu-id="ba576-120">Драйверы выноски</span><span class="sxs-lookup"><span data-stu-id="ba576-120">Callout Drivers</span></span>

<span data-ttu-id="ba576-121">Драйверы выноски предоставляют дополнительные функции фильтрации, добавляя пользовательские функции выноски в механизм фильтрации на одном или нескольких слоях фильтрации в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="ba576-121">Callout drivers provide additional filtering functionality by adding custom callout functions to the filter engine at one or more of the kernel-mode filtering layers.</span></span> <span data-ttu-id="ba576-122">Выноски поддерживают глубокую проверку и пакет, а также потоковую модификацию.</span><span class="sxs-lookup"><span data-stu-id="ba576-122">Callouts support deep inspection and packet as well as stream modification.</span></span> <span data-ttu-id="ba576-123">После того как драйвер выноски добавил свои функции-выноски в механизм фильтрации, в процесс фильтрации можно добавить фильтры, указывающие функцию выноски данного драйвера.</span><span class="sxs-lookup"><span data-stu-id="ba576-123">After a callout driver has added its callout functions to the filter engine, filters that specify a given driver's callout function can be added to the filtering process.</span></span> <span data-ttu-id="ba576-124">Такие фильтры могут быть добавлены как приложением управления пользовательским режимом, так и самим драйвером выноски.</span><span class="sxs-lookup"><span data-stu-id="ba576-124">Such filters can be added by either a user-mode management application or by the callout driver itself.</span></span> <span data-ttu-id="ba576-125">Интерфейс режима ядра, поставляемый в комплекте Windows Development Kit, должен использоваться только там, где это необходимо, а не как замена API пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="ba576-125">The kernel-mode interface, delivered in the Windows Development Kit, should only be used where needed and not as a substitute for the user-mode API.</span></span>

> [!Note]  
> <span data-ttu-id="ba576-126">Дополнительные сведения о драйверах выноски см. в разделе Windows Filtering Platform раздела [Windows Development Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).</span><span class="sxs-lookup"><span data-stu-id="ba576-126">For more information on callout drivers, see the Windows Filtering Platform section of the [Windows Development Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).</span></span>

 

<span data-ttu-id="ba576-127">Платформа фильтрации Windows включает ряд встроенных функций выноски, которые можно использовать для безопасного обмена данными IPsec, параметров фильтрации с отслеживанием состояния и фильтрации в скрытом режиме.</span><span class="sxs-lookup"><span data-stu-id="ba576-127">The Windows Filtering Platform includes a number of built-in callout functions that can be used for IPsec secure data communication, stateful filtering settings, and stealth-mode filtering.</span></span> <span data-ttu-id="ba576-128">Полный список встроенных функций выноски см. [**в разделе Встроенные идентификаторы выносок**](built-in-callout-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="ba576-128">See [**Built-in Callout Identifiers**](built-in-callout-identifiers.md) for a complete list of built-in callout functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba576-129">См. также</span><span class="sxs-lookup"><span data-stu-id="ba576-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba576-130">Объектная модель</span><span class="sxs-lookup"><span data-stu-id="ba576-130">Object Model</span></span>](object-model.md)
</dt> <dt>

[<span data-ttu-id="ba576-131">Операция WFP</span><span class="sxs-lookup"><span data-stu-id="ba576-131">WFP Operation</span></span>](basic-operation.md)
</dt> <dt>

[<span data-ttu-id="ba576-132">Драйверы для вызова платформы фильтрации Windows — руководство по проектированию</span><span class="sxs-lookup"><span data-stu-id="ba576-132">Windows Filtering Platform Callout Drivers - Design Guide</span></span>](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[<span data-ttu-id="ba576-133">Драйверы для вызова платформы фильтрации Windows — Справочник</span><span class="sxs-lookup"><span data-stu-id="ba576-133">Windows Filtering Platform Callout Drivers - Reference</span></span>](/windows-hardware/drivers/ddi/_netvista/)
</dt> </dl>

 

 