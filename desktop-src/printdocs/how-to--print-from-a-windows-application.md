---
description: В этом разделе описывается, как выполнить печать из собственной программы Windows.
ms.assetid: D0AE8FF8-D02D-43D3-80CA-E13EAA894F87
title: Практические руководства. печать из программы Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84229823944d7f7104da359b953e579f1b21cdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693600"
---
# <a name="how-to-print-from-a-windows-program"></a><span data-ttu-id="0667e-103">Практические руководства. печать из программы Windows</span><span class="sxs-lookup"><span data-stu-id="0667e-103">How To: Print from a Windows Program</span></span>

<span data-ttu-id="0667e-104">В этом разделе описывается, как выполнить печать из собственной программы Windows.</span><span class="sxs-lookup"><span data-stu-id="0667e-104">This section describes how to print from a native Windows program.</span></span>

## <a name="overview"></a><span data-ttu-id="0667e-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="0667e-105">Overview</span></span>

<span data-ttu-id="0667e-106">Печать обычно является неотъемлемой частью собственной программы Windows.</span><span class="sxs-lookup"><span data-stu-id="0667e-106">Printing is usually an integral part of a native Windows program.</span></span> <span data-ttu-id="0667e-107">Таким образом, это не функция, которую можно легко добавить после написания программы.</span><span class="sxs-lookup"><span data-stu-id="0667e-107">Therefore, it is not a feature that you can add easily after you have written the program.</span></span> <span data-ttu-id="0667e-108">С другой стороны, если программа разработана для использования XPS-документов, то при наличии любого дополнительного кода для отрисовки содержимого документа для печати он не потребуется.</span><span class="sxs-lookup"><span data-stu-id="0667e-108">That being said, if the program is designed to use XPS documents it will not need much, if any, additional code to render the document content for printing.</span></span> <span data-ttu-id="0667e-109">XPS-документы приложения можно отправлять непосредственно на принтер, имеющий драйвер принтера XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="0667e-109">The XPS documents of the application can be sent directly to a printer that has an XPSDrv printer driver.</span></span>

<span data-ttu-id="0667e-110">Используйте [API документа XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) для создания содержимого документа и [API печати XPS](xps-printing.md) для отправки содержимого документа на принтер.</span><span class="sxs-lookup"><span data-stu-id="0667e-110">Use the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) to create the document content and the [XPS Print API](xps-printing.md) to send the document content to the printer.</span></span> <span data-ttu-id="0667e-111">API печати XPS обрабатывает содержимое документа для принтера назначения.</span><span class="sxs-lookup"><span data-stu-id="0667e-111">The XPS Print API processes the document content for the destination printer.</span></span> <span data-ttu-id="0667e-112">Если на выбранном принтере имеется драйвер принтера XPSDrv, документ будет отправлен на принтер без дополнительного преобразования.</span><span class="sxs-lookup"><span data-stu-id="0667e-112">If the selected printer has an XPSDrv printer driver, the document will be sent to the printer without any additional conversion.</span></span> <span data-ttu-id="0667e-113">Если на выбранном принтере установлен драйвер принтера на основе GDI, программа также может отправить содержимое на принтер, а API печати XPS преобразует содержимое документа таким образом, чтобы оно было совместимо с драйвером принтера на основе GDI.</span><span class="sxs-lookup"><span data-stu-id="0667e-113">If the selected printer has a GDI-based printer driver, the program can also send the content to the printer, and the XPS Print API converts the document content so that it will be compatible with the GDI-based printer driver.</span></span> <span data-ttu-id="0667e-114">В любом случае обработка, выполняемая приложением, выполняется одинаково.</span><span class="sxs-lookup"><span data-stu-id="0667e-114">In either case, the processing that the application performs is the same.</span></span>

## <a name="printing-tasks"></a><span data-ttu-id="0667e-115">Задачи печати</span><span class="sxs-lookup"><span data-stu-id="0667e-115">Printing tasks</span></span>

<span data-ttu-id="0667e-116">В следующих разделах описаны основные шаги печати содержимого программы.</span><span class="sxs-lookup"><span data-stu-id="0667e-116">The following topics describe the basic steps of printing program content.</span></span>

1.  <span data-ttu-id="0667e-117">**Получение сведений о задании печати от пользователя.**</span><span class="sxs-lookup"><span data-stu-id="0667e-117">**Collect print job information from user.**</span></span>

    <span data-ttu-id="0667e-118">Как правило, пользователь инициирует задание печати при выборе параметра Печать в меню, и программа отображает диалоговое окно Печать для получения сведений о задании печати.</span><span class="sxs-lookup"><span data-stu-id="0667e-118">Typically, a user initiates a print job when they select the print option from a menu and the program displays a print dialog box to collect the details of the print job.</span></span> <span data-ttu-id="0667e-119">Пользователь обычно выбирает принтер, число копий и сведения о конфигурации принтера, такие как двусторонняя печать и сшивание.</span><span class="sxs-lookup"><span data-stu-id="0667e-119">The user typically selects the printer, the number of copies, and printer configuration details such as two-sided printing and stapling.</span></span>

    <span data-ttu-id="0667e-120">Сведения о том, как это сделать, см. в разделе [руководство. Получение сведений о задании печати от пользователя](preparing-to-print.md).</span><span class="sxs-lookup"><span data-stu-id="0667e-120">For information about how to do this, see [How To: Collect Print Job Information from the User](preparing-to-print.md).</span></span>

