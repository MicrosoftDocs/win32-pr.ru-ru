---
description: Представляет запись в списке атрибутов.
ms.assetid: daa0c97d-2ebe-4e14-b1f8-e4be3075b13e
title: Структура ATTRIBUTE_LIST_ENTRY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_LIST_ENTRY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 67ee65a22c9e880c76d3b250c4859077f471b018
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895369"
---
# <a name="attribute_list_entry-structure"></a><span data-ttu-id="240fb-103">\_ \_ Структура ввода списка атрибутов</span><span class="sxs-lookup"><span data-stu-id="240fb-103">ATTRIBUTE\_LIST\_ENTRY structure</span></span>

<span data-ttu-id="240fb-104">\[Эта структура допустима только для томов NTFS версии 3; Он может быть изменен в будущих версиях.\]</span><span class="sxs-lookup"><span data-stu-id="240fb-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="240fb-105">Представляет запись в списке атрибутов.</span><span class="sxs-lookup"><span data-stu-id="240fb-105">Represents an entry in the attribute list.</span></span>

## <a name="syntax"></a><span data-ttu-id="240fb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="240fb-106">Syntax</span></span>


```C++
typedef struct _ATTRIBUTE_LIST_ENTRY {
  ATTRIBUTE_TYPE_CODE   AttributeTypeCode;
  USHORT                RecordLength;
  UCHAR                 AttributeNameLength;
  UCHAR                 AttributeNameOffset;
  VCN                   LowestVcn;
  MFT_SEGMENT_REFERENCE SegmentReference;
  USHORT                Reserved;
  WCHAR                 AttributeName[1];
} ATTRIBUTE_LIST_ENTRY, *PATTRIBUTE_LIST_ENTRY;
```



## <a name="members"></a><span data-ttu-id="240fb-107">Члены</span><span class="sxs-lookup"><span data-stu-id="240fb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="240fb-108">**аттрибутетипекоде**</span><span class="sxs-lookup"><span data-stu-id="240fb-108">**AttributeTypeCode**</span></span>
</dt> <dd>

<span data-ttu-id="240fb-109">Код типа атрибута.</span><span class="sxs-lookup"><span data-stu-id="240fb-109">The attribute type code.</span></span>



