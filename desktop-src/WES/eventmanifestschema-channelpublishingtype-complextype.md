---
title: Сложный тип Чаннелпублишингтипе
description: Определяет свойства ведения журнала для сеанса, используемого каналом. | Сложный тип Чаннелпублишингтипе
ms.assetid: 4b3980f4-8652-4070-97c0-99cd1a9fc85a
keywords:
- Журнал событий сложных типов Чаннелпублишингтипе
topic_type:
- apiref
api_name:
- ChannelPublishingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af84685f25705f6f8c54a85b9befb6df791593ed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694054"
---
# <a name="channelpublishingtype-complex-type"></a><span data-ttu-id="c15e2-105">Сложный тип Чаннелпублишингтипе</span><span class="sxs-lookup"><span data-stu-id="c15e2-105">ChannelPublishingType Complex Type</span></span>

<span data-ttu-id="c15e2-106">Определяет свойства ведения журнала для сеанса, используемого каналом.</span><span class="sxs-lookup"><span data-stu-id="c15e2-106">Defines the logging properties for the session that the channel uses.</span></span>

``` syntax
<xs:complexType name="ChannelPublishingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="level"
            type="UInt8Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="UInt64Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="controlGuid"
            type="GUIDType"
            minOccurs="0"
         />
        <xs:element name="bufferSize"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="minBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="fileMax"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="maxBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="latency"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="clockType"
            default="SystemTime"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="SystemTime"
                     />
                    <xs:enumeration
                        value="QPC"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="sidType"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="None"
                     />
                    <xs:enumeration
                        value="Publishing"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c15e2-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c15e2-107">Child elements</span></span>



| <span data-ttu-id="c15e2-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="c15e2-108">Element</span></span>                                                                              | <span data-ttu-id="c15e2-109">Тип</span><span class="sxs-lookup"><span data-stu-id="c15e2-109">Type</span></span>                                                              | <span data-ttu-id="c15e2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c15e2-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c15e2-111">**bufferSize**</span><span class="sxs-lookup"><span data-stu-id="c15e2-111">**bufferSize**</span></span>](eventmanifestschema-buffersize-channelpublishingtype-element.md)   | [<span data-ttu-id="c15e2-112">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="c15e2-112">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="c15e2-113">Объем памяти (в килобайтах), выделяемой для каждого буфера.</span><span class="sxs-lookup"><span data-stu-id="c15e2-113">The amount of memory, in kilobytes, to allocate for each buffer.</span></span> <span data-ttu-id="c15e2-114">Если предполагается относительно низкий уровень событий, размер буфера должен быть установлен на размер страницы памяти.</span><span class="sxs-lookup"><span data-stu-id="c15e2-114">If you expect a relatively low event rate, the buffer size should be set to the memory page size.</span></span> <span data-ttu-id="c15e2-115">Если ожидается, что частота событий будет относительно высока, необходимо указать больший размер буфера и увеличить максимальное число буферов.</span><span class="sxs-lookup"><span data-stu-id="c15e2-115">If the event rate is expected to be relatively high, you should specify a larger buffer size and increase the maximum number of buffers.</span></span><br/> <span data-ttu-id="c15e2-116">Размер буфера влияет на скорость заполнения буферов и должна быть сброшена.</span><span class="sxs-lookup"><span data-stu-id="c15e2-116">The buffer size affects the rate at which buffers fill and must be flushed.</span></span> <span data-ttu-id="c15e2-117">Хотя для небольшого размера буфера требуется меньше памяти, это увеличивает скорость, с которой буферы должны быть сброшены.</span><span class="sxs-lookup"><span data-stu-id="c15e2-117">Although a small buffer size requires less memory, it increases the rate at which buffers must be flushed.</span></span><br/> <span data-ttu-id="c15e2-118">Размер буфера по умолчанию для аналитических и отладочных каналов составляет 4 КБ, а для администратора и рабочей области — 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="c15e2-118">The default buffer size for Analytic and Debug channels is 4 KB and for Admin and Operational it is 64 KB.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="c15e2-119">**клокктипе**</span><span class="sxs-lookup"><span data-stu-id="c15e2-119">**clockType**</span></span>](eventmanifestschema-clocktype-channelpublishingtype-element.md)     |                                                                   | <span data-ttu-id="c15e2-120">Разрешение часов, используемое при записи метки времени для каждого события.</span><span class="sxs-lookup"><span data-stu-id="c15e2-120">The clock resolution to use when logging the time stamp for each event.</span></span> <span data-ttu-id="c15e2-121">Можно указать SystemTime или QPC.</span><span class="sxs-lookup"><span data-stu-id="c15e2-121">You can specify SystemTime or QPC.</span></span> <span data-ttu-id="c15e2-122">SystemTime предоставляет отметку времени с низким разрешением (10 миллисекунд), но она сравнительно дешевле извлекать.</span><span class="sxs-lookup"><span data-stu-id="c15e2-122">SystemTime provides a low-resolution (10 milliseconds) time stamp but is comparatively less expensive to retrieve.</span></span> <span data-ttu-id="c15e2-123">Значение по умолчанию — SystemTime.</span><span class="sxs-lookup"><span data-stu-id="c15e2-123">The default is SystemTime.</span></span> <br/> <span data-ttu-id="c15e2-124">Счетчик производительности запросов (QPC) предоставляет отметку времени высокого разрешения (100 наносекунд), но она сравнительно важна для получения.</span><span class="sxs-lookup"><span data-stu-id="c15e2-124">Query performance counter (QPC) provides a high-resolution (100 nanoseconds) time stamp but is comparatively more expensive to retrieve.</span></span> <span data-ttu-id="c15e2-125">При наличии высокой частоты событий или при слиянии событий из разных буферов потребитель должен QPC.</span><span class="sxs-lookup"><span data-stu-id="c15e2-125">You should QPC if you have high event rates or if the consumer merges events from different buffers.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="c15e2-126">**контролгуид**</span><span class="sxs-lookup"><span data-stu-id="c15e2-126">**controlGuid**</span></span>](eventmanifestschema-controlguid-channelpublishingtype-element.md) | [<span data-ttu-id="c15e2-127">**гуидтипе**</span><span class="sxs-lookup"><span data-stu-id="c15e2-127">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="c15e2-128">Определяет идентификатор GUID сеанса для сеанса ETW, содержащего события WPP.</span><span class="sxs-lookup"><span data-stu-id="c15e2-128">Identifies the session GUID for an ETW session that contains WPP events.</span></span> <span data-ttu-id="c15e2-129">Этот параметр разрешен только для каналов типа "Отладка".</span><span class="sxs-lookup"><span data-stu-id="c15e2-129">This setting is only allowed for channels of type Debug.</span></span> <span data-ttu-id="c15e2-130">Эти каналы нельзя полностью включить, если ключевые слова имеют нулевое значение (0x0000000000000000).</span><span class="sxs-lookup"><span data-stu-id="c15e2-130">These channels cannot be fully enabled with keywords set to zero (0x0000000000000000).</span></span> <span data-ttu-id="c15e2-131">Они должны быть включены с ключевыми словами, для которых задано значение 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="c15e2-131">They must be enabled with keywords set to 0xffffffffffffffff.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="c15e2-132">**филемакс**</span><span class="sxs-lookup"><span data-stu-id="c15e2-132">**fileMax**</span></span>                                                                          | [<span data-ttu-id="c15e2-133">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="c15e2-133">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="c15e2-134">Максимальное количество случаев, когда служба должна создавать новый файл журнала при включении канала (включается при перезапуске компьютера).</span><span class="sxs-lookup"><span data-stu-id="c15e2-134">The maximum number of times that you want the service to create a new log file when the channel is enabled (includes when the computer is restarted).</span></span> <span data-ttu-id="c15e2-135">Если значение равно 0 или 1, то при каждом включении канала служба будет перезаписывать файл журнала, а предыдущие события будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="c15e2-135">If the value is 0 or 1, the service will overwrite the log file each time the channel is enabled and the previous events will be lost.</span></span> <span data-ttu-id="c15e2-136">Если значение больше 1, служба создает новый файл журнала каждый раз, когда канал будет включен, чтобы сохранить события.</span><span class="sxs-lookup"><span data-stu-id="c15e2-136">If the value is greater than 1, the service will create a new log file each time the channel is enabled in order to preserve the events.</span></span> <span data-ttu-id="c15e2-137">Значение по умолчанию — 1, а максимальное — 16.</span><span class="sxs-lookup"><span data-stu-id="c15e2-137">The default is 1 and the maximum that you can specify is 16.</span></span><br/> <span data-ttu-id="c15e2-138">Служба добавляет три цифры десятичное число от 0 до Филемакс 1 к каждому имени файла.</span><span class="sxs-lookup"><span data-stu-id="c15e2-138">The service appends a three digit decimal number between 0 and fileMax 1 to each file name.</span></span> <span data-ttu-id="c15e2-139">Например, *filename*. ETL.XXX, где XXX — это десятичное число с тремя цифрами.</span><span class="sxs-lookup"><span data-stu-id="c15e2-139">For example, *filename*.etl.xxx, where xxx is the three digit decimal number.</span></span> <span data-ttu-id="c15e2-140">Файлы находятся в журналах% WINDIR% \\ system32 \\ виневт \\ .</span><span class="sxs-lookup"><span data-stu-id="c15e2-140">The files are located in %windir%\\System32\\winevt\\Logs.</span></span><br/> |
| [<span data-ttu-id="c15e2-141">**словами**</span><span class="sxs-lookup"><span data-stu-id="c15e2-141">**keywords**</span></span>](eventmanifestschema-keywords-channelpublishingtype-element.md)       | [<span data-ttu-id="c15e2-142">**UInt64Type**</span><span class="sxs-lookup"><span data-stu-id="c15e2-142">**UInt64Type**</span></span>](eventmanifestschema-hexint64type-simpletype.md) | <span data-ttu-id="c15e2-143">Битовая маска, определяющая категорию событий, записываемых в канал.</span><span class="sxs-lookup"><span data-stu-id="c15e2-143">A bitmask that determines the category of events that are written to the channel.</span></span> <span data-ttu-id="c15e2-144">Если значение атрибута **keywords** равно 0, то все события, записываемые поставщиком, записываются в канал. в противном случае в канал записываются только те события, в которых определено ключевое слово, включенное в битовую маску **ключевых слов** .</span><span class="sxs-lookup"><span data-stu-id="c15e2-144">If the value of **keywords** attribute is 0, all events that the provider writes are written to the channel; otherwise only events that have defined a keyword that is included in the **keywords** bitmask are written to the channel.</span></span> <span data-ttu-id="c15e2-145">Значение по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="c15e2-145">The default is 0.</span></span><br/> <span data-ttu-id="c15e2-146">Для отладочных каналов, которые имеют набор атрибутов Контролгуид, необходимо задать атрибуту **keywords** значение 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="c15e2-146">Debug channels that have the controlGuid attribute set must set the **keywords** attribute to 0xFFFFFFFFFFFFFFFF.</span></span><br/> <span data-ttu-id="c15e2-147">Сеанс передает значение ключевых слов поставщику, когда он включает поставщик.</span><span class="sxs-lookup"><span data-stu-id="c15e2-147">The session passes the keywords value to the provider when it enables the provider.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="c15e2-148">**явно**</span><span class="sxs-lookup"><span data-stu-id="c15e2-148">**latency**</span></span>](eventmanifestschema-latency-channelpublishingtype-element.md)         | [<span data-ttu-id="c15e2-149">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="c15e2-149">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="c15e2-150">Время ожидания перед очисткой буферов (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="c15e2-150">The time to wait before flushing the buffers, in milliseconds.</span></span> <span data-ttu-id="c15e2-151">Если значение равно нулю, ETW очищает буферы, как только они становятся заполненными.</span><span class="sxs-lookup"><span data-stu-id="c15e2-151">If zero, ETW flushes the buffers as soon as they become full.</span></span> <span data-ttu-id="c15e2-152">Если значение не равно нулю, ETW очищает все буферы, содержащие события, на основе значения, даже если буфер не полон.</span><span class="sxs-lookup"><span data-stu-id="c15e2-152">If nonzero, ETW flushes all buffers that contain events based on the value even if the buffer is not full.</span></span> <span data-ttu-id="c15e2-153">Как правило, необходимо очищать буферы только в том случае, если они заполнены.</span><span class="sxs-lookup"><span data-stu-id="c15e2-153">Typically, you want to flush buffers only when they become full.</span></span> <span data-ttu-id="c15e2-154">Принудительная очистка буферов может привести к увеличению размера файла журнала с незаполненным буферным пространством.</span><span class="sxs-lookup"><span data-stu-id="c15e2-154">Forcing the buffers to flush can increase the file size of the log file with unfilled buffer space.</span></span> <span data-ttu-id="c15e2-155">Значение по умолчанию — 1 секунда для администраторов и операционных журналов и 5 секунд для журналов аналитики и отладки.</span><span class="sxs-lookup"><span data-stu-id="c15e2-155">The default value is 1 second for Admin and Operational logs and 5 seconds for Analytic and Debug logs.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="c15e2-156">**уровень**</span><span class="sxs-lookup"><span data-stu-id="c15e2-156">**level**</span></span>](eventmanifestschema-level-channelpublishingtype-element.md)             | [<span data-ttu-id="c15e2-157">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="c15e2-157">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="c15e2-158">Степень серьезности событий, записываемых в канал.</span><span class="sxs-lookup"><span data-stu-id="c15e2-158">The severity level of the events to write to the channel.</span></span> <span data-ttu-id="c15e2-159">Служба записывает события в канал со значением уровня, которое меньше или равно указанному значению.</span><span class="sxs-lookup"><span data-stu-id="c15e2-159">The service writes events to the channel that have a level value that is less than or equal to the specified value.</span></span> <span data-ttu-id="c15e2-160">Значение по умолчанию равно 0, что означает запись событий с любым уровнем.</span><span class="sxs-lookup"><span data-stu-id="c15e2-160">The default is 0, which means to log events with any level value.</span></span><br/> <span data-ttu-id="c15e2-161">Сеанс передает значение уровня поставщику, когда он включает поставщик.</span><span class="sxs-lookup"><span data-stu-id="c15e2-161">The session passes the level value to the provider when it enables the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="c15e2-162">**максбуфферс**</span><span class="sxs-lookup"><span data-stu-id="c15e2-162">**maxBuffers**</span></span>](eventmanifestschema-maxbuffers-channelpublishingtype-element.md)   | [<span data-ttu-id="c15e2-163">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="c15e2-163">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="c15e2-164">Максимальное количество буферов, выделяемых для сеанса.</span><span class="sxs-lookup"><span data-stu-id="c15e2-164">The maximum number of buffers to allocate for the session.</span></span> <span data-ttu-id="c15e2-165">Обычно это значение является минимальным числом буферов плюс двадцать.</span><span class="sxs-lookup"><span data-stu-id="c15e2-165">Typically, this value is the minimum number of buffers plus twenty.</span></span> <span data-ttu-id="c15e2-166">Это значение должно быть больше или равно значению, указанному для Минбуфферс.</span><span class="sxs-lookup"><span data-stu-id="c15e2-166">This value must be greater than or equal to the value specified for minBuffers.</span></span><br/> <span data-ttu-id="c15e2-167">По умолчанию максимальное количество буферов для аналитических и отладочных каналов составляет 10 КБ, а для администратора и рабочего элемента — 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="c15e2-167">The default maximum number of buffers for Analytic and Debug channels is 10 KB and for Admin and Operational it is 64 KB.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="c15e2-168">**минбуфферс**</span><span class="sxs-lookup"><span data-stu-id="c15e2-168">**minBuffers**</span></span>](eventmanifestschema-minbuffers-channelpublishingtype-element.md)   | [<span data-ttu-id="c15e2-169">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="c15e2-169">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="c15e2-170">Минимальное число буферов, выделяемых для сеанса.</span><span class="sxs-lookup"><span data-stu-id="c15e2-170">The minimum number of buffers to allocate for the session.</span></span> <span data-ttu-id="c15e2-171">По умолчанию используется значение ноль.</span><span class="sxs-lookup"><span data-stu-id="c15e2-171">The default is zero.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="c15e2-172">**Идентификатор типа безопасности**</span><span class="sxs-lookup"><span data-stu-id="c15e2-172">**sidType**</span></span>](eventmanifestschema-sidtype-channelpublishingtype-element.md)         |                                                                   | <span data-ttu-id="c15e2-173">Определяет, следует ли включать идентификатор безопасности (SID) участника с каждым событием, записанным в канал.</span><span class="sxs-lookup"><span data-stu-id="c15e2-173">Determines whether to include a security identifier (SID) of the principal with each event written to the channel.</span></span> <span data-ttu-id="c15e2-174">Чтобы включить идентификатор безопасности в событие, задайте для этого атрибута значение "публикация".</span><span class="sxs-lookup"><span data-stu-id="c15e2-174">To include the SID with the event, set this attribute to "Publishing".</span></span> <span data-ttu-id="c15e2-175">Идентификатор безопасности задается на основе удостоверения потока во время записи события.</span><span class="sxs-lookup"><span data-stu-id="c15e2-175">The SID is set based on the thread identity at the time the event is written.</span></span> <span data-ttu-id="c15e2-176">Если вы не хотите включать идентификатор SID в событие, установите для этого атрибута значение "нет".</span><span class="sxs-lookup"><span data-stu-id="c15e2-176">If you do not want to include the SID with the event, set this attribute to "None".</span></span> <span data-ttu-id="c15e2-177">Значение по умолчанию — Publish.</span><span class="sxs-lookup"><span data-stu-id="c15e2-177">The default is "Publishing".</span></span><br/>                                                                                                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="c15e2-178">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c15e2-178">Remarks</span></span>

<span data-ttu-id="c15e2-179">Вы можете указать эту информацию публикации для типов каналов аналитики и отладки или для любого канала, который указывает пользовательскую изоляцию.</span><span class="sxs-lookup"><span data-stu-id="c15e2-179">You can specify this publishing information for Analytic and Debug channel types or for any channel that specifies Custom isolation.</span></span>

<span data-ttu-id="c15e2-180">Хотя можно указать уровень и ключевые слова, следует учитывать, что эти данные будут единственными событиями, которые будут получены от поставщика для этого канала.</span><span class="sxs-lookup"><span data-stu-id="c15e2-180">Although you can specify level and keywords, you should consider that these will be the only events that you will receive from the provider for that channel.</span></span>

<span data-ttu-id="c15e2-181">Когда буфер заполнен, ETW очищает буфер в файле журнала.</span><span class="sxs-lookup"><span data-stu-id="c15e2-181">When a buffer is full, ETW flushes the buffer to the log file.</span></span> <span data-ttu-id="c15e2-182">Если буферы заполняются быстрее, чем могут быть сброшены, новые буферы выделяются и добавляются в буферный пул сеанса вплоть до указанного максимального числа.</span><span class="sxs-lookup"><span data-stu-id="c15e2-182">If the buffers are filled faster than they can be flushed, new buffers are allocated and added to the session's buffer pool, up to the maximum number specified.</span></span> <span data-ttu-id="c15e2-183">За пределами этого ограничения сеанс отклоняет входящие события до тех пор, пока буфер не станет доступным.</span><span class="sxs-lookup"><span data-stu-id="c15e2-183">Beyond this limit, the session discards incoming events until a buffer becomes available.</span></span>

## <a name="requirements"></a><span data-ttu-id="c15e2-184">Требования</span><span class="sxs-lookup"><span data-stu-id="c15e2-184">Requirements</span></span>



| <span data-ttu-id="c15e2-185">Требование</span><span class="sxs-lookup"><span data-stu-id="c15e2-185">Requirement</span></span> | <span data-ttu-id="c15e2-186">Значение</span><span class="sxs-lookup"><span data-stu-id="c15e2-186">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c15e2-187">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c15e2-187">Minimum supported client</span></span><br/> | <span data-ttu-id="c15e2-188">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c15e2-188">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c15e2-189">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c15e2-189">Minimum supported server</span></span><br/> | <span data-ttu-id="c15e2-190">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c15e2-190">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





