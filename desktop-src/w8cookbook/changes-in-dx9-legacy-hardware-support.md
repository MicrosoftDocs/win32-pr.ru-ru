---
title: Изменения в поддержке устаревшего оборудования DX9
description: Изменения в поддержке устаревшего оборудования DX9
ms.assetid: 25C7DFC7-58F4-4F6D-8D26-6DBA92424A0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1ae5c4b15a2019450cc5b209f34561d8ec672d
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "105691682"
---
# <a name="changes-in-dx9-legacy-hardware-support"></a><span data-ttu-id="17f8b-103">Изменения в поддержке устаревшего оборудования DX9</span><span class="sxs-lookup"><span data-stu-id="17f8b-103">Changes in DX9 legacy hardware support</span></span>

## <a name="platform"></a><span data-ttu-id="17f8b-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="17f8b-104">Platform</span></span>

<span data-ttu-id="17f8b-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="17f8b-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="17f8b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="17f8b-106">Description</span></span>

<span data-ttu-id="17f8b-107">Intel и AMD и ATI больше не поддерживают свои DX9 графические компоненты и не будут обновлять драйверы для этих устройств для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="17f8b-107">Intel and AMD/ATI no longer support their DX9 graphics parts and will not be updating drivers for these devices for Windows 8.</span></span> <span data-ttu-id="17f8b-108">Кроме того, эти устройства не попадают в комплект для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="17f8b-108">Furthermore, these devices are not covered in-box for Windows 8.</span></span> <span data-ttu-id="17f8b-109">Последние драйверы для этих устройств доступны в WU и на веб-сайтах OEM/IHV. Многие даты из Vista и многие из этих драйверов окончательной версии демонстрируют проблемы в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="17f8b-109">The last drivers for these devices are those available on WU and on the OEM/IHV’s websites; many date from Vista, and many of these final version drivers exhibit problems on Windows 8.</span></span> <span data-ttu-id="17f8b-110">Кроме того, компания nVidia недавно объявила о том, что они не будут поддерживать DX9 (в Vista и более ранних версиях) мобильные (записные книжки) для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="17f8b-110">In addition, nVidia has recently stated that they will not support their DX9 (Vista and older) mobile (notebook) parts for Windows 8.</span></span> <span data-ttu-id="17f8b-111">Они продолжают поддерживать свои настольные DX9 части.</span><span class="sxs-lookup"><span data-stu-id="17f8b-111">They continue to support their desktop DX9 parts.</span></span>

<span data-ttu-id="17f8b-112">Все эти сочетания драйверов и частей находятся в списке резервного программного обеспечения Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="17f8b-112">All of these driver/part combinations are on the Internet Explorer 9 software fallback list.</span></span> <span data-ttu-id="17f8b-113">Это означает, что по соображениям производительности или стабильности Internet Explorer 9 использует программную отрисовку на этих устройствах.</span><span class="sxs-lookup"><span data-stu-id="17f8b-113">This means that for either performance or stability reasons, Internet Explorer 9 uses software rendering on these devices.</span></span> <span data-ttu-id="17f8b-114">Это хороший индикатор того, что опыт работы с приложениями Магазина Windows не будет удовлетворительным для этих драйверов и частей.</span><span class="sxs-lookup"><span data-stu-id="17f8b-114">This is a good indication that the experience with Windows Store apps will not be satisfactory on these drivers and parts.</span></span>

## <a name="manifestation"></a><span data-ttu-id="17f8b-115">Проявление</span><span class="sxs-lookup"><span data-stu-id="17f8b-115">Manifestation</span></span>

<span data-ttu-id="17f8b-116">Так как для этих устройств встроенная поддержка не предусмотрена, многие пользователи с этими частями будут запускаться с помощью встроенного драйвера Microsoft Basic.</span><span class="sxs-lookup"><span data-stu-id="17f8b-116">As there is no in-box support for these devices, many users with these parts will wind up running on the Microsoft Basic Display Driver.</span></span> <span data-ttu-id="17f8b-117">Это программный графический процессор 1,2 WDDM, основанный на деформации, и на самом деле быстрее, чем некоторые части этого класса, например серии Intel GMA500.</span><span class="sxs-lookup"><span data-stu-id="17f8b-117">This is a WARP-based WDDM 1.2 software GPU, and is actually faster than some of the parts in this class, for example, the Intel GMA500 series).</span></span> <span data-ttu-id="17f8b-118">Он поддерживает Aero-стекло и DWM, а также может запускать приложения для Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="17f8b-118">It supports aero-glass and DWM, and can run Windows Store apps.</span></span>

<span data-ttu-id="17f8b-119">Однако у него есть ряд важных ограничений.</span><span class="sxs-lookup"><span data-stu-id="17f8b-119">However, it has some important limitations:</span></span>

-   <span data-ttu-id="17f8b-120">Он не поддерживает несколько мониторов и проекций.</span><span class="sxs-lookup"><span data-stu-id="17f8b-120">It doesn’t support multiple monitors or projection</span></span>
-   <span data-ttu-id="17f8b-121">Он не поддерживает спящий режим, хотя поддерживает спящий режим</span><span class="sxs-lookup"><span data-stu-id="17f8b-121">It doesn’t support sleep, though it does support hibernation</span></span>
-   <span data-ttu-id="17f8b-122">Обычно это не позволит изменить разрешение экрана.</span><span class="sxs-lookup"><span data-stu-id="17f8b-122">It often will not allow changing screen resolution</span></span>

## <a name="mitigation"></a><span data-ttu-id="17f8b-123">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="17f8b-123">Mitigation</span></span>

<span data-ttu-id="17f8b-124">Если после тестирования вы обнаружите, что взаимодействие с пользователем неприемлемо, вы можете настроить требования к оборудованию для своих продуктов, исключающих эти старые DX9 Intel и AMD.</span><span class="sxs-lookup"><span data-stu-id="17f8b-124">If after testing, you find that the user experience is not acceptable, you may choose to set hardware requirements for their products that exclude these older DX9 Intel and AMD parts.</span></span> <span data-ttu-id="17f8b-125">Вы также можете предупредить клиентов о том, что они могут иметь неприемлемый опыт работы с этими частями.</span><span class="sxs-lookup"><span data-stu-id="17f8b-125">You may also choose to alert your customers that they may have an unacceptable experience on these parts.</span></span>

## <a name="tests"></a><span data-ttu-id="17f8b-126">Тесты</span><span class="sxs-lookup"><span data-stu-id="17f8b-126">Tests</span></span>

<span data-ttu-id="17f8b-127">Оцените производительность и эффективность работы этих устройств:</span><span class="sxs-lookup"><span data-stu-id="17f8b-127">Evaluate the performance and experience on these devices:</span></span>

-   <span data-ttu-id="17f8b-128">Каковы такие возможности, как в последней доступной версии драйвера?</span><span class="sxs-lookup"><span data-stu-id="17f8b-128">What is the experience like on the final driver version available?</span></span>
-   <span data-ttu-id="17f8b-129">Каковы такие возможности, как в МСБДД?</span><span class="sxs-lookup"><span data-stu-id="17f8b-129">What is the experience like on the MSBDD?</span></span>

 

 