| <span data-ttu-id="240fb-110">Значение</span><span class="sxs-lookup"><span data-stu-id="240fb-110">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="240fb-111">Значение</span><span class="sxs-lookup"><span data-stu-id="240fb-111">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <span data-ttu-id="240fb-112"><dt>**$Standard \_ СВЕДЕНИЯ**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="240fb-112"><dt>**$STANDARD\_INFORMATION**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="240fb-113">Атрибуты файлов (например, только для чтения и архивация), метки времени (например, создание файла и Последнее изменение) и число жестких связей.</span><span class="sxs-lookup"><span data-stu-id="240fb-113">File attributes (such as read-only and archive), time stamps (such as file creation and last modified), and the hard link count.</span></span><br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <span data-ttu-id="240fb-114"><dt>**$Attribute \_ Список**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="240fb-114"><dt>**$ATTRIBUTE\_LIST**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="240fb-115">Список атрибутов, образующих файл, и ссылка на файл записи MFT, в которой расположен каждый атрибут.</span><span class="sxs-lookup"><span data-stu-id="240fb-115">A list of attributes that make up the file and the file reference of the MFT file record in which each attribute is located.</span></span><br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <span data-ttu-id="240fb-116"><dt>**$File \_ ИМЯ**</dt> <dt>0x30</dt></span><span class="sxs-lookup"><span data-stu-id="240fb-116"><dt>**$FILE\_NAME**</dt> <dt>0x30</dt></span></span> </dl>                                  | <span data-ttu-id="240fb-117">Имя файла в символах Юникода.</span><span class="sxs-lookup"><span data-stu-id="240fb-117">The name of the file, in Unicode characters.</span></span><br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <span data-ttu-id="240fb-118"><dt>**$Object \_ Идентификатор**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="240fb-118"><dt>**$OBJECT\_ID**</dt> <dt>0x40</dt></span></span> </dl>                                  | <span data-ttu-id="240fb-119">16-байтовый идентификатор объекта, назначенный службой отслеживания ссылок.</span><span class="sxs-lookup"><span data-stu-id="240fb-119">An 16-byte object identifier assigned by the link-tracking service.</span></span><br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <span data-ttu-id="240fb-120"><dt>**$Volume \_ ИМЯ**</dt> <dt>0x60</dt></span><span class="sxs-lookup"><span data-stu-id="240fb-120"><dt>**$VOLUME\_NAME**</dt> <dt>0x60</dt></span></span> </dl>                            | <span data-ttu-id="240fb-121">Метка тома.</span><span class="sxs-lookup"><span data-stu-id="240fb-121">The volume label.</span></span> <span data-ttu-id="240fb-122">Содержится в файле $Volume.</span><span class="sxs-lookup"><span data-stu-id="240fb-122">Present in the $Volume file.</span></span><br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <span data-ttu-id="240fb-123"><dt>**$Volume \_ СВЕДЕНИЯ**</dt> <dt>0x70</dt></span><span class="sxs-lookup"><span data-stu-id="240fb-123"><dt>**$VOLUME\_INFORMATION**</dt> <dt>0x70</dt></span></span> </dl>       | <span data-ttu-id="240fb-124">Сведения о томе.</span><span class="sxs-lookup"><span data-stu-id="240fb-124">The volume information.</span></span> <span data-ttu-id="240fb-125">Содержится в файле $Volume.</span><span class="sxs-lookup"><span data-stu-id="240fb-125">Present in the $Volume file.</span></span><br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <span data-ttu-id="240fb-126"><dt>**$Data**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="240fb-126"><dt>**$DATA**</dt> <dt>0x80</dt></span></span> </dl>                                                  | <span data-ttu-id="240fb-127">Содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="240fb-127">The contents of the file.</span></span><br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <span data-ttu-id="240fb-128"><dt>**$Index \_ КОРНЕВой**</dt> <dt>0x90</dt></span><span class="sxs-lookup"><span data-stu-id="240fb-128"><dt>**$INDEX\_ROOT**</dt> <dt>0x90</dt></span></span> </dl>                               | <span data-ttu-id="240fb-129">Используется для реализации выделения имен файлов для больших каталогов.</span><span class="sxs-lookup"><span data-stu-id="240fb-129">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <span data-ttu-id="240fb-130"><dt>**$Index \_**</dt> <dt>0x82</dt> выделения</span><span class="sxs-lookup"><span data-stu-id="240fb-130"><dt>**$INDEX\_ALLOCATION**</dt> <dt>0xA0</dt></span></span> </dl>             | <span data-ttu-id="240fb-131">Используется для реализации выделения имен файлов для больших каталогов.</span><span class="sxs-lookup"><span data-stu-id="240fb-131">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <span data-ttu-id="240fb-132"><dt>**$Bitmap**</dt> <dt>0xB0</dt></span><span class="sxs-lookup"><span data-stu-id="240fb-132"><dt>**$BITMAP**</dt> <dt>0xB0</dt></span></span> </dl>                                            | <span data-ttu-id="240fb-133">Индекс точечного рисунка для большого каталога.</span><span class="sxs-lookup"><span data-stu-id="240fb-133">A bitmap index for a large directory.</span></span><br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <span data-ttu-id="240fb-134"><dt>**$REPARSE \_ ТОЧКА**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="240fb-134"><dt>**$REPARSE\_POINT**</dt> <dt>0xC0</dt></span></span> </dl>                      | <span data-ttu-id="240fb-135">Данные точки повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="240fb-135">The reparse point data.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="240fb-136">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="240fb-136">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="240fb-137">Размер этой структуры, а также необязательный буфер имен в байтах.</span><span class="sxs-lookup"><span data-stu-id="240fb-137">The size of this structure, plus the optional name buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="240fb-138">**аттрибутенамеленгс**</span><span class="sxs-lookup"><span data-stu-id="240fb-138">**AttributeNameLength**</span></span>
</dt> <dd>

<span data-ttu-id="240fb-139">Размер необязательного имени атрибута в символах.</span><span class="sxs-lookup"><span data-stu-id="240fb-139">The size of the optional attribute name, in characters.</span></span> <span data-ttu-id="240fb-140">Если имя существует, это значение не равно нулю, а структура сразу после строки в Юникоде указанного числа символов.</span><span class="sxs-lookup"><span data-stu-id="240fb-140">If a name exists, this value is nonzero and the structure is followed immediately by a Unicode string of the specified number of characters.</span></span>

