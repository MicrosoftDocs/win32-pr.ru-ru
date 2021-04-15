---
description: Транспорт Windows Sockets и Namespace&\# 8211; поставщики услуг — это библиотеки DLL с единой экспортированной точкой входа для функции инициализации поставщика услуг вспстартуп или нспстартуп соответственно.
ms.assetid: a3422513-92e2-4011-a756-04ed853e9d56
title: Модель интерфейса функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a500de391dd5f65da610ba79d33938443794262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701524"
---
# <a name="function-interface-model"></a><span data-ttu-id="e9e97-103">Модель интерфейса функции</span><span class="sxs-lookup"><span data-stu-id="e9e97-103">Function Interface Model</span></span>

<span data-ttu-id="e9e97-104">Транспорт Windows Sockets и пространство имен — поставщики служб — это библиотеки DLL с единой экспортированной точкой входа для функции инициализации поставщика услуг [**вспстартуп**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) или [**нспстартуп**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)соответственно.</span><span class="sxs-lookup"><span data-stu-id="e9e97-104">Windows Sockets transport and namespace–service providers are DLLs with a single exported procedure entry point for the service provider initialization function [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) or [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup), respectively.</span></span> <span data-ttu-id="e9e97-105">Все остальные функции поставщика услуг становятся доступными для \_32.dll Ws2 через таблицу диспетчеризации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="e9e97-105">All other service provider functions are made accessible to the Ws2\_32.dll through the service provider's dispatch table.</span></span> <span data-ttu-id="e9e97-106">Библиотеки DLL поставщика услуг загружаются в память Ws2 \_32.dll только при необходимости и выгружаются, когда их службы больше не требуются.</span><span class="sxs-lookup"><span data-stu-id="e9e97-106">Service provider DLL's are loaded into memory by the Ws2\_32.dll only when needed, and are unloaded when their services are no longer required.</span></span>

<span data-ttu-id="e9e97-107">Индекс SPI также определяет несколько обстоятельств, в которых поставщик услуг транспорта вызывает Ws2 \_32.dll (отозванные вызовы) для получения служб поддержки DLL.</span><span class="sxs-lookup"><span data-stu-id="e9e97-107">The SPI also defines several circumstances in which a transport service provider calls up into the Ws2\_32.dll (upcalls) to obtain DLL support services.</span></span> <span data-ttu-id="e9e97-108">Библиотека DLL поставщика транспортной службы получает32.dll Ws2ную \_ таблицу диспетчеризации, используя параметр *Упкаллтабле* для [**вспстартуп**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span><span class="sxs-lookup"><span data-stu-id="e9e97-108">The transport service provider DLL is given the Ws2\_32.dll's upcall dispatch table through the *UpcallTable* parameter to [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span></span>

<span data-ttu-id="e9e97-109">Расширение имени файла для поставщиков служб должно быть изменено с "DLL" на ". WSP "или". NSP ".</span><span class="sxs-lookup"><span data-stu-id="e9e97-109">Service providers should have their file name extension changed from "DLL" to ".WSP" or ".NSP".</span></span> <span data-ttu-id="e9e97-110">Это требование не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e9e97-110">This requirement is not strict.</span></span> <span data-ttu-id="e9e97-111">Поставщик услуг по-прежнему будет работать с \_32.dll Ws2 с любым расширением имени файла.</span><span class="sxs-lookup"><span data-stu-id="e9e97-111">A service provider will still operate with the Ws2\_32.dll with any file name extension.</span></span>

<span data-ttu-id="e9e97-112">В стандарте Winsock SPI используется следующее соглашение об именовании префикса функции:</span><span class="sxs-lookup"><span data-stu-id="e9e97-112">The Winsock SPI uses the following function prefix naming convention:</span></span>

| <span data-ttu-id="e9e97-113">Prefix</span><span class="sxs-lookup"><span data-stu-id="e9e97-113">Prefix</span></span> | <span data-ttu-id="e9e97-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e9e97-114">Meaning</span></span>                          | <span data-ttu-id="e9e97-115">Описание</span><span class="sxs-lookup"><span data-stu-id="e9e97-115">Description</span></span>                                       |
|--------|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="e9e97-116">WPS</span><span class="sxs-lookup"><span data-stu-id="e9e97-116">WSP</span></span>    | <span data-ttu-id="e9e97-117">Поставщик службы сокетов Windows</span><span class="sxs-lookup"><span data-stu-id="e9e97-117">Windows Sockets Service Provider</span></span> | <span data-ttu-id="e9e97-118">Точки входа поставщика услуг транспорта</span><span class="sxs-lookup"><span data-stu-id="e9e97-118">Transport service provider entry points</span></span>           |
| <span data-ttu-id="e9e97-119">впу</span><span class="sxs-lookup"><span data-stu-id="e9e97-119">WPU</span></span>    | <span data-ttu-id="e9e97-120">Вызов поставщика сокетов Windows</span><span class="sxs-lookup"><span data-stu-id="e9e97-120">Windows Sockets Provider Upcall</span></span>  | <span data-ttu-id="e9e97-121">Ws2 \_32.dll точки входа для поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="e9e97-121">Ws2\_32.dll entry points for service providers</span></span>    |
| <span data-ttu-id="e9e97-122">WSC</span><span class="sxs-lookup"><span data-stu-id="e9e97-122">WSC</span></span>    | <span data-ttu-id="e9e97-123">Конфигурация сокетов Windows</span><span class="sxs-lookup"><span data-stu-id="e9e97-123">Windows Sockets Configuration</span></span>    | <span data-ttu-id="e9e97-124">WS2 \_32.dll точки входа для приложений установки</span><span class="sxs-lookup"><span data-stu-id="e9e97-124">WS2\_32.dll entry points for installation applets</span></span> |
| <span data-ttu-id="e9e97-125">NSP</span><span class="sxs-lookup"><span data-stu-id="e9e97-125">NSP</span></span>    | <span data-ttu-id="e9e97-126">Поставщик пространства имен</span><span class="sxs-lookup"><span data-stu-id="e9e97-126">Namespace Provider</span></span>               | <span data-ttu-id="e9e97-127">Точки входа поставщика пространства имен</span><span class="sxs-lookup"><span data-stu-id="e9e97-127">Namespace provider entry points</span></span>                   |



 

<span data-ttu-id="e9e97-128">Как описано выше, эти точки входа не экспортируются (за исключением [**вспстартуп**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) и [**нспстартуп**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), но доступны через обмен таблицами диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="e9e97-128">As described above, these entry points are not exported (with the exception of [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) and [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), but are accessed through an exchange of dispatch tables.</span></span>

 

 



