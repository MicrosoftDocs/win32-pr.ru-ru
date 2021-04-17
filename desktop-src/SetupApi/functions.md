---
description: 'Следующие функции являются частью API установки:'
ms.assetid: 0a9518b7-f231-48f2-ba50-5b802f8ccaed
title: Функции (API установки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24051c52d7c7555e1e1b84c03fafd6faf6ad1b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663427"
---
# <a name="functions-setup-api"></a><span data-ttu-id="20e4e-103">Функции (API установки)</span><span class="sxs-lookup"><span data-stu-id="20e4e-103">Functions (Setup API)</span></span>

<span data-ttu-id="20e4e-104">\[Эти функции доступны для использования в операционных системах, указанных в разделах требования.</span><span class="sxs-lookup"><span data-stu-id="20e4e-104">\[These functions are available for use in the operating systems indicated in the Requirements sections.</span></span> <span data-ttu-id="20e4e-105">В последующих версиях они могут быть изменены или недоступны.</span><span class="sxs-lookup"><span data-stu-id="20e4e-105">They may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="20e4e-106">SetupAPI больше не следует использовать для установки приложений.</span><span class="sxs-lookup"><span data-stu-id="20e4e-106">SetupAPI should no longer be used for installing applications.</span></span> <span data-ttu-id="20e4e-107">Вместо этого используйте установщик Windows для разработки установщиков приложений.</span><span class="sxs-lookup"><span data-stu-id="20e4e-107">Instead, use the Windows Installer for developing application installers.</span></span> <span data-ttu-id="20e4e-108">SetupAPI будет использоваться для установки драйверов устройств.\]</span><span class="sxs-lookup"><span data-stu-id="20e4e-108">SetupAPI continues to be used for installing device drivers.\]</span></span>

<span data-ttu-id="20e4e-109">Следующие функции являются частью API установки:</span><span class="sxs-lookup"><span data-stu-id="20e4e-109">The following functions are part of the Setup API:</span></span>

-   [<span data-ttu-id="20e4e-110">**инсталлхинфсектион**</span><span class="sxs-lookup"><span data-stu-id="20e4e-110">**InstallHinfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-installhinfsectiona)
-   [<span data-ttu-id="20e4e-111">**сетупаддинсталлсектионтодискспацелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-111">**SetupAddInstallSectionToDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista)
-   [<span data-ttu-id="20e4e-112">**сетупаддсектионтодискспацелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-112">**SetupAddSectionToDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista)
-   [<span data-ttu-id="20e4e-113">**сетупаддтодискспацелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-113">**SetupAddToDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)
-   [<span data-ttu-id="20e4e-114">**сетупаддтосаурцелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-114">**SetupAddToSourceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista)
-   [<span data-ttu-id="20e4e-115">**сетупаджустдискспацелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-115">**SetupAdjustDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupadjustdiskspacelista)
-   [<span data-ttu-id="20e4e-116">**сетупбаккуперрор**</span><span class="sxs-lookup"><span data-stu-id="20e4e-116">**SetupBackupError**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupbackuperrora)
-   [<span data-ttu-id="20e4e-117">**сетупканцелтемпорарисаурцелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-117">**SetupCancelTemporarySourceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist)
-   [<span data-ttu-id="20e4e-118">**сетупклосефилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="20e4e-118">**SetupCloseFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)
-   [<span data-ttu-id="20e4e-119">**сетупклосеинффиле**</span><span class="sxs-lookup"><span data-stu-id="20e4e-119">**SetupCloseInfFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile)
-   [<span data-ttu-id="20e4e-120">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="20e4e-120">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
-   [<span data-ttu-id="20e4e-121">**сетупконфигуревмифроминфсектион**</span><span class="sxs-lookup"><span data-stu-id="20e4e-121">**SetupConfigureWmiFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupconfigurewmifrominfsectiona)
-   [<span data-ttu-id="20e4e-122">**сетупкоперрор**</span><span class="sxs-lookup"><span data-stu-id="20e4e-122">**SetupCopyError**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora)
-   [<span data-ttu-id="20e4e-123">**сетупкопйоеминф**</span><span class="sxs-lookup"><span data-stu-id="20e4e-123">**SetupCopyOEMInf**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyoeminfa)
-   [<span data-ttu-id="20e4e-124">**сетупкреатедискспацелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-124">**SetupCreateDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista)
-   [<span data-ttu-id="20e4e-125">**сетупдекомпрессоркопифиле**</span><span class="sxs-lookup"><span data-stu-id="20e4e-125">**SetupDecompressOrCopyFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea)
-   [<span data-ttu-id="20e4e-126">**сетупдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="20e4e-126">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
-   [<span data-ttu-id="20e4e-127">**сетупделетиррор**</span><span class="sxs-lookup"><span data-stu-id="20e4e-127">**SetupDeleteError**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)
-   [<span data-ttu-id="20e4e-128">**сетупдестройдискспацелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-128">**SetupDestroyDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist)
-   [<span data-ttu-id="20e4e-129">**сетупдупликатедискспацелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-129">**SetupDuplicateDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupduplicatediskspacelista)
-   [<span data-ttu-id="20e4e-130">**сетупенуминфсектионс**</span><span class="sxs-lookup"><span data-stu-id="20e4e-130">**SetupEnumInfSections**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupenuminfsectionsa)
-   [<span data-ttu-id="20e4e-131">**сетупфиндфирстлине**</span><span class="sxs-lookup"><span data-stu-id="20e4e-131">**SetupFindFirstLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)
-   [<span data-ttu-id="20e4e-132">**сетупфинднекстлине**</span><span class="sxs-lookup"><span data-stu-id="20e4e-132">**SetupFindNextLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)
-   [<span data-ttu-id="20e4e-133">**сетупфинднекстматчлине**</span><span class="sxs-lookup"><span data-stu-id="20e4e-133">**SetupFindNextMatchLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)
-   [<span data-ttu-id="20e4e-134">**сетупфрисаурцелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-134">**SetupFreeSourceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista)
-   [<span data-ttu-id="20e4e-135">**сетупжетбинарифиелд**</span><span class="sxs-lookup"><span data-stu-id="20e4e-135">**SetupGetBinaryField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)
-   [<span data-ttu-id="20e4e-136">**сетупжетфиелдкаунт**</span><span class="sxs-lookup"><span data-stu-id="20e4e-136">**SetupGetFieldCount**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfieldcount)
-   [<span data-ttu-id="20e4e-137">**сетупжетфилекомпрессионинфо**</span><span class="sxs-lookup"><span data-stu-id="20e4e-137">**SetupGetFileCompressionInfo**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa)
-   [<span data-ttu-id="20e4e-138">**сетупжетфилекомпрессионинфоекс**</span><span class="sxs-lookup"><span data-stu-id="20e4e-138">**SetupGetFileCompressionInfoEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoexa)
-   [<span data-ttu-id="20e4e-139">**сетупжетфилекуеуекаунт**</span><span class="sxs-lookup"><span data-stu-id="20e4e-139">**SetupGetFileQueueCount**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilequeuecount)
-   [<span data-ttu-id="20e4e-140">**сетупжетфилекуеуефлагс**</span><span class="sxs-lookup"><span data-stu-id="20e4e-140">**SetupGetFileQueueFlags**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilequeueflags)
-   [<span data-ttu-id="20e4e-141">**сетупжетинффилелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-141">**SetupGetInfFileList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista)
-   [<span data-ttu-id="20e4e-142">**сетупжетинфинформатион**</span><span class="sxs-lookup"><span data-stu-id="20e4e-142">**SetupGetInfInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)
-   [<span data-ttu-id="20e4e-143">**сетупжетинтфиелд**</span><span class="sxs-lookup"><span data-stu-id="20e4e-143">**SetupGetIntField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)
-   [<span data-ttu-id="20e4e-144">**сетупжетлинебиндекс**</span><span class="sxs-lookup"><span data-stu-id="20e4e-144">**SetupGetLineByIndex**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)
-   [<span data-ttu-id="20e4e-145">**сетупжетлинекаунт**</span><span class="sxs-lookup"><span data-stu-id="20e4e-145">**SetupGetLineCount**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinecounta)
-   [<span data-ttu-id="20e4e-146">**сетупжетлинетекст**</span><span class="sxs-lookup"><span data-stu-id="20e4e-146">**SetupGetLineText**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)
-   [<span data-ttu-id="20e4e-147">**сетупжетмултисзфиелд**</span><span class="sxs-lookup"><span data-stu-id="20e4e-147">**SetupGetMultiSzField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)
-   [<span data-ttu-id="20e4e-148">**сетупжетсаурцефилелокатион**</span><span class="sxs-lookup"><span data-stu-id="20e4e-148">**SetupGetSourceFileLocation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)
-   [<span data-ttu-id="20e4e-149">**сетупжетсаурцефилесизе**</span><span class="sxs-lookup"><span data-stu-id="20e4e-149">**SetupGetSourceFileSize**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)
-   [<span data-ttu-id="20e4e-150">**сетупжетсаурцеинфо**</span><span class="sxs-lookup"><span data-stu-id="20e4e-150">**SetupGetSourceInfo**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)
-   [<span data-ttu-id="20e4e-151">**сетупжетстрингфиелд**</span><span class="sxs-lookup"><span data-stu-id="20e4e-151">**SetupGetStringField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)
-   [<span data-ttu-id="20e4e-152">**сетупжеттаржетпас**</span><span class="sxs-lookup"><span data-stu-id="20e4e-152">**SetupGetTargetPath**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)
-   [<span data-ttu-id="20e4e-153">**сетупинитдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="20e4e-153">**SetupInitDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback)
-   [<span data-ttu-id="20e4e-154">**сетупинитдефаулткуеуекаллбаккекс**</span><span class="sxs-lookup"><span data-stu-id="20e4e-154">**SetupInitDefaultQueueCallbackEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)
-   [<span data-ttu-id="20e4e-155">**сетупинитиализефилелог**</span><span class="sxs-lookup"><span data-stu-id="20e4e-155">**SetupInitializeFileLog**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga)
-   [<span data-ttu-id="20e4e-156">**сетупинсталлфиле**</span><span class="sxs-lookup"><span data-stu-id="20e4e-156">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
-   [<span data-ttu-id="20e4e-157">**сетупинсталлфиликс**</span><span class="sxs-lookup"><span data-stu-id="20e4e-157">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
-   [<span data-ttu-id="20e4e-158">**сетупинсталлфилесфроминфсектион**</span><span class="sxs-lookup"><span data-stu-id="20e4e-158">**SetupInstallFilesFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)
-   [<span data-ttu-id="20e4e-159">**сетупинсталлфроминфсектион**</span><span class="sxs-lookup"><span data-stu-id="20e4e-159">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
-   [<span data-ttu-id="20e4e-160">**сетупинсталлсервицесфроминфсектион**</span><span class="sxs-lookup"><span data-stu-id="20e4e-160">**SetupInstallServicesFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona)
-   [<span data-ttu-id="20e4e-161">**сетупинсталлсервицесфроминфсектионекс**</span><span class="sxs-lookup"><span data-stu-id="20e4e-161">**SetupInstallServicesFromInfSectionEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectionexa)
-   [<span data-ttu-id="20e4e-162">**сетупитератекабинет**</span><span class="sxs-lookup"><span data-stu-id="20e4e-162">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
-   [<span data-ttu-id="20e4e-163">**SetupLogFile**</span><span class="sxs-lookup"><span data-stu-id="20e4e-163">**SetupLogFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea)
-   [<span data-ttu-id="20e4e-164">**сетупложеррор**</span><span class="sxs-lookup"><span data-stu-id="20e4e-164">**SetupLogError**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuplogerrora)
-   [<span data-ttu-id="20e4e-165">**сетупопенаппендинффиле**</span><span class="sxs-lookup"><span data-stu-id="20e4e-165">**SetupOpenAppendInfFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea)
-   [<span data-ttu-id="20e4e-166">**сетупопенфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="20e4e-166">**SetupOpenFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)
-   [<span data-ttu-id="20e4e-167">**сетупопенинффиле**</span><span class="sxs-lookup"><span data-stu-id="20e4e-167">**SetupOpenInfFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea)
-   [<span data-ttu-id="20e4e-168">**сетупопенмастеринф**</span><span class="sxs-lookup"><span data-stu-id="20e4e-168">**SetupOpenMasterInf**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupopenmasterinf)
-   [<span data-ttu-id="20e4e-169">**сетуппромптфордиск**</span><span class="sxs-lookup"><span data-stu-id="20e4e-169">**SetupPromptForDisk**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)
-   [<span data-ttu-id="20e4e-170">**сетуппромптребут**</span><span class="sxs-lookup"><span data-stu-id="20e4e-170">**SetupPromptReboot**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)
-   [<span data-ttu-id="20e4e-171">**сетупкуеридривесиндискспацелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-171">**SetupQueryDrivesInDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista)
-   [<span data-ttu-id="20e4e-172">**сетупкуерифилелог**</span><span class="sxs-lookup"><span data-stu-id="20e4e-172">**SetupQueryFileLog**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga)
-   [<span data-ttu-id="20e4e-173">**сетупкуеринффилеинформатион**</span><span class="sxs-lookup"><span data-stu-id="20e4e-173">**SetupQueryInfFileInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)
-   [<span data-ttu-id="20e4e-174">**сетупкуеринфоригиналфилеинформатион**</span><span class="sxs-lookup"><span data-stu-id="20e4e-174">**SetupQueryInfOriginalFileInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinforiginalfileinformationa)
-   [<span data-ttu-id="20e4e-175">**сетупкуеринфверсионинформатион**</span><span class="sxs-lookup"><span data-stu-id="20e4e-175">**SetupQueryInfVersionInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa)
-   [<span data-ttu-id="20e4e-176">**сетупкуерисаурцелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-176">**SetupQuerySourceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista)
-   [<span data-ttu-id="20e4e-177">**сетупкуериспацерекуиредондриве**</span><span class="sxs-lookup"><span data-stu-id="20e4e-177">**SetupQuerySpaceRequiredOnDrive**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea)
-   [<span data-ttu-id="20e4e-178">**сетупкуеуекопи**</span><span class="sxs-lookup"><span data-stu-id="20e4e-178">**SetupQueueCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)
-   [<span data-ttu-id="20e4e-179">**сетупкуеуекопиндирект**</span><span class="sxs-lookup"><span data-stu-id="20e4e-179">**SetupQueueCopyIndirect**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopyindirecta)
-   [<span data-ttu-id="20e4e-180">**сетупкуеуекописектион**</span><span class="sxs-lookup"><span data-stu-id="20e4e-180">**SetupQueueCopySection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)
-   [<span data-ttu-id="20e4e-181">**сетупкуеуедефаулткопи**</span><span class="sxs-lookup"><span data-stu-id="20e4e-181">**SetupQueueDefaultCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)
-   [<span data-ttu-id="20e4e-182">**сетупкуеуеделете**</span><span class="sxs-lookup"><span data-stu-id="20e4e-182">**SetupQueueDelete**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)
-   [<span data-ttu-id="20e4e-183">**сетупкуеуеделетесектион**</span><span class="sxs-lookup"><span data-stu-id="20e4e-183">**SetupQueueDeleteSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)
-   [<span data-ttu-id="20e4e-184">**сетупкуеуеренаме**</span><span class="sxs-lookup"><span data-stu-id="20e4e-184">**SetupQueueRename**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)
-   [<span data-ttu-id="20e4e-185">**сетупкуеуеренамесектион**</span><span class="sxs-lookup"><span data-stu-id="20e4e-185">**SetupQueueRenameSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)
-   [<span data-ttu-id="20e4e-186">**сетупремовефилеложентри**</span><span class="sxs-lookup"><span data-stu-id="20e4e-186">**SetupRemoveFileLogEntry**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya)
-   [<span data-ttu-id="20e4e-187">**сетупремовефромдискспацелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-187">**SetupRemoveFromDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista)
-   [<span data-ttu-id="20e4e-188">**сетупремовефромсаурцелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-188">**SetupRemoveFromSourceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista)
-   [<span data-ttu-id="20e4e-189">**сетупремовеинсталлсектионфромдискспацелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-189">**SetupRemoveInstallSectionFromDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista)
-   [<span data-ttu-id="20e4e-190">**сетупремовесектионфромдискспацелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-190">**SetupRemoveSectionFromDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista)
-   [<span data-ttu-id="20e4e-191">**сетупренамиррор**</span><span class="sxs-lookup"><span data-stu-id="20e4e-191">**SetupRenameError**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)
-   [<span data-ttu-id="20e4e-192">**сетупсканфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="20e4e-192">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
-   [<span data-ttu-id="20e4e-193">**сетупсетдиректорид**</span><span class="sxs-lookup"><span data-stu-id="20e4e-193">**SetupSetDirectoryId**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetdirectoryida)
-   [<span data-ttu-id="20e4e-194">**сетупсетдиректоридекс**</span><span class="sxs-lookup"><span data-stu-id="20e4e-194">**SetupSetDirectoryIdEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetdirectoryidexa)
-   [<span data-ttu-id="20e4e-195">**сетупсетфилекуеуеалтернатеплатформ**</span><span class="sxs-lookup"><span data-stu-id="20e4e-195">**SetupSetFileQueueAlternatePlatform**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetfilequeuealternateplatforma)
-   [<span data-ttu-id="20e4e-196">**сетупсетфилекуеуефлагс**</span><span class="sxs-lookup"><span data-stu-id="20e4e-196">**SetupSetFileQueueFlags**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetfilequeueflags)
-   [<span data-ttu-id="20e4e-197">**сетупсетплатформпасоверриде**</span><span class="sxs-lookup"><span data-stu-id="20e4e-197">**SetupSetPlatformPathOverride**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea)
-   [<span data-ttu-id="20e4e-198">**сетупсетсаурцелист**</span><span class="sxs-lookup"><span data-stu-id="20e4e-198">**SetupSetSourceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista)
-   [<span data-ttu-id="20e4e-199">**сетуптермдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="20e4e-199">**SetupTermDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback)
-   [<span data-ttu-id="20e4e-200">**сетуптерминатефилелог**</span><span class="sxs-lookup"><span data-stu-id="20e4e-200">**SetupTerminateFileLog**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog)
-   [<span data-ttu-id="20e4e-201">**сетупунинсталлневликопиединфс**</span><span class="sxs-lookup"><span data-stu-id="20e4e-201">**SetupUninstallNewlyCopiedInfs**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupuninstallnewlycopiedinfs)
-   [<span data-ttu-id="20e4e-202">**сетупунинсталлоеминф**</span><span class="sxs-lookup"><span data-stu-id="20e4e-202">**SetupUninstallOEMInf**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupuninstalloeminfa)
-   [<span data-ttu-id="20e4e-203">**сетупверифинффиле**</span><span class="sxs-lookup"><span data-stu-id="20e4e-203">**SetupVerifyInfFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupverifyinffilea)

 

 



