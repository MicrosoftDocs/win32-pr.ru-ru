---
title: Функции (STG)
description: Функции — это подпрограммы или подпрограммы, возвращающие определенное значение или значения. В следующих разделах описаны структурированные функции хранения.
ms.assetid: 5fbb05ae-594d-4fa5-97d2-a2371e94c054
keywords:
- Структурированное хранилище Стрктд STG, Reference, functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f49c091b5ba9619b649e620da7b436ebac4ccb
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2021
ms.locfileid: "105669523"
---
# <a name="structured-storage-functions"></a><span data-ttu-id="354a5-105">Функции структурированного хранилища</span><span class="sxs-lookup"><span data-stu-id="354a5-105">Structured Storage functions</span></span>

<span data-ttu-id="354a5-106">Функции — это подпрограммы или подпрограммы, возвращающие определенное значение или значения.</span><span class="sxs-lookup"><span data-stu-id="354a5-106">Functions are routines or subroutines that return a specific value or values.</span></span> <span data-ttu-id="354a5-107">Функции структурированного хранилища описаны в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="354a5-107">Structured Storage functions are described in the following sections:</span></span>

-   [<span data-ttu-id="354a5-108">**креатеилоккбитесонхглобал**</span><span class="sxs-lookup"><span data-stu-id="354a5-108">**CreateILockBytesOnHGlobal**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-createilockbytesonhglobal)
-   [<span data-ttu-id="354a5-109">**CreateStreamOnHGlobal**</span><span class="sxs-lookup"><span data-stu-id="354a5-109">**CreateStreamOnHGlobal**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
-   [<span data-ttu-id="354a5-110">**фмтидтопропстгнаме**</span><span class="sxs-lookup"><span data-stu-id="354a5-110">**FmtIdToPropStgName**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-fmtidtopropstgname)
-   [<span data-ttu-id="354a5-111">**фрипропвариантаррай**</span><span class="sxs-lookup"><span data-stu-id="354a5-111">**FreePropVariantArray**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-freepropvariantarray)
-   [<span data-ttu-id="354a5-112">**жетконвертстг**</span><span class="sxs-lookup"><span data-stu-id="354a5-112">**GetConvertStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-getconvertstg)
-   [<span data-ttu-id="354a5-113">**жесглобалфромилоккбитес**</span><span class="sxs-lookup"><span data-stu-id="354a5-113">**GetHGlobalFromILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-gethglobalfromilockbytes)
-   [<span data-ttu-id="354a5-114">**жесглобалфромстреам**</span><span class="sxs-lookup"><span data-stu-id="354a5-114">**GetHGlobalFromStream**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-gethglobalfromstream)
-   [<span data-ttu-id="354a5-115">**олеконвертисторажетулестреам**</span><span class="sxs-lookup"><span data-stu-id="354a5-115">**OleConvertIStorageToOLESTREAM**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertistoragetoolestream)
-   [<span data-ttu-id="354a5-116">**олеконвертисторажетулестреамекс**</span><span class="sxs-lookup"><span data-stu-id="354a5-116">**OleConvertIStorageToOLESTREAMEx**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertistoragetoolestreamex)
-   [<span data-ttu-id="354a5-117">**олеконвертолестреамтоистораже**</span><span class="sxs-lookup"><span data-stu-id="354a5-117">**OleConvertOLESTREAMToIStorage**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertolestreamtoistorage)
-   [<span data-ttu-id="354a5-118">**олеконвертолестреамтоисторажеекс**</span><span class="sxs-lookup"><span data-stu-id="354a5-118">**OleConvertOLESTREAMToIStorageEx**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertolestreamtoistorageex)
-   [<span data-ttu-id="354a5-119">**пропстгнаметофмтид**</span><span class="sxs-lookup"><span data-stu-id="354a5-119">**PropStgNameToFmtId**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-propstgnametofmtid)
-   [<span data-ttu-id="354a5-120">**пропвариантклеар**</span><span class="sxs-lookup"><span data-stu-id="354a5-120">**PropVariantClear**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)
-   [<span data-ttu-id="354a5-121">**пропварианткопи**</span><span class="sxs-lookup"><span data-stu-id="354a5-121">**PropVariantCopy**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-propvariantcopy)
-   [<span data-ttu-id="354a5-122">**пропвариантинит**</span><span class="sxs-lookup"><span data-stu-id="354a5-122">**PropVariantInit**</span></span>](/windows/desktop/api/PropIdl/nf-propidl-propvariantinit)
-   [<span data-ttu-id="354a5-123">**реадклассстг**</span><span class="sxs-lookup"><span data-stu-id="354a5-123">**ReadClassStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-readclassstg)
-   [<span data-ttu-id="354a5-124">**реадклассстм**</span><span class="sxs-lookup"><span data-stu-id="354a5-124">**ReadClassStm**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-readclassstm)
-   [<span data-ttu-id="354a5-125">**реадфмтусертипестг**</span><span class="sxs-lookup"><span data-stu-id="354a5-125">**ReadFmtUserTypeStg**</span></span>](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg)
-   [<span data-ttu-id="354a5-126">**стгконвертпропертитовариант**</span><span class="sxs-lookup"><span data-stu-id="354a5-126">**StgConvertPropertyToVariant**</span></span>](/windows/desktop/api/Propidl/nf-propidl-stgconvertpropertytovariant)
-   [<span data-ttu-id="354a5-127">**сетконвертстг**</span><span class="sxs-lookup"><span data-stu-id="354a5-127">**SetConvertStg**</span></span>](/windows/desktop/api/Ole2/nf-ole2-setconvertstg)
-   [<span data-ttu-id="354a5-128">**стгконвертварианттопроперти**</span><span class="sxs-lookup"><span data-stu-id="354a5-128">**StgConvertVariantToProperty**</span></span>](/windows/desktop/api/Propidl/nf-propidl-stgconvertvarianttoproperty)
-   [<span data-ttu-id="354a5-129">**стгкреатедокфиле**</span><span class="sxs-lookup"><span data-stu-id="354a5-129">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
-   [<span data-ttu-id="354a5-130">**стгкреатедокфилеонилоккбитес**</span><span class="sxs-lookup"><span data-stu-id="354a5-130">**StgCreateDocfileOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
-   [<span data-ttu-id="354a5-131">**стгкреатепропсетстг**</span><span class="sxs-lookup"><span data-stu-id="354a5-131">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
-   [<span data-ttu-id="354a5-132">**стгкреатепропстг**</span><span class="sxs-lookup"><span data-stu-id="354a5-132">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
-   [<span data-ttu-id="354a5-133">**стгкреатесторажеекс**</span><span class="sxs-lookup"><span data-stu-id="354a5-133">**StgCreateStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
-   [<span data-ttu-id="354a5-134">**стгдесериализепропвариант**</span><span class="sxs-lookup"><span data-stu-id="354a5-134">**StgDeserializePropVariant**</span></span>](/windows/desktop/api/Propvarutil/nf-propvarutil-stgdeserializepropvariant)
-   [<span data-ttu-id="354a5-135">**стгжетифилллоккбитесонфиле**</span><span class="sxs-lookup"><span data-stu-id="354a5-135">**StgGetIFillLockBytesOnFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile)
-   [<span data-ttu-id="354a5-136">**стгжетифилллоккбитесонилоккбитес**</span><span class="sxs-lookup"><span data-stu-id="354a5-136">**StgGetIFillLockBytesOnILockBytes**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes)
-   [<span data-ttu-id="354a5-137">**стгиссторажефиле**</span><span class="sxs-lookup"><span data-stu-id="354a5-137">**StgIsStorageFile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile)
-   [<span data-ttu-id="354a5-138">**стгиссторажеилоккбитес**</span><span class="sxs-lookup"><span data-stu-id="354a5-138">**StgIsStorageILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgisstorageilockbytes)
-   [<span data-ttu-id="354a5-139">**стгопенасинкдокфилеонифилллоккбитес**</span><span class="sxs-lookup"><span data-stu-id="354a5-139">**StgOpenAsyncDocfileOnIFillLockBytes**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes)
-   [<span data-ttu-id="354a5-140">**стгопенлайаутдокфиле**</span><span class="sxs-lookup"><span data-stu-id="354a5-140">**StgOpenLayoutDocfile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stgopenlayoutdocfile)
-   [<span data-ttu-id="354a5-141">**стгопенпропстг**</span><span class="sxs-lookup"><span data-stu-id="354a5-141">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
-   [<span data-ttu-id="354a5-142">**стгопенстораже**</span><span class="sxs-lookup"><span data-stu-id="354a5-142">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
-   [<span data-ttu-id="354a5-143">**стгопенсторажеекс**</span><span class="sxs-lookup"><span data-stu-id="354a5-143">**StgOpenStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
-   [<span data-ttu-id="354a5-144">**стгопенсторажеонилоккбитес**</span><span class="sxs-lookup"><span data-stu-id="354a5-144">**StgOpenStorageOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
-   [<span data-ttu-id="354a5-145">**стгпропертиленгсасвариант**</span><span class="sxs-lookup"><span data-stu-id="354a5-145">**StgPropertyLengthAsVariant**</span></span>](/windows/desktop/api/Propapi/nf-propapi-stgpropertylengthasvariant)
-   [<span data-ttu-id="354a5-146">**стгсериализепропвариант**</span><span class="sxs-lookup"><span data-stu-id="354a5-146">**StgSerializePropVariant**</span></span>](/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant)
-   [<span data-ttu-id="354a5-147">**стгсеттимес**</span><span class="sxs-lookup"><span data-stu-id="354a5-147">**StgSetTimes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgsettimes)
-   [<span data-ttu-id="354a5-148">**вритеклассстг**</span><span class="sxs-lookup"><span data-stu-id="354a5-148">**WriteClassStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg)
-   [<span data-ttu-id="354a5-149">**вритеклассстм**</span><span class="sxs-lookup"><span data-stu-id="354a5-149">**WriteClassStm**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-writeclassstm)
-   [<span data-ttu-id="354a5-150">**вритефмтусертипестг**</span><span class="sxs-lookup"><span data-stu-id="354a5-150">**WriteFmtUserTypeStg**</span></span>](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg)

 

 
