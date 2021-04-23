---
description: Структура данных PROPERTYINFO определяет одно свойство протокола.
ms.assetid: 878777ab-141d-4cc5-b0c1-f2ac8f770bf0
title: Структура PROPERTYINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 435b08c5dd5e020dce2bde9be03a0d41299836c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991675"
---
# <a name="propertyinfo-structure"></a><span data-ttu-id="47ad1-103">Структура PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="47ad1-103">PROPERTYINFO structure</span></span>

<span data-ttu-id="47ad1-104">Структура данных **PROPERTYINFO** определяет одно свойство протокола.</span><span class="sxs-lookup"><span data-stu-id="47ad1-104">The **PROPERTYINFO** data structure defines one property of the protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="47ad1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47ad1-105">Syntax</span></span>


```C++
typedef struct _PROPERTYINFO {
  HPROPERTY hProperty;
  DWORD     Version;
  LPSTR     Label;
  LPSTR     Comment;
  BYTE      DataType;
  BYTE      DataQualifier;
  union {
    LPVOID  lpExtendedInfo;
    LPRANGE lpRange;
    LPSET   lpSet;
    DWORD   Bitmask;
    DWORD   Value;
  };
  WORD      FormatStringSize;
  LPVOID    InstanceData;
} PROPERTYINFO, *LPPROPERTYINFO;
```



## <a name="members"></a><span data-ttu-id="47ad1-106">Члены</span><span class="sxs-lookup"><span data-stu-id="47ad1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="47ad1-107">**хпроперти**</span><span class="sxs-lookup"><span data-stu-id="47ad1-107">**hProperty**</span></span>
</dt> <dd>

<span data-ttu-id="47ad1-108">Присвойте этому полю нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="47ad1-108">Set this field to zero.</span></span> <span data-ttu-id="47ad1-109">В выходных данных сетевой монитор возвращает маркер свойства после добавления свойства в базу данных свойств.</span><span class="sxs-lookup"><span data-stu-id="47ad1-109">On output, Network Monitor returns a handle to the property after the property is added to the property database.</span></span>

</dd> <dt>

<span data-ttu-id="47ad1-110">**Version**</span><span class="sxs-lookup"><span data-stu-id="47ad1-110">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="47ad1-111">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="47ad1-111">Reserved.</span></span> <span data-ttu-id="47ad1-112">Необходимо задать значение 0.</span><span class="sxs-lookup"><span data-stu-id="47ad1-112">Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="47ad1-113">**Label**</span><span class="sxs-lookup"><span data-stu-id="47ad1-113">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="47ad1-114">Имя свойства.</span><span class="sxs-lookup"><span data-stu-id="47ad1-114">Name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="47ad1-115">**Комментарий**</span><span class="sxs-lookup"><span data-stu-id="47ad1-115">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="47ad1-116">Описание свойства.</span><span class="sxs-lookup"><span data-stu-id="47ad1-116">Description of the property.</span></span> <span data-ttu-id="47ad1-117">Описание появится в строке состояния сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="47ad1-117">The description appears on the Network Monitor status bar.</span></span>

</dd> <dt>

<span data-ttu-id="47ad1-118">**DataType**</span><span class="sxs-lookup"><span data-stu-id="47ad1-118">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="47ad1-119">Тип данных свойства.</span><span class="sxs-lookup"><span data-stu-id="47ad1-119">Data type of the property.</span></span> <span data-ttu-id="47ad1-120">Этот элемент может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="47ad1-120">This member can have one of the following values.</span></span>



