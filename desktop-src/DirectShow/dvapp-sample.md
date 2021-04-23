---
description: Пример Двапп
ms.assetid: 80375170-d0d6-4371-abe3-078703e158b1
title: Пример Двапп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86653781d08921bf638e7798fb34f3a86e8d34a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140203"
---
# <a name="dvapp-sample"></a><span data-ttu-id="d4f5c-103">Пример Двапп</span><span class="sxs-lookup"><span data-stu-id="d4f5c-103">DVApp Sample</span></span>

## <a name="description"></a><span data-ttu-id="d4f5c-104">Описание</span><span class="sxs-lookup"><span data-stu-id="d4f5c-104">Description</span></span>

<span data-ttu-id="d4f5c-105">Приложение для записи цифрового видео (DV).</span><span class="sxs-lookup"><span data-stu-id="d4f5c-105">Digital Video (DV) capture application.</span></span>

<span data-ttu-id="d4f5c-106">В этом образце показано, как создавать различные типы графов фильтров для управления видеокамерами.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-106">This sample demonstrates how to build various types of filter graphs for controlling DV camcorders.</span></span> <span data-ttu-id="d4f5c-107">Здесь также показано, как выполнять захват, просмотр, передачу и управление устройствами с помощью цифровой видеокамеры.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-107">It also shows how to perform capture, preview, transmit, and device control with a DV camcorder.</span></span>

### <a name="usage"></a><span data-ttu-id="d4f5c-108">Использование</span><span class="sxs-lookup"><span data-stu-id="d4f5c-108">Usage</span></span>

<span data-ttu-id="d4f5c-109">Приложение Двапп поддерживает следующие режимы:</span><span class="sxs-lookup"><span data-stu-id="d4f5c-109">The DVApp application supports the following modes:</span></span>

-   <span data-ttu-id="d4f5c-110">Предварительный просмотр: отображает DV с видеокамеры в видеоокно.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-110">Preview: Renders DV from the camcorder to a video window.</span></span>
-   <span data-ttu-id="d4f5c-111">DV to Type-1 file: захватывает DV-данные с видеокамеры в файл DV типа 1.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-111">DV to type-1 file: Captures DV data from the camcorder to a type-1 DV file.</span></span>
-   <span data-ttu-id="d4f5c-112">Type-1 File to DV: передает данные из DV-файла типа 1 на видеокамеру.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-112">Type-1 file to DV: Transmits data from a type-1 DV file to the camcorder.</span></span>
-   <span data-ttu-id="d4f5c-113">DV to Type-2 file: захватывает DV-данные с видеокамеры до файла DV типа 2.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-113">DV to type-2 file: Captures DV data from the camcorder to a type-2 DV file.</span></span>
-   <span data-ttu-id="d4f5c-114">Type-2 File to DV: передает данные из DV-файла типа 2 на видеокамеру.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-114">Type-2 file to DV: Transmits data from a type-2 DV file to the camcorder.</span></span>

<span data-ttu-id="d4f5c-115">Режимы записи и передачи также выполняют предварительную версию.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-115">The capture and transmit modes also perform preview.</span></span> <span data-ttu-id="d4f5c-116">В каждом из этих режимов **отсутствует параметр Предварительный просмотр** , который отключает предварительный просмотр.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-116">Each of those modes has a **No Preview** option as well, which disables preview.</span></span> <span data-ttu-id="d4f5c-117">Захват без предварительного просмотра более эффективен и может уменьшить количество удаленных кадров.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-117">Capturing without preview is more efficient and can reduce the number of dropped frames.</span></span>

