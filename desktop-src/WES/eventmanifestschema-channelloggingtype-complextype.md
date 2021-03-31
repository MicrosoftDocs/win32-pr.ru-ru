---
title: Сложный тип Чаннеллоггингтипе
description: Определяет свойства файла журнала, который осуществляет резервное копирование канала, например его емкость и последовательный или циклический режим. | Сложный тип Чаннеллоггингтипе
ms.assetid: 58da75dd-d303-4a57-8c9b-5fde575c3cbb
keywords:
- Журнал событий сложных типов Чаннеллоггингтипе
topic_type:
- apiref
api_name:
- ChannelLoggingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4cfaf6dfa225799befcd0c7fb068c0f779ea33eb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104157115"
---
# <a name="channelloggingtype-complex-type"></a><span data-ttu-id="fa34b-105">Сложный тип Чаннеллоггингтипе</span><span class="sxs-lookup"><span data-stu-id="fa34b-105">ChannelLoggingType Complex Type</span></span>

<span data-ttu-id="fa34b-106">Определяет свойства файла журнала, который осуществляет резервное копирование канала, например его емкость и последовательный или циклический режим.</span><span class="sxs-lookup"><span data-stu-id="fa34b-106">Defines the properties of the log file that backs the channel, such as its capacity and whether it is sequential or circular.</span></span>

