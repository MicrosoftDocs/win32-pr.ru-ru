---
title: Сериализация
description: Сериализация — это процесс записи значений в структурах данных C (структурах, массивах и примитивных значениях) в виде XML-элемента. Десериализация является обратным процессом.
ms.assetid: aa092156-30ae-4f8a-baa2-450f38a78153
keywords:
- Веб-службы сериализации для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f986c6cec9a035424aaafe1c51f4dc0d3ee014
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "104273214"
---
# <a name="serialization"></a><span data-ttu-id="d16d0-107">Сериализация</span><span class="sxs-lookup"><span data-stu-id="d16d0-107">Serialization</span></span>

<span data-ttu-id="d16d0-108">Сериализация — это процесс записи значений в структурах данных C (структурах, массивах и примитивных значениях) в виде XML-элемента.</span><span class="sxs-lookup"><span data-stu-id="d16d0-108">Serialization is the process of writing values in C data structures (structs, arrays, and primitive values) as an XML element.</span></span> <span data-ttu-id="d16d0-109">Десериализация является обратным процессом.</span><span class="sxs-lookup"><span data-stu-id="d16d0-109">Deserialization is the reverse process.</span></span>


<span data-ttu-id="d16d0-110">Сериализация — это процесс записи значений в структурах данных C (структуры, массивы и примитивные значения) в виде XML-элемента.</span><span class="sxs-lookup"><span data-stu-id="d16d0-110">Serialization is the process of writing values in C data structures (structures, arrays, and primitive values) as an XML element.</span></span> <span data-ttu-id="d16d0-111">Десериализация является обратным процессом.</span><span class="sxs-lookup"><span data-stu-id="d16d0-111">Deserialization is the reverse process.</span></span>

<span data-ttu-id="d16d0-112">Оба процесса полагаются на описание сопоставления между структурами данных C и XML.</span><span class="sxs-lookup"><span data-stu-id="d16d0-112">Both processes rely on a description of the mapping between the C data structures and the XML.</span></span>

![Схема, показывающая, как сериализация и десериализация зависят от описания сопоставления между структурами данных C и XML.](images/xmlmapping.png)

<span data-ttu-id="d16d0-114">Для сериализации значения приложение вызывает [**всвритилемент**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**всвритеаттрибуте**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) или [**всвритетипе**](/windows/desktop/api/WebServices/nf-webservices-wswritetype).</span><span class="sxs-lookup"><span data-stu-id="d16d0-114">To serialize a value, the application calls [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) or [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype).</span></span>

<span data-ttu-id="d16d0-115">Для десериализации значения приложение вызывает [**всреаделемент**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**всреадаттрибуте**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) или [**всреадтипе**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype).</span><span class="sxs-lookup"><span data-stu-id="d16d0-115">To deserialize a value, the application calls [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) or [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype).</span></span>

## <a name="security"></a><span data-ttu-id="d16d0-116">Безопасность</span><span class="sxs-lookup"><span data-stu-id="d16d0-116">Security</span></span>

<span data-ttu-id="d16d0-117">[Модуль чтения XML](xml-reader.md) используется в процессе десериализации.</span><span class="sxs-lookup"><span data-stu-id="d16d0-117">[XML Reader](xml-reader.md) is used in deserialization process.</span></span> <span data-ttu-id="d16d0-118">Сведения о безопасности, связанные с XML, см. в разделе "безопасность" в модуле чтения XML.</span><span class="sxs-lookup"><span data-stu-id="d16d0-118">Refer to the security section in XML Reader for XML related security information.</span></span>

<span data-ttu-id="d16d0-119">Десериализатор продолжит десериализацию данных, пока не завершит чтение десериализуемых элементов.</span><span class="sxs-lookup"><span data-stu-id="d16d0-119">The deserializer continues to deserialize data until it has completed reading the element being deserialized.</span></span> <span data-ttu-id="d16d0-120">Процесс десериализации завершается сбоем при обнаружении XML-документа, который не соответствует описанию десериализуемых данных.</span><span class="sxs-lookup"><span data-stu-id="d16d0-120">Deserialization process fails when it encounter any XML document that does not conform to the description of the data being deserialized.</span></span> <span data-ttu-id="d16d0-121">На этом этапе используемый модуль чтения XML становится недопустимым, и возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="d16d0-121">At that point XML reader being used becomes invalid, and an error is returned.</span></span>

