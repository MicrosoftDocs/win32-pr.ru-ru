---
description: Представляет запись атрибута.
ms.assetid: f9d9458c-b179-441c-9f62-ff0ac2f75329
title: Структура ATTRIBUTE_RECORD_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_RECORD_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ae710ca04f11cb70c1bad9b5e6fec25f8fb5e94f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895366"
---
# <a name="attribute_record_header-structure"></a><span data-ttu-id="e887f-103">\_ \_ Структура заголовка записи атрибута</span><span class="sxs-lookup"><span data-stu-id="e887f-103">ATTRIBUTE\_RECORD\_HEADER structure</span></span>

<span data-ttu-id="e887f-104">\[Эта структура допустима только для томов NTFS версии 3; Он может быть изменен в будущих версиях.\]</span><span class="sxs-lookup"><span data-stu-id="e887f-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="e887f-105">Представляет запись атрибута.</span><span class="sxs-lookup"><span data-stu-id="e887f-105">Represents an attribute record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e887f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e887f-106">Syntax</span></span>


```C++
typedef struct _ATTRIBUTE_RECORD_HEADER {
  ATTRIBUTE_TYPE_CODE TypeCode;
  ULONG               RecordLength;
  UCHAR               FormCode;
  UCHAR               NameLength;
  USHORT              NameOffset;
  USHORT              Flags;
  USHORT              Instance;
  union {
    struct {
      ULONG  ValueLength;
      USHORT ValueOffset;
      UCHAR  Reserved[2];
    } Resident;
    struct {
      VCN      LowestVcn;
      VCN      HighestVcn;
      USHORT   MappingPairsOffset;
      UCHAR    Reserved[6];
      LONGLONG AllocatedLength;
      LONGLONG FileSize;
      LONGLONG ValidDataLength;
      LONGLONG TotalAllocated;
    } Nonresident;
  } Form;
} ATTRIBUTE_RECORD_HEADER, *PATTRIBUTE_RECORD_HEADER;
```



## <a name="members"></a><span data-ttu-id="e887f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="e887f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e887f-108">**Код типа**</span><span class="sxs-lookup"><span data-stu-id="e887f-108">**TypeCode**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-109">Код типа атрибута.</span><span class="sxs-lookup"><span data-stu-id="e887f-109">The attribute type code.</span></span>