<span data-ttu-id="d4f5c-118">Приложение запускается в режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-118">The application starts in preview mode.</span></span> <span data-ttu-id="d4f5c-119">Чтобы выбрать другой режим, выберите режим в меню **режим диаграммы** .</span><span class="sxs-lookup"><span data-stu-id="d4f5c-119">To select another mode, choose a mode from the **Graph Mode** menu.</span></span> <span data-ttu-id="d4f5c-120">Для каждого режима Двапп создает граф фильтра, который поддерживает функциональность этого режима.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-120">For each mode, DVApp builds a filter graph that supports the functionality of that mode.</span></span> <span data-ttu-id="d4f5c-121">Чтобы сохранить граф в виде файла Графедит (ГРФ), выберите команду **сохранить граф в файл** в меню **файл** .</span><span class="sxs-lookup"><span data-stu-id="d4f5c-121">To save the graph as a GraphEdit (.grf) file, select **Save Graph to File** from the **File** menu.</span></span> <span data-ttu-id="d4f5c-122">Закройте Двапп, прежде чем открывать файл в Графедит.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-122">Quit DVApp before opening the file in GraphEdit.</span></span>

<span data-ttu-id="d4f5c-123">Для записи в файл:</span><span class="sxs-lookup"><span data-stu-id="d4f5c-123">To capture to a file:</span></span>

1.  <span data-ttu-id="d4f5c-124">В меню **файл** выберите команду **задать выходной файл** и введите имя файла.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-124">From the **File** menu, choose **Set Output File** and enter a file name.</span></span>
2.  <span data-ttu-id="d4f5c-125">В меню **режим графа** выберите режим *DV в виде файла* (тип 1 или тип 2 с предварительной версией или без нее).</span><span class="sxs-lookup"><span data-stu-id="d4f5c-125">From the **Graph Mode** menu, select a *DV to File* mode (type 1 or type 2, with or without preview).</span></span>
3.  <span data-ttu-id="d4f5c-126">Щелкните **запись**.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-126">Click **Record**.</span></span>
4.  <span data-ttu-id="d4f5c-127">Если видеокамера находится в режиме Втр, нажмите кнопку **воспроизвести**.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-127">If the camcorder is in VTR mode, click **Play**.</span></span>
5.  <span data-ttu-id="d4f5c-128">Чтобы отключить запись, нажмите кнопку " **Закрыть**".</span><span class="sxs-lookup"><span data-stu-id="d4f5c-128">To stop capturing, click **Stop**.</span></span>

<span data-ttu-id="d4f5c-129">Для передачи из файла на видеокамера:</span><span class="sxs-lookup"><span data-stu-id="d4f5c-129">To transmit from a file to the camcorder:</span></span>

1.  <span data-ttu-id="d4f5c-130">В меню **файл** выберите команду **задать входной файл** и выберите DV-файл.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-130">From the **File** menu, click **Set Input File** and select a DV file.</span></span> <span data-ttu-id="d4f5c-131">Файл должен соответствовать выбранному режиму (тип 1 или тип 2).</span><span class="sxs-lookup"><span data-stu-id="d4f5c-131">The file must match the selected mode (type 1 or type 2).</span></span>
2.  <span data-ttu-id="d4f5c-132">В меню **режим графа** выберите *файл в формате DV* (тип 1 или 2, с предварительным просмотром или без него).</span><span class="sxs-lookup"><span data-stu-id="d4f5c-132">From the **Graph Mode** menu, select a *File to DV* mode (type 1 or type 2, with or without preview).</span></span>
3.  <span data-ttu-id="d4f5c-133">Нажмите кнопку **Воспроизвести**.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-133">Click **Play**.</span></span>
4.  <span data-ttu-id="d4f5c-134">Чтобы записать данные на ленту, щелкните **запись**.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-134">To record the data to tape, click **Record**.</span></span>
5.  <span data-ttu-id="d4f5c-135">Чтобы отключить передачу, нажмите кнопку " **Закрыть**".</span><span class="sxs-lookup"><span data-stu-id="d4f5c-135">To stop transmitting, click **Stop**.</span></span>

