---
title: Определение шаблонов данных событий
description: Поставщики используют шаблоны данных для определения данных событий, которые они включают в событие, и для определения данных фильтра, которые сеанс трассировки ETW может передать поставщику при включении поставщика.
ms.assetid: 064227a2-7ce8-461a-9dc0-7519652e6628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067230472c8de5ce29145e221c109b3f390f0a6c
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "103890328"
---
# <a name="defining-event-data-templates"></a><span data-ttu-id="9bda8-103">Определение шаблонов данных событий</span><span class="sxs-lookup"><span data-stu-id="9bda8-103">Defining Event Data Templates</span></span>

<span data-ttu-id="9bda8-104">Поставщики используют шаблоны данных для определения данных событий, которые они включают в событие, и для определения данных фильтра, которые сеанс трассировки ETW может передать поставщику при включении поставщика.</span><span class="sxs-lookup"><span data-stu-id="9bda8-104">Providers use data templates to define the event-specific data that they include with an event and to define the filter data that an ETW tracing session can pass to the provider when it enables the provider.</span></span> <span data-ttu-id="9bda8-105">Если событие не содержит данных, связанных с событиями, шаблон не будет определен.</span><span class="sxs-lookup"><span data-stu-id="9bda8-105">If the event does not include event-specific data, you will not define a template.</span></span> <span data-ttu-id="9bda8-106">Чтобы определить шаблон, используйте элемент **template** .</span><span class="sxs-lookup"><span data-stu-id="9bda8-106">To define a template, use the **template** element.</span></span> <span data-ttu-id="9bda8-107">Шаблон включает элемент данных для каждого элемента данных, который поставщик включает в событие.</span><span class="sxs-lookup"><span data-stu-id="9bda8-107">A template includes a data item for each piece of data that the provider includes with the event.</span></span> <span data-ttu-id="9bda8-108">Можно указать целочисленные типы, строки, массивы и структуры.</span><span class="sxs-lookup"><span data-stu-id="9bda8-108">You can specify integral types, strings, arrays, and structures.</span></span> <span data-ttu-id="9bda8-109">Данные событий необходимо записать в том порядке, в котором элементы данных были определены в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="9bda8-109">You must write the event data in the order that the data items were defined in the template.</span></span>

<span data-ttu-id="9bda8-110">Можно также включить в шаблон XML-фрагмент, который потребители должны использовать для определения способа отображения данных события.</span><span class="sxs-lookup"><span data-stu-id="9bda8-110">You can also include in the template, an XML fragment that consumers should use to determine how to render the event data.</span></span> <span data-ttu-id="9bda8-111">Если фрагмент не включен, потребители должны визуализировать данные событий в том порядке, в котором элементы данных были определены в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="9bda8-111">If you do not include the fragment, consumers should render the event data in the order that the data items were defined in the template.</span></span>

<span data-ttu-id="9bda8-112">При определении шаблона необходимо присвоить ему идентификатор шаблона, который используется для ссылки на шаблон в определении события.</span><span class="sxs-lookup"><span data-stu-id="9bda8-112">When you define a template, you must give it a template identifier that you use to reference the template in an event definition.</span></span> <span data-ttu-id="9bda8-113">Каждый элемент данных в шаблоне должен указывать имя и тип входных данных (список входных типов см. в разделе "Примечания" сложного типа [**InputType**](eventmanifestschema-inputtype-complextype.md) ).</span><span class="sxs-lookup"><span data-stu-id="9bda8-113">Each data item in the template must specify a name and input data type (for a list of input types, see the Remarks section of the [**InputType**](eventmanifestschema-inputtype-complextype.md) complex type).</span></span> <span data-ttu-id="9bda8-114">Если тип входных данных может быть визуализирован в нескольких форматах, следует указать тип выходных данных, который сообщает потребителям о том, как визуализировать элемент данных.</span><span class="sxs-lookup"><span data-stu-id="9bda8-114">If the input data type can be rendered in multiple formats, you should specify the output data type that tells consumers how to render the data item.</span></span> <span data-ttu-id="9bda8-115">Например, тип входных данных UInt32 можно визуализировать как целое число без знака, идентификатор потока, IPv4-адрес и код ошибки Win32.</span><span class="sxs-lookup"><span data-stu-id="9bda8-115">For example, an UInt32 input data type can be rendered as an unsigned integer, thread identifier, IPv4 address, and Win32 error code among others.</span></span> <span data-ttu-id="9bda8-116">Если тип выходных данных не указан, потребители должны использовать тип вывода по умолчанию входного типа для отрисовки элемента данных.</span><span class="sxs-lookup"><span data-stu-id="9bda8-116">If you do not specify the output data type, consumers should use the input type's default output type to render the data item.</span></span>

