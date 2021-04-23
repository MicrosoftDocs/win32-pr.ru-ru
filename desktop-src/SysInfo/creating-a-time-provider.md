---
description: Поставщик времени реализуется в виде библиотеки DLL. Каждая библиотека DLL может поддерживать несколько поставщиков времени. Каждый поставщик отвечает за собственную конфигурацию и синхронизацию.
ms.assetid: 04f523d7-7e99-4bf5-941f-ae67f4b9df0a
title: Создание поставщика времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac5a12e19651d88c3328ac72280c486a54c4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664714"
---
# <a name="creating-a-time-provider"></a><span data-ttu-id="af381-105">Создание поставщика времени</span><span class="sxs-lookup"><span data-stu-id="af381-105">Creating a Time Provider</span></span>

<span data-ttu-id="af381-106">Поставщик времени реализуется в виде библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="af381-106">A time provider is implemented as a DLL.</span></span> <span data-ttu-id="af381-107">Каждая библиотека DLL может поддерживать несколько поставщиков времени.</span><span class="sxs-lookup"><span data-stu-id="af381-107">Each DLL can support multiple time providers.</span></span> <span data-ttu-id="af381-108">Каждый поставщик отвечает за собственную конфигурацию и синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="af381-108">Each provider is responsible for its own configuration and synchronization.</span></span>

<span data-ttu-id="af381-109">Поставщики времени должны реализовывать следующие функции обратного вызова:</span><span class="sxs-lookup"><span data-stu-id="af381-109">Time providers must implement the following callback functions:</span></span>

-   [<span data-ttu-id="af381-110">**тимепровклосе**</span><span class="sxs-lookup"><span data-stu-id="af381-110">**TimeProvClose**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)
-   [<span data-ttu-id="af381-111">**тимепровкомманд**</span><span class="sxs-lookup"><span data-stu-id="af381-111">**TimeProvCommand**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)
-   [<span data-ttu-id="af381-112">**тимепровопен**</span><span class="sxs-lookup"><span data-stu-id="af381-112">**TimeProvOpen**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)

<span data-ttu-id="af381-113">После загрузки библиотеки DLL поставщика Диспетчер поставщиков времени вызывает [**тимепровопен**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen), передавая имя поставщика и указатели на следующие функции:</span><span class="sxs-lookup"><span data-stu-id="af381-113">After it has loaded the provider DLL, the time provider manager calls [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen), passing the name of the provider and pointers to the following functions:</span></span>

-   [<span data-ttu-id="af381-114">**алертсамплесаваилфунк**</span><span class="sxs-lookup"><span data-stu-id="af381-114">**AlertSamplesAvailFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)
-   [<span data-ttu-id="af381-115">**жеттимесисинфофунк**</span><span class="sxs-lookup"><span data-stu-id="af381-115">**GetTimeSysInfoFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)
-   [<span data-ttu-id="af381-116">**логтимепровевентфунк**</span><span class="sxs-lookup"><span data-stu-id="af381-116">**LogTimeProvEventFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

<span data-ttu-id="af381-117">Эти функции предназначены для использования поставщиком времени.</span><span class="sxs-lookup"><span data-stu-id="af381-117">These functions are for use by the time provider.</span></span> <span data-ttu-id="af381-118">Поставщик времени использует [**тимепровопен**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) для возврата маркера поставщика, используемого диспетчером поставщиков времени при отправке команд поставщику времени.</span><span class="sxs-lookup"><span data-stu-id="af381-118">The time provider uses [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) to return a provider handle that the time provider manager uses when sending commands to the time provider.</span></span> <span data-ttu-id="af381-119">Значение Handle определяется поставщиком времени и используется в основном для различения разных поставщиков, реализованных в одной и той же библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="af381-119">The handle value is defined by the time provider and is used primarily to distinguish between different providers implemented in the same DLL.</span></span> <span data-ttu-id="af381-120">Поставщик времени может регистрировать важные события с помощью [**логтимепровевентфунк**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).</span><span class="sxs-lookup"><span data-stu-id="af381-120">The time provider can log significant events using [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).</span></span>

<span data-ttu-id="af381-121">Диспетчер поставщиков времени использует [**тимепровкомманд**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) для отправки команд поставщику времени.</span><span class="sxs-lookup"><span data-stu-id="af381-121">The time provider manager uses [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) to send commands to the time provider.</span></span> <span data-ttu-id="af381-122">Когда поставщику времени необходимо уведомить Диспетчер поставщиков времени о наличии доступных образцов времени, он вызывает [**алертсамплесаваилфунк**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc).</span><span class="sxs-lookup"><span data-stu-id="af381-122">When the time provider needs to notify the time provider manager that it has time samples available, it calls [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc).</span></span> <span data-ttu-id="af381-123">Затем Диспетчер поставщиков времени вызывает **тимепровкомманд** с помощью команды TPC \_ ресамплинг для получения образцов времени.</span><span class="sxs-lookup"><span data-stu-id="af381-123">The time provider manager then calls **TimeProvCommand** with the TPC\_GetSamples command to retrieve the time samples.</span></span> <span data-ttu-id="af381-124">Для запроса образца диспетчером поставщиков времени может потребоваться до 16 секунд.</span><span class="sxs-lookup"><span data-stu-id="af381-124">It can take up to 16 seconds for the time provider manager to request the sample.</span></span> <span data-ttu-id="af381-125">Поэтому приложение не должно ждать запроса.</span><span class="sxs-lookup"><span data-stu-id="af381-125">Therefore, the application should not wait for the request.</span></span>

<span data-ttu-id="af381-126">Чтобы обеспечить точность, поставщик времени должен получить все сведения, связанные со временем, с помощью [**жеттимесисинфофунк**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).</span><span class="sxs-lookup"><span data-stu-id="af381-126">To ensure accuracy, the time provider should retrieve all time-related information using [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).</span></span>

<span data-ttu-id="af381-127">Когда время завершения работы поставщика времени завершается, Диспетчер поставщиков времени вызывает [**тимепровклосе**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).</span><span class="sxs-lookup"><span data-stu-id="af381-127">When it is time to shut down the time provider, the time provider manager calls [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).</span></span>

 

 