<span data-ttu-id="d4f5c-136">Если видеокамера находится в режиме Втр, пользователь может управлять транспортным механизмом через кнопки в стиле ВИДЕОМАГНИТОФОНА приложения.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-136">If the camcorder is in VTR mode, the user can control the transport mechanism through the application's VCR-style buttons.</span></span> <span data-ttu-id="d4f5c-137">Чтобы найти ленту, введите целевой код времени и нажмите кнопку "Поиск".</span><span class="sxs-lookup"><span data-stu-id="d4f5c-137">To seek the tape, enter the target timecode and click the seek button.</span></span>

<span data-ttu-id="d4f5c-138">Чтобы ограничить объем данных, выделяемых приложением, выберите **Размер захвата** в меню **файл** .</span><span class="sxs-lookup"><span data-stu-id="d4f5c-138">To limit how much data the application captures, choose **Capture Size** from the **File** menu.</span></span>

<span data-ttu-id="d4f5c-139">Чтобы проверить формат ленты (NTSC или PAL), выберите пункт **проверить ленту** в меню **Параметры** .</span><span class="sxs-lookup"><span data-stu-id="d4f5c-139">To check the tape format (NTSC or PAL), choose **Check Tape** from the **Options** menu.</span></span>

<span data-ttu-id="d4f5c-140">Чтобы изменить размер окна предварительного просмотра, выберите **изменить размер декодирования** в меню **Параметры** .</span><span class="sxs-lookup"><span data-stu-id="d4f5c-140">To change the size of the preview window, choose **Change Decode Size** from the **Options** menu.</span></span>

### <a name="programming-notes"></a><span data-ttu-id="d4f5c-141">Заметки о программировании</span><span class="sxs-lookup"><span data-stu-id="d4f5c-141">Programming Notes</span></span>

<span data-ttu-id="d4f5c-142">Основное назначение этого приложения — продемонстрировать, как создавать различные видеозаписи и передавать графы.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-142">The main purpose of this application is to show how to build various DV capture and transmit graphs.</span></span>

### <a name="device-arrival-and-removal"></a><span data-ttu-id="d4f5c-143">Получение и удаление устройства</span><span class="sxs-lookup"><span data-stu-id="d4f5c-143">Device Arrival and Removal</span></span>

<span data-ttu-id="d4f5c-144">Приложение обрабатывает прибытие и удаление устройства, используя два разных метода.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-144">The application handles device arrival and removal, using two different techniques.</span></span> <span data-ttu-id="d4f5c-145">Для прибытия устройства цикл обработки сообщений приложения реагирует на \_ сообщения WM девицечанже.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-145">For device arrival, the application's message loop responds to WM\_DEVICECHANGE messages.</span></span> <span data-ttu-id="d4f5c-146">Для удаления устройства приложение реагирует на события [**\_ \_ потерянного устройства EC**](ec-device-lost.md) из диспетчера графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-146">For device removal, the application responds to [**EC\_DEVICE\_LOST**](ec-device-lost.md) events from the filter graph manager.</span></span> <span data-ttu-id="d4f5c-147">Любой из этих подходов работает, хотя \_ событие «потеря устройства EC» зависит от \_ наличия устройства в графе фильтра.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-147">Either approach works, although the EC\_DEVICE\_LOST event depends on the existence of the device in the filter graph.</span></span>

<span data-ttu-id="d4f5c-148">Приложение обрабатывает только одно устройство за раз.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-148">The application only handles one device at a time.</span></span> <span data-ttu-id="d4f5c-149">Если текущее устройство удалено, приложение ищет другое устройство DV в системе.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-149">If the current device is removed, the application looks for another DV device on the system.</span></span>

