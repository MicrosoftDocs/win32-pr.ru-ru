---
description: Компонент ETYPE/SAP фильтра записи уведомляет драйвер сетевой монитор о том, чтобы принимать кадры, имеющие определенное сочетание ETYPE и точек доступа к службам (SAPs).
ms.assetid: 57dcf1cd-f27f-4bd3-a5a8-9e978a2d213e
title: Создание части фильтра ETYPE или SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b072d123ca18d3aa2b3f2c91db4a8461473a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999101"
---
# <a name="writing-etypesap-filter-portion"></a><span data-ttu-id="da3bc-103">Создание части фильтра ETYPE или SAP</span><span class="sxs-lookup"><span data-stu-id="da3bc-103">Writing Etype/SAP Filter Portion</span></span>

<span data-ttu-id="da3bc-104">Компонент ETYPE/SAP фильтра записи уведомляет драйвер сетевой монитор о том, чтобы принимать кадры, имеющие определенное сочетание ETYPE и [*точек доступа к службам*](s.md) (SAPS).</span><span class="sxs-lookup"><span data-stu-id="da3bc-104">The Etype/SAP portion of the capture filter notifies the Network Monitor driver to accept frames that have a specific combination of Etypes and [*service access points*](s.md) (SAPs).</span></span> <span data-ttu-id="da3bc-105">ETYPE и SAPs — это оба способа, с которыми следуют протоколы низкого уровня, такие как Ethernet, LLC и Snap.</span><span class="sxs-lookup"><span data-stu-id="da3bc-105">Etypes and SAPs are both ways that low-level protocols such as Ethernet, LLC, and Snap indicate which protocol follows them.</span></span> <span data-ttu-id="da3bc-106">В частности, внесены следующие изменения.</span><span class="sxs-lookup"><span data-stu-id="da3bc-106">Specifically:</span></span>

-   <span data-ttu-id="da3bc-107">Ethernet указывает ETYPE</span><span class="sxs-lookup"><span data-stu-id="da3bc-107">Ethernet specifies an Etype</span></span>
-   <span data-ttu-id="da3bc-108">LLC указывает SAP</span><span class="sxs-lookup"><span data-stu-id="da3bc-108">LLC specifies a SAP</span></span>
-   <span data-ttu-id="da3bc-109">Привязка указывает ETYPE</span><span class="sxs-lookup"><span data-stu-id="da3bc-109">Snap specifies an Etype</span></span>

## <a name="etypesap-capture-filter-flags"></a><span data-ttu-id="da3bc-110">Флаги фильтра захвата ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="da3bc-110">Etype/SAP Capture Filter Flags</span></span>

