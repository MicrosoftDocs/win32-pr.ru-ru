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
# <a name="serialization"></a>Сериализация

Сериализация — это процесс записи значений в структурах данных C (структурах, массивах и примитивных значениях) в виде XML-элемента. Десериализация является обратным процессом.


Сериализация — это процесс записи значений в структурах данных C (структуры, массивы и примитивные значения) в виде XML-элемента. Десериализация является обратным процессом.

Оба процесса полагаются на описание сопоставления между структурами данных C и XML.

![Схема, показывающая, как сериализация и десериализация зависят от описания сопоставления между структурами данных C и XML.](images/xmlmapping.png)

Для сериализации значения приложение вызывает [**всвритилемент**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**всвритеаттрибуте**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) или [**всвритетипе**](/windows/desktop/api/WebServices/nf-webservices-wswritetype).

Для десериализации значения приложение вызывает [**всреаделемент**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**всреадаттрибуте**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) или [**всреадтипе**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype).

## <a name="security"></a>Безопасность

[Модуль чтения XML](xml-reader.md) используется в процессе десериализации. Сведения о безопасности, связанные с XML, см. в разделе "безопасность" в модуле чтения XML.

Десериализатор продолжит десериализацию данных, пока не завершит чтение десериализуемых элементов. Процесс десериализации завершается сбоем при обнаружении XML-документа, который не соответствует описанию десериализуемых данных. На этом этапе используемый модуль чтения XML становится недопустимым, и возвращается ошибка.

По умолчанию десериализация является нестандартной. Некоторые условия, которые приводят к сбою десериализации, включают, но не ограничиваются:

-   Отсутствуют ожидаемые элементы
-   Непредусмотренные поля элементов отображаются между обязательными элементами
-   Содержимое лишних элементов после обязательных полей, если только **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**
-   Непредвиденные атрибуты, если не указан флаг [**WS \_ STRUCT \_ Ignore \_ необработанных \_ атрибутов**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx)
-   Непредвиденное значение типа данных, находящийся за пределами указанного диапазона
-   Число повторяющихся элементов выходит за пределы указанного диапазона

Сериализация большого объема данных может привести к чрезмерному выделению памяти и может привести к атаке типа "отказ в обслуживании". Пользователь, который десериализует данные, должен указать объект кучи для выделения данных, и пользователь может использовать ограничение выделения кучи для предотвращения атаки выделения памяти.

Поддержка диапазона для типов данных, включая максимальную длину для строки, максимальное число элементов в массиве и т. д. позволяет пользователю управлять максимальным размером для различных типов данных. Пользователь может указать диапазон в описании или схеме данных, чтобы ограничить максимальный размер различных данных.

Строковое значение, содержащее внедренный нуль, поддерживается в форматах сети (текст, двоичный, MTOM). При десериализации строки с внедренным нулем пользователь должен использовать подсчитанную строку (WS \_ String), поэтому ноль не будет путать вычисление длины строки. Если строковое значение, содержащее внедренный нуль, десериализуется в поле, которое ожидает строку, завершающуюся нулем, возвращается ошибка, а десериализация завершается ошибкой. Если всутил используется для формирования описаний данных, \_ следует использовать параметр/стринг: WS String, если ожидается строка с внедренным нулем.

С сериализацией используются следующие обратные вызовы:

-   [**\_ \_ обратный вызов сравнения ДЛИТЕЛЬности WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**\_ \_ обратный вызов типа WS Read \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**\_ \_ обратный вызов типа записи WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

С сериализацией используются следующие перечисления:

-   [**\_сопоставление полей \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping)
-   [**\_Параметры поля \_ WS**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type)
-   [**\_параметр WS Read \_**](/windows/desktop/api/WebServices/ne-webservices-ws_read_option)
-   [**\_тип WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type)
-   [**\_Сопоставление типов \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type_mapping)
-   [**\_параметр записи \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_write_option)

С сериализацией используются следующие функции:

-   [**всреадаттрибуте**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute)
-   [**всреаделемент**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)
-   [**всреадтипе**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)
-   [**всвритеаттрибуте**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute)
-   [**всвритилемент**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement)
-   [**всвритетипе**](/windows/desktop/api/WebServices/nf-webservices-wswritetype)

При сериализации используются следующие структуры:

-   [**\_Описание атрибута \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_attribute_description)
-   [**\_Описание логического типа WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_bool_description)
-   [**\_Описание WS bytes \_**](/windows/desktop/api/WebServices/ns-webservices-ws_bytes_description)
-   [**\_ \_ Описание массива байтов \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_byte_array_description)
-   [**\_ \_ Описание массива WS \_ char**](/windows/desktop/api/WebServices/ns-webservices-ws_char_array_description)
-   [**\_Описание настраиваемого \_ типа WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_type_description)
-   [**\_Описание WS DateTime \_**](/windows/desktop/api/WebServices/ns-webservices-ws_datetime_description)
-   [**\_десятичное \_ Описание WS**](/windows/desktop/api/WebServices/ns-webservices-ws_decimal_description)
-   [**\_значение по умолчанию для WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_default_value)
-   [**\_Двойное \_ Описание WS**](/windows/desktop/api/WebServices/ns-webservices-ws_double_description)
-   [**\_Описание длительности WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_duration_description)
-   [**\_Описание элемента \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)
-   [**\_Описание адреса конечной точки WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description)
-   [**\_Описание ПЕРЕЧИСЛЕНИЯ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_enum_description)
-   [**\_значение ПЕРЕЧИСЛЕНИЯ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_enum_value)
-   [**\_Описание ошибки \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_description)
-   [**\_Описание поля \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description)
-   [**\_Описание WS float \_**](/windows/desktop/api/WebServices/ns-webservices-ws_float_description)
-   [**\_Описание идентификатора GUID WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_guid_description)
-   [**\_Описание WS INT16 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int16_description)
-   [**\_Описание WS Int32 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int32_description)
-   [**\_Описание WS Int64 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int64_description)
-   [**Описание "WS \_ INT8" \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int8_description)
-   [**\_диапазон элементов \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_item_range)
-   [**\_Описание строки \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_string_description)
-   [**\_Описание структуры \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)
-   [**Описание для WS \_ TIMESPAN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_timespan_description)
-   [**\_Описание WS UINT16 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint16_description)
-   [**\_Описание WS UINT32 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint32_description)
-   [**Описание спецификации WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint64_description)
-   [**\_Описание WS UINT8 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint8_description)
-   [**\_Описание WS Union \_**](/windows/desktop/api/WebServices/ns-webservices-ws_union_description)
-   [**\_ \_ Описание поля WS \_ Union**](/windows/desktop/api/WebServices/ns-webservices-ws_union_field_description)
-   [**\_Описание уникального \_ идентификатора WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_unique_id_description)
-   [**\_ \_ Описание массива WS \_ UTF8**](/windows/desktop/api/WebServices/ns-webservices-ws_utf8_array_description)
-   [**\_Описание WS void \_**](/windows/desktop/api/WebServices/ns-webservices-ws_void_description)
-   [**\_Описание WS ВСЗ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_wsz_description)
-   [**\_XML- \_ \_ Описание QNAME для WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_description)
-   [**\_Описание XML- \_ строки \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string_description)

 

 