| <span data-ttu-id="e887f-110">Значение</span><span class="sxs-lookup"><span data-stu-id="e887f-110">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="e887f-111">Значение</span><span class="sxs-lookup"><span data-stu-id="e887f-111">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <span data-ttu-id="e887f-112"><dt>**$Standard \_ СВЕДЕНИЯ**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="e887f-112"><dt>**$STANDARD\_INFORMATION**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="e887f-113">Атрибуты файлов (например, только для чтения и архивация), метки времени (например, создание файла и Последнее изменение) и число жестких связей.</span><span class="sxs-lookup"><span data-stu-id="e887f-113">File attributes (such as read-only and archive), time stamps (such as file creation and last modified), and the hard link count.</span></span><br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <span data-ttu-id="e887f-114"><dt>**$Attribute \_ Список**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="e887f-114"><dt>**$ATTRIBUTE\_LIST**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="e887f-115">Список атрибутов, образующих файл, и ссылка на файл записи MFT, в которой расположен каждый атрибут.</span><span class="sxs-lookup"><span data-stu-id="e887f-115">A list of attributes that make up the file and the file reference of the MFT file record in which each attribute is located.</span></span><br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <span data-ttu-id="e887f-116"><dt>**$File \_ ИМЯ**</dt> <dt>0x30</dt></span><span class="sxs-lookup"><span data-stu-id="e887f-116"><dt>**$FILE\_NAME**</dt> <dt>0x30</dt></span></span> </dl>                                  | <span data-ttu-id="e887f-117">Имя файла в символах Юникода.</span><span class="sxs-lookup"><span data-stu-id="e887f-117">The name of the file, in Unicode characters.</span></span><br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <span data-ttu-id="e887f-118"><dt>**$Object \_ Идентификатор**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="e887f-118"><dt>**$OBJECT\_ID**</dt> <dt>0x40</dt></span></span> </dl>                                  | <span data-ttu-id="e887f-119">64-байтовый идентификатор объекта, назначенный службой отслеживания ссылок.</span><span class="sxs-lookup"><span data-stu-id="e887f-119">An 64-byte object identifier assigned by the link-tracking service.</span></span><br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <span data-ttu-id="e887f-120"><dt>**$Volume \_ ИМЯ**</dt> <dt>0x60</dt></span><span class="sxs-lookup"><span data-stu-id="e887f-120"><dt>**$VOLUME\_NAME**</dt> <dt>0x60</dt></span></span> </dl>                            | <span data-ttu-id="e887f-121">Метка тома.</span><span class="sxs-lookup"><span data-stu-id="e887f-121">The volume label.</span></span> <span data-ttu-id="e887f-122">Содержится в файле $Volume.</span><span class="sxs-lookup"><span data-stu-id="e887f-122">Present in the $Volume file.</span></span><br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <span data-ttu-id="e887f-123"><dt>**$Volume \_ СВЕДЕНИЯ**</dt> <dt>0x70</dt></span><span class="sxs-lookup"><span data-stu-id="e887f-123"><dt>**$VOLUME\_INFORMATION**</dt> <dt>0x70</dt></span></span> </dl>       | <span data-ttu-id="e887f-124">Сведения о томе.</span><span class="sxs-lookup"><span data-stu-id="e887f-124">The volume information.</span></span> <span data-ttu-id="e887f-125">Содержится в файле $Volume.</span><span class="sxs-lookup"><span data-stu-id="e887f-125">Present in the $Volume file.</span></span><br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <span data-ttu-id="e887f-126"><dt>**$Data**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="e887f-126"><dt>**$DATA**</dt> <dt>0x80</dt></span></span> </dl>                                                  | <span data-ttu-id="e887f-127">Содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="e887f-127">The contents of the file.</span></span><br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <span data-ttu-id="e887f-128"><dt>**$Index \_ КОРНЕВой**</dt> <dt>0x90</dt></span><span class="sxs-lookup"><span data-stu-id="e887f-128"><dt>**$INDEX\_ROOT**</dt> <dt>0x90</dt></span></span> </dl>                               | <span data-ttu-id="e887f-129">Используется для реализации выделения имен файлов для больших каталогов.</span><span class="sxs-lookup"><span data-stu-id="e887f-129">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <span data-ttu-id="e887f-130"><dt>**$Index \_**</dt> <dt>0x82</dt> выделения</span><span class="sxs-lookup"><span data-stu-id="e887f-130"><dt>**$INDEX\_ALLOCATION**</dt> <dt>0xA0</dt></span></span> </dl>             | <span data-ttu-id="e887f-131">Используется для реализации выделения имен файлов для больших каталогов.</span><span class="sxs-lookup"><span data-stu-id="e887f-131">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <span data-ttu-id="e887f-132"><dt>**$Bitmap**</dt> <dt>0xB0</dt></span><span class="sxs-lookup"><span data-stu-id="e887f-132"><dt>**$BITMAP**</dt> <dt>0xB0</dt></span></span> </dl>                                            | <span data-ttu-id="e887f-133">Индекс точечного рисунка для большого каталога.</span><span class="sxs-lookup"><span data-stu-id="e887f-133">A bitmap index for a large directory.</span></span><br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <span data-ttu-id="e887f-134"><dt>**$REPARSE \_ ТОЧКА**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="e887f-134"><dt>**$REPARSE\_POINT**</dt> <dt>0xC0</dt></span></span> </dl>                      | <span data-ttu-id="e887f-135">Данные точки повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="e887f-135">The reparse point data.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="e887f-136">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="e887f-136">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-137">Размер записи атрибута в байтах.</span><span class="sxs-lookup"><span data-stu-id="e887f-137">The size of the attribute record, in bytes.</span></span> <span data-ttu-id="e887f-138">Это значение отражает требуемый размер для варианта записи и всегда округляется до ближайшей границы куадворд.</span><span class="sxs-lookup"><span data-stu-id="e887f-138">This value reflects the required size for the record variant and is always rounded to the nearest quadword boundary.</span></span>

</dd> <dt>

