---
description: Сетевой монитор захватывает сетевой трафик для просмотра и анализа. Она позволяет выполнять такие задачи, как анализ ранее перехваченных данных в пользовательских методах и извлечение данных из определенных парсеров протоколов.
ms.assetid: a70b6e22-e744-4760-b878-9ee35428fed5
title: Сетевой монитор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51a57dd2373d7a10fedd68a72dbc4021efdb921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546351"
---
# <a name="network-monitor"></a><span data-ttu-id="e688c-104">Сетевой монитор</span><span class="sxs-lookup"><span data-stu-id="e688c-104">Network Monitor</span></span>

## <a name="purpose"></a><span data-ttu-id="e688c-105">Назначение</span><span class="sxs-lookup"><span data-stu-id="e688c-105">Purpose</span></span>

<span data-ttu-id="e688c-106">Сетевой монитор захватывает сетевой трафик для просмотра и анализа.</span><span class="sxs-lookup"><span data-stu-id="e688c-106">Network Monitor captures network traffic for display and analysis.</span></span> <span data-ttu-id="e688c-107">Она позволяет выполнять такие задачи, как анализ ранее перехваченных данных в пользовательских методах и извлечение данных из определенных парсеров протоколов.</span><span class="sxs-lookup"><span data-stu-id="e688c-107">It enables you to perform tasks such as analyzing previously captured data in user-defined methods and extract data from defined protocol parsers.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e688c-108">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="e688c-108">Developer audience</span></span>

<span data-ttu-id="e688c-109">Доступ ко всем наборам API, предоставленным сетевой монитор, можно получить с помощью C/C++.</span><span class="sxs-lookup"><span data-stu-id="e688c-109">All API sets provided by Network Monitor can be accessed using C/C++.</span></span> <span data-ttu-id="e688c-110">Разработчики, работающие также с [*поставщиками сетевых пакетов*](n.md) , также должны быть знакомы с COM.</span><span class="sxs-lookup"><span data-stu-id="e688c-110">Those developers also working with [*network packet providers*](n.md) must also be familiar with COM.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e688c-111">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="e688c-111">Run-time requirements</span></span>

<span data-ttu-id="e688c-112">Чтобы вызвать из API сетевой монитор, необходимо работать на Windows NT Server 4,0, Windows 2000 Server или Windows Server 2003 или установить сервер Microsoft Systems Management Server.</span><span class="sxs-lookup"><span data-stu-id="e688c-112">To call from the Network Monitor API, you must be running on Windows NT Server 4.0, Windows 2000 Server, or Windows Server 2003, or have Microsoft Systems Management Server installed.</span></span>

<span data-ttu-id="e688c-113">Драйвер НПП и поддерживаемые функции включают все версии Windows NT 4,0 и Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e688c-113">The NPP driver and supported features include all versions of Windows NT 4.0 and Windows 2000 Server.</span></span>

> [!Note]  
> <span data-ttu-id="e688c-114">Сетевой монитор 2,1 и более ранних версий не поддерживаются в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="e688c-114">Network Monitor 2.1 and earlier are not supported on Windows Vista and later.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="e688c-115">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="e688c-115">In this section</span></span>



| <span data-ttu-id="e688c-116">Раздел</span><span class="sxs-lookup"><span data-stu-id="e688c-116">Topic</span></span>                                                                 | <span data-ttu-id="e688c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e688c-117">Description</span></span>                                                                                           |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e688c-118">Пакет SDK для сетевой монитор</span><span class="sxs-lookup"><span data-stu-id="e688c-118">The Network Monitor SDK</span></span>](the-network-monitor-sdk.md)<br/>     | <span data-ttu-id="e688c-119">Введение в пакет SDK для сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="e688c-119">Introduction to the Network Monitor SDK.</span></span><br/>                                                   |
| [<span data-ttu-id="e688c-120">Сведения о сетевой монитор 2,1</span><span class="sxs-lookup"><span data-stu-id="e688c-120">About Network Monitor 2.1</span></span>](about-network-monitor-2-1.md)<br/> | <span data-ttu-id="e688c-121">Сетевой монитор концепции и службы.</span><span class="sxs-lookup"><span data-stu-id="e688c-121">Network Monitor concepts and services.</span></span><br/>                                                     |
| [<span data-ttu-id="e688c-122">Использование сетевой монитор 2,1</span><span class="sxs-lookup"><span data-stu-id="e688c-122">Using Network Monitor 2.1</span></span>](using-network-monitor-2-1.md)<br/> | <span data-ttu-id="e688c-123">Разделы, связанные с задачами, в которых описывается использование функций сетевой монитор и COM-компонентов.</span><span class="sxs-lookup"><span data-stu-id="e688c-123">Task-related topics that describe how to use Network Monitor functions and COM components.</span></span><br/> |
| [<span data-ttu-id="e688c-124">Ссылки</span><span class="sxs-lookup"><span data-stu-id="e688c-124">Reference</span></span>](reference.md)<br/>                                 | <span data-ttu-id="e688c-125">Справочные разделы по сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="e688c-125">Reference topics for Network Monitor.</span></span><br/>                                                      |
| [<span data-ttu-id="e688c-126">Словарь терминов</span><span class="sxs-lookup"><span data-stu-id="e688c-126">Glossary</span></span>](glossary.md)<br/>                                   | <span data-ttu-id="e688c-127">Определения и терминология для сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="e688c-127">Definitions and terminology for Network Monitor.</span></span><br/>                                           |



 

 

 