2.  <span data-ttu-id="0667e-121">**Создать индикатор хода выполнения.**</span><span class="sxs-lookup"><span data-stu-id="0667e-121">**Create progress indicator.**</span></span>

    <span data-ttu-id="0667e-122">Индикатор выполнения предоставляет пользователю отзыв о ходе выполнения задания печати.</span><span class="sxs-lookup"><span data-stu-id="0667e-122">A progress indicator provides the user with feedback about how the print job is progressing.</span></span> <span data-ttu-id="0667e-123">Индикатор хода выполнения может находиться в виде индикатора выполнения, который является частью диалогового окна, включающего кнопку **отмены** для задания, или индикатором выполнения в строке состояния в нижней части главного окна.</span><span class="sxs-lookup"><span data-stu-id="0667e-123">The progress indicator can be a progress bar that is part of a dialog box that includes the **Cancel** button for the job, or it can be a progress bar in the status bar at the bottom of the main window.</span></span>

    <span data-ttu-id="0667e-124">Сведения о работе индикатора выполнения см. в разделе [инструкции. Отображение хода выполнения задания печати](cancel-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="0667e-124">For information about the progress indicator works, see [How To: Display the Print Job Progress](cancel-dialog-box.md).</span></span>

    <span data-ttu-id="0667e-125">Дополнительные сведения о том, как отобразить ход выполнения задания печати, см. в разделе рекомендации по [разработке пользовательского интерфейса приложения Windows](/windows/desktop/windows-application-ui-development) .</span><span class="sxs-lookup"><span data-stu-id="0667e-125">For more ideas about how to display the progress of the print job, see the information in the [Windows Application UI Development](/windows/desktop/windows-application-ui-development) guidelines.</span></span>

3.  <span data-ttu-id="0667e-126">**Запустите поток печати.**</span><span class="sxs-lookup"><span data-stu-id="0667e-126">**Start the printing thread.**</span></span>

    <span data-ttu-id="0667e-127">После того как программа собрал сведения о задании печати от пользователя, она может запустить поток печати, чтобы выполнить фактическую обработку документа для печати.</span><span class="sxs-lookup"><span data-stu-id="0667e-127">After the program has collected the print job information from the user, it can start the printing thread to perform the actual processing of the document for printing.</span></span>

    <span data-ttu-id="0667e-128">Сведения о потоке печати см. [в разделе как запускать и прекращать поток печати](how-to--start-and-stop-a-printing-thread.md).</span><span class="sxs-lookup"><span data-stu-id="0667e-128">For information about the printing thread, see [How To: Start and Stop a Printing Thread](how-to--start-and-stop-a-printing-thread.md).</span></span>

4.  <span data-ttu-id="0667e-129">**Прорисовка данных задания печати.**</span><span class="sxs-lookup"><span data-stu-id="0667e-129">**Render print job data.**</span></span>

    <span data-ttu-id="0667e-130">Поток печати визуализирует данные документа для печати.</span><span class="sxs-lookup"><span data-stu-id="0667e-130">The printing thread renders the document data for printing.</span></span> <span data-ttu-id="0667e-131">Эту обработку следует разбить на отдельные этапы обработки, чтобы пользователь мог прервать обработку и отменить задание, а также запретить потоку обработки блокировать другие потоки и процессы.</span><span class="sxs-lookup"><span data-stu-id="0667e-131">You should break down this processing into discrete processing steps so that the user can interrupt the processing and cancel the job as well as to not allow the processing thread to block other threads and processes.</span></span>

    <span data-ttu-id="0667e-132">Сведения о том, как отрисовывает данные задания печати, см. [в разделе как отобразить данные задания](how-to--render-the-print-job-data.md)печати.</span><span class="sxs-lookup"><span data-stu-id="0667e-132">For information about how the renders the print job data, see [How To: Render Print Job Data](how-to--render-the-print-job-data.md).</span></span>

5.  <span data-ttu-id="0667e-133">**Отслеживание хода выполнения задания печати.**</span><span class="sxs-lookup"><span data-stu-id="0667e-133">**Monitor print job progress.**</span></span>

    <span data-ttu-id="0667e-134">По мере выполнения каждого шага обработки обновите индикатор выполнения для информирования об использовании.</span><span class="sxs-lookup"><span data-stu-id="0667e-134">As each processing step is performed, update the progress bar to inform the use.</span></span> <span data-ttu-id="0667e-135">Вычислите этапы обработки, чтобы завершить выполнение запрошенного задания, а затем обновляет индикатор выполнения по мере выполнения этих шагов.</span><span class="sxs-lookup"><span data-stu-id="0667e-135">Compute the processing steps to complete the requested job and then updates the progress bar as those steps are performed.</span></span>

6.  <span data-ttu-id="0667e-136">**Закройте задание печати и завершите поток печати.**</span><span class="sxs-lookup"><span data-stu-id="0667e-136">**Close print job and terminate printing thread.**</span></span>

    <span data-ttu-id="0667e-137">После того как программа отправила задание печати на принтер или пользователь отменил задание печати, необходимо закрыть задание печати и освободить ресурсы, используемые заданием печати.</span><span class="sxs-lookup"><span data-stu-id="0667e-137">After the program has sent the print job to the printer, or if the user has cancelled the print job, you must close the print job and release the resources used by the print job.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0667e-138">См. также</span><span class="sxs-lookup"><span data-stu-id="0667e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0667e-139">Инструкции. Получение сведений о задании печати от пользователя</span><span class="sxs-lookup"><span data-stu-id="0667e-139">How To: Collect Print Job Information from the User</span></span>](preparing-to-print.md)
</dt> </dl>

 

 