<span data-ttu-id="d4f5c-150">На некоторых видеокамерах пользователь должен завершить работу устройства при переключении между режимом камеры и режимом Втр, который запускает сообщение с потерей устройства.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-150">On some DV camcorders, the user must shut off the device when switching it between camera mode and VTR mode, which triggers a device-lost message.</span></span> <span data-ttu-id="d4f5c-151">Приложение отвечает, включая или отключая соответствующие команды меню.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-151">The application responds by enabling or disabling the appropriate menu commands.</span></span> <span data-ttu-id="d4f5c-152">Однако если пользователь переключается между режимами, видеокамера может не генерировать сообщение, потерянное устройством.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-152">However, if the user toggles rapidly between modes, the camcorder might not generate a device-lost message.</span></span> <span data-ttu-id="d4f5c-153">Можно принудительно обновить меню, выбрав **режим обновления** в меню **Параметры** .</span><span class="sxs-lookup"><span data-stu-id="d4f5c-153">You can force the menus to update by choosing **Refresh Mode** from the **Options** menu.</span></span> <span data-ttu-id="d4f5c-154">Некоторые видеокамеры могут переключаться в режим без выключения, но при переключении в режим ВТРи сообщение будет отправлено только при пересылке устройства.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-154">Some DV camcorders can toggle modes without shutting off, but send a device-lost message only when they switch to VTR mode.</span></span>

### <a name="device-control"></a><span data-ttu-id="d4f5c-155">Управление устройством</span><span class="sxs-lookup"><span data-stu-id="d4f5c-155">Device Control</span></span>

<span data-ttu-id="d4f5c-156">Функциональные возможности кнопки **Воспроизведение** и **запись** зависят от текущего режима:</span><span class="sxs-lookup"><span data-stu-id="d4f5c-156">The functionality of the **Play** and **Record** button depends on the current mode:</span></span>

-   <span data-ttu-id="d4f5c-157">Предварительный просмотр: граф фильтра запускается автоматически.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-157">Preview: The filter graph runs automatically.</span></span> <span data-ttu-id="d4f5c-158">Кнопка **Воспроизведение** запускает транспорт.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-158">The **Play** button starts the transport.</span></span>
-   <span data-ttu-id="d4f5c-159">Записать в файл: кнопка **записи** запускает граф, а кнопка **Воспроизведение** запускает транспорт.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-159">Capture to file: The **Record** button runs the graph, and the **Play** button starts the transport.</span></span>
-   <span data-ttu-id="d4f5c-160">Передать на устройство. Кнопка **воспроизведения** запускает граф, а кнопка **запись** запускает транспорт.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-160">Transmit to device: The **Play** button runs the graph, and the **Record** button starts the transport.</span></span>

<span data-ttu-id="d4f5c-161">Пример приложения не выполняет точную запись в виде кадров.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-161">The sample application does not perform frame-accurate capture.</span></span> <span data-ttu-id="d4f5c-162">В различных точках приложение вызывает функцию **Sleep** для ожидания ответа устройства.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-162">At various points, the application calls the **Sleep** function to wait for the device to respond.</span></span> <span data-ttu-id="d4f5c-163">Новые видеокамеры с новыми ЦИФРами отправляют уведомление при изменении состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-163">Newer DV camcorders send a notification when the state of the device changes.</span></span> <span data-ttu-id="d4f5c-164">Старые устройства могут не поддерживать уведомления. в этом примере вызов **спящего режима** является более простым решением.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-164">Older devices might not support notification; for the purposes of a sample, calling **Sleep** is a simpler solution.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="d4f5c-165">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="d4f5c-165">Downloading the Sample</span></span>

<span data-ttu-id="d4f5c-166">Чтобы скачать примеры пакета SDK для DirectShow, установите последнюю версию [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d4f5c-166">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="d4f5c-167">Этот пример устанавливается по следующему пути: *\[ \] корневые примеры SDK* \\ \\ мультимедиа \\ DirectShow \\ Capture \\ двапп.</span><span class="sxs-lookup"><span data-stu-id="d4f5c-167">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Capture\\DVApp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4f5c-168">См. также</span><span class="sxs-lookup"><span data-stu-id="d4f5c-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4f5c-169">Управление видеокамерой</span><span class="sxs-lookup"><span data-stu-id="d4f5c-169">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> <dt>

[<span data-ttu-id="d4f5c-170">Цифровое видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="d4f5c-170">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="d4f5c-171">Примеры DirectShow</span><span class="sxs-lookup"><span data-stu-id="d4f5c-171">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