<span data-ttu-id="e887f-139">**формкоде**</span><span class="sxs-lookup"><span data-stu-id="e887f-139">**FormCode**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-140">Код формы атрибута.</span><span class="sxs-lookup"><span data-stu-id="e887f-140">The attribute form code.</span></span>



| <span data-ttu-id="e887f-141">Значение</span><span class="sxs-lookup"><span data-stu-id="e887f-141">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="e887f-142">Значение</span><span class="sxs-lookup"><span data-stu-id="e887f-142">Meaning</span></span>                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="RESIDENT_FORM"></span><span id="resident_form"></span><dl> <span data-ttu-id="e887f-143"><dt>**Резидентная \_ ФОРМА**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="e887f-143"><dt>**RESIDENT\_FORM**</dt> <dt>0x00</dt></span></span> </dl>          | <span data-ttu-id="e887f-144">Значение содержится в записи файла и сразу после заголовка записи атрибута.</span><span class="sxs-lookup"><span data-stu-id="e887f-144">The value is contained in the file record and immediately follows the attribute record header.</span></span><br/> |
| <span id="NONRESIDENT_FORM"></span><span id="nonresident_form"></span><dl> <span data-ttu-id="e887f-145"><dt>**НЕрезидентная \_ ФОРМА**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="e887f-145"><dt>**NONRESIDENT\_FORM**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="e887f-146">Значение содержится в других секторах на диске.</span><span class="sxs-lookup"><span data-stu-id="e887f-146">The value is contained in other sectors on the disk.</span></span><br/>                                           |



 

</dd> <dt>

<span data-ttu-id="e887f-147">**NameLength**</span><span class="sxs-lookup"><span data-stu-id="e887f-147">**NameLength**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-148">Размер необязательного имени атрибута, в символах или 0, если имя атрибута отсутствует.</span><span class="sxs-lookup"><span data-stu-id="e887f-148">The size of the optional attribute name, in characters, or 0 if there is no attribute name.</span></span> <span data-ttu-id="e887f-149">Максимальная длина имени атрибута — 255 символов.</span><span class="sxs-lookup"><span data-stu-id="e887f-149">The maximum attribute name length is 255 characters.</span></span>

</dd> <dt>

<span data-ttu-id="e887f-150">**намеоффсет**</span><span class="sxs-lookup"><span data-stu-id="e887f-150">**NameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-151">Смещение имени атрибута от начала записи атрибута в байтах.</span><span class="sxs-lookup"><span data-stu-id="e887f-151">The offset of the attribute name from the start of the attribute record, in bytes.</span></span> <span data-ttu-id="e887f-152">Если элемент **намеленгс** имеет значение 0, этот член не определен.</span><span class="sxs-lookup"><span data-stu-id="e887f-152">If the **NameLength** member is 0, this member is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="e887f-153">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="e887f-153">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-154">Флаги атрибута.</span><span class="sxs-lookup"><span data-stu-id="e887f-154">The attribute flags.</span></span>

<dl> <dt>

<span data-ttu-id="e887f-155"><span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**Атрибут \_ ФЛАГ \_ \_ маски сжатия** (0x00FF)</span><span class="sxs-lookup"><span data-stu-id="e887f-155"><span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**ATTRIBUTE\_FLAG\_COMPRESSION\_MASK** (0x00FF)</span></span>
</dt> <dt>

<span data-ttu-id="e887f-156"><span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**Атрибут \_ ФЛАГ \_ разреженного** (0x8000)</span><span class="sxs-lookup"><span data-stu-id="e887f-156"><span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**ATTRIBUTE\_FLAG\_SPARSE** (0x8000)</span></span>
</dt> <dt>

<span data-ttu-id="e887f-157"><span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**Атрибут \_ ФЛАГ \_ зашифрован** (0x4000)</span><span class="sxs-lookup"><span data-stu-id="e887f-157"><span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**ATTRIBUTE\_FLAG\_ENCRYPTED** (0x4000)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="e887f-158">**Экземпляр**</span><span class="sxs-lookup"><span data-stu-id="e887f-158">**Instance**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-159">Уникальный экземпляр для этого атрибута в записи файла.</span><span class="sxs-lookup"><span data-stu-id="e887f-159">The unique instance for this attribute in the file record.</span></span>

</dd> <dt>

