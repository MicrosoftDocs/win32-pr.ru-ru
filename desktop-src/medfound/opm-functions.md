---
description: В выходных данных диспетчера защиты (ОПМ) используются следующие функции.
ms.assetid: 7ecde6ae-56fd-451b-bebb-224c6801be05
title: Функции ОПМ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b4ef210ace3f7f179b59980cedb962a5bee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711438"
---
# <a name="opm-functions"></a><span data-ttu-id="d7c8c-103">Функции ОПМ</span><span class="sxs-lookup"><span data-stu-id="d7c8c-103">OPM Functions</span></span>

<span data-ttu-id="d7c8c-104">В [выходных данных диспетчера защиты](output-protection-manager.md) (ОПМ) используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="d7c8c-104">The following functions are used with [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>



| <span data-ttu-id="d7c8c-105">Функция</span><span class="sxs-lookup"><span data-stu-id="d7c8c-105">Function</span></span>                                                                                             | <span data-ttu-id="d7c8c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d7c8c-106">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7c8c-107">**опмжетвидеуутпутфортаржет**</span><span class="sxs-lookup"><span data-stu-id="d7c8c-107">**OPMGetVideoOutputForTarget**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputfortarget)                                     | <span data-ttu-id="d7c8c-108">Возвращает объект вывода видео для целевого объекта VidPN на указанном адаптере.</span><span class="sxs-lookup"><span data-stu-id="d7c8c-108">Returns a video output object for the VidPN target on the specified adapter.</span></span>                                                          |
| [<span data-ttu-id="d7c8c-109">**опмжетвидеуутпутсфромхмонитор**</span><span class="sxs-lookup"><span data-stu-id="d7c8c-109">**OPMGetVideoOutputsFromHMONITOR**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)                             | <span data-ttu-id="d7c8c-110">Создает объект диспетчера выходной защиты (ОПМ) для каждого физического монитора, связанного с определенным маркером **хмонитор** .</span><span class="sxs-lookup"><span data-stu-id="d7c8c-110">Creates an Output Protection Manager (OPM) object for each physical monitor that is associated with a particular **HMONITOR** handle.</span></span> |
| [<span data-ttu-id="d7c8c-111">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span><span class="sxs-lookup"><span data-stu-id="d7c8c-111">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) | <span data-ttu-id="d7c8c-112">Создает объект ОПМ для каждого физического монитора, связанного с определенным устройством Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d7c8c-112">Creates an OPM object for each physical monitor that is associated with a particular Direct3D device.</span></span>                                 |



 

<span data-ttu-id="d7c8c-113">Для доступа к функциям в драйвере экрана используются следующие функции ОПМ.</span><span class="sxs-lookup"><span data-stu-id="d7c8c-113">The following functions are used by OPM to access functionality in the display driver.</span></span> <span data-ttu-id="d7c8c-114">Приложения не должны вызывать эти функции.</span><span class="sxs-lookup"><span data-stu-id="d7c8c-114">Applications should not call these functions.</span></span>

-   [<span data-ttu-id="d7c8c-115">**конфигуреопмпротектедаутпут**</span><span class="sxs-lookup"><span data-stu-id="d7c8c-115">**ConfigureOPMProtectedOutput**</span></span>](configureopmprotectedoutput.md)
-   [<span data-ttu-id="d7c8c-116">**креатеопмпротектедаутпутс**</span><span class="sxs-lookup"><span data-stu-id="d7c8c-116">**CreateOPMProtectedOutputs**</span></span>](createopmprotectedoutputs.md)
-   [<span data-ttu-id="d7c8c-117">**дестройопмпротектедаутпут**</span><span class="sxs-lookup"><span data-stu-id="d7c8c-117">**DestroyOPMProtectedOutput**</span></span>](destroyopmprotectedoutput.md)
-   [<span data-ttu-id="d7c8c-118">**Метода getcertificate**</span><span class="sxs-lookup"><span data-stu-id="d7c8c-118">**GetCertificate**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate)
-   [<span data-ttu-id="d7c8c-119">**жетцертификатесизе**</span><span class="sxs-lookup"><span data-stu-id="d7c8c-119">**GetCertificateSize**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize)
-   [<span data-ttu-id="d7c8c-120">**жеткоппкомпатиблеопминформатион**</span><span class="sxs-lookup"><span data-stu-id="d7c8c-120">**GetCOPPCompatibleOPMInformation**</span></span>](getcoppcompatibleopminformation.md)
-   [<span data-ttu-id="d7c8c-121">**жетопминформатион**</span><span class="sxs-lookup"><span data-stu-id="d7c8c-121">**GetOPMInformation**</span></span>](getopminformation.md)
-   [<span data-ttu-id="d7c8c-122">**жетопмрандомнумбер**</span><span class="sxs-lookup"><span data-stu-id="d7c8c-122">**GetOPMRandomNumber**</span></span>](getopmrandomnumber.md)
-   [<span data-ttu-id="d7c8c-123">**жетсугжестедопмпротектедаутпутаррайсизе**</span><span class="sxs-lookup"><span data-stu-id="d7c8c-123">**GetSuggestedOPMProtectedOutputArraySize**</span></span>](getsuggestedopmprotectedoutputarraysize.md)
-   [<span data-ttu-id="d7c8c-124">**сетопмсигнингкэйандсекуенценумберс**</span><span class="sxs-lookup"><span data-stu-id="d7c8c-124">**SetOPMSigningKeyAndSequenceNumbers**</span></span>](setopmsigningkeyandsequencenumbers.md)

## <a name="related-topics"></a><span data-ttu-id="d7c8c-125">См. также</span><span class="sxs-lookup"><span data-stu-id="d7c8c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7c8c-126">Справочник по программированию ОПМ</span><span class="sxs-lookup"><span data-stu-id="d7c8c-126">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="d7c8c-127">Диспетчер выходной защиты</span><span class="sxs-lookup"><span data-stu-id="d7c8c-127">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