</dd> <dt>

<span data-ttu-id="240fb-141">**аттрибутенамеоффсет**</span><span class="sxs-lookup"><span data-stu-id="240fb-141">**AttributeNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="240fb-142">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="240fb-142">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="240fb-143">**ловествкн**</span><span class="sxs-lookup"><span data-stu-id="240fb-143">**LowestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="240fb-144">Наименьший номер виртуального кластера (VCN) для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="240fb-144">The lowest virtual cluster number (VCN) for this attribute.</span></span> <span data-ttu-id="240fb-145">Этот элемент равен нулю, если атрибуту не требуется несколько сегментов записи файла и если эта запись не является ссылкой на сегмент, отличный от первого.</span><span class="sxs-lookup"><span data-stu-id="240fb-145">This member is zero unless the attribute requires multiple file record segments and unless this entry is a reference to a segment other than the first one.</span></span> <span data-ttu-id="240fb-146">В этом случае это значение является наименьшим значением VCN, описанным в упоминаемом сегменте.</span><span class="sxs-lookup"><span data-stu-id="240fb-146">In this case, this value is the lowest VCN that is described by the referenced segment.</span></span>

</dd> <dt>

<span data-ttu-id="240fb-147">**сегментреференце**</span><span class="sxs-lookup"><span data-stu-id="240fb-147">**SegmentReference**</span></span>
</dt> <dd>

<span data-ttu-id="240fb-148">Сегмент основной таблицы файлов (MFT), в котором находится атрибут.</span><span class="sxs-lookup"><span data-stu-id="240fb-148">The master file table (MFT) segment in which the attribute resides.</span></span> <span data-ttu-id="240fb-149">См [**. \_ \_ Справочник по сегментам MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="240fb-149">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="240fb-150">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="240fb-150">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="240fb-151">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="240fb-151">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="240fb-152">**AttributeName**</span><span class="sxs-lookup"><span data-stu-id="240fb-152">**AttributeName**</span></span>
</dt> <dd>

<span data-ttu-id="240fb-153">Начало необязательного имени атрибута.</span><span class="sxs-lookup"><span data-stu-id="240fb-153">The start of the optional attribute name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="240fb-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="240fb-154">Remarks</span></span>

<span data-ttu-id="240fb-155">Список Attributes представляет собой упорядоченный список структур **\_ \_ элементов списка атрибутов** с куадворд по рассогласованию.</span><span class="sxs-lookup"><span data-stu-id="240fb-155">The attributes list is an ordered list of quadword-aligned **ATTRIBUTE\_LIST\_ENTRY** structures.</span></span> <span data-ttu-id="240fb-156">Этот список сначала упорядочивается по коду типа атрибута, а затем по имени атрибута (если он есть).</span><span class="sxs-lookup"><span data-stu-id="240fb-156">This list is ordered first by the attribute type code and then by the attribute name (if present).</span></span> <span data-ttu-id="240fb-157">Ни один из двух атрибутов не может иметь одинаковый код типа, имя и наименьшее значение VCN.</span><span class="sxs-lookup"><span data-stu-id="240fb-157">No two attributes can have the same type code, name, and lowest VCN.</span></span> <span data-ttu-id="240fb-158">Таким образом, может существовать не более одного атрибута для каждого кода типа без имени.</span><span class="sxs-lookup"><span data-stu-id="240fb-158">Therefore, there can be at most one attribute for each type code without a name.</span></span>

<span data-ttu-id="240fb-159">Это определение структуры допустимо только для основной версии 3 и дополнительной версии 0 или 1, как сообщается [**фсктл \_ Получение \_ \_ \_ данных тома NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="240fb-159">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="240fb-160">Обратите внимание, что для этой структуры нет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="240fb-160">Note that there is no associated header file for this structure.</span></span>

## <a name="see-also"></a><span data-ttu-id="240fb-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="240fb-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="240fb-162">Основная таблица файлов</span><span class="sxs-lookup"><span data-stu-id="240fb-162">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
