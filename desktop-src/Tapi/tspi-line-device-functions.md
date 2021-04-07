---
description: В этом разделе содержится алфавитный список доступных функций устройств в телефонной линии SPI.
ms.assetid: 2a27fbb7-93b5-4106-afd3-e63456650fb9
title: Функции для устройства телефонной связи TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea2ca54096ac89b76a4658129362e87d4281fcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910304"
---
# <a name="tspi-line-device-functions"></a><span data-ttu-id="f47d5-103">Функции для устройства телефонной связи TSPI</span><span class="sxs-lookup"><span data-stu-id="f47d5-103">TSPI Line Device Functions</span></span>

<span data-ttu-id="f47d5-104">В этом разделе содержится алфавитный список доступных функций устройств в телефонной линии SPI.</span><span class="sxs-lookup"><span data-stu-id="f47d5-104">This section contains an alphabetic list of the available line device functions in the Telephony SPI.</span></span> <span data-ttu-id="f47d5-105">Сведения для каждой функции включают следующее:</span><span class="sxs-lookup"><span data-stu-id="f47d5-105">The information for each function includes the following:</span></span>

-   <span data-ttu-id="f47d5-106">Оператор назначения функции.</span><span class="sxs-lookup"><span data-stu-id="f47d5-106">A statement of the function's purpose.</span></span>
-   <span data-ttu-id="f47d5-107">Правильный синтаксис функции.</span><span class="sxs-lookup"><span data-stu-id="f47d5-107">The correct syntax for the function.</span></span>
-   <span data-ttu-id="f47d5-108">Описание параметров функции, включая допустимые состояния вызова.</span><span class="sxs-lookup"><span data-stu-id="f47d5-108">A description of the function's parameters, including valid call states.</span></span>
-   <span data-ttu-id="f47d5-109">Описание возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="f47d5-109">A description of the function's return value.</span></span>
-   <span data-ttu-id="f47d5-110">Раздел примечаний, который может включать любые или все из следующих элементов: список допустимых состояний вызова для записи функции и типичные переходы состояния вызова по завершении запроса. Описание того, какие члены больших структур данных должны быть заполнены поставщиком услуг, и какие члены должны сохранять свои значения без изменений; и сравнение с соответствующей функцией в TAPI.</span><span class="sxs-lookup"><span data-stu-id="f47d5-110">A Remarks section that can include any or all of the following: a list of the valid call states on entry of the function and typical call state transitions when the request completes; a description of which members of large data structures must be filled in by the service provider and which members must have their values preserved intact; and comparison with a corresponding function within TAPI.</span></span>
-   <span data-ttu-id="f47d5-111">Ссылки на другие функции, сообщения или структуры данных.</span><span class="sxs-lookup"><span data-stu-id="f47d5-111">References to other functions, messages, or data structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="f47d5-112">Реальные состояния, в которых может выполняться функция, могут быть ограничены возможностями поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="f47d5-112">The actual states in which a function can be performed may be limited by the capabilities of the service provider.</span></span> <span data-ttu-id="f47d5-113">Поставщики услуг должны задать элемент **двкаллфеатурес** в структуре [**Линекаллстатус**](/windows/win32/api/tapi/ns-tapi-linecallstatus) , элемент **дваддрессфеатурес** в структуре [**линеаддрессстатус**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) и элемент **двлинефеатурес** в структуре [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) , чтобы указать приложениям, разрешены ли в этот момент времени функция или нет.</span><span class="sxs-lookup"><span data-stu-id="f47d5-113">Service providers must set the **dwCallFeatures** member in the [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus) structure, the **dwAddressFeatures** member in the [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) structure, and the **dwLineFeatures** member in the [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) structure to indicate to applications whether or not a function is permitted at that point in time.</span></span>

     

<span data-ttu-id="f47d5-114">В этом разделе содержатся следующие функции устройства ТСПИ Line:</span><span class="sxs-lookup"><span data-stu-id="f47d5-114">This section contains the following TSPI line device functions:</span></span>

