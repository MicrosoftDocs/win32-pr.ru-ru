---
description: Начиная с TAPI 2,1, для управления и вывода диалоговых окон можно использовать библиотеки DLL пользовательского интерфейса поставщика услуг телефонии. TAPI загружает библиотеку DLL в процесс приложения, вызывающего любую из функций поставщика услуг, которые могут отображать диалоговое окно.
ms.assetid: 0a0320d1-fb75-405e-8074-b37cef956c9f
title: Новые возможности для ТСПИ версии 2,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51642fb9ac960732f8e4a56805652333d0c32468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673960"
---
# <a name="whats-new-for-tspi-version-21"></a><span data-ttu-id="4946a-104">Новые возможности для ТСПИ версии 2,1</span><span class="sxs-lookup"><span data-stu-id="4946a-104">What's New for TSPI Version 2.1</span></span>

<span data-ttu-id="4946a-105">Начиная с TAPI 2,1, для управления и вывода диалоговых окон можно использовать библиотеки DLL пользовательского интерфейса поставщика услуг телефонии.</span><span class="sxs-lookup"><span data-stu-id="4946a-105">Starting with TAPI 2.1, the telephony service provider user interface DLLs can be used to manage and display dialog boxes.</span></span> <span data-ttu-id="4946a-106">TAPI загружает библиотеку DLL в процесс приложения, вызывающего любую из функций поставщика услуг, которые могут отображать диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4946a-106">TAPI loads the DLL into the process of an application that invokes any of the service provider functions that can display a dialog.</span></span>

<span data-ttu-id="4946a-107">Начиная с TAPI 2,1, можно реализовать обработчики запросов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="4946a-107">Starting with TAPI 2.1, proxy request handlers can be implemented.</span></span> <span data-ttu-id="4946a-108">Обработчик — это полное приложение телефонии, которое обычно выполняется на сервере телефонии и предоставляет службы, которые более правильно реализуются в приложении, чем драйвер.</span><span class="sxs-lookup"><span data-stu-id="4946a-108">A handler is a full telephony application that normally executes on a telephony server and provides services that are more appropriately implemented in an application than a driver.</span></span>

<span data-ttu-id="4946a-109">Функции и сообщения, которые были впервые или изменены для ТСПИ версии 2,1, следующие:</span><span class="sxs-lookup"><span data-stu-id="4946a-109">Functions and messages that were new or changed for TSPI version 2.1 are as follows:</span></span>

