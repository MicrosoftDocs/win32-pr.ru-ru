---
description: Функции изменения изображений позволяют изменять исполняемый образ.
ms.assetid: 195959cb-e1ab-4c76-b7f9-f20522feac8c
title: Функции изменения изображений ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f6be83457738d1237865940463f438d3b73afa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807072"
---
# <a name="imagehlp-image-modification-functions"></a><span data-ttu-id="4e2d0-103">Функции изменения изображений ImageHlp</span><span class="sxs-lookup"><span data-stu-id="4e2d0-103">ImageHlp Image Modification Functions</span></span>

<span data-ttu-id="4e2d0-104">Функции изменения изображений позволяют изменять исполняемый образ.</span><span class="sxs-lookup"><span data-stu-id="4e2d0-104">The image modification functions allow you to change the executable image.</span></span> <span data-ttu-id="4e2d0-105">Они преимущественно используются средствами разработки и устанавливают программы.</span><span class="sxs-lookup"><span data-stu-id="4e2d0-105">They are mostly for use by development tools and install programs.</span></span> <span data-ttu-id="4e2d0-106">Они могут использоваться для привязки образа, вычисления его контрольной суммы (что важно для обеспечения целостности образа), изменения адреса загрузки и создания файлов символов.</span><span class="sxs-lookup"><span data-stu-id="4e2d0-106">They can be used to bind an image, compute its checksum (which is important for ensuring image integrity), change its load address, and produce symbol files.</span></span>

<span data-ttu-id="4e2d0-107">Ниже приведены функции изменения изображений.</span><span class="sxs-lookup"><span data-stu-id="4e2d0-107">The following are the image modification functions.</span></span>

-   [<span data-ttu-id="4e2d0-108">**BindImage**</span><span class="sxs-lookup"><span data-stu-id="4e2d0-108">**BindImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimage)
-   [<span data-ttu-id="4e2d0-109">**биндимажеекс**</span><span class="sxs-lookup"><span data-stu-id="4e2d0-109">**BindImageEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimageex)
-   [<span data-ttu-id="4e2d0-110">**чекксуммаппедфиле**</span><span class="sxs-lookup"><span data-stu-id="4e2d0-110">**CheckSumMappedFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-checksummappedfile)
-   [<span data-ttu-id="4e2d0-111">**мапфилеандчекксум**</span><span class="sxs-lookup"><span data-stu-id="4e2d0-111">**MapFileAndCheckSum**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-mapfileandchecksuma)
-   [<span data-ttu-id="4e2d0-112">**ребасеимаже**</span><span class="sxs-lookup"><span data-stu-id="4e2d0-112">**ReBaseImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage)
-   [<span data-ttu-id="4e2d0-113">**сплитсимболс**</span><span class="sxs-lookup"><span data-stu-id="4e2d0-113">**SplitSymbols**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-splitsymbols)
-   [<span data-ttu-id="4e2d0-114">**статусраутине**</span><span class="sxs-lookup"><span data-stu-id="4e2d0-114">**StatusRoutine**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-pimagehlp_status_routine)
-   [<span data-ttu-id="4e2d0-115">**таучфилетимес**</span><span class="sxs-lookup"><span data-stu-id="4e2d0-115">**TouchFileTimes**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-touchfiletimes)
-   [<span data-ttu-id="4e2d0-116">**упдатедебугинфофиле**</span><span class="sxs-lookup"><span data-stu-id="4e2d0-116">**UpdateDebugInfoFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofile)
-   [<span data-ttu-id="4e2d0-117">**упдатедебугинфофиликс**</span><span class="sxs-lookup"><span data-stu-id="4e2d0-117">**UpdateDebugInfoFileEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofileex)

 

 