``` syntax
<xs:complexType name="ChannelLoggingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="autoBackup"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="retention"
            type="boolean"
            default="0"
            minOccurs="0"
         />
        <xs:element name="maxSize"
            type="UInt64Type"
            default="1048576"
            minOccurs="0"
         />
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

## <a name="child-elements"></a><span data-ttu-id="fa34b-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fa34b-107">Child elements</span></span>



| <span data-ttu-id="fa34b-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="fa34b-108">Element</span></span>                                                                         | <span data-ttu-id="fa34b-109">Тип</span><span class="sxs-lookup"><span data-stu-id="fa34b-109">Type</span></span>                                                              | <span data-ttu-id="fa34b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="fa34b-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa34b-111">**Автоматической архивации**</span><span class="sxs-lookup"><span data-stu-id="fa34b-111">**autoBackup**</span></span>](eventmanifestschema-autobackup-channelloggingtype-element.md) | <span data-ttu-id="fa34b-112">Логическое</span><span class="sxs-lookup"><span data-stu-id="fa34b-112">boolean</span></span>                                                           | <span data-ttu-id="fa34b-113">Определяет, следует ли создавать новый файл журнала, когда текущий файл журнала достигает максимального размера.</span><span class="sxs-lookup"><span data-stu-id="fa34b-113">Determines whether to create a new log file when the current log file reaches its maximum size.</span></span> <span data-ttu-id="fa34b-114">Задайте значение **true** , чтобы запросить, что служба создает новый файл, когда файл журнала достигает максимального размера. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="fa34b-114">Set to **true** to request that the service create a new file when the log file reaches its maximum size; otherwise, **false**.</span></span> <span data-ttu-id="fa34b-115">Параметр [**автоархивации**](eventmanifestschema-autobackup-channelloggingtype-element.md) можно установить в **значение true** , только если параметру [**retention**](eventmanifestschema-retention-channelloggingtype-element.md) присвоено значение **true**.</span><span class="sxs-lookup"><span data-stu-id="fa34b-115">You can set [**autoBackup**](eventmanifestschema-autobackup-channelloggingtype-element.md) to **true** only if [**retention**](eventmanifestschema-retention-channelloggingtype-element.md) is set to **true**.</span></span> <span data-ttu-id="fa34b-116">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="fa34b-116">The default is **false**.</span></span><br/> <span data-ttu-id="fa34b-117">Количество файлов резервных копий, которые может создать служба (ограничивается только доступным местом на диске), не ограничено.</span><span class="sxs-lookup"><span data-stu-id="fa34b-117">There is no limit to the number of backup files that the service can create (limited only by available disk space).</span></span> <span data-ttu-id="fa34b-118">Имена файлов резервных копий имеют формат Archive-*channelName* - *timestamp*. evtx и находятся в папке% WINDIR% \\ system32 \\ виневт \\ logs.</span><span class="sxs-lookup"><span data-stu-id="fa34b-118">The backup file names are of the form Archive-*channelName*-*timestamp*.evtx and are located in %windir%\\System32\\winevt\\Logs folder.</span></span><br/> |
| [<span data-ttu-id="fa34b-119">**maxSize**</span><span class="sxs-lookup"><span data-stu-id="fa34b-119">**maxSize**</span></span>](eventmanifestschema-maxsize-channelloggingtype-element.md)       | [<span data-ttu-id="fa34b-120">**UInt64Type**</span><span class="sxs-lookup"><span data-stu-id="fa34b-120">**UInt64Type**</span></span>](eventmanifestschema-hexint64type-simpletype.md) | <span data-ttu-id="fa34b-121">Максимальный размер файла журнала в байтах.</span><span class="sxs-lookup"><span data-stu-id="fa34b-121">The maximum size, in bytes, of the log file.</span></span> <span data-ttu-id="fa34b-122">Значение по умолчанию (и минимум) — 1 МБ.</span><span class="sxs-lookup"><span data-stu-id="fa34b-122">The default (and minimum) value is 1 MB.</span></span> <span data-ttu-id="fa34b-123">Если размер физического журнала меньше заданного максимального размера и требуется дополнительное пространство в журнале для хранения событий, служба выделит другой блок пространства, даже если итоговый физический размер журнала будет больше заданного максимального размера.</span><span class="sxs-lookup"><span data-stu-id="fa34b-123">If the physical log size is less than the configured maximum size and additional space is required in the log to store events, the service will allocate another block of space even if the resulting physical size of the log will be larger than the configured maximum size.</span></span> <span data-ttu-id="fa34b-124">Служба выделяет блоки размером 1 МБ, поэтому размер физического размера может дорасти до 1 МБ, превышающий заданный максимальный размер.</span><span class="sxs-lookup"><span data-stu-id="fa34b-124">The service allocates blocks of 1 MB so the physical size could grow to up to 1 MB larger than the configured max size.</span></span> <br/>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="fa34b-125">**хранения**</span><span class="sxs-lookup"><span data-stu-id="fa34b-125">**retention**</span></span>](eventmanifestschema-retention-channelloggingtype-element.md)   | <span data-ttu-id="fa34b-126">Логическое</span><span class="sxs-lookup"><span data-stu-id="fa34b-126">boolean</span></span>                                                           | <span data-ttu-id="fa34b-127">Определяет, является ли файл журнала последовательным или циклическим файлом журнала.</span><span class="sxs-lookup"><span data-stu-id="fa34b-127">Determines whether the log file is a sequential or circular log file.</span></span> <span data-ttu-id="fa34b-128">Задайте значение **true** для последовательного файла журнала и **значение false** для циклического файла журнала.</span><span class="sxs-lookup"><span data-stu-id="fa34b-128">Set to **true** for a sequential log file and **false** for a circular log file.</span></span> <span data-ttu-id="fa34b-129">Значение по умолчанию — **false** для типов администраторов и операционных каналов и **true** для типов каналов аналитики и отладки.</span><span class="sxs-lookup"><span data-stu-id="fa34b-129">The default is **false** for Admin and Operational channel types and **true** for Analytic and Debug channel types.</span></span><br/> <span data-ttu-id="fa34b-130">Для запроса циклического журнала необходимо сначала отключить канал.</span><span class="sxs-lookup"><span data-stu-id="fa34b-130">To query a circular log, you must first disable the channel.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="fa34b-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa34b-131">Remarks</span></span>

<span data-ttu-id="fa34b-132">Для любого типа канала можно указать атрибут **MAXSIZE** .</span><span class="sxs-lookup"><span data-stu-id="fa34b-132">You can specify the **maxSize** attribute for any channel type.</span></span>

<span data-ttu-id="fa34b-133">Атрибут **автоархивации** можно указать только для типов администрирования и операционные каналы.</span><span class="sxs-lookup"><span data-stu-id="fa34b-133">You can specify the **autoBackup** attribute only for Admin and Operational channel types.</span></span>

<span data-ttu-id="fa34b-134">Для атрибута **retention** можно задать значение false (циклическое ведение журнала) для типов администрирования и операционные каналы.</span><span class="sxs-lookup"><span data-stu-id="fa34b-134">You can set the **retention** attribute to false (circular logging) for Admin and Operational channel types.</span></span> <span data-ttu-id="fa34b-135">Для атрибута **retention** можно задать значение false (циклическое ведение журнала) для типовых каналов аналитики и отладки, но для просмотра событий в Просмотр событий Windows необходимо сначала отключить канал.</span><span class="sxs-lookup"><span data-stu-id="fa34b-135">You can set the **retention** attribute to false (circular logging) for Analytic and Debug channel types but to view the events in the Windows Event Viewer, you will need to first disable the channel.</span></span> <span data-ttu-id="fa34b-136">Обратите внимание, что при повторном включении канала события удаляются из канала.</span><span class="sxs-lookup"><span data-stu-id="fa34b-136">Note that when you enable the channel again, the events are removed from the channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa34b-137">Требования</span><span class="sxs-lookup"><span data-stu-id="fa34b-137">Requirements</span></span>



| <span data-ttu-id="fa34b-138">Требование</span><span class="sxs-lookup"><span data-stu-id="fa34b-138">Requirement</span></span> | <span data-ttu-id="fa34b-139">Значение</span><span class="sxs-lookup"><span data-stu-id="fa34b-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fa34b-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa34b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="fa34b-141">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa34b-141">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fa34b-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa34b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="fa34b-143">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fa34b-143">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