<span data-ttu-id="e887f-160">**Form**</span><span class="sxs-lookup"><span data-stu-id="e887f-160">**Form**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-161">Если элемент **формкоде** является резидентной \_ формой, объединение является **резидентной** структурой.</span><span class="sxs-lookup"><span data-stu-id="e887f-161">If the **FormCode** member is RESIDENT\_FORM, the union is a **Resident** structure.</span></span> <span data-ttu-id="e887f-162">Если **формкоде** является нерезидентной \_ формой, объединение является **нерезидентной** структурой.</span><span class="sxs-lookup"><span data-stu-id="e887f-162">If **FormCode** is NONRESIDENT\_FORM, the union is a **Nonresident** structure.</span></span>

<dl> <dt>

<span data-ttu-id="e887f-163">**Принтера**</span><span class="sxs-lookup"><span data-stu-id="e887f-163">**Resident**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e887f-164">**валуеленгс**</span><span class="sxs-lookup"><span data-stu-id="e887f-164">**ValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-165">Размер значения атрибута в байтах.</span><span class="sxs-lookup"><span data-stu-id="e887f-165">The size of the attribute value, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e887f-166">**валуеоффсет**</span><span class="sxs-lookup"><span data-stu-id="e887f-166">**ValueOffset**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-167">Смещение значения от начала записи атрибута в байтах.</span><span class="sxs-lookup"><span data-stu-id="e887f-167">The offset to the value from the start of the attribute record, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e887f-168">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="e887f-168">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-169">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="e887f-169">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e887f-170">**Нерезидентная**</span><span class="sxs-lookup"><span data-stu-id="e887f-170">**Nonresident**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e887f-171">**ловествкн**</span><span class="sxs-lookup"><span data-stu-id="e887f-171">**LowestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-172">Самый низкий номер виртуального кластера (VCN), охватываемый этой записью атрибута.</span><span class="sxs-lookup"><span data-stu-id="e887f-172">The lowest virtual cluster number (VCN) covered by this attribute record.</span></span>

</dd> <dt>

<span data-ttu-id="e887f-173">**хигхествкн**</span><span class="sxs-lookup"><span data-stu-id="e887f-173">**HighestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-174">Самое высокое значение VCN, охваченное этой записью атрибута.</span><span class="sxs-lookup"><span data-stu-id="e887f-174">The highest VCN covered by this attribute record.</span></span>

</dd> <dt>

<span data-ttu-id="e887f-175">**маппингпаирсоффсет**</span><span class="sxs-lookup"><span data-stu-id="e887f-175">**MappingPairsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-176">Смещение массива пар сопоставлений от начала записи атрибута в байтах.</span><span class="sxs-lookup"><span data-stu-id="e887f-176">The offset to the mapping pairs array from the start of the attribute record, in bytes.</span></span> <span data-ttu-id="e887f-177">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="e887f-177">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e887f-178">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="e887f-178">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-179">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="e887f-179">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e887f-180">**аллокатедленгс**</span><span class="sxs-lookup"><span data-stu-id="e887f-180">**AllocatedLength**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-181">Выделенный размер файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="e887f-181">The allocated size of the file, in bytes.</span></span> <span data-ttu-id="e887f-182">Это значение кратно размеру кластера.</span><span class="sxs-lookup"><span data-stu-id="e887f-182">This value is an even multiple of the cluster size.</span></span> <span data-ttu-id="e887f-183">Этот элемент является недопустимым, если элемент **ловествкн** не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="e887f-183">This member is not valid if the **LowestVcn** member is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="e887f-184">**Размер файла**</span><span class="sxs-lookup"><span data-stu-id="e887f-184">**FileSize**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-185">Размер файла (максимальный байт, который можно прочитать плюс 1) в байтах.</span><span class="sxs-lookup"><span data-stu-id="e887f-185">The file size (highest byte that can be read plus 1), in bytes.</span></span> <span data-ttu-id="e887f-186">Этот элемент является недопустимым, если **ловествкн** не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="e887f-186">This member is not valid if **LowestVcn** is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="e887f-187">**валиддаталенгс**</span><span class="sxs-lookup"><span data-stu-id="e887f-187">**ValidDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-188">Допустимая длина данных (наибольший инициализированный байт плюс 1) в байтах.</span><span class="sxs-lookup"><span data-stu-id="e887f-188">The valid data length (highest initialized byte plus 1), in bytes.</span></span> <span data-ttu-id="e887f-189">Это значение округляется до ближайшей границы кластера.</span><span class="sxs-lookup"><span data-stu-id="e887f-189">This value is rounded to the nearest cluster boundary.</span></span> <span data-ttu-id="e887f-190">Этот элемент является недопустимым, если **ловествкн** не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="e887f-190">This member is not valid if **LowestVcn** is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="e887f-191">**тоталаллокатед**</span><span class="sxs-lookup"><span data-stu-id="e887f-191">**TotalAllocated**</span></span>
</dt> <dd>

