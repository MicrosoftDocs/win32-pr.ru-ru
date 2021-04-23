---
description: Создание образцов потоков из существующего объекта данных ASF
ms.assetid: eb27f122-d958-495d-98ea-8befd105a9a8
title: Создание образцов потоков из существующего объекта данных ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee612c9352e3295d6b4957922e385de40a9a1fa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143102"
---
# <a name="generating-stream-samples-from-an-existing-asf-data-object"></a><span data-ttu-id="4634c-103">Создание образцов потоков из существующего объекта данных ASF</span><span class="sxs-lookup"><span data-stu-id="4634c-103">Generating Stream Samples from an Existing ASF Data Object</span></span>

<span data-ttu-id="4634c-104">Объект- *Разделитель* ASF — это компонент уровня вмконтаинер, который анализирует объект данных ASF в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="4634c-104">The ASF *splitter* object is a WMContainer layer component that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="4634c-105">Перед передачей пакетов данных в разделитель приложение должно инициализировать, настроить и выбрать потоки в разделителе, чтобы подготовить их для процесса анализа.</span><span class="sxs-lookup"><span data-stu-id="4634c-105">Before passing data packets to the splitter, the application must initialize, configure, and select streams on the splitter in order to prepare it for the parsing process.</span></span> <span data-ttu-id="4634c-106">Дополнительные сведения см. в разделе [Создание объекта РАЗДЕЛИТЕЛЯ ASF](creating-the-asf-splitter-object.md) и [Настройка объекта разделителя ASF](configuring-the-asf-splitter-object.md).</span><span class="sxs-lookup"><span data-stu-id="4634c-106">For information, see [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md) and [Configuring the ASF Splitter Object](configuring-the-asf-splitter-object.md).</span></span>

<span data-ttu-id="4634c-107">Ниже перечислены методы, необходимые для синтаксического анализа объекта данных ASF.</span><span class="sxs-lookup"><span data-stu-id="4634c-107">The methods required for parsing the ASF Data Object are:</span></span>

-   <span data-ttu-id="4634c-108">[**Имфасфсплиттер::P арседата**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) , который начинает процесс анализа путем помещения в разделитель буфера, содержащего пакеты данных.</span><span class="sxs-lookup"><span data-stu-id="4634c-108">[**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) that starts the parsing process by pushing the buffer containing data packets to the splitter.</span></span>
-   <span data-ttu-id="4634c-109">[**Имфасфсплиттер:: жетнекстсампле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) , собирающий потоковые примеры, созданные из буфера, переданного в разделитель.</span><span class="sxs-lookup"><span data-stu-id="4634c-109">[**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) that collects stream samples that were generated from the buffer passed to splitter.</span></span>

## <a name="finding-the-data-offset"></a><span data-ttu-id="4634c-110">Поиск смещения данных</span><span class="sxs-lookup"><span data-stu-id="4634c-110">Finding the Data Offset</span></span>

<span data-ttu-id="4634c-111">Перед началом процесса анализа приложение должно располагать объект данных в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="4634c-111">Before starting the parsing process, the application must locate the Data Object within the ASF file.</span></span> <span data-ttu-id="4634c-112">Существует два способа получить смещение объекта данных от начала файла:</span><span class="sxs-lookup"><span data-stu-id="4634c-112">There are two ways to get the offset of the Data Object from the start of the file:</span></span>