<span data-ttu-id="d16d0-122">По умолчанию десериализация является нестандартной.</span><span class="sxs-lookup"><span data-stu-id="d16d0-122">By default deserialization is strict.</span></span> <span data-ttu-id="d16d0-123">Некоторые условия, которые приводят к сбою десериализации, включают, но не ограничиваются:</span><span class="sxs-lookup"><span data-stu-id="d16d0-123">Some conditions that cause deserialization to fail include but not limited to:</span></span>

-   <span data-ttu-id="d16d0-124">Отсутствуют ожидаемые элементы</span><span class="sxs-lookup"><span data-stu-id="d16d0-124">Expected elements is missing</span></span>
-   <span data-ttu-id="d16d0-125">Непредусмотренные поля элементов отображаются между обязательными элементами</span><span class="sxs-lookup"><span data-stu-id="d16d0-125">Unexpected element fields appear between required elements</span></span>
-   <span data-ttu-id="d16d0-126">Содержимое лишних элементов после обязательных полей, если только **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**</span><span class="sxs-lookup"><span data-stu-id="d16d0-126">Extra element content after required fields, unless the **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**</span></span>
-   <span data-ttu-id="d16d0-127">Непредвиденные атрибуты, если не указан флаг [**WS \_ STRUCT \_ Ignore \_ необработанных \_ атрибутов**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="d16d0-127">Unexpected attributes, unless [**WS\_STRUCT\_IGNORE\_UNHANDLED\_ATTRIBUTES**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx) flag is specified</span></span>
-   <span data-ttu-id="d16d0-128">Непредвиденное значение типа данных, находящийся за пределами указанного диапазона</span><span class="sxs-lookup"><span data-stu-id="d16d0-128">Unexpected data type value that is out of specified range</span></span>
-   <span data-ttu-id="d16d0-129">Число повторяющихся элементов выходит за пределы указанного диапазона</span><span class="sxs-lookup"><span data-stu-id="d16d0-129">Count of repeating element is out of the specified range</span></span>

<span data-ttu-id="d16d0-130">Сериализация большого объема данных может привести к чрезмерному выделению памяти и может привести к атаке типа "отказ в обслуживании".</span><span class="sxs-lookup"><span data-stu-id="d16d0-130">Serializing large amount of data might cause excessive memory allocation and can cause denial of service attack.</span></span> <span data-ttu-id="d16d0-131">Пользователь, который десериализует данные, должен указать объект кучи для выделения данных, и пользователь может использовать ограничение выделения кучи для предотвращения атаки выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="d16d0-131">The user that is deserializing data must specify a Heap object to allocate the data, and the user can use the heap allocation limit to prevent memory allocation attack.</span></span>

<span data-ttu-id="d16d0-132">Поддержка диапазона для типов данных, включая максимальную длину для строки, максимальное число элементов в массиве и т. д. позволяет пользователю управлять максимальным размером для различных типов данных.</span><span class="sxs-lookup"><span data-stu-id="d16d0-132">Range support for data types, including max length for string, max element count in array, etc. allows the user to control the maximum size for different data types.</span></span> <span data-ttu-id="d16d0-133">Пользователь может указать диапазон в описании или схеме данных, чтобы ограничить максимальный размер различных данных.</span><span class="sxs-lookup"><span data-stu-id="d16d0-133">User can specify range in data description or schema to limit the maximum size of different data.</span></span>

<span data-ttu-id="d16d0-134">Строковое значение, содержащее внедренный нуль, поддерживается в форматах сети (текст, двоичный, MTOM).</span><span class="sxs-lookup"><span data-stu-id="d16d0-134">A string value containing an embedded zero is supported in the wire formats (text, binary, MTOM).</span></span> <span data-ttu-id="d16d0-135">При десериализации строки с внедренным нулем пользователь должен использовать подсчитанную строку (WS \_ String), поэтому ноль не будет путать вычисление длины строки.</span><span class="sxs-lookup"><span data-stu-id="d16d0-135">When deserializing a string with an embedded zero, the user should use a counted string (WS\_STRING) so the zero will not confuse the calculation of the length of the string.</span></span> <span data-ttu-id="d16d0-136">Если строковое значение, содержащее внедренный нуль, десериализуется в поле, которое ожидает строку, завершающуюся нулем, возвращается ошибка, а десериализация завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d16d0-136">If a string value containing an embedded zero is deserialized into a field that is expecting a zero-terminated string, an error is returned, and deserialization fails.</span></span> <span data-ttu-id="d16d0-137">Если всутил используется для формирования описаний данных, \_ следует использовать параметр/стринг: WS String, если ожидается строка с внедренным нулем.</span><span class="sxs-lookup"><span data-stu-id="d16d0-137">If wsutil is used to generate data descriptions, /string:WS\_STRING option should be used if string with embedded zero is expected.</span></span>

<span data-ttu-id="d16d0-138">С сериализацией используются следующие обратные вызовы:</span><span class="sxs-lookup"><span data-stu-id="d16d0-138">The following callbacks are used with serialization:</span></span>

-   [<span data-ttu-id="d16d0-139">**\_ \_ обратный вызов сравнения ДЛИТЕЛЬности WS \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-139">**WS\_DURATION\_COMPARISON\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [<span data-ttu-id="d16d0-140">**\_ \_ обратный вызов типа WS Read \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-140">**WS\_READ\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [<span data-ttu-id="d16d0-141">**\_ \_ обратный вызов типа записи WS \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-141">**WS\_WRITE\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

<span data-ttu-id="d16d0-142">С сериализацией используются следующие перечисления:</span><span class="sxs-lookup"><span data-stu-id="d16d0-142">The following enumerations are used with serialization:</span></span>

-   [<span data-ttu-id="d16d0-143">**\_сопоставление полей \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-143">**WS\_FIELD\_MAPPING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping)
-   [<span data-ttu-id="d16d0-144">**\_Параметры поля \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-144">**WS\_FIELD\_OPTIONS**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type)
-   [<span data-ttu-id="d16d0-145">**\_параметр WS Read \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-145">**WS\_READ\_OPTION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_read_option)
-   [<span data-ttu-id="d16d0-146">**\_тип WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-146">**WS\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_type)
-   [<span data-ttu-id="d16d0-147">**\_Сопоставление типов \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-147">**WS\_TYPE\_MAPPING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_type_mapping)
-   [<span data-ttu-id="d16d0-148">**\_параметр записи \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-148">**WS\_WRITE\_OPTION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_write_option)

<span data-ttu-id="d16d0-149">С сериализацией используются следующие функции:</span><span class="sxs-lookup"><span data-stu-id="d16d0-149">The following functions are used with serialization:</span></span>

-   [<span data-ttu-id="d16d0-150">**всреадаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="d16d0-150">**WsReadAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute)
-   [<span data-ttu-id="d16d0-151">**всреаделемент**</span><span class="sxs-lookup"><span data-stu-id="d16d0-151">**WsReadElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)
-   [<span data-ttu-id="d16d0-152">**всреадтипе**</span><span class="sxs-lookup"><span data-stu-id="d16d0-152">**WsReadType**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)
-   [<span data-ttu-id="d16d0-153">**всвритеаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="d16d0-153">**WsWriteAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute)
-   [<span data-ttu-id="d16d0-154">**всвритилемент**</span><span class="sxs-lookup"><span data-stu-id="d16d0-154">**WsWriteElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteelement)
-   [<span data-ttu-id="d16d0-155">**всвритетипе**</span><span class="sxs-lookup"><span data-stu-id="d16d0-155">**WsWriteType**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritetype)

<span data-ttu-id="d16d0-156">При сериализации используются следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="d16d0-156">The following structures are used with serialization:</span></span>

-   [<span data-ttu-id="d16d0-157">**\_Описание атрибута \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-157">**WS\_ATTRIBUTE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_attribute_description)
-   [<span data-ttu-id="d16d0-158">**\_Описание логического типа WS \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-158">**WS\_BOOL\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_bool_description)
-   [<span data-ttu-id="d16d0-159">**\_Описание WS bytes \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-159">**WS\_BYTES\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_bytes_description)
-   [<span data-ttu-id="d16d0-160">**\_ \_ Описание массива байтов \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-160">**WS\_BYTE\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_byte_array_description)
-   [<span data-ttu-id="d16d0-161">**\_ \_ Описание массива WS \_ char**</span><span class="sxs-lookup"><span data-stu-id="d16d0-161">**WS\_CHAR\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_char_array_description)
-   [<span data-ttu-id="d16d0-162">**\_Описание настраиваемого \_ типа WS \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-162">**WS\_CUSTOM\_TYPE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_type_description)
-   [<span data-ttu-id="d16d0-163">**\_Описание WS DateTime \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-163">**WS\_DATETIME\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_datetime_description)
-   [<span data-ttu-id="d16d0-164">**\_десятичное \_ Описание WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-164">**WS\_DECIMAL\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_decimal_description)
-   [<span data-ttu-id="d16d0-165">**\_значение по умолчанию для WS \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-165">**WS\_DEFAULT\_VALUE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_default_value)
-   [<span data-ttu-id="d16d0-166">**\_Двойное \_ Описание WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-166">**WS\_DOUBLE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_double_description)
-   [<span data-ttu-id="d16d0-167">**\_Описание длительности WS \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-167">**WS\_DURATION\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_duration_description)
-   [<span data-ttu-id="d16d0-168">**\_Описание элемента \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-168">**WS\_ELEMENT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)
-   [<span data-ttu-id="d16d0-169">**\_Описание адреса конечной точки WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-169">**WS\_ENDPOINT\_ADDRESS\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description)
-   [<span data-ttu-id="d16d0-170">**\_Описание ПЕРЕЧИСЛЕНИЯ \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-170">**WS\_ENUM\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_enum_description)
-   [<span data-ttu-id="d16d0-171">**\_значение ПЕРЕЧИСЛЕНИЯ \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-171">**WS\_ENUM\_VALUE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_enum_value)
-   [<span data-ttu-id="d16d0-172">**\_Описание ошибки \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-172">**WS\_FAULT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_fault_description)
-   [<span data-ttu-id="d16d0-173">**\_Описание поля \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-173">**WS\_FIELD\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_field_description)
-   [<span data-ttu-id="d16d0-174">**\_Описание WS float \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-174">**WS\_FLOAT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_float_description)
-   [<span data-ttu-id="d16d0-175">**\_Описание идентификатора GUID WS \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-175">**WS\_GUID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_guid_description)
-   [<span data-ttu-id="d16d0-176">**\_Описание WS INT16 \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-176">**WS\_INT16\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int16_description)
-   [<span data-ttu-id="d16d0-177">**\_Описание WS Int32 \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-177">**WS\_INT32\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int32_description)
-   [<span data-ttu-id="d16d0-178">**\_Описание WS Int64 \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-178">**WS\_INT64\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int64_description)
-   [<span data-ttu-id="d16d0-179">**Описание "WS \_ INT8" \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-179">**WS\_INT8\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int8_description)
-   [<span data-ttu-id="d16d0-180">**\_диапазон элементов \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-180">**WS\_ITEM\_RANGE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_item_range)
-   [<span data-ttu-id="d16d0-181">**\_Описание строки \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-181">**WS\_STRING\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_description)
-   [<span data-ttu-id="d16d0-182">**\_Описание структуры \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-182">**WS\_STRUCT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)
-   [<span data-ttu-id="d16d0-183">**Описание для WS \_ TIMESPAN \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-183">**WS\_TIMESPAN\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_timespan_description)
-   [<span data-ttu-id="d16d0-184">**\_Описание WS UINT16 \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-184">**WS\_UINT16\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint16_description)
-   [<span data-ttu-id="d16d0-185">**\_Описание WS UINT32 \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-185">**WS\_UINT32\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint32_description)
-   [<span data-ttu-id="d16d0-186">**Описание спецификации WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-186">**WS\_UINT64\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint64_description)
-   [<span data-ttu-id="d16d0-187">**\_Описание WS UINT8 \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-187">**WS\_UINT8\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint8_description)
-   [<span data-ttu-id="d16d0-188">**\_Описание WS Union \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-188">**WS\_UNION\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_union_description)
-   [<span data-ttu-id="d16d0-189">**\_ \_ Описание поля WS \_ Union**</span><span class="sxs-lookup"><span data-stu-id="d16d0-189">**WS\_UNION\_FIELD\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_union_field_description)
-   [<span data-ttu-id="d16d0-190">**\_Описание уникального \_ идентификатора WS \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-190">**WS\_UNIQUE\_ID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_unique_id_description)
-   [<span data-ttu-id="d16d0-191">**\_ \_ Описание массива WS \_ UTF8**</span><span class="sxs-lookup"><span data-stu-id="d16d0-191">**WS\_UTF8\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_utf8_array_description)
-   [<span data-ttu-id="d16d0-192">**\_Описание WS void \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-192">**WS\_VOID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_void_description)
-   [<span data-ttu-id="d16d0-193">**\_Описание WS ВСЗ \_**</span><span class="sxs-lookup"><span data-stu-id="d16d0-193">**WS\_WSZ\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_wsz_description)
-   [<span data-ttu-id="d16d0-194">**\_XML- \_ \_ Описание QNAME для WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-194">**WS\_XML\_QNAME\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_description)
-   [<span data-ttu-id="d16d0-195">**\_Описание XML- \_ строки \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d16d0-195">**WS\_XML\_STRING\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string_description)

 

 




