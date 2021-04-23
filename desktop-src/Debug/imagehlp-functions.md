---
description: Ниже перечислены функции ImageHlp.
ms.assetid: 926f412e-25ba-4f9c-a118-b5a1bc723379
title: Функции ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e921707474f68e288f67e84dda9e361922bca0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990690"
---
# <a name="imagehlp-functions"></a><span data-ttu-id="57341-103">Функции ImageHlp</span><span class="sxs-lookup"><span data-stu-id="57341-103">ImageHlp Functions</span></span>

<span data-ttu-id="57341-104">Ниже перечислены функции ImageHlp.</span><span class="sxs-lookup"><span data-stu-id="57341-104">The following are the ImageHlp functions.</span></span>

## <a name="image-access"></a><span data-ttu-id="57341-105">Доступ к изображениям</span><span class="sxs-lookup"><span data-stu-id="57341-105">Image Access</span></span>

<span data-ttu-id="57341-106">Функции доступа к изображениям обращаются к данным в исполняемом образе.</span><span class="sxs-lookup"><span data-stu-id="57341-106">The image access functions access the data in an executable image.</span></span> <span data-ttu-id="57341-107">Функции предоставляют высокоуровневый доступ к основам образов и очень специфичный доступ к наиболее распространенным частям данных изображения.</span><span class="sxs-lookup"><span data-stu-id="57341-107">The functions provide high-level access to the base of images and very specific access to the most common parts of an image's data.</span></span>

<dl>

[<span data-ttu-id="57341-108">**жетимажеконфигинформатион**</span><span class="sxs-lookup"><span data-stu-id="57341-108">**GetImageConfigInformation**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-getimageconfiginformation)  
[<span data-ttu-id="57341-109">**жетимажеунуседхеадербитес**</span><span class="sxs-lookup"><span data-stu-id="57341-109">**GetImageUnusedHeaderBytes**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-getimageunusedheaderbytes)  
[<span data-ttu-id="57341-110">**Загрузить образ**</span><span class="sxs-lookup"><span data-stu-id="57341-110">**ImageLoad**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageload)  
[<span data-ttu-id="57341-111">**имажеунлоад**</span><span class="sxs-lookup"><span data-stu-id="57341-111">**ImageUnload**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageunload)  
[<span data-ttu-id="57341-112">**мапандлоад**</span><span class="sxs-lookup"><span data-stu-id="57341-112">**MapAndLoad**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-mapandload)  
[<span data-ttu-id="57341-113">**сетимажеконфигинформатион**</span><span class="sxs-lookup"><span data-stu-id="57341-113">**SetImageConfigInformation**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-setimageconfiginformation)  
[<span data-ttu-id="57341-114">**унмапандлоад**</span><span class="sxs-lookup"><span data-stu-id="57341-114">**UnMapAndLoad**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-unmapandload)  
</dl>

## <a name="image-integrity"></a><span data-ttu-id="57341-115">Целостность образа</span><span class="sxs-lookup"><span data-stu-id="57341-115">Image Integrity</span></span>

<span data-ttu-id="57341-116">Функции целостности изображений управляют набором сертификатов в файле образа.</span><span class="sxs-lookup"><span data-stu-id="57341-116">The image integrity functions manage the set of certificates in an image file.</span></span>

<dl>

[<span data-ttu-id="57341-117">**дижестфунктион**</span><span class="sxs-lookup"><span data-stu-id="57341-117">**DigestFunction**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)  
[<span data-ttu-id="57341-118">**имажеаддцертификате**</span><span class="sxs-lookup"><span data-stu-id="57341-118">**ImageAddCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)  
[<span data-ttu-id="57341-119">**имажеенумератецертификатес**</span><span class="sxs-lookup"><span data-stu-id="57341-119">**ImageEnumerateCertificates**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)  
[<span data-ttu-id="57341-120">**имажежетцертификатедата**</span><span class="sxs-lookup"><span data-stu-id="57341-120">**ImageGetCertificateData**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)  
[<span data-ttu-id="57341-121">**имажежетцертификатехеадер**</span><span class="sxs-lookup"><span data-stu-id="57341-121">**ImageGetCertificateHeader**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)  
[<span data-ttu-id="57341-122">**имажежетдижестстреам**</span><span class="sxs-lookup"><span data-stu-id="57341-122">**ImageGetDigestStream**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)  
[<span data-ttu-id="57341-123">**имажеремовецертификате**</span><span class="sxs-lookup"><span data-stu-id="57341-123">**ImageRemoveCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)  
</dl>

## <a name="image-modification"></a><span data-ttu-id="57341-124">Изменение изображения</span><span class="sxs-lookup"><span data-stu-id="57341-124">Image Modification</span></span>

<span data-ttu-id="57341-125">Функции изменения изображений позволяют изменять исполняемый образ.</span><span class="sxs-lookup"><span data-stu-id="57341-125">The image modification functions allow you to change the executable image.</span></span>

<dl>

[<span data-ttu-id="57341-126">**BindImage**</span><span class="sxs-lookup"><span data-stu-id="57341-126">**BindImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimage)  
[<span data-ttu-id="57341-127">**биндимажеекс**</span><span class="sxs-lookup"><span data-stu-id="57341-127">**BindImageEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimageex)  
[<span data-ttu-id="57341-128">**чекксуммаппедфиле**</span><span class="sxs-lookup"><span data-stu-id="57341-128">**CheckSumMappedFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-checksummappedfile)  
[<span data-ttu-id="57341-129">**мапфилеандчекксум**</span><span class="sxs-lookup"><span data-stu-id="57341-129">**MapFileAndCheckSum**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-mapfileandchecksuma)  
[<span data-ttu-id="57341-130">**ребасеимаже**</span><span class="sxs-lookup"><span data-stu-id="57341-130">**ReBaseImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage)  
[<span data-ttu-id="57341-131">**ReBaseImage64**</span><span class="sxs-lookup"><span data-stu-id="57341-131">**ReBaseImage64**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage64)  
[<span data-ttu-id="57341-132">**сплитсимболс**</span><span class="sxs-lookup"><span data-stu-id="57341-132">**SplitSymbols**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-splitsymbols)  
[<span data-ttu-id="57341-133">**статусраутине**</span><span class="sxs-lookup"><span data-stu-id="57341-133">**StatusRoutine**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-pimagehlp_status_routine)  
[<span data-ttu-id="57341-134">**таучфилетимес**</span><span class="sxs-lookup"><span data-stu-id="57341-134">**TouchFileTimes**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-touchfiletimes)  
[<span data-ttu-id="57341-135">**упдатедебугинфофиле**</span><span class="sxs-lookup"><span data-stu-id="57341-135">**UpdateDebugInfoFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofile)  
[<span data-ttu-id="57341-136">**упдатедебугинфофиликс**</span><span class="sxs-lookup"><span data-stu-id="57341-136">**UpdateDebugInfoFileEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofileex)  
</dl>

 

 