-   [<span data-ttu-id="f47d5-115">**ТСПИ \_ линеакцепт**</span><span class="sxs-lookup"><span data-stu-id="f47d5-115">**TSPI\_lineAccept**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept)
-   [<span data-ttu-id="f47d5-116">**ТСПИ \_ линеаддтоконференце**</span><span class="sxs-lookup"><span data-stu-id="f47d5-116">**TSPI\_lineAddToConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineaddtoconference)
-   [<span data-ttu-id="f47d5-117">**ТСПИ \_ линеансвер**</span><span class="sxs-lookup"><span data-stu-id="f47d5-117">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer)
-   [<span data-ttu-id="f47d5-118">**ТСПИ \_ линеблиндтрансфер**</span><span class="sxs-lookup"><span data-stu-id="f47d5-118">**TSPI\_lineBlindTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineblindtransfer)
-   [<span data-ttu-id="f47d5-119">**ТСПИ \_ линеклосе**</span><span class="sxs-lookup"><span data-stu-id="f47d5-119">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose)
-   [<span data-ttu-id="f47d5-120">**ТСПИ \_ линеклосекалл**</span><span class="sxs-lookup"><span data-stu-id="f47d5-120">**TSPI\_lineCloseCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)
-   [<span data-ttu-id="f47d5-121">**ТСПИ \_ линеклосемспинстанце**</span><span class="sxs-lookup"><span data-stu-id="f47d5-121">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [<span data-ttu-id="f47d5-122">**ТСПИ \_ линекомплетекалл**</span><span class="sxs-lookup"><span data-stu-id="f47d5-122">**TSPI\_lineCompleteCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecompletecall)
-   [<span data-ttu-id="f47d5-123">**ТСПИ \_ линекомплететрансфер**</span><span class="sxs-lookup"><span data-stu-id="f47d5-123">**TSPI\_lineCompleteTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [<span data-ttu-id="f47d5-124">**ТСПИ \_ линекондитионалмедиадетектион**</span><span class="sxs-lookup"><span data-stu-id="f47d5-124">**TSPI\_lineConditionalMediaDetection**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   [<span data-ttu-id="f47d5-125">**ТСПИ \_ линеконфигдиалог**</span><span class="sxs-lookup"><span data-stu-id="f47d5-125">**TSPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)
-   [<span data-ttu-id="f47d5-126">**ТСПИ \_ линеконфигдиаложедит**</span><span class="sxs-lookup"><span data-stu-id="f47d5-126">**TSPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit)
-   [<span data-ttu-id="f47d5-127">**ТСПИ \_ линекреатемспинстанце**</span><span class="sxs-lookup"><span data-stu-id="f47d5-127">**TSPI\_lineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [<span data-ttu-id="f47d5-128">**ТСПИ \_ линедевспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="f47d5-128">**TSPI\_lineDevSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
-   [<span data-ttu-id="f47d5-129">**ТСПИ \_ линедевспеЦификфеатуре**</span><span class="sxs-lookup"><span data-stu-id="f47d5-129">**TSPI\_lineDevSpecificFeature**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
-   [<span data-ttu-id="f47d5-130">**ТСПИ \_ линедиал**</span><span class="sxs-lookup"><span data-stu-id="f47d5-130">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)
-   [<span data-ttu-id="f47d5-131">**ТСПИ \_ линедроп**</span><span class="sxs-lookup"><span data-stu-id="f47d5-131">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)
-   [<span data-ttu-id="f47d5-132">ТСПИ \_ линедропнувнер</span><span class="sxs-lookup"><span data-stu-id="f47d5-132">TSPI\_lineDropNoOwner</span></span>](tspi-linedropnoowner.md)
-   [<span data-ttu-id="f47d5-133">ТСПИ \_ линедропонклосе</span><span class="sxs-lookup"><span data-stu-id="f47d5-133">TSPI\_lineDropOnClose</span></span>](tspi-linedroponclose.md)
-   [<span data-ttu-id="f47d5-134">**ТСПИ \_ линефорвард**</span><span class="sxs-lookup"><span data-stu-id="f47d5-134">**TSPI\_lineForward**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [<span data-ttu-id="f47d5-135">**ТСПИ \_ линегасердигитс**</span><span class="sxs-lookup"><span data-stu-id="f47d5-135">**TSPI\_lineGatherDigits**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegatherdigits)
-   [<span data-ttu-id="f47d5-136">**ТСПИ \_ линеженератедигитс**</span><span class="sxs-lookup"><span data-stu-id="f47d5-136">**TSPI\_lineGenerateDigits**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits)
-   [<span data-ttu-id="f47d5-137">**ТСПИ \_ линеженератетоне**</span><span class="sxs-lookup"><span data-stu-id="f47d5-137">**TSPI\_lineGenerateTone**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratetone)
-   [<span data-ttu-id="f47d5-138">**ТСПИ \_ линежетаддресскапс**</span><span class="sxs-lookup"><span data-stu-id="f47d5-138">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)
-   [<span data-ttu-id="f47d5-139">**ТСПИ \_ линежетаддрессид**</span><span class="sxs-lookup"><span data-stu-id="f47d5-139">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)
-   [<span data-ttu-id="f47d5-140">**ТСПИ \_ линежетаддрессстатус**</span><span class="sxs-lookup"><span data-stu-id="f47d5-140">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus)
-   [<span data-ttu-id="f47d5-141">**ТСПИ \_ линежеткалладдрессид**</span><span class="sxs-lookup"><span data-stu-id="f47d5-141">**TSPI\_lineGetCallAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid)
-   [<span data-ttu-id="f47d5-142">**ТСПИ \_ линежеткаллхубтраккинг**</span><span class="sxs-lookup"><span data-stu-id="f47d5-142">**TSPI\_lineGetCallHubTracking**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallhubtracking)
-   [<span data-ttu-id="f47d5-143">**ТСПИ \_ линежеткаллидс**</span><span class="sxs-lookup"><span data-stu-id="f47d5-143">**TSPI\_lineGetCallIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallids)
-   [<span data-ttu-id="f47d5-144">**ТСПИ \_ линежеткаллинфо**</span><span class="sxs-lookup"><span data-stu-id="f47d5-144">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)
-   [<span data-ttu-id="f47d5-145">**ТСПИ \_ линежеткаллстатус**</span><span class="sxs-lookup"><span data-stu-id="f47d5-145">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)
-   [<span data-ttu-id="f47d5-146">**ТСПИ \_ линежетдевкапс**</span><span class="sxs-lookup"><span data-stu-id="f47d5-146">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)
-   [<span data-ttu-id="f47d5-147">**ТСПИ \_ линежетдевконфиг**</span><span class="sxs-lookup"><span data-stu-id="f47d5-147">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)
-   [<span data-ttu-id="f47d5-148">**ТСПИ \_ линежетекстенсионид**</span><span class="sxs-lookup"><span data-stu-id="f47d5-148">**TSPI\_lineGetExtensionID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetextensionid)
-   [<span data-ttu-id="f47d5-149">**ТСПИ \_ линежетикон**</span><span class="sxs-lookup"><span data-stu-id="f47d5-149">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)
-   [<span data-ttu-id="f47d5-150">**ТСПИ \_ линежетид**</span><span class="sxs-lookup"><span data-stu-id="f47d5-150">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [<span data-ttu-id="f47d5-151">**ТСПИ \_ линежетлинедевстатус**</span><span class="sxs-lookup"><span data-stu-id="f47d5-151">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)
-   [<span data-ttu-id="f47d5-152">**ТСПИ \_ линежетнумаддрессидс**</span><span class="sxs-lookup"><span data-stu-id="f47d5-152">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids)
-   [<span data-ttu-id="f47d5-153">**ТСПИ \_ линехолд**</span><span class="sxs-lookup"><span data-stu-id="f47d5-153">**TSPI\_lineHold**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linehold)
-   [<span data-ttu-id="f47d5-154">**ТСПИ \_ линемакекалл**</span><span class="sxs-lookup"><span data-stu-id="f47d5-154">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [<span data-ttu-id="f47d5-155">**ТСПИ \_ линемонитордигитс**</span><span class="sxs-lookup"><span data-stu-id="f47d5-155">**TSPI\_lineMonitorDigits**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)
-   [<span data-ttu-id="f47d5-156">**ТСПИ \_ линемонитормедиа**</span><span class="sxs-lookup"><span data-stu-id="f47d5-156">**TSPI\_lineMonitorMedia**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemonitormedia)
-   [<span data-ttu-id="f47d5-157">**ТСПИ \_ линемонитортонес**</span><span class="sxs-lookup"><span data-stu-id="f47d5-157">**TSPI\_lineMonitorTones**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemonitortones)
-   [<span data-ttu-id="f47d5-158">**ТСПИ \_ линемспидентифи**</span><span class="sxs-lookup"><span data-stu-id="f47d5-158">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [<span data-ttu-id="f47d5-159">**ТСПИ \_ линенеготиатикстверсион**</span><span class="sxs-lookup"><span data-stu-id="f47d5-159">**TSPI\_lineNegotiateExtVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion)
-   [<span data-ttu-id="f47d5-160">**ТСПИ \_ линенеготиатетспиверсион**</span><span class="sxs-lookup"><span data-stu-id="f47d5-160">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion)
-   [<span data-ttu-id="f47d5-161">**ТСПИ \_ линеопен**</span><span class="sxs-lookup"><span data-stu-id="f47d5-161">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)
-   [<span data-ttu-id="f47d5-162">**ТСПИ \_ линепарк**</span><span class="sxs-lookup"><span data-stu-id="f47d5-162">**TSPI\_linePark**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linepark)
-   [<span data-ttu-id="f47d5-163">**ТСПИ \_ линепиккуп**</span><span class="sxs-lookup"><span data-stu-id="f47d5-163">**TSPI\_linePickup**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [<span data-ttu-id="f47d5-164">**ТСПИ \_ линепрепареаддтоконференце**</span><span class="sxs-lookup"><span data-stu-id="f47d5-164">**TSPI\_linePrepareAddToConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [<span data-ttu-id="f47d5-165">**ТСПИ \_ линерецеивемспдата**</span><span class="sxs-lookup"><span data-stu-id="f47d5-165">**TSPI\_lineReceiveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [<span data-ttu-id="f47d5-166">**ТСПИ \_ линередирект**</span><span class="sxs-lookup"><span data-stu-id="f47d5-166">**TSPI\_lineRedirect**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineredirect)
-   [<span data-ttu-id="f47d5-167">**ТСПИ \_ линерелеасеусерусеринфо**</span><span class="sxs-lookup"><span data-stu-id="f47d5-167">**TSPI\_lineReleaseUserUserInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereleaseuseruserinfo)
-   [<span data-ttu-id="f47d5-168">**ТСПИ \_ линеремовефромконференце**</span><span class="sxs-lookup"><span data-stu-id="f47d5-168">**TSPI\_lineRemoveFromConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineremovefromconference)
-   [<span data-ttu-id="f47d5-169">**ТСПИ \_ линесекурекалл**</span><span class="sxs-lookup"><span data-stu-id="f47d5-169">**TSPI\_lineSecureCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesecurecall)
-   [<span data-ttu-id="f47d5-170">**ТСПИ \_ линеселектекстверсион**</span><span class="sxs-lookup"><span data-stu-id="f47d5-170">**TSPI\_lineSelectExtVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion)
-   [<span data-ttu-id="f47d5-171">**ТСПИ \_ линесендусерусеринфо**</span><span class="sxs-lookup"><span data-stu-id="f47d5-171">**TSPI\_lineSendUserUserInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesenduseruserinfo)
-   [<span data-ttu-id="f47d5-172">**ТСПИ \_ линесетаппспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="f47d5-172">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific)
-   [<span data-ttu-id="f47d5-173">**ТСПИ \_ линесеткаллдата**</span><span class="sxs-lookup"><span data-stu-id="f47d5-173">**TSPI\_lineSetCallData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [<span data-ttu-id="f47d5-174">**ТСПИ \_ линесеткаллхубтраккинг**</span><span class="sxs-lookup"><span data-stu-id="f47d5-174">**TSPI\_lineSetCallHubTracking**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallhubtracking)
-   [<span data-ttu-id="f47d5-175">**ТСПИ \_ линесеткаллпарамс**</span><span class="sxs-lookup"><span data-stu-id="f47d5-175">**TSPI\_lineSetCallParams**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallparams)
-   [<span data-ttu-id="f47d5-176">**ТСПИ \_ линесеткаллкуалитйофсервице**</span><span class="sxs-lookup"><span data-stu-id="f47d5-176">**TSPI\_lineSetCallQualityOfService**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [<span data-ttu-id="f47d5-177">**ТСПИ \_ линесеткаллтреатмент**</span><span class="sxs-lookup"><span data-stu-id="f47d5-177">**TSPI\_lineSetCallTreatment**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [<span data-ttu-id="f47d5-178">ТСПИ \_ линесеткуррентлокатион</span><span class="sxs-lookup"><span data-stu-id="f47d5-178">TSPI\_lineSetCurrentLocation</span></span>](tspi-linesetcurrentlocation.md)
-   [<span data-ttu-id="f47d5-179">**ТСПИ \_ линесетдефаултмедиадетектион**</span><span class="sxs-lookup"><span data-stu-id="f47d5-179">**TSPI\_lineSetDefaultMediaDetection**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection)
-   [<span data-ttu-id="f47d5-180">**ТСПИ \_ линесетдевконфиг**</span><span class="sxs-lookup"><span data-stu-id="f47d5-180">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)
-   [<span data-ttu-id="f47d5-181">**ТСПИ \_ линесетлинедевстатус**</span><span class="sxs-lookup"><span data-stu-id="f47d5-181">**TSPI\_lineSetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [<span data-ttu-id="f47d5-182">**ТСПИ \_ линесетмедиаконтрол**</span><span class="sxs-lookup"><span data-stu-id="f47d5-182">**TSPI\_lineSetMediaControl**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediacontrol)
-   [<span data-ttu-id="f47d5-183">**ТСПИ \_ линесетмедиамоде**</span><span class="sxs-lookup"><span data-stu-id="f47d5-183">**TSPI\_lineSetMediaMode**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediamode)
-   [<span data-ttu-id="f47d5-184">**ТСПИ \_ линесетстатусмессажес**</span><span class="sxs-lookup"><span data-stu-id="f47d5-184">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)
-   [<span data-ttu-id="f47d5-185">**ТСПИ \_ линесеттерминал**</span><span class="sxs-lookup"><span data-stu-id="f47d5-185">**TSPI\_lineSetTerminal**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal)
-   [<span data-ttu-id="f47d5-186">**ТСПИ \_ линесетупконференце**</span><span class="sxs-lookup"><span data-stu-id="f47d5-186">**TSPI\_lineSetupConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [<span data-ttu-id="f47d5-187">**ТСПИ \_ линесетуптрансфер**</span><span class="sxs-lookup"><span data-stu-id="f47d5-187">**TSPI\_lineSetupTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [<span data-ttu-id="f47d5-188">**ТСПИ \_ линесвафолд**</span><span class="sxs-lookup"><span data-stu-id="f47d5-188">**TSPI\_lineSwapHold**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineswaphold)
-   [<span data-ttu-id="f47d5-189">**ТСПИ \_ линеункомплетекалл**</span><span class="sxs-lookup"><span data-stu-id="f47d5-189">**TSPI\_lineUncompleteCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineuncompletecall)
-   [<span data-ttu-id="f47d5-190">**ТСПИ \_ линеунхолд**</span><span class="sxs-lookup"><span data-stu-id="f47d5-190">**TSPI\_lineUnhold**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineunhold)
-   [<span data-ttu-id="f47d5-191">**ТСПИ \_ линеунпарк**</span><span class="sxs-lookup"><span data-stu-id="f47d5-191">**TSPI\_lineUnpark**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