<span data-ttu-id="da3bc-111">Используйте следующие сведения для установки флагов в элементе **филтерфлагс** структуры [**каптурефилтер**](capturefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="da3bc-111">Use the following information to set the flags in the **FilterFlags** member of the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span>



| <span data-ttu-id="da3bc-112">Flag</span><span class="sxs-lookup"><span data-stu-id="da3bc-112">Flag</span></span>                                         | <span data-ttu-id="da3bc-113">Значение</span><span class="sxs-lookup"><span data-stu-id="da3bc-113">Meaning</span></span>                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da3bc-114">\_Флаги каптурефилтер \_ включают \_ все \_ SAPS</span><span class="sxs-lookup"><span data-stu-id="da3bc-114">CAPTUREFILTER\_ FLAGS\_INCLUDE\_ ALL\_SAPS</span></span>   | <span data-ttu-id="da3bc-115">Передает все значения SAP и уведомляет драйвер о том, что все значения SAP являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="da3bc-115">Passes all SAP values and notifies the driver that all SAP values are valid.</span></span> <span data-ttu-id="da3bc-116">Если в сочетании с любыми значениями в элементе **лпсаптабле** , этот флаг уведомляет драйвер о том, что все значения SAP, кроме указанных в **лпсаптабле** , являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="da3bc-116">If combined with any values in the **lpSapTable** member, this flag notifies the driver that all SAP values except those in the **lpSapTable** are valid.</span></span><br/>           |
| <span data-ttu-id="da3bc-117">\_Флаги каптурефилтер \_ включают \_ все \_ ETYPE</span><span class="sxs-lookup"><span data-stu-id="da3bc-117">CAPTUREFILTER\_ FLAGS\_INCLUDE\_ ALL\_ETYPES</span></span> | <span data-ttu-id="da3bc-118">Передает все значения ETYPE и уведомляет драйвер о том, что все значения ETYPE допустимы.</span><span class="sxs-lookup"><span data-stu-id="da3bc-118">Passes all Etype values and notifies the driver that all Etype values are valid.</span></span> <span data-ttu-id="da3bc-119">Если в сочетании с любыми значениями в элементе **лпетипетабле** , этот флаг уведомляет драйвер о том, что все значения ETYPE, кроме значений в **лпетипетабле** , являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="da3bc-119">If combined with any values in the **lpEtypeTable** member, this flag notifies the driver that all Etype values except those in the **lpEtypeTable** are valid.</span></span><br/> |
| <span data-ttu-id="da3bc-120">КАПТУРЕФИЛТЕР \_ \_ только локальные флаги \_</span><span class="sxs-lookup"><span data-stu-id="da3bc-120">CAPTUREFILTER\_ FLAGS\_LOCAL\_ONLY</span></span>           | <span data-ttu-id="da3bc-121">Установка этого флага не приведет к установке сетевого адаптера в P-Mode.</span><span class="sxs-lookup"><span data-stu-id="da3bc-121">Setting this flag will not set a NIC to P-Mode.</span></span> <span data-ttu-id="da3bc-122">Вы увидите только локальный трафик (все кадры на локальном компьютере).</span><span class="sxs-lookup"><span data-stu-id="da3bc-122">You will only see local traffic (any frames to the local machine).</span></span>                                                                                                                                          |
| <span data-ttu-id="da3bc-123">\_Флаги каптурефилтер \_ сохраняют \_ необработанные</span><span class="sxs-lookup"><span data-stu-id="da3bc-123">CAPTUREFILTER\_ FLAGS\_KEEP\_RAW</span></span>             | <span data-ttu-id="da3bc-124">Сохраняет кадры MAC SMT и Token Ring.</span><span class="sxs-lookup"><span data-stu-id="da3bc-124">Keeps SMT and Token Ring MAC frames.</span></span>                                                                                                                                                                                                                        |



 

## <a name="etypesap-capture-filter-settings"></a><span data-ttu-id="da3bc-125">Параметры фильтра захвата ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="da3bc-125">Etype/SAP Capture Filter Settings</span></span>

<span data-ttu-id="da3bc-126">Используйте следующие сведения, чтобы задать элементы **лпсаптабле** и **лпетипетабле** структуры [**каптурефилтер**](capturefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="da3bc-126">Use the following information to set the **lpSapTable** and **lpEtypeTable** members of the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span>



| <span data-ttu-id="da3bc-127">Параметр</span><span class="sxs-lookup"><span data-stu-id="da3bc-127">Setting</span></span>          | <span data-ttu-id="da3bc-128">Значение</span><span class="sxs-lookup"><span data-stu-id="da3bc-128">Meaning</span></span>                                                                                                                                                                                                                                                              |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da3bc-129">**лпсаптабле**</span><span class="sxs-lookup"><span data-stu-id="da3bc-129">**lpSapTable**</span></span>   | <span data-ttu-id="da3bc-130">Список значений SAP, которые должен передать драйвер.</span><span class="sxs-lookup"><span data-stu-id="da3bc-130">Lists the SAP values that you want the driver to pass.</span></span> <span data-ttu-id="da3bc-131">Этот список указывает драйверу сетевой монитор проверить любой кадр, содержащий совпадение.</span><span class="sxs-lookup"><span data-stu-id="da3bc-131">This list tells the Network Monitor driver to validate any frame that contains a match.</span></span> <span data-ttu-id="da3bc-132">Если \_ Флаги \_ каптурефилтер \_ включают \_ параметр ALL SAPS, то он становится списком исключений (если он найден, не Pass).</span><span class="sxs-lookup"><span data-stu-id="da3bc-132">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS is set, this becomes an exception list (if found, do not pass).</span></span>           |
| <span data-ttu-id="da3bc-133">**лпетипетабле**</span><span class="sxs-lookup"><span data-stu-id="da3bc-133">**lpEtypeTable**</span></span> | <span data-ttu-id="da3bc-134">Список значений ETYPE, которые должен передать драйвер сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="da3bc-134">Lists the Etype values that you want the Network Monitor driver to pass.</span></span> <span data-ttu-id="da3bc-135">Этот список только сообщает драйверу о необходимости проверки любого кадра, содержащего совпадение.</span><span class="sxs-lookup"><span data-stu-id="da3bc-135">This list alone tells the driver to validate any frame that contains a match.</span></span> <span data-ttu-id="da3bc-136">Если \_ установлены флаги каптурефилтер \_ \_ \_ , то он становится списком исключений (если он найден, не Pass).</span><span class="sxs-lookup"><span data-stu-id="da3bc-136">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES is set, this becomes an exception list (if found, do not pass).</span></span> |



 

 

 




