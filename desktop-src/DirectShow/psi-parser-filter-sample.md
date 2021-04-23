---
description: Образец фильтра средства синтаксического анализа PSI
ms.assetid: e815d57f-25e5-4a71-8f40-e7abec0db236
title: Образец фильтра средства синтаксического анализа PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1099375d2dbabf9ee6c8e891b0a1780bebbb599d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104570241"
---
# <a name="psi-parser-filter-sample"></a><span data-ttu-id="81b32-103">Образец фильтра средства синтаксического анализа PSI</span><span class="sxs-lookup"><span data-stu-id="81b32-103">PSI Parser Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="81b32-104">Описание</span><span class="sxs-lookup"><span data-stu-id="81b32-104">Description</span></span>

<span data-ttu-id="81b32-105">Фильтр средства синтаксического анализа PSI получает сведения о программе (PSI) из транспортного потока MPEG-2 и извлекает сведения о программе из таблицы взаимосвязей программ (PAT) и таблиц схемы программы (PMT).</span><span class="sxs-lookup"><span data-stu-id="81b32-105">The PSI Parser filter receives Program Specific Information (PSI) from an MPEG-2 transport stream and extracts program information from the Program Association Table (PAT) and Program Map Tables (PMT).</span></span> <span data-ttu-id="81b32-106">Эта информация позволяет приложению настроить демультиплексор MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="81b32-106">This information enables an application to configure the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="81b32-107">Фильтр поддерживает пользовательский интерфейс [**IMpeg2PsiParser**](impeg2psiparser.md)для получения сведений PSI.</span><span class="sxs-lookup"><span data-stu-id="81b32-107">The filter supports a custom interface, [**IMpeg2PsiParser**](impeg2psiparser.md), for retrieving the PSI information.</span></span>