-   <span data-ttu-id="4634c-113">Перед инициализацией объекта Контентинфо можно вызвать метод [**имфасфконтентинфо:: жесеадерсизе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) .</span><span class="sxs-lookup"><span data-stu-id="4634c-113">Before you have initialized the ContentInfo object, you can call the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="4634c-114">Для этого метода требуется буфер, который содержит первые 30 байт заголовка ASF.</span><span class="sxs-lookup"><span data-stu-id="4634c-114">This method requires a buffer that contains the first 30 bytes of the ASF header.</span></span> <span data-ttu-id="4634c-115">Он возвращает размер всего заголовка, указывающего смещение первого пакета данных.</span><span class="sxs-lookup"><span data-stu-id="4634c-115">It returns the size of the entire header that indicates the offset to the first data packet.</span></span> <span data-ttu-id="4634c-116">Это значение также включает размер заголовка объекта данных 50 байт.</span><span class="sxs-lookup"><span data-stu-id="4634c-116">This value also includes the Data Object header size of 50 bytes.</span></span>
-   <span data-ttu-id="4634c-117">После инициализации объекта Контентинфо можно получить дескриптор представления, вызвав [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor), а затем запросив дескриптор представления для атрибута [**\_ \_ \_ \_ \_ смещения начальной загрузки данных MF PD ASF**](mf-pd-asf-data-start-offset-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="4634c-117">After you have initialized the ContentInfo object, you can get the presentation descriptor by calling [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor), and then querying the presentation descriptor for the [**MF\_PD\_ASF\_DATA\_START\_OFFSET**](mf-pd-asf-data-start-offset-attribute.md) attribute.</span></span> <span data-ttu-id="4634c-118">Значением этого атрибута является размер заголовка.</span><span class="sxs-lookup"><span data-stu-id="4634c-118">The value of this attribute is the header size.</span></span>
    > [!Note]  
    > <span data-ttu-id="4634c-119">Атрибут [**\_ \_ \_ \_ длины данных в формате MF PD ASF**](mf-pd-asf-data-length-attribute.md) в дескрипторе представления определяет длину объекта данных ASF.</span><span class="sxs-lookup"><span data-stu-id="4634c-119">The [**MF\_PD\_ASF\_DATA\_LENGTH**](mf-pd-asf-data-length-attribute.md) attribute on the presentation descriptor specifies the length of the ASF Data Object.</span></span>

     

<span data-ttu-id="4634c-120">В обоих случаях возвращаемое значение — это размер объекта заголовка плюс размер раздела заголовка объекта данных.</span><span class="sxs-lookup"><span data-stu-id="4634c-120">In both cases, the returned value is the size of the Header Object plus the size of the header section of the Data Object.</span></span> <span data-ttu-id="4634c-121">Таким образом, полученное значение является смещением к началу пакетов данных в объекте данных ASF.</span><span class="sxs-lookup"><span data-stu-id="4634c-121">Therefore, the resulting value is the offset to the start of the data packets in the ASF Data Object.</span></span> <span data-ttu-id="4634c-122">После начала отправки данных в разделитель данные должны начинаться с этого смещения с начала файла ASF.</span><span class="sxs-lookup"><span data-stu-id="4634c-122">When you begin sending data to the splitter, the data must start at this offset from the beginning of the ASF file.</span></span>

<span data-ttu-id="4634c-123">Значение смещения передается в качестве параметра в **парседата** , который начинает процесс анализа.</span><span class="sxs-lookup"><span data-stu-id="4634c-123">The offset value is passed as a parameter to **ParseData** that starts the parsing process.</span></span>

<span data-ttu-id="4634c-124">Объект данных делится на пакеты данных.</span><span class="sxs-lookup"><span data-stu-id="4634c-124">The Data Object is divided into data packets.</span></span> <span data-ttu-id="4634c-125">Каждый пакет данных содержит заголовок пакета данных, который предоставляет сведения о синтаксическом анализе пакетов и полезных данных — фактические данные цифрового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4634c-125">Each data packet contains a data packet header that provides packet parsing information and the payload data—the actual digital media data.</span></span> <span data-ttu-id="4634c-126">В сценарии поиска приложению может потребоваться, чтобы разделитель начал синтаксический анализ в определенном пакете данных.</span><span class="sxs-lookup"><span data-stu-id="4634c-126">In a seeking scenario, the application might want the splitter to start parsing at a particular data packet.</span></span> <span data-ttu-id="4634c-127">Для этого можно использовать индексатор ASF для получения смещения.</span><span class="sxs-lookup"><span data-stu-id="4634c-127">To do this, you can use the ASF Indexer is used to retrieve the offset.</span></span> <span data-ttu-id="4634c-128">Индексатор возвращает значение смещения, которое начинается с границы пакета.</span><span class="sxs-lookup"><span data-stu-id="4634c-128">The indexer returns an offset value that starts at the packet boundary.</span></span> <span data-ttu-id="4634c-129">Если индексатор не используется, убедитесь, что смещение начинается в начале заголовка пакета данных.</span><span class="sxs-lookup"><span data-stu-id="4634c-129">If you are not using the indexer, make sure that the offset starts at the start of the data packet header.</span></span> <span data-ttu-id="4634c-130">Если в разделитель передается недопустимое смещение, например, значение не указывает на границу пакета, вызовы **парсехеадер** и **жетнекстсампле** выполняются успешно, но **жетнекстсампле** не получает никаких выборок и принимает **значение NULL** в параметре *псампле* .</span><span class="sxs-lookup"><span data-stu-id="4634c-130">If an invalid offset is passed to the splitter, such as the value does not point at the packet boundary, **ParseHeader** and **GetNextSample** calls succeed but **GetNextSample** does not retrieve any samples and **NULL** is received in the *pSample* parameter.</span></span>

<span data-ttu-id="4634c-131">Если разделитель настроен для синтаксического анализа в обратном направлении, разделитель всегда начинает анализ в конце буфера мультимедиа, который передается в **парседата**.</span><span class="sxs-lookup"><span data-stu-id="4634c-131">If the splitter is configured to parse in the reverse direction, then the splitter always starts parsing at the end of the media buffer that is passed to **ParseData**.</span></span> <span data-ttu-id="4634c-132">Таким образом, для отмены синтаксического анализа в вызове **парседата** передайте смещение в параметре *кбленгс* , который задает длину данных и устанавливает *кббуффероффсет* в ноль.</span><span class="sxs-lookup"><span data-stu-id="4634c-132">Therefore, for reverse parsing in the call to **ParseData**, pass the offset in the *cbLength* parameter, which specifies the length of the data and set *cbBufferOffset* to zero.</span></span>

## <a name="generating-samples-for-asf-data-packets"></a><span data-ttu-id="4634c-133">Создание образцов для пакетов данных ASF</span><span class="sxs-lookup"><span data-stu-id="4634c-133">Generating Samples for ASF Data Packets</span></span>

<span data-ttu-id="4634c-134">Приложение начинает процесс синтаксического анализа, передавая пакеты данных в разделитель.</span><span class="sxs-lookup"><span data-stu-id="4634c-134">An application starts the parsing process by passing the data packets to the splitter.</span></span> <span data-ttu-id="4634c-135">Входные данные для разделителя — это ряд буферов мультимедиа, содержащих все фрагменты объекта данных или.</span><span class="sxs-lookup"><span data-stu-id="4634c-135">The input to the splitter is a series of media buffers that contain the entire or fragments of the Data Object.</span></span> <span data-ttu-id="4634c-136">Выходные данные разделителя — это ряд примеров мультимедиа, содержащих данные пакета.</span><span class="sxs-lookup"><span data-stu-id="4634c-136">The output from the splitter is a series of media samples that contain the packet data.</span></span>

<span data-ttu-id="4634c-137">Чтобы передать входные данные в разделитель, создайте буфер мультимедиа и заполните его данными из раздела "объект данных" ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="4634c-137">To pass input data to the splitter, create a media buffer and fill it with data from the Data Object section of the ASF file.</span></span> <span data-ttu-id="4634c-138">(Дополнительные сведения о буферах мультимедиа см. в разделе [буферы мультимедиа](media-buffers.md).) Затем передайте буфер мультимедиа методу [**имфасфсплиттер::P арседата**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) .</span><span class="sxs-lookup"><span data-stu-id="4634c-138">(For more information about media buffers, see [Media Buffers](media-buffers.md).) Then, pass the media buffer to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="4634c-139">Также можно указать:</span><span class="sxs-lookup"><span data-stu-id="4634c-139">You can also specify:</span></span>

-   <span data-ttu-id="4634c-140">Смещение в буфере, с которого разделитель должен начать анализ.</span><span class="sxs-lookup"><span data-stu-id="4634c-140">The offset into the buffer where the splitter should start parsing.</span></span> <span data-ttu-id="4634c-141">Если смещение равно нулю, анализ начинается в начале буфера.</span><span class="sxs-lookup"><span data-stu-id="4634c-141">If the offset is zero, parsing begins at the start of the buffer.</span></span> <span data-ttu-id="4634c-142">Дополнительные сведения о настройке смещения данных см. в подразделе «Поиск смещения данных» этого раздела.</span><span class="sxs-lookup"><span data-stu-id="4634c-142">For information about setting the data offset, see the "Finding the Data Offset" section in this topic.</span></span>
-   <span data-ttu-id="4634c-143">Объем анализируемых данных.</span><span class="sxs-lookup"><span data-stu-id="4634c-143">The amount of data to parse.</span></span> <span data-ttu-id="4634c-144">Если это значение равно нулю, разделитель анализируется до достижения конца буфера, как указано в методе [**имфмедиабуффер:: жеткуррентленгс**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) .</span><span class="sxs-lookup"><span data-stu-id="4634c-144">If this value is zero, the splitter parses until it reaches the end of the buffer, as specified by the [**IMFMediaBuffer::GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) method.</span></span>

<span data-ttu-id="4634c-145">Разделитель создает образцы мультимедиа, ссылаясь на данные в буферах мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4634c-145">The splitter generates media samples by referencing the data in the media buffers.</span></span> <span data-ttu-id="4634c-146">Клиент может получить выходные примеры, вызвав [**имфасфсплиттер:: жетнекстсампле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) в цикле, пока не будет больше данных для синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="4634c-146">The client can retrieve the output samples by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in a loop until there is no more data to parse.</span></span> <span data-ttu-id="4634c-147">Если **жетнекстсампле** возвращает \_ \_ флаг статусфлагс неполный ASF в параметре *пдвстатусфлагс* , это означает, что есть больше примеров для извлечения, и приложение может снова вызвать **жетнекстсампле** .</span><span class="sxs-lookup"><span data-stu-id="4634c-147">If **GetNextSample** returns the ASF\_STATUSFLAGS\_INCOMPLETE flag in the *pdwStatusFlags* parameter, it means there are more samples to retrieve, and the application can call **GetNextSample** again.</span></span> <span data-ttu-id="4634c-148">В противном случае вызовите **парседата** , чтобы передать больше данных в разделитель.</span><span class="sxs-lookup"><span data-stu-id="4634c-148">Otherwise, call **ParseData** to pass more data to the splitter.</span></span> <span data-ttu-id="4634c-149">Для созданных образцов разделитель задает следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="4634c-149">For the generated samples, the splitter sets the following information:</span></span>

-   <span data-ttu-id="4634c-150">Разделитель задает отметку времени для всех создаваемых образцов.</span><span class="sxs-lookup"><span data-stu-id="4634c-150">The splitter sets a time stamp on all the samples that it generates.</span></span> <span data-ttu-id="4634c-151">Время образца представляет время презентации и не включает в себя время предподготовки.</span><span class="sxs-lookup"><span data-stu-id="4634c-151">The sample time represents the presentation time and does not include the preroll time.</span></span> <span data-ttu-id="4634c-152">Приложение может вызвать [**имфсампле:: жетсамплетиме**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) , чтобы получить время презентации в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="4634c-152">The application can call [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) to get the presentation time, in 100-nanosecond units.</span></span>
-   <span data-ttu-id="4634c-153">Если прерывание происходит во время создания образца, разделитель задает атрибут [**Немфсампликстенсионности \_**](mfsampleextension-discontinuity-attribute.md) в первом примере после прекращения его выполнения.</span><span class="sxs-lookup"><span data-stu-id="4634c-153">If a break occurs during sample generation, the splitter sets the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute on the first sample after the discontinuity.</span></span> <span data-ttu-id="4634c-154">Прекращение обычно вызывается отброшенными пакетами сетевого подключения, повреждением данных файлов или переключением разделителя из одного исходного потока в другой.</span><span class="sxs-lookup"><span data-stu-id="4634c-154">Discontinuities are usually caused by dropped packets on a network connection, corrupt file data, or the splitter switching from one source stream to another.</span></span>
-   <span data-ttu-id="4634c-155">Для видео разделитель проверяет, содержит ли пример ключевой кадр.</span><span class="sxs-lookup"><span data-stu-id="4634c-155">For video, the splitter checks whether the sample contains a key frame.</span></span> <span data-ttu-id="4634c-156">Если это так, разделитель устанавливает атрибут [**мфсампликстенсион \_ клеанпоинт**](mfsampleextension-cleanpoint-attribute.md) в образце.</span><span class="sxs-lookup"><span data-stu-id="4634c-156">If it does, the splitter sets the [**MFSampleExtension\_CleanPoint**](mfsampleextension-cleanpoint-attribute.md) attribute on the sample.</span></span>

<span data-ttu-id="4634c-157">Если разделитель анализирует пакеты данных, полученные с сервера мультимедиа, длина пакета может быть переменной.</span><span class="sxs-lookup"><span data-stu-id="4634c-157">If the splitter is parsing data packets that are received from a media server, it is possible that the packet length is variable.</span></span> <span data-ttu-id="4634c-158">В этом случае клиент должен вызвать **парседата** для каждого пакета и установить атрибут [**\_ \_ границы пакета мфасфсплиттер**](mfasfsplitter-packet-boundary-attribute.md) в каждом буфере, который отправляется в разделитель.</span><span class="sxs-lookup"><span data-stu-id="4634c-158">In this case, the client must call **ParseData** for each packet and set the [**MFASFSPLITTER\_PACKET\_BOUNDARY**](mfasfsplitter-packet-boundary-attribute.md) attribute on each buffer that is sent to the splitter.</span></span> <span data-ttu-id="4634c-159">Этот атрибут указывает элементу Splitter, содержит ли буфер мультимедиа начало пакета ASF.</span><span class="sxs-lookup"><span data-stu-id="4634c-159">This attribute indicates to the splitter whether the media buffer contains the start of an ASF packet.</span></span> <span data-ttu-id="4634c-160">Присвойте атрибуту **значение true** , если в буфере содержится начало нового пакета.</span><span class="sxs-lookup"><span data-stu-id="4634c-160">Set the attribute to **TRUE** if the buffer contains the start of a new packet.</span></span> <span data-ttu-id="4634c-161">Если буфер содержит продолжение предыдущего пакета, присвойте атрибуту **значение false**.</span><span class="sxs-lookup"><span data-stu-id="4634c-161">If the buffer contains a continuation of the previous packet, set the attribute to **FALSE**.</span></span> <span data-ttu-id="4634c-162">Буферы не могут охватывать несколько пакетов.</span><span class="sxs-lookup"><span data-stu-id="4634c-162">The buffers cannot span multiple packets.</span></span>

<span data-ttu-id="4634c-163">Перед передачей новых буферов мультимедиа в разделитель приложение должно вызвать [**имфасфсплиттер:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush).</span><span class="sxs-lookup"><span data-stu-id="4634c-163">Before passing new media buffers to the splitter, the application must call [**IMFASFSplitter::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush).</span></span> <span data-ttu-id="4634c-164">Этот метод сбрасывает разделитель и очищает любой частичный кадр, который ожидает завершения.</span><span class="sxs-lookup"><span data-stu-id="4634c-164">This method resets the splitter and clears any partial frame that is waiting to be completed.</span></span> <span data-ttu-id="4634c-165">Это полезно в сценарии поиска, когда смещение находится в другом месте.</span><span class="sxs-lookup"><span data-stu-id="4634c-165">This is useful in a seeking scenario where the offset is at a different location.</span></span>

### <a name="example"></a><span data-ttu-id="4634c-166">Пример</span><span class="sxs-lookup"><span data-stu-id="4634c-166">Example</span></span>

<span data-ttu-id="4634c-167">В следующем примере кода показано, как анализировать пакеты данных.</span><span class="sxs-lookup"><span data-stu-id="4634c-167">The following code example shows how to parse data packets.</span></span> <span data-ttu-id="4634c-168">В этом примере выполняется анализ с начала объекта данных до конца потока и отображаются сведения о примерах, содержащих ключевые кадры.</span><span class="sxs-lookup"><span data-stu-id="4634c-168">This example parses from the beginning of the Data Object to the end of the stream and displays information about the samples that contain key frames.</span></span> <span data-ttu-id="4634c-169">Полный пример использования этого кода см. в разделе [учебник. чтение файла ASF](tutorial--reading-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="4634c-169">For a complete example that uses this code, see [Tutorial: Reading an ASF File](tutorial--reading-an-asf-file.md).</span></span>


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="4634c-170">См. также</span><span class="sxs-lookup"><span data-stu-id="4634c-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4634c-171">Разделитель ASF</span><span class="sxs-lookup"><span data-stu-id="4634c-171">ASF Splitter</span></span>](asf-splitter.md)
</dt> </dl>

 

 



