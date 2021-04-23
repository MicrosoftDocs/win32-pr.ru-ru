---
title: Справочник по устанавливаемому драйверу
description: Справочник по устанавливаемому драйверу
ms.assetid: 869b92f1-2711-4198-9911-3df1ebc58d5f
keywords:
- Windows мультимедиа, ссылка на устанавливаемый драйвер
- Руководство по мультимедиа, устанавливаемому драйверу
- устанавливаемые драйверы, Справочник
- Справочник по устанавливаемому драйверу, сведения
- Справочник по устанавливаемым драйверам, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90475063f9d9211e841902fe73d2f09dc6130d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890496"
---
# <a name="installable-driver-reference"></a><span data-ttu-id="41bf5-108">Справочник по устанавливаемому драйверу</span><span class="sxs-lookup"><span data-stu-id="41bf5-108">Installable Driver Reference</span></span>

<span data-ttu-id="41bf5-109">Функции и сообщения, связанные с устанавливаемыми драйверами, группируются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="41bf5-109">The functions and messages associated with installable drivers are grouped as follows.</span></span>

## <a name="loading-and-unloading-drivers"></a><span data-ttu-id="41bf5-110">Загрузка и выгрузка драйверов</span><span class="sxs-lookup"><span data-stu-id="41bf5-110">Loading and Unloading Drivers</span></span>

-   [<span data-ttu-id="41bf5-111">жетдривермодулехандле</span><span class="sxs-lookup"><span data-stu-id="41bf5-111">GetDriverModuleHandle</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)
-   [<span data-ttu-id="41bf5-112">опендривер</span><span class="sxs-lookup"><span data-stu-id="41bf5-112">OpenDriver</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver)
-   [<span data-ttu-id="41bf5-113">сенддривермессаже</span><span class="sxs-lookup"><span data-stu-id="41bf5-113">SendDriverMessage</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage)

## <a name="closedriver"></a><span data-ttu-id="41bf5-114">клоседривер</span><span class="sxs-lookup"><span data-stu-id="41bf5-114">CloseDriver</span></span>

-   [<span data-ttu-id="41bf5-115">**DRV, \_ закрытие**</span><span class="sxs-lookup"><span data-stu-id="41bf5-115">**DRV\_CLOSE**</span></span>](drv-close.md)
-   [<span data-ttu-id="41bf5-116">**\_Отключение DRV**</span><span class="sxs-lookup"><span data-stu-id="41bf5-116">**DRV\_DISABLE**</span></span>](drv-disable.md)
-   [<span data-ttu-id="41bf5-117">**\_параметр DRV Enable**</span><span class="sxs-lookup"><span data-stu-id="41bf5-117">**DRV\_ENABLE**</span></span>](drv-enable.md)
-   [<span data-ttu-id="41bf5-118">**DRV \_ Free**</span><span class="sxs-lookup"><span data-stu-id="41bf5-118">**DRV\_FREE**</span></span>](drv-free.md)
-   [<span data-ttu-id="41bf5-119">**\_Загрузка DRV**</span><span class="sxs-lookup"><span data-stu-id="41bf5-119">**DRV\_LOAD**</span></span>](drv-load.md)
-   [<span data-ttu-id="41bf5-120">**DRV — \_ открытый**</span><span class="sxs-lookup"><span data-stu-id="41bf5-120">**DRV\_OPEN**</span></span>](drv-open.md)

## <a name="configuring-a-driver"></a><span data-ttu-id="41bf5-121">Настройка драйвера</span><span class="sxs-lookup"><span data-stu-id="41bf5-121">Configuring a Driver</span></span>

-   [<span data-ttu-id="41bf5-122">**DRV \_ Настройка**</span><span class="sxs-lookup"><span data-stu-id="41bf5-122">**DRV\_CONFIGURE**</span></span>](drv-configure.md)
-   [<span data-ttu-id="41bf5-123">**DRV \_ куериконфигуре**</span><span class="sxs-lookup"><span data-stu-id="41bf5-123">**DRV\_QUERYCONFIGURE**</span></span>](drv-queryconfigure.md)
-   [<span data-ttu-id="41bf5-124">**дрвконфигинфо**</span><span class="sxs-lookup"><span data-stu-id="41bf5-124">**DRVCONFIGINFO**</span></span>](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)

## <a name="installing-a-driver"></a><span data-ttu-id="41bf5-125">Установка драйвера</span><span class="sxs-lookup"><span data-stu-id="41bf5-125">Installing a Driver</span></span>

-   [<span data-ttu-id="41bf5-126">**\_Установка DRV**</span><span class="sxs-lookup"><span data-stu-id="41bf5-126">**DRV\_INSTALL**</span></span>](drv-install.md)
-   [<span data-ttu-id="41bf5-127">**\_Удаление DRV**</span><span class="sxs-lookup"><span data-stu-id="41bf5-127">**DRV\_REMOVE**</span></span>](drv-remove.md)

## <a name="driver-functions"></a><span data-ttu-id="41bf5-128">Функции драйвера</span><span class="sxs-lookup"><span data-stu-id="41bf5-128">Driver Functions</span></span>

-   [<span data-ttu-id="41bf5-129">дефдриверпрок</span><span class="sxs-lookup"><span data-stu-id="41bf5-129">DefDriverProc</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc)
-   [<span data-ttu-id="41bf5-130">дриверкаллбакк</span><span class="sxs-lookup"><span data-stu-id="41bf5-130">DriverCallback</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback)
-   [<span data-ttu-id="41bf5-131">дриверпрок</span><span class="sxs-lookup"><span data-stu-id="41bf5-131">DriverProc</span></span>](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc)

## <a name="related-topics"></a><span data-ttu-id="41bf5-132">См. также</span><span class="sxs-lookup"><span data-stu-id="41bf5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41bf5-133">Устанавливаемые драйверы</span><span class="sxs-lookup"><span data-stu-id="41bf5-133">Installable Drivers</span></span>](installable-drivers.md)
</dt> </dl>

 

 