<span data-ttu-id="81b32-108">Этот фильтр предназначен для устройств MPEG-2, таких как видеокамеры MPEG-2 (IEEE 1394) и устройства D-ВХС.</span><span class="sxs-lookup"><span data-stu-id="81b32-108">This filter is designed for MPEG-2 devices, such as IEEE 1394 MPEG-2 camcorders and D-VHS devices.</span></span> <span data-ttu-id="81b32-109">Дополнительные сведения см. в разделе [драйвер мстапе](mstape-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="81b32-109">See [MSTape Driver](mstape-driver.md) for more information.</span></span> <span data-ttu-id="81b32-110">Источники вещания цифрового телевидения должны использовать фильтр TIF для получения сведений о программе.</span><span class="sxs-lookup"><span data-stu-id="81b32-110">Digital television broadcast sources should use a TIF filter to get program information.</span></span>

## <a name="usage"></a><span data-ttu-id="81b32-111">Использование</span><span class="sxs-lookup"><span data-stu-id="81b32-111">Usage</span></span>

<span data-ttu-id="81b32-112">Проверить фильтр анализатора PSI в Графедит можно следующим образом:</span><span class="sxs-lookup"><span data-stu-id="81b32-112">You can test the PSI Parser filter in GraphEdit as follows:</span></span>

1.  <span data-ttu-id="81b32-113">Запустите Графедит.</span><span class="sxs-lookup"><span data-stu-id="81b32-113">Launch GraphEdit.</span></span>
2.  <span data-ttu-id="81b32-114">Вставьте источник транспорта MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="81b32-114">Insert an MPEG-2 transport source.</span></span> <span data-ttu-id="81b32-115">Видеокамеры MPEG-2 и устройства D-ВХС отображаются в категории источников видеозаписи как "устройство подразделений Microsoft AV/C".</span><span class="sxs-lookup"><span data-stu-id="81b32-115">MPEG-2 camcorders and D-VHS devices appear as "Microsoft AV/C Tape Subunit Device" in the Video Capture Sources category.</span></span>
3.  <span data-ttu-id="81b32-116">Соедините фильтр источников с фильтром демультиплексора MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="81b32-116">Connect the source filter to the MPEG-2 Demultiplexer filter.</span></span>
4.  <span data-ttu-id="81b32-117">Используйте страницу свойств в демультиплексирование, чтобы создать выходной ПИН-код с типом носителя MPEG-2 PSI.</span><span class="sxs-lookup"><span data-stu-id="81b32-117">Use the property page on the demux to create an output pin with an "MPEG-2 PSI" media type.</span></span> <span data-ttu-id="81b32-118">Этот ПИН-код доставляет разделы PAT и ПЛТ.</span><span class="sxs-lookup"><span data-stu-id="81b32-118">This pin will deliver the PAT and PMT sections.</span></span>
5.  <span data-ttu-id="81b32-119">Используйте страницу свойств демультиплексирование, чтобы связать идентификатор потока 0x00 с выходным закреплением.</span><span class="sxs-lookup"><span data-stu-id="81b32-119">Use the demux property page to map PID 0x00 to the output pin.</span></span> <span data-ttu-id="81b32-120">Задайте тип содержимого "разделы MPEG2 PSI".</span><span class="sxs-lookup"><span data-stu-id="81b32-120">Set the content type to "MPEG2 PSI Sections".</span></span>
6.  <span data-ttu-id="81b32-121">Подключите закрепление выходных данных демультиплексирование к средству синтаксического анализа PSI, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="81b32-121">Connect the demux output pin to PSI Parser, as shown in the following diagram.</span></span>

    ![граф фильтра средства синтаксического анализа psi](images/psi-parser.png)

7.  <span data-ttu-id="81b32-123">Запустите граф, чтобы передать данные PSI в фильтр средства синтаксического анализа PSI.</span><span class="sxs-lookup"><span data-stu-id="81b32-123">Run the graph, in order to feed PSI data to the PSI Parser filter.</span></span> <span data-ttu-id="81b32-124">По мере того как фильтр декодирует разделы PAT, он автоматически сопоставляет идентификаторы исходящих данных ПЛТ с одним и тем же выходным закреплением на демультиплексирование, чтобы он получал разделы ПЛТ.</span><span class="sxs-lookup"><span data-stu-id="81b32-124">As the filter decodes the PAT sections, it automatically maps the PMT PIDs to the same output pin on the demux, so that it receives the PMT sections.</span></span>
8.  <span data-ttu-id="81b32-125">Используйте страницу свойств средства синтаксического анализа PSI для выбора номера программы.</span><span class="sxs-lookup"><span data-stu-id="81b32-125">Use the PSI Parser property page to select a program number.</span></span> <span data-ttu-id="81b32-126">В списке простейших потоков на странице свойств будет показан идентификатор процесса и тип потока, связанный с каждым из простейших потоков в выбранной программе.</span><span class="sxs-lookup"><span data-stu-id="81b32-126">The elementary stream list in the property page will show the PID and stream type associated with each elementary stream in the selected program.</span></span> <span data-ttu-id="81b32-127">Страница свойств предназначена для распознавания типов потоков, определенных в стандарте ISO/IEC 13818-1.</span><span class="sxs-lookup"><span data-stu-id="81b32-127">The property page is designed to recognize stream types defined in ISO/IEC 13818-1.</span></span>
9.  <span data-ttu-id="81b32-128">Введите номер PID в поле ввода **аудио PID** и номер PID видео в поле редактирования **PID** .</span><span class="sxs-lookup"><span data-stu-id="81b32-128">Enter the audio PID number in the **Audio PID** edit box, and the video PID number in the **Video PID** edit box.</span></span>
10. <span data-ttu-id="81b32-129">Нажмите кнопку **Просмотреть программу** .</span><span class="sxs-lookup"><span data-stu-id="81b32-129">Click the **View Program** button.</span></span> <span data-ttu-id="81b32-130">Средство синтаксического анализа PSI настроит контакты вывода в демультиплексирование в соответствии со сведениями о потоке программы и отрисовывает контакты.</span><span class="sxs-lookup"><span data-stu-id="81b32-130">The PSI Parser will configure the output pins on the demux to match the program stream information and render the pins.</span></span>

> [!Note]  
> <span data-ttu-id="81b32-131">Страница свойств средства синтаксического анализа PSI предназначена для упрощения тестирования и предоставления примера кода, который настраивает демультиплексор MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="81b32-131">The PSI Parser property page is provided to make testing easier, and to provide sample code that configures the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="81b32-132">Не рекомендуется использовать приложения.</span><span class="sxs-lookup"><span data-stu-id="81b32-132">It is not recommended for applications to use.</span></span> <span data-ttu-id="81b32-133">Приложения должны программно настраивать демультиплексирование.</span><span class="sxs-lookup"><span data-stu-id="81b32-133">Applications should configure the demux programmatically.</span></span>

 

<span data-ttu-id="81b32-134">Чтобы использовать фильтр анализатора PSI в приложении, начните с создания графа фильтра из источника MPEG-2 в формат MPEG-2 демультиплексирование.</span><span class="sxs-lookup"><span data-stu-id="81b32-134">To use the PSI Parser filter in an application, start by building the filter graph from the MPEG-2 source to the MPEG-2 demux.</span></span> <span data-ttu-id="81b32-135">Код для этого шага здесь не показан, так как точная конфигурация графа будет зависеть от источника.</span><span class="sxs-lookup"><span data-stu-id="81b32-135">Code for this step is not shown here, because the exact graph configuration will depend on the source.</span></span>

<span data-ttu-id="81b32-136">Затем создайте закрепление вывода на демультиплексирование для данных PSI.</span><span class="sxs-lookup"><span data-stu-id="81b32-136">Next, create an output pin on the demux for the PSI data.</span></span> <span data-ttu-id="81b32-137">Сопоставьте идентификатор потока 0x00, зарезервированный для разделов PAT, с этим закреплением, как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="81b32-137">Map PID 0x00, which is reserved for PAT sections, to this pin, as shown in the following code:</span></span>


```C++
// Set the media type to MPEG-2 table sections.
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;

// Create the pin.
IPin *pPsiPin;
hr = pDemux->CreateOutputPin(&mt, L"PSI", &pPsiPin);
if (SUCCEEDED(hr))
{
    // Map to PID 0.
    ULONG Pid = 0x00;
    hr = pPid->MapPID(1, &Pid, MEDIA_MPEG2_PSI);
}
```



<span data-ttu-id="81b32-138">Дополнительные сведения см. [в разделе Использование демультиплексора MPEG-2](using-the-mpeg-2-demultiplexer.md).</span><span class="sxs-lookup"><span data-stu-id="81b32-138">For more information, see [Using the MPEG-2 Demultiplexer](using-the-mpeg-2-demultiplexer.md).</span></span>

<span data-ttu-id="81b32-139">Добавьте фильтр средства синтаксического анализа PSI в граф и соедините его с выходным закреплением на демультиплексирование.</span><span class="sxs-lookup"><span data-stu-id="81b32-139">Add the PSI Parser filter to the graph and connect it to the output pin on the demux.</span></span> <span data-ttu-id="81b32-140">Запросите средство синтаксического анализа PSI для интерфейса [**IMpeg2PsiParser**](impeg2psiparser.md) .</span><span class="sxs-lookup"><span data-stu-id="81b32-140">Query the PSI Parser for the [**IMpeg2PsiParser**](impeg2psiparser.md) interface.</span></span> <span data-ttu-id="81b32-141">Теперь запустите граф и дождитесь \_ \_ событий изменения программы EC, которые сообщают о новом разделе Pat или ПЛТ.</span><span class="sxs-lookup"><span data-stu-id="81b32-141">Now run the graph and wait for EC\_PROGRAM\_CHANGED events, which signal a new PAT or PMT section.</span></span> <span data-ttu-id="81b32-142">Это событие является пользовательским событием, определенным фильтром средства синтаксического анализа PSI.</span><span class="sxs-lookup"><span data-stu-id="81b32-142">This event is a custom event defined by the PSI Parser filter.</span></span> <span data-ttu-id="81b32-143">При получении \_ события изменения программы EC \_ можно получить доступные сведения PSI, вызвав методы **IMpeg2PsiParser** .</span><span class="sxs-lookup"><span data-stu-id="81b32-143">When you receive an EC\_PROGRAM\_CHANGED event, you can get the available PSI information by calling **IMpeg2PsiParser** methods.</span></span> <span data-ttu-id="81b32-144">В этом разделе описываются наиболее часто используемые методы.</span><span class="sxs-lookup"><span data-stu-id="81b32-144">This section describes the methods you will need most often.</span></span>

<span data-ttu-id="81b32-145">Чтобы получить количество программ, используйте метод [**IMpeg2PsiParser:: жеткаунтофпрограмс**](impeg2psiparser-getcountofprograms.md) :</span><span class="sxs-lookup"><span data-stu-id="81b32-145">To get the number of programs, use the [**IMpeg2PsiParser::GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md) method:</span></span>


```C++
int NumProgs = 0;
hr = pPsi->GetCountOfPrograms(&NumProgs);
```



<span data-ttu-id="81b32-146">Чтобы получить номер программы для конкретной программы, используйте метод [**IMpeg2PsiParser:: жетрекордпрограмнумбер**](impeg2psiparser-getrecordprogramnumber.md) :</span><span class="sxs-lookup"><span data-stu-id="81b32-146">To get the program number for a specific program, use the [**IMpeg2PsiParser::GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md) method:</span></span>


```C++
WORD ProgNum = 0;
for (int i = 0; i < NumProgs; i++)
{
    hr = pPsi->GetRecordProgramNumber(i, &ProgNum);
    ...
}
```



<span data-ttu-id="81b32-147">Номер программы используется для получения записей о выплатах для отдельных программ.</span><span class="sxs-lookup"><span data-stu-id="81b32-147">The program number is used to obtain the PMT entries for individual programs.</span></span> <span data-ttu-id="81b32-148">Чтобы получить количество простейших потоков в программе, используйте метод [**жеткаунтофелементаристреамс**](impeg2psiparser-getcountofelementarystreams.md) :</span><span class="sxs-lookup"><span data-stu-id="81b32-148">To get the number of elementary streams in a program, use the [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) method:</span></span>


```C++
WORD cElemStreams = 0;
hr = pPsi->GetCountOfElementaryStreams(ProgNum, &cElemStreams);
```



<span data-ttu-id="81b32-149">Для каждого элементарного потока метод [**IMpeg2PsiParser:: жетрекорделементарипид**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) возвращает идентификатор процесса, а метод [**IMpeg2PsiParser:: жетрекордстреамтипе**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) Возвращает тип потока:</span><span class="sxs-lookup"><span data-stu-id="81b32-149">For each elementary stream, the [**IMpeg2PsiParser::GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) method returns the PID, and the [**IMpeg2PsiParser::GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) method returns the stream type:</span></span>


```C++
BYTE ESType = 0;
WORD ESPid = 0;
for (WORD j = 0; j < cElemStreams; j++)
{
    hr = pPsi->GetRecordElementaryPid(ProgNum, j, &ESPid);
    hr = pPsi->GetRecordStreamType(ProgNum, j, &ESType);
}
```



<span data-ttu-id="81b32-150">Идентификатор процесса и тип потока позволяют настроить новые выходные сигналы в демультиплексоре MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="81b32-150">The PID and the stream type enable you to configure new output pins on the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="81b32-151">Для этого может потребоваться знание исходного источника.</span><span class="sxs-lookup"><span data-stu-id="81b32-151">This may require some knowledge of the original source.</span></span> <span data-ttu-id="81b32-152">Например, ISO/IEC 13818-1 определяет типы потоков с 0x80 по 0xFF как "пользователь Private", но другие стандарты, основанные на MPEG-2, могут назначить другие значения для этих типов.</span><span class="sxs-lookup"><span data-stu-id="81b32-152">For example, ISO/IEC 13818-1 defines stream types 0x80 through 0xFF as "user private," but other standards that are based on MPEG-2 may assign other meanings to these types.</span></span>

<span data-ttu-id="81b32-153">Демультиплексор MPEG-2 может создавать новые и новые сопоставления идентификаторов PID во время работы графа, но для соединения ПИН-кодов необходимо отключить граф.</span><span class="sxs-lookup"><span data-stu-id="81b32-153">The MPEG-2 Demultiplexer can create new pins and new PID mappings while the graph is running, but you must stop the graph to connect pins.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="81b32-154">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="81b32-154">Downloading the Sample</span></span>

<span data-ttu-id="81b32-155">Чтобы скачать примеры пакета SDK для DirectShow, установите последнюю версию [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="81b32-155">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="81b32-156">Этот пример устанавливается по следующему пути: *\[ \] корневые примеры SDK* \\ \\ мультимедиа \\ DirectShow \\ фильтры \\ псипарсер.</span><span class="sxs-lookup"><span data-stu-id="81b32-156">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\PSIParser.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81b32-157">См. также</span><span class="sxs-lookup"><span data-stu-id="81b32-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81b32-158">Примеры DirectShow</span><span class="sxs-lookup"><span data-stu-id="81b32-158">DirectShow Samples</span></span>](directshow-samples.md)
</dt> <dt>

[<span data-ttu-id="81b32-159">**Интерфейс IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="81b32-159">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> </dl>

 

 