| <span data-ttu-id="47ad1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="47ad1-121">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="47ad1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="47ad1-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_TYPE_VOID"></span><span id="prop_type_void"></span><dl> <span data-ttu-id="47ad1-123"><dt>**\_тип Prop \_ void**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-123"><dt>**PROP\_TYPE\_VOID**</dt></span></span> </dl>                                           | <span data-ttu-id="47ad1-124">Неизвестный тип свойства.</span><span class="sxs-lookup"><span data-stu-id="47ad1-124">Property type is unknown.</span></span> <span data-ttu-id="47ad1-125">Нет подразумеваемой длины или формата.</span><span class="sxs-lookup"><span data-stu-id="47ad1-125">There is no implied length or format.</span></span><br/>                                                                                                                                                                                                                                  |
| <span id="PROP_TYPE_SUMMARY"></span><span id="prop_type_summary"></span><dl> <span data-ttu-id="47ad1-126"><dt>**\_ \_ Сводка по типу Prop**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-126"><dt>**PROP\_TYPE\_SUMMARY**</dt></span></span> </dl>                                  | <span data-ttu-id="47ad1-127">Формирование сводки по типу свойства.</span><span class="sxs-lookup"><span data-stu-id="47ad1-127">Summarizing property type.</span></span> <span data-ttu-id="47ad1-128">Указывает первый экземпляр свойства, который средство синтаксического анализа присоединяет к кадру.</span><span class="sxs-lookup"><span data-stu-id="47ad1-128">Indicates the first property instance that the parser attaches to a frame.</span></span> <span data-ttu-id="47ad1-129">\_Сводка типа Prop \_ может использоваться в качестве заполнителя для групп свойств.</span><span class="sxs-lookup"><span data-stu-id="47ad1-129">PROP\_TYPE\_SUMMARY can serve as a placeholder for groups of properties.</span></span> <span data-ttu-id="47ad1-130">Это значение указывает, что свойство не определено в протоколе *RFC*.</span><span class="sxs-lookup"><span data-stu-id="47ad1-130">This value indicates that the property is not defined in the protocol *RFC*.</span></span><br/> |
| <span id="PROP_TYPE_BYTE"></span><span id="prop_type_byte"></span><dl> <span data-ttu-id="47ad1-131"><dt>**Тип свойства PROP \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-131"><dt>**PROP\_TYPE\_BYTE**</dt></span></span> </dl>                                           | <span data-ttu-id="47ad1-132">Числовые данные с размером в один байт (8-разрядная сущность).</span><span class="sxs-lookup"><span data-stu-id="47ad1-132">Numeric data with a size of one byte (8-bit entity).</span></span><br/>                                                                                                                                                                                                                                             |
| <span id="PROP_TYPE_WORD"></span><span id="prop_type_word"></span><dl> <span data-ttu-id="47ad1-133"><dt>**\_слово типа \_ prop**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-133"><dt>**PROP\_TYPE\_WORD**</dt></span></span> </dl>                                           | <span data-ttu-id="47ad1-134">Числовые данные с размером в два байта (16-разрядная сущность).</span><span class="sxs-lookup"><span data-stu-id="47ad1-134">Numeric data with a size of two bytes (16-bit entity).</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_DWORD"></span><span id="prop_type_dword"></span><dl> <span data-ttu-id="47ad1-135"><dt>**PROP \_ тип \_ DWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-135"><dt>**PROP\_TYPE\_DWORD**</dt></span></span> </dl>                                        | <span data-ttu-id="47ad1-136">Числовые данные размером четыре байта (32-разрядная сущность).</span><span class="sxs-lookup"><span data-stu-id="47ad1-136">Numeric data with a size of four bytes (32-bit entity).</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="PROP_TYPE_LARGEINT"></span><span id="prop_type_largeint"></span><dl> <span data-ttu-id="47ad1-137"><dt>**PROP \_ тип \_ ларжеинт**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-137"><dt>**PROP\_TYPE\_LARGEINT**</dt></span></span> </dl>                               | <span data-ttu-id="47ad1-138">Числовые данные размером 8 байт (64-разрядная сущность).</span><span class="sxs-lookup"><span data-stu-id="47ad1-138">Numeric data with a size of eight bytes (64-bit entity).</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="PROP_TYPE_ADDR"></span><span id="prop_type_addr"></span><dl> <span data-ttu-id="47ad1-139"><dt>**Тип свойства " \_ \_ адрес"**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-139"><dt>**PROP\_TYPE\_ADDR**</dt></span></span> </dl>                                           | <span data-ttu-id="47ad1-140">МАС-адрес (6-байтовая сущность).</span><span class="sxs-lookup"><span data-stu-id="47ad1-140">MAC address (6-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_TIME"></span><span id="prop_type_time"></span><dl> <span data-ttu-id="47ad1-141"><dt>**\_тип Prop \_ время**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-141"><dt>**PROP\_TYPE\_TIME**</dt></span></span> </dl>                                           | <span data-ttu-id="47ad1-142">Структура **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="47ad1-142">**SYSTEMTIME** structure.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_STRING"></span><span id="prop_type_string"></span><dl> <span data-ttu-id="47ad1-143"><dt>**\_Строка типа \_ prop**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-143"><dt>**PROP\_TYPE\_STRING**</dt></span></span> </dl>                                     | <span data-ttu-id="47ad1-144">Текстовые данные ASCII.</span><span class="sxs-lookup"><span data-stu-id="47ad1-144">ASCII text data.</span></span> <span data-ttu-id="47ad1-145">Этот тип данных не завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="47ad1-145">This data type is not NULL-terminated.</span></span> <br/> <span data-ttu-id="47ad1-146">Для данных в Юникоде, если заданы текстовые данные ASCII, \_ флаг ифлаг Unicode также должен быть задан при вызове функции экземпляра свойства Attach.</span><span class="sxs-lookup"><span data-stu-id="47ad1-146">For Unicode data, when ASCII text data is specified, the IFLAG\_UNICODE flag must also be set when the attach property instance function is called.</span></span><br/>                                                                          |
| <span id="PROP_TYPE_IP_ADDRESS"></span><span id="prop_type_ip_address"></span><dl> <span data-ttu-id="47ad1-147"><dt>**\_ \_ IP-адрес типа Prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-147"><dt>**PROP\_TYPE\_IP\_ADDRESS**</dt></span></span> </dl>                        | <span data-ttu-id="47ad1-148">IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="47ad1-148">IP Address.</span></span> <span data-ttu-id="47ad1-149">(4-байтовая сущность).</span><span class="sxs-lookup"><span data-stu-id="47ad1-149">(4-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_IPX_ADDRESS"></span><span id="prop_type_ipx_address"></span><dl> <span data-ttu-id="47ad1-150"><dt>**Тип свойства PROP \_ \_ IPX- \_ адрес**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-150"><dt>**PROP\_TYPE\_IPX\_ADDRESS**</dt></span></span> </dl>                     | <span data-ttu-id="47ad1-151">IPX-адрес.</span><span class="sxs-lookup"><span data-stu-id="47ad1-151">IPX Address.</span></span> <span data-ttu-id="47ad1-152">(10-байтовая сущность).</span><span class="sxs-lookup"><span data-stu-id="47ad1-152">(10-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                   |
| <span id="PROP_TYPE_BYTESWAPPED_WORD"></span><span id="prop_type_byteswapped_word"></span><dl> <span data-ttu-id="47ad1-153"><dt>**\_тип Prop \_ битесваппед \_ слово**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-153"><dt>**PROP\_TYPE\_BYTESWAPPED\_WORD**</dt></span></span> </dl>      | <span data-ttu-id="47ad1-154">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="47ad1-154">Obsolete.</span></span> <span data-ttu-id="47ad1-155">Для данных слов с переключением байтов установите тип **DataType** в Prop \_ Type \_ и установите флаг ифлаг в \_ переключении при вызове функции экземпляра свойства **attach** .</span><span class="sxs-lookup"><span data-stu-id="47ad1-155">For byte-swapped WORD data, set **DataType** to PROP\_TYPE\_WORD and set the IFLAG\_SWAPPED flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                                |
| <span id="PROP_TYPE_BYTESWAPPED_DWORD"></span><span id="prop_type_byteswapped_dword"></span><dl> <span data-ttu-id="47ad1-156"><dt>**PROP \_ тип \_ битесваппед \_ DWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-156"><dt>**PROP\_TYPE\_BYTESWAPPED\_DWORD**</dt></span></span> </dl>   | <span data-ttu-id="47ad1-157">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="47ad1-157">Obsolete.</span></span> <span data-ttu-id="47ad1-158">Для данных типа DWORD с закачки байтов задайте для **DataType** значение Prop \_ типа \_ DWORD и установите флаг ифлаг \_ переключений при вызове функции экземпляра свойства **attach** .</span><span class="sxs-lookup"><span data-stu-id="47ad1-158">For byte-swapped DWORD data, set **DataType** to PROP\_TYPE\_DWORD and set the IFLAG\_SWAPPED flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                              |
| <span id="PROP_TYPE_TYPED_STRING"></span><span id="prop_type_typed_string"></span><dl> <span data-ttu-id="47ad1-159"><dt>**\_ \_ типизированная строка типа Prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-159"><dt>**PROP\_TYPE\_TYPED\_STRING**</dt></span></span> </dl>                  | <span data-ttu-id="47ad1-160">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="47ad1-160">Obsolete.</span></span> <span data-ttu-id="47ad1-161">Для строковых данных типа "переменная" задайте тип **DataType** в виде \_ строки типа Prop \_ и установите \_ флаг Юникода ифлаг при вызове функции экземпляра свойства **attach** .</span><span class="sxs-lookup"><span data-stu-id="47ad1-161">For variable-type string data, set **DataType** to PROP\_TYPE\_STRING and set the IFLAG\_UNICODE flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                           |
| <span id="PROP_TYPE_RAW_DATA"></span><span id="prop_type_raw_data"></span><dl> <span data-ttu-id="47ad1-162"><dt>**\_ \_ необработанные \_ данные типа Prop**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-162"><dt>**PROP\_TYPE\_RAW\_DATA**</dt></span></span> </dl>                              | <span data-ttu-id="47ad1-163">Необработанные данные неизвестной длины и формата.</span><span class="sxs-lookup"><span data-stu-id="47ad1-163">Raw data of unknown length and format.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_COMMENT"></span><span id="prop_type_comment"></span><dl> <span data-ttu-id="47ad1-164"><dt>**\_Комментарий типа \_ prop**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-164"><dt>**PROP\_TYPE\_COMMENT**</dt></span></span> </dl>                                  | <span data-ttu-id="47ad1-165">То же, что и \_ тип Prop \_ void.</span><span class="sxs-lookup"><span data-stu-id="47ad1-165">Same as PROP\_TYPE\_VOID.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_SRCFRIENDLYNAME"></span><span id="prop_type_srcfriendlyname"></span><dl> <span data-ttu-id="47ad1-166"><dt>**PROP \_ тип \_ сркфриендлинаме**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-166"><dt>**PROP\_TYPE\_SRCFRIENDLYNAME**</dt></span></span> </dl>          | <span data-ttu-id="47ad1-167">Адрес понятного имени источника.</span><span class="sxs-lookup"><span data-stu-id="47ad1-167">Address of source-friendly name.</span></span> <span data-ttu-id="47ad1-168">Сетевой монитор не предоставляет встроенную поддержку форматирования для этого типа данных.</span><span class="sxs-lookup"><span data-stu-id="47ad1-168">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                |
| <span id="PROP_TYPE_DSTFRIENDLYNAME"></span><span id="prop_type_dstfriendlyname"></span><dl> <span data-ttu-id="47ad1-169"><dt>**PROP \_ тип \_ дстфриендлинаме**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-169"><dt>**PROP\_TYPE\_DSTFRIENDLYNAME**</dt></span></span> </dl>          | <span data-ttu-id="47ad1-170">Адрес понятного имени назначения.</span><span class="sxs-lookup"><span data-stu-id="47ad1-170">Address of destination friendly name.</span></span> <span data-ttu-id="47ad1-171">Сетевой монитор не предоставляет встроенную поддержку форматирования для этого типа данных.</span><span class="sxs-lookup"><span data-stu-id="47ad1-171">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                           |
| <span id="PROP_TYPE_TOKENRING_ADDRESS"></span><span id="prop_type_tokenring_address"></span><dl> <span data-ttu-id="47ad1-172"><dt>**\_тип Prop \_ токенринг \_ адрес**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-172"><dt>**PROP\_TYPE\_TOKENRING\_ADDRESS**</dt></span></span> </dl>   | <span data-ttu-id="47ad1-173">Кольцевой адрес.</span><span class="sxs-lookup"><span data-stu-id="47ad1-173">Token-ring address.</span></span> <span data-ttu-id="47ad1-174">Сетевой монитор не предоставляет встроенную поддержку форматирования для этого типа данных.</span><span class="sxs-lookup"><span data-stu-id="47ad1-174">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                             |
| <span id="PROP_TYPE_FDDI_ADDRESS"></span><span id="prop_type_fddi_address"></span><dl> <span data-ttu-id="47ad1-175"><dt>**\_тип Prop \_ \_ адрес FDDI**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-175"><dt>**PROP\_TYPE\_FDDI\_ADDRESS**</dt></span></span> </dl>                  | <span data-ttu-id="47ad1-176">Адрес FDDI.</span><span class="sxs-lookup"><span data-stu-id="47ad1-176">FDDI address.</span></span> <span data-ttu-id="47ad1-177">Сетевой монитор не предоставляет встроенную поддержку форматирования для этого типа данных.</span><span class="sxs-lookup"><span data-stu-id="47ad1-177">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                                   |
| <span id="PROP_TYPE_ETHERNET_ADDRESS"></span><span id="prop_type_ethernet_address"></span><dl> <span data-ttu-id="47ad1-178"><dt>**\_тип свойства \_ prop \_ адрес Ethernet**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-178"><dt>**PROP\_TYPE\_ETHERNET\_ADDRESS**</dt></span></span> </dl>      | <span data-ttu-id="47ad1-179">Адрес Ethernet.</span><span class="sxs-lookup"><span data-stu-id="47ad1-179">Ethernet address.</span></span> <span data-ttu-id="47ad1-180">Сетевой монитор не предоставляет встроенную поддержку форматирования для этого типа данных.</span><span class="sxs-lookup"><span data-stu-id="47ad1-180">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                               |
| <span id="PROP_TYPE_OBJECT_IDENTIFIER"></span><span id="prop_type_object_identifier"></span><dl> <span data-ttu-id="47ad1-181"><dt>**\_ \_ идентификатор объекта типа \_ prop**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-181"><dt>**PROP\_TYPE\_OBJECT\_IDENTIFIER**</dt></span></span> </dl>   | <span data-ttu-id="47ad1-182">Идентификатор объекта SNMP в кодировке ЛИЧЕСТВО.</span><span class="sxs-lookup"><span data-stu-id="47ad1-182">BER-encoded SNMP object identifier.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="PROP_TYPE_VINES_IP_ADDRESS"></span><span id="prop_type_vines_ip_address"></span><dl> <span data-ttu-id="47ad1-183"><dt>**\_тип Prop \_ \_ IP- \_ адрес Vines**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-183"><dt>**PROP\_TYPE\_VINES\_IP\_ADDRESS**</dt></span></span> </dl>     | <span data-ttu-id="47ad1-184">IP-адрес vines (6-байтовая сущность).</span><span class="sxs-lookup"><span data-stu-id="47ad1-184">Vines IP address (6-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="PROP_TYPE_VAR_LEN_SMALL_INT"></span><span id="prop_type_var_len_small_int"></span><dl> <span data-ttu-id="47ad1-185"><dt>**\_тип Prop \_ var \_ \_ малый \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-185"><dt>**PROP\_TYPE\_VAR\_LEN\_SMALL\_INT**</dt></span></span> </dl> | <span data-ttu-id="47ad1-186">Числовое значение без предварительно определенной длины, но не более 8 байт.</span><span class="sxs-lookup"><span data-stu-id="47ad1-186">Numeric value without a pre-determined length, but no more than 8 bytes long.</span></span> <span data-ttu-id="47ad1-187">Длина присоединенных данных определяет длину значения.</span><span class="sxs-lookup"><span data-stu-id="47ad1-187">The length of the attached data determines the length of the value.</span></span><br/>                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="47ad1-188">**Квалификаторы**</span><span class="sxs-lookup"><span data-stu-id="47ad1-188">**DataQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="47ad1-189">Квалификатор данных свойства.</span><span class="sxs-lookup"><span data-stu-id="47ad1-189">The data qualifier of a property.</span></span> <span data-ttu-id="47ad1-190">Этот элемент предоставляет точную информацию о типе данных.</span><span class="sxs-lookup"><span data-stu-id="47ad1-190">This member provides precise information about the data type.</span></span>

<span data-ttu-id="47ad1-191">**Квалификатор** данных может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="47ad1-191">**DataQualifier** can have one of the following values.</span></span>



| <span data-ttu-id="47ad1-192">Значение</span><span class="sxs-lookup"><span data-stu-id="47ad1-192">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="47ad1-193">Значение</span><span class="sxs-lookup"><span data-stu-id="47ad1-193">Meaning</span></span>                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_QUAL_NONE"></span><span id="prop_qual_none"></span><dl> <span data-ttu-id="47ad1-194"><dt>**PROP \_ куал \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-194"><dt>**PROP\_QUAL\_NONE**</dt></span></span> </dl>                                      | <span data-ttu-id="47ad1-195">Единственным указанием свойства является тип данных свойства.</span><span class="sxs-lookup"><span data-stu-id="47ad1-195">The property data type is the only specification of the property.</span></span> <br/> <span data-ttu-id="47ad1-196">Если это значение задано, член объединения структуры устанавливается в **значение NULL**, а затем игнорируется.</span><span class="sxs-lookup"><span data-stu-id="47ad1-196">When this value is set, the union member of the structure is set to **NULL**, and then ignored.</span></span><br/>                                                                                                                                        |
| <span id="PROP_QUAL_RANGE"></span><span id="prop_qual_range"></span><dl> <span data-ttu-id="47ad1-197"><dt>**\_куал \_ диапазон свойств**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-197"><dt>**PROP\_QUAL\_RANGE**</dt></span></span> </dl>                                   | <span data-ttu-id="47ad1-198">Числовое значение должно находиться в пределах заданного диапазона.</span><span class="sxs-lookup"><span data-stu-id="47ad1-198">The numeric value is expected to be within a given range.</span></span> <span data-ttu-id="47ad1-199">Определите диапазон в элементе **лпранже** .</span><span class="sxs-lookup"><span data-stu-id="47ad1-199">Define the range in the **lpRange** member.</span></span><br/>                                                                                                                                                                                                                |
| <span id="PROP_QUAL_SET"></span><span id="prop_qual_set"></span><dl> <span data-ttu-id="47ad1-200"><dt>**\_Параметр prop куал \_ Set**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-200"><dt>**PROP\_QUAL\_SET**</dt></span></span> </dl>                                         | <span data-ttu-id="47ad1-201">Значение свойства сравнивается с набором значений, указанных в элементе **лпсет** объединения структуры.</span><span class="sxs-lookup"><span data-stu-id="47ad1-201">The value of a property is compared to a set of values that are specified in the **lpSet** member of the structure's union.</span></span> <span data-ttu-id="47ad1-202">Значением свойства может быть **Byte**, **Word**, **DWORD**, **ларжеинт** или **time**.</span><span class="sxs-lookup"><span data-stu-id="47ad1-202">The value of a property can be a **BYTE**, **WORD**, **DWORD**, **LARGEINT** or **TIME**.</span></span><br/>                                                                                                |
| <span id="PROP_QUAL_BITFIELD"></span><span id="prop_qual_bitfield"></span><dl> <span data-ttu-id="47ad1-203"><dt>**PROP \_ куал, \_ битовое поле**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-203"><dt>**PROP\_QUAL\_BITFIELD**</dt></span></span> </dl>                          | <span data-ttu-id="47ad1-204">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="47ad1-204">Obsolete.</span></span><br/>                                                                                                                                                                                                                                                                                                            |
| <span id="PROP_QUAL_LABELED_SET"></span><span id="prop_qual_labeled_set"></span><dl> <span data-ttu-id="47ad1-205"><dt>**\_Параметр prop куал \_ с меткой \_ Set**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-205"><dt>**PROP\_QUAL\_LABELED\_SET**</dt></span></span> </dl>                | <span data-ttu-id="47ad1-206">Значение свойства сравнивается со значением в наборе пар меток значений.</span><span class="sxs-lookup"><span data-stu-id="47ad1-206">The value of a property is compared to a value in a set of value label pairs.</span></span> <span data-ttu-id="47ad1-207">Пары меток значений указываются в элементе **лпсет** объединения структуры.</span><span class="sxs-lookup"><span data-stu-id="47ad1-207">The value label pairs are specified in the **lpSet** member of the structure's union.</span></span> <br/> <span data-ttu-id="47ad1-208">Во время отображения, если значение свойства совпадает со значением в наборе, отображается и значение, и связанная метка.</span><span class="sxs-lookup"><span data-stu-id="47ad1-208">At display time, if the value of the property matches a value in the set, then both a value, and the associated label are displayed.</span></span><br/> |
| <span id="PROP_QUAL_LABELED_BITFIELD"></span><span id="prop_qual_labeled_bitfield"></span><dl> <span data-ttu-id="47ad1-209"><dt>**PROP \_ куал \_ с меткой \_ битового поля**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-209"><dt>**PROP\_QUAL\_LABELED\_BITFIELD**</dt></span></span> </dl> | <span data-ttu-id="47ad1-210">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="47ad1-210">Obsolete.</span></span> <span data-ttu-id="47ad1-211">\_ \_ Вместо этого используйте флаги Prop куал.</span><span class="sxs-lookup"><span data-stu-id="47ad1-211">Use PROP\_QUAL\_FLAGS instead.</span></span><br/>                                                                                                                                                                                                                                                                             |
| <span id="PROP_QUAL_CONST"></span><span id="prop_qual_const"></span><dl> <span data-ttu-id="47ad1-212"><dt>**PROP \_ куал \_ const**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-212"><dt>**PROP\_QUAL\_CONST**</dt></span></span> </dl>                                   | <span data-ttu-id="47ad1-213">Значение свойства сравнивается с константой, указанной в элементе **value** объединения.</span><span class="sxs-lookup"><span data-stu-id="47ad1-213">The value of a property is compared to a constant that is specified in the **Value** member of the union.</span></span> <br/> <span data-ttu-id="47ad1-214">В момент отображения, если значения и константы свойств не совпадают, отображается отформатированное сообщение об ошибке со значением, заданным как обычная.</span><span class="sxs-lookup"><span data-stu-id="47ad1-214">At display time, if the property values and constant do not match, a formatted error message appears with the value set as Normal.</span></span><br/>                                                             |
| <span id="PROP_QUAL_FLAGS"></span><span id="prop_qual_flags"></span><dl> <span data-ttu-id="47ad1-215"><dt>**\_куал \_ ФЛАГи Prop**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-215"><dt>**PROP\_QUAL\_FLAGS**</dt></span></span> </dl>                                   | <span data-ttu-id="47ad1-216">Значение свойства сравнивается с определенными битами, указанными в элементе **лпсет** объединения.</span><span class="sxs-lookup"><span data-stu-id="47ad1-216">The value of the property is compared to specific BITs identified in the **lpSet** member of the union.</span></span><br/>                                                                                                                                                                                                              |
| <span id="PROP_QUAL_ARRAY"></span><span id="prop_qual_array"></span><dl> <span data-ttu-id="47ad1-217"><dt>**PROP \_ куал, \_ массив**</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-217"><dt>**PROP\_QUAL\_ARRAY**</dt></span></span> </dl>                                   | <span data-ttu-id="47ad1-218">Значение свойства указывает массив значений.</span><span class="sxs-lookup"><span data-stu-id="47ad1-218">The value of a property specifies an array of values.</span></span> <span data-ttu-id="47ad1-219">Длина присоединенных данных определяет длину массива.</span><span class="sxs-lookup"><span data-stu-id="47ad1-219">The length of attached data determines the length of an array.</span></span> <br/> <span data-ttu-id="47ad1-220">Если \_ \_ задано значение свойства Prop куал Array, член объединения структуры данных **PROPERTYINFO** устанавливается в **значение NULL** и игнорируется.</span><span class="sxs-lookup"><span data-stu-id="47ad1-220">When the PROP\_QUAL\_ARRAY value is set, the union member of the **PROPERTYINFO** data structure is set to **NULL** and ignored.</span></span><br/>                                                    |



 

</dd> <dt>

<span data-ttu-id="47ad1-221">**лпекстендединфо**</span><span class="sxs-lookup"><span data-stu-id="47ad1-221">**lpExtendedInfo**</span></span>
</dt> <dd>

<span data-ttu-id="47ad1-222">Зарезервировано (член объединения).</span><span class="sxs-lookup"><span data-stu-id="47ad1-222">Reserved (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="47ad1-223">**лпранже**</span><span class="sxs-lookup"><span data-stu-id="47ad1-223">**lpRange**</span></span>
</dt> <dd>

<span data-ttu-id="47ad1-224">Указатель на структуру [диапазона](range.md) , определяющую диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="47ad1-224">Pointer to a [RANGE](range.md) structure that defines a range of values.</span></span> <span data-ttu-id="47ad1-225">Этот элемент должен быть задан, если элементу **квалификатора** данных этой структуры задано значение Prop \_ куал \_ Range (элемент Union).</span><span class="sxs-lookup"><span data-stu-id="47ad1-225">This member must be set if the **DataQualifier** member of this structure is set to PROP\_QUAL\_RANGE (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="47ad1-226">**лпсет**</span><span class="sxs-lookup"><span data-stu-id="47ad1-226">**lpSet**</span></span>
</dt> <dd>

<span data-ttu-id="47ad1-227">Указатель на [набор](set.md) , указывающий набор значений или меток.</span><span class="sxs-lookup"><span data-stu-id="47ad1-227">Pointer to a [SET](set.md) structure that specifies a set of values or labels.</span></span> <span data-ttu-id="47ad1-228">Этот элемент должен быть задан, если члену **квалификатора** структуры задано значение Prop \_ КУАЛ \_ Set, PROP \_ куал \_ \_ Set или Prop \_ куал \_ Flags (Member of Union).</span><span class="sxs-lookup"><span data-stu-id="47ad1-228">This member must be set if the **DataQualifier** member of the structure is set to PROP\_QUAL\_SET, PROP\_QUAL\_LABELED\_SET, or PROP\_QUAL\_FLAGS (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="47ad1-229">**Битовые**</span><span class="sxs-lookup"><span data-stu-id="47ad1-229">**Bitmask**</span></span>
</dt> <dd>

<span data-ttu-id="47ad1-230">Устаревший (член объединения).</span><span class="sxs-lookup"><span data-stu-id="47ad1-230">Obsolete (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="47ad1-231">**Значение**</span><span class="sxs-lookup"><span data-stu-id="47ad1-231">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="47ad1-232">Постоянное значение, используемое, если для **квалификатора** данных установлено значение Prop \_ куал \_ const (член объединения).</span><span class="sxs-lookup"><span data-stu-id="47ad1-232">Constant value used when the **DataQualifier** is set to PROP\_QUAL\_CONST (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="47ad1-233">**форматстрингсизе**</span><span class="sxs-lookup"><span data-stu-id="47ad1-233">**FormatStringSize**</span></span>
</dt> <dd>

<span data-ttu-id="47ad1-234">Максимальный размер, используемый только для описания свойства.</span><span class="sxs-lookup"><span data-stu-id="47ad1-234">Maximum size used only for the property description.</span></span>

</dd> <dt>

<span data-ttu-id="47ad1-235">**инстанцедата**</span><span class="sxs-lookup"><span data-stu-id="47ad1-235">**InstanceData**</span></span>
</dt> <dd>

<span data-ttu-id="47ad1-236">Укажите функцию Format, которая вызывается для форматирования отображаемых данных для свойства.</span><span class="sxs-lookup"><span data-stu-id="47ad1-236">Specify the format function that is called to format the displayed data for the property.</span></span> <span data-ttu-id="47ad1-237">Чтобы использовать универсальный модуль форматирования, укажите функцию **форматпропертинстанце** .</span><span class="sxs-lookup"><span data-stu-id="47ad1-237">To use the generic formatter, specify the **FormatPropertyInstance** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47ad1-238">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47ad1-238">Remarks</span></span>

<span data-ttu-id="47ad1-239">Структура **PROPERTYINFO** используется в вызовах функции [AddProperty](/previous-versions/bb251873(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="47ad1-239">The **PROPERTYINFO** structure is used in calls to the [AddProperty](/previous-versions/bb251873(v=msdn.10)) function.</span></span> <span data-ttu-id="47ad1-240">Функция **AddProperty** добавляет одно определение свойства в [*базу данных свойств*](p.md)средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="47ad1-240">The **AddProperty** function adds a single property definition to the parser [*property database*](p.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="47ad1-241">Требования</span><span class="sxs-lookup"><span data-stu-id="47ad1-241">Requirements</span></span>



| <span data-ttu-id="47ad1-242">Требование</span><span class="sxs-lookup"><span data-stu-id="47ad1-242">Requirement</span></span> | <span data-ttu-id="47ad1-243">Значение</span><span class="sxs-lookup"><span data-stu-id="47ad1-243">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="47ad1-244">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47ad1-244">Minimum supported client</span></span><br/> | <span data-ttu-id="47ad1-245">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="47ad1-245">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="47ad1-246">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47ad1-246">Minimum supported server</span></span><br/> | <span data-ttu-id="47ad1-247">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="47ad1-247">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="47ad1-248">Заголовок</span><span class="sxs-lookup"><span data-stu-id="47ad1-248">Header</span></span><br/>                   | <dl> <span data-ttu-id="47ad1-249"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="47ad1-249"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47ad1-250">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47ad1-250">See also</span></span>

<dl> <dt>

<span data-ttu-id="47ad1-251">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="47ad1-251">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="47ad1-252">РАЗНООБРАЗ</span><span class="sxs-lookup"><span data-stu-id="47ad1-252">RANGE</span></span>](range.md)
</dt> <dt>

[<span data-ttu-id="47ad1-253">SET</span><span class="sxs-lookup"><span data-stu-id="47ad1-253">SET</span></span>](set.md)
</dt> </dl>

 