<span data-ttu-id="9bda8-117">Чтобы указать массив, включите атрибут **Count** в элемент данных и задайте для него число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="9bda8-117">To specify an array, include the **count** attribute on the data item and set it to the number of elements in the array.</span></span> <span data-ttu-id="9bda8-118">Массив может быть массивом размера переменной или массивом фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="9bda8-118">The array can be a variable size array or fixed size array.</span></span> <span data-ttu-id="9bda8-119">Если массив является массивом фиксированного размера, задайте для параметра **Count** значение size массива.</span><span class="sxs-lookup"><span data-stu-id="9bda8-119">If the array is a fixed size array, set **count** to the size of the array.</span></span> <span data-ttu-id="9bda8-120">Например, если массив целых чисел имеет фиксированный размер 10, установите значение **счетчика** равным 10.</span><span class="sxs-lookup"><span data-stu-id="9bda8-120">For example, if an array of integers has a fixed size of 10, set **count** to 10.</span></span> <span data-ttu-id="9bda8-121">При написании массива необходимо записать 40 байт данных.</span><span class="sxs-lookup"><span data-stu-id="9bda8-121">When you write the array, you must write 40 bytes of data.</span></span>

<span data-ttu-id="9bda8-122">Если массив является массивом размера переменной, задайте параметру **Count** имя элемента данных, который содержит размер массива.</span><span class="sxs-lookup"><span data-stu-id="9bda8-122">If the array is a variable size array, set **count** to the name of the data item that contains the size of the array.</span></span> <span data-ttu-id="9bda8-123">Если массив содержит указатели, адреса указателей записываются в виде данных события, а не данных, на которые указывает точка указателей.</span><span class="sxs-lookup"><span data-stu-id="9bda8-123">If the array contains pointers, the address of the pointers are written as the event data, not the data to which the pointers point.</span></span>

<span data-ttu-id="9bda8-124">Если элемент данных является двоичным BLOB-объектом, необходимо указать атрибут **length** .</span><span class="sxs-lookup"><span data-stu-id="9bda8-124">You must specify the **length** attribute if the data item is a binary blob.</span></span> <span data-ttu-id="9bda8-125">Можно также указать атрибут **length** для строк фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="9bda8-125">You can also specify the **length** attribute for fixed length strings.</span></span>

<span data-ttu-id="9bda8-126">Укажите атрибут **Map** , если элемент данных представляет значение перечисления, и вы хотите, чтобы потребитель печатал строку для значения, а не самого значения.</span><span class="sxs-lookup"><span data-stu-id="9bda8-126">Specify the **map** attribute if the data item represents an enumeration value and you want the consumer to print a string for the value instead of the value itself.</span></span>

<span data-ttu-id="9bda8-127">При включении структур в шаблон следует писать члены структуры по отдельности, а не писать структуру, если вы не гарантируете выравнивание по 8 байтам.</span><span class="sxs-lookup"><span data-stu-id="9bda8-127">If you include structures in the template, you should write the members of the structure individually instead of writing the structure unless you can guarantee 8-byte boundary alignment.</span></span>

<span data-ttu-id="9bda8-128">Следует тщательно продумать сведения, включаемые в события, особенно если события записываются в глобальные каналы.</span><span class="sxs-lookup"><span data-stu-id="9bda8-128">You should carefully consider the information that you include in the events, especially when the events are written into the global channels.</span></span> <span data-ttu-id="9bda8-129">Как правило, в события не следует включать частные сведения.</span><span class="sxs-lookup"><span data-stu-id="9bda8-129">As a general rule, you should not include private information in the events.</span></span> <span data-ttu-id="9bda8-130">Сюда входят пароли в виде открытого текста и персональные данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="9bda8-130">This includes plaintext passwords and personal user information.</span></span> <span data-ttu-id="9bda8-131">Кроме того, программы, выполняемые пользователем, URL-адреса, посещенные пользователем, и другие сведения, относящиеся к действиям пользователя на компьютере, следует считать частными.</span><span class="sxs-lookup"><span data-stu-id="9bda8-131">Additionally, programs run by the user, URLs that the user visited, and other information related to the user activities on the computer should be considered private.</span></span>