-   [<span data-ttu-id="4946a-110">**TSPI_lineConditionalMediaDetection**</span><span class="sxs-lookup"><span data-stu-id="4946a-110">**TSPI_lineConditionalMediaDetection**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   <span data-ttu-id="4946a-111">**TSPI_lineDropNoOwner**—**устарело**</span><span class="sxs-lookup"><span data-stu-id="4946a-111">**TSPI_lineDropNoOwner**—**obsolete**</span></span>
-   <span data-ttu-id="4946a-112">**TSPI_lineDropOnClose**—**устарело**</span><span class="sxs-lookup"><span data-stu-id="4946a-112">**TSPI_lineDropOnClose**—**obsolete**</span></span>
-   [<span data-ttu-id="4946a-113">**TSPI_lineGetID**</span><span class="sxs-lookup"><span data-stu-id="4946a-113">**TSPI_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [<span data-ttu-id="4946a-114">**TSPI_lineSetCallData**</span><span class="sxs-lookup"><span data-stu-id="4946a-114">**TSPI_lineSetCallData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [<span data-ttu-id="4946a-115">**TSPI_lineSetCallQualityOfService**</span><span class="sxs-lookup"><span data-stu-id="4946a-115">**TSPI_lineSetCallQualityOfService**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [<span data-ttu-id="4946a-116">**TSPI_lineSetCallTreatment**</span><span class="sxs-lookup"><span data-stu-id="4946a-116">**TSPI_lineSetCallTreatment**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [<span data-ttu-id="4946a-117">**TSPI_lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="4946a-117">**TSPI_lineSetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [<span data-ttu-id="4946a-118">**TSPI_phoneGetID**</span><span class="sxs-lookup"><span data-stu-id="4946a-118">**TSPI_phoneGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonegetid)
-   [<span data-ttu-id="4946a-119">**TSPI_providerInit**</span><span class="sxs-lookup"><span data-stu-id="4946a-119">**TSPI_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)
-   [<span data-ttu-id="4946a-120">**TSPI_providerShutdown**</span><span class="sxs-lookup"><span data-stu-id="4946a-120">**TSPI_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)
-   <span data-ttu-id="4946a-121">[**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4946a-121">[**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))</span></span>
-   <span data-ttu-id="4946a-122">[**LINE_GENERATE**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4946a-122">[**LINE_GENERATE**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))</span></span>
-   <span data-ttu-id="4946a-123">[**LINE_MONITORDIGITS**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4946a-123">[**LINE_MONITORDIGITS**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))</span></span>
-   <span data-ttu-id="4946a-124">[**LINE_MONITORMEDIA**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4946a-124">[**LINE_MONITORMEDIA**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))</span></span>
-   <span data-ttu-id="4946a-125">[**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4946a-125">[**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))</span></span>
-   <span data-ttu-id="4946a-126">[**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4946a-126">[**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))</span></span>
-   <span data-ttu-id="4946a-127">[**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4946a-127">[**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))</span></span>

<span data-ttu-id="4946a-128">Библиотека DLL пользовательского интерфейса поставщика услуг телефонии предоставляет возможность взаимодействия с пользователем в контексте приложения, а не самого поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="4946a-128">The Telephony service provider user interface DLL provides a means of allowing user interaction within the context of the application rather than the service provider itself.</span></span> <span data-ttu-id="4946a-129">ТСПИ версии 2,1 доставляет следующие новые функции, сообщения и структуры для реализации:</span><span class="sxs-lookup"><span data-stu-id="4946a-129">TSPI version 2.1 delivered the following new functions, messages, and structures for implementation:</span></span>

-   [<span data-ttu-id="4946a-130">**TSPI_providerFreeDialogInstance**</span><span class="sxs-lookup"><span data-stu-id="4946a-130">**TSPI_providerFreeDialogInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance)
-   [<span data-ttu-id="4946a-131">**TSPI_providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="4946a-131">**TSPI_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata)
-   [<span data-ttu-id="4946a-132">**TSPI_providerUIIdentify**</span><span class="sxs-lookup"><span data-stu-id="4946a-132">**TSPI_providerUIIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify)
-   [<span data-ttu-id="4946a-133">**TUISPI_lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="4946a-133">**TUISPI_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)
-   [<span data-ttu-id="4946a-134">**TUISPI_lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="4946a-134">**TUISPI_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit)
-   [<span data-ttu-id="4946a-135">**TUISPI_phoneConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="4946a-135">**TUISPI_phoneConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog)
-   [<span data-ttu-id="4946a-136">**TUISPI_providerConfig**</span><span class="sxs-lookup"><span data-stu-id="4946a-136">**TUISPI_providerConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig)
-   [<span data-ttu-id="4946a-137">**TUISPI_providerGenericDialog**</span><span class="sxs-lookup"><span data-stu-id="4946a-137">**TUISPI_providerGenericDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog)
-   [<span data-ttu-id="4946a-138">**TUISPI_providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="4946a-138">**TUISPI_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
-   [<span data-ttu-id="4946a-139">**TUISPI_providerInstall**</span><span class="sxs-lookup"><span data-stu-id="4946a-139">**TUISPI_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)
-   [<span data-ttu-id="4946a-140">**TUISPI_providerRemove**</span><span class="sxs-lookup"><span data-stu-id="4946a-140">**TUISPI_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)
-   [<span data-ttu-id="4946a-141">**туиспикреатедиалогинстанцепарамс**</span><span class="sxs-lookup"><span data-stu-id="4946a-141">**TUISPICREATEDIALOGINSTANCEPARAMS**</span></span>](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
-   [<span data-ttu-id="4946a-142">**туиспидллкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="4946a-142">**TUISPIDLLCALLBACK**</span></span>](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
-   [<span data-ttu-id="4946a-143">**LINE_CREATEDIALOGINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="4946a-143">**LINE_CREATEDIALOGINSTANCE**</span></span>](line-createdialoginstance.md)
-   [<span data-ttu-id="4946a-144">**LINE_SENDDIALOGINSTANCEDATA**</span><span class="sxs-lookup"><span data-stu-id="4946a-144">**LINE_SENDDIALOGINSTANCEDATA**</span></span>](line-senddialoginstancedata.md)

 

 