<span data-ttu-id="e887f-192">Общее значение, выделенное для файла (сумма выделенных кластеров).</span><span class="sxs-lookup"><span data-stu-id="e887f-192">The total allocated for the file (the sum of the allocated clusters).</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e887f-193">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e887f-193">Remarks</span></span>

<span data-ttu-id="e887f-194">Обратите внимание, что для этой структуры нет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="e887f-194">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="e887f-195">Это определение структуры допустимо только для основной версии 3 и дополнительной версии 0 или 1, как сообщается [**фсктл \_ Получение \_ \_ \_ данных тома NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="e887f-195">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="e887f-196">Записи атрибутов всегда выводятся по границе куадворд.</span><span class="sxs-lookup"><span data-stu-id="e887f-196">Attribute records are always aligned on a quadword boundary.</span></span>

<span data-ttu-id="e887f-197">Если атрибут не является резидентным, заголовок записи атрибута содержит список сведений о извлечении, которые предоставляют сопоставление между VCN и Number логического кластера (LCN) для атрибута.</span><span class="sxs-lookup"><span data-stu-id="e887f-197">If the attribute is nonresident, the attribute record header contains a list of retrieval information that provides a mapping between VCN and logical cluster number (LCN) for the attribute.</span></span> <span data-ttu-id="e887f-198">Если сведения о извлечении не помещаются в основном сегменте файла, они могут храниться в сегменте записи внешнего файла сами по себе.</span><span class="sxs-lookup"><span data-stu-id="e887f-198">If the retrieval information does not fit in the base file segment, it can be stored in an external file record segment by itself.</span></span> <span data-ttu-id="e887f-199">Если он по-прежнему не помещается в сегмент записи внешнего файла, в списке атрибутов можно включить несколько записей для атрибута, требующих дополнительных сведений для получения.</span><span class="sxs-lookup"><span data-stu-id="e887f-199">If it still does not fit into one external file record segment, there is a provision in the attribute list to contain multiple entries for an attribute that requires additional retrieval information.</span></span>

<span data-ttu-id="e887f-200">Массив пар сопоставления хранится в сжатой форме и предполагает, что информация распакована и кэшируется системой.</span><span class="sxs-lookup"><span data-stu-id="e887f-200">The mapping pairs array is stored in a compressed form and assumes that the information is decompressed and cached by the system.</span></span> <span data-ttu-id="e887f-201">Он состоит из серии пар Некствкн/Куррентлкн.</span><span class="sxs-lookup"><span data-stu-id="e887f-201">It consists of a series of NextVcn/CurrentLcn pairs.</span></span> <span data-ttu-id="e887f-202">Например, если файл имеет один запуск из 8 кластеров, начиная с LCN 128, а файл начинается с Ловествкн 0, то массив пар сопоставлений содержит только одну запись, которая имеет Некствкн = 8 и Куррентлкн = 128.</span><span class="sxs-lookup"><span data-stu-id="e887f-202">For example, if a file has a single run of 8 clusters starting at LCN 128 and the file starts at LowestVcn 0, then the mapping pairs array has just one entry, which is NextVcn=8 and CurrentLcn=128.</span></span> <span data-ttu-id="e887f-203">Массив представляет собой байтовый поток, который сохраняет изменения в рабочих переменных при последовательной обработке.</span><span class="sxs-lookup"><span data-stu-id="e887f-203">The array is a byte stream that stores the changes to the working variables when processed sequentially.</span></span> <span data-ttu-id="e887f-204">Поток байтов интерпретируется как поток Triple с нулевым нулем, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="e887f-204">The byte stream is to be interpreted as a zero-terminated stream of triples, as follows:</span></span>

<span data-ttu-id="e887f-205">Счетчик Byte = *v* + (*l* \* 16)</span><span class="sxs-lookup"><span data-stu-id="e887f-205">count byte = *v* + (*l* \* 16)</span></span>

<span data-ttu-id="e887f-206">где *v* — число измененных младших байтов VCN, а *l* — число измененных байт LCN с низким порядковым номером.</span><span class="sxs-lookup"><span data-stu-id="e887f-206">where *v* is the number of changed low-order VCN bytes and *l* is the number of changed low-order LCN bytes.</span></span>

<span data-ttu-id="e887f-207">Алгоритм распаковки выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e887f-207">The decompression algorithm is as follows:</span></span>

1.  <span data-ttu-id="e887f-208">Инициализируйте Некствкн `Attribute->LowestVcn` и куррентлкн до 0.</span><span class="sxs-lookup"><span data-stu-id="e887f-208">Initialize NextVcn to `Attribute->LowestVcn` and CurrentLcn to 0.</span></span>
2.  <span data-ttu-id="e887f-209">Инициализирует указатель потока байтов на `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset` .</span><span class="sxs-lookup"><span data-stu-id="e887f-209">Initialize the byte stream pointer to `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset`.</span></span>
3.  <span data-ttu-id="e887f-210">Задайте для Куррентвкн значение Некствкн.</span><span class="sxs-lookup"><span data-stu-id="e887f-210">Set CurrentVcn to NextVcn.</span></span>
4.  <span data-ttu-id="e887f-211">Считывает следующий байт из потока.</span><span class="sxs-lookup"><span data-stu-id="e887f-211">Read the next byte from the stream.</span></span> <span data-ttu-id="e887f-212">Если значение равно 0, то Break; иначе Извлеките *v* и *l* , как описано выше.</span><span class="sxs-lookup"><span data-stu-id="e887f-212">If it is 0, then break; else extract *v* and *l* as previously described.</span></span>
5.  <span data-ttu-id="e887f-213">Интерпретирует следующие *v* байты как количество со знаком, а сначала байт нижнего порядка.</span><span class="sxs-lookup"><span data-stu-id="e887f-213">Interpret the next *v* bytes as a signed quantity, with the low-order byte first.</span></span> <span data-ttu-id="e887f-214">Распакуйте подписывание подписывания на 64 бит и добавьте его в Некствкн.</span><span class="sxs-lookup"><span data-stu-id="e887f-214">Unpack it sign-extended into 64 bits and add it to NextVcn.</span></span>
6.  <span data-ttu-id="e887f-215">Интерпретировать следующие *l* байты как количество со знаком, начиная с младшего байта.</span><span class="sxs-lookup"><span data-stu-id="e887f-215">Interpret the next *l* bytes as a signed quantity, with the low-order byte first.</span></span> <span data-ttu-id="e887f-216">Распакуйте подписывание подписывания на 64 бит и добавьте его в Куррентлкн.</span><span class="sxs-lookup"><span data-stu-id="e887f-216">Unpack it sign-extended into 64 bits and add it to CurrentLcn.</span></span> <span data-ttu-id="e887f-217">Если это Куррентлкн 0, то Вкнс из Куррентвкн в Некствкн – 1 не распределены.</span><span class="sxs-lookup"><span data-stu-id="e887f-217">If this produces a CurrentLcn of 0, then the VCNs from CurrentVcn to NextVcn–1 are unallocated.</span></span>
7.  <span data-ttu-id="e887f-218">Обновите кэшированные сведения о сопоставлении из Куррентвкн, Некствкн и Куррентлкн.</span><span class="sxs-lookup"><span data-stu-id="e887f-218">Update the cached mapping information from CurrentVcn, NextVcn, and CurrentLcn.</span></span>
8.  <span data-ttu-id="e887f-219">Перейдите к шагу 3.</span><span class="sxs-lookup"><span data-stu-id="e887f-219">Go to step 3.</span></span>

## <a name="see-also"></a><span data-ttu-id="e887f-220">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e887f-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e887f-221">Основная таблица файлов</span><span class="sxs-lookup"><span data-stu-id="e887f-221">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