<span data-ttu-id="9bda8-132">Если необходимо записывать URL-адреса и имена пользователей в события, не записывайте их в каналы Windows (система и приложение), так как эти каналы доступны для чтения всеми пользователями, прошедшими проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="9bda8-132">If you must record URLs and user names in the events, do not write them to the Windows channels (System and Application) because these channels are readable by all authenticated users.</span></span> <span data-ttu-id="9bda8-133">Вместо этого запишите их в собственные рабочие или аналитические каналы.</span><span class="sxs-lookup"><span data-stu-id="9bda8-133">Instead, write them to your own Operational or Analytic channels.</span></span> <span data-ttu-id="9bda8-134">Установите разрешения на доступ к этим каналам, чтобы разрешить только администраторам чтение событий.</span><span class="sxs-lookup"><span data-stu-id="9bda8-134">Set the access permissions on these channels to allow only administrators to read the events.</span></span> <span data-ttu-id="9bda8-135">Может потребоваться предоставить соответствующее раскрытие, чтобы уведомить пользователей о том, что личные данные становятся доступными администраторам.</span><span class="sxs-lookup"><span data-stu-id="9bda8-135">You may need to provide an appropriate disclosure to notify users of the fact that private information is made available to the administrators.</span></span>

<span data-ttu-id="9bda8-136">В следующем примере показано, как определить шаблон.</span><span class="sxs-lookup"><span data-stu-id="9bda8-136">The following example shows how to define a template.</span></span> <span data-ttu-id="9bda8-137">Необходимо указать атрибут **tid** шаблона, на который ссылается определение события или определение фильтра.</span><span class="sxs-lookup"><span data-stu-id="9bda8-137">You must specify the template's **tid** attribute that you reference in the event definition or filter definition.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <maps>
                    <valueMap name="TransferType">
                        <map value="1" message="$(string.TransferType.Download)"/>
                        <map value="2" message="$(string.TransferType.Upload)"/>
                        <map value="3" message="$(string.TransferType.UploadReply)"/>
                    </valueMap>
                    <bitMap name="DaysOfTheWeek">
                        <map value="0x1" message="$(string.DaysOfTheWeek.Sunday)"/>
                        <map value="0x2" message="$(string.DaysOfTheWeek.Monday)"/>
                        <map value="0x4" message="$(string.DaysOfTheWeek.Tuesday)"/>
                        <map value="0x8" message="$(string.DaysOfTheWeek.Wednesday)"/>
                        <map value="0x10" message="$(string.DaysOfTheWeek.Thursday)"/>
                        <map value="0x20" message="$(string.DaysOfTheWeek.Friday)"/>
                        <map value="0x40" message="$(string.DaysOfTheWeek.Saturday)"/>
                    </bitMap>
                </maps>

                <templates>
                    <template tid="t2">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="Day" inType="win:UInt32" map="DaysOfTheWeek"/>
                        <data name="Transfer" inType="win:UInt32" map="TransferType"/>
                    </template>

                    <template tid="t3">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="ErrorCode" inType="win:Int32" outType="win:HResult"/>
                        <data name="FilesCount" inType="win:UInt16" />
                        <data name="Files" inType="win:UnicodeString" count="FilesCount"/>
                        <data name="BufferSize" inType="win:UInt32" />
                        <data name="Buffer" inType="win:Binary" length="BufferSize"/>
                        <data name="Certificate" inType="win:Binary" length="11" />
                        <data name="IsLocal" inType="win:Boolean" />
                        <data name="Path" inType="win:UnicodeString" />
                        <data name="ValuesCount" inType="win:UInt16" />
                        <struct name="Values" count="ValuesCount" >
                            <data name="Value" inType="win:UInt16" />
                            <data name="Name" inType="win:UnicodeString" />
                        </struct>
                    </template>
                </templates>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="TransferType.Download" value="Download"/>
                <string id="TransferType.Upload" value="Upload"/>
                <string id="TransferType.UploadReply" value="Upload-reply"/>
                <string id="DaysOfTheWeek.Sunday" value="Sunday"/>
                <string id="DaysOfTheWeek.Monday" value="Monday"/>
                <string id="DaysOfTheWeek.Tuesday" value="Tuesday"/>
                <string id="DaysOfTheWeek.Wednesday" value="Wednesday"/>
                <string id="DaysOfTheWeek.Thursday" value="Thursday"/>
                <string id="DaysOfTheWeek.Friday" value="Friday"/>
                <string id="DaysOfTheWeek.Saturday" value="Saturday"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
