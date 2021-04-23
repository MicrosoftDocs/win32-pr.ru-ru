---
description: В следующей таблице перечислены все значения HRESULT, которые могут возвращаться методами API документа XPS.
ms.assetid: 9e6db1e3-7151-4538-8607-b7185ebc0110
title: Ошибки документа XPS (Кспсобжектмодел. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a221858e177172a0062185cbe1bcc127ccc728fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263884"
---
# <a name="xps-document-errors"></a><span data-ttu-id="3720f-103">Ошибки документа XPS</span><span class="sxs-lookup"><span data-stu-id="3720f-103">XPS Document Errors</span></span>

<span data-ttu-id="3720f-104">В следующей таблице перечислены все значения **HRESULT** , которые могут возвращаться методами API документа XPS.</span><span class="sxs-lookup"><span data-stu-id="3720f-104">The following table lists all the **HRESULT** values that can be returned by the methods of the XPS Document API.</span></span> <span data-ttu-id="3720f-105">Обратите внимание, что не каждый метод возвращает все возвращаемые значения, перечисленные в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="3720f-105">Note that not every method returns every return value that is listed in this table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3720f-106">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="3720f-106">Return code/value</span></span></th>
<th><span data-ttu-id="3720f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3720f-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="XPS_E_ALREADY_OWNED"></span><span id="xps_e_already_owned"></span><dl> <span data-ttu-id="3720f-108"><dt><strong>XPS_E_ALREADY_OWNED</strong></dt> <dt>0x80520503</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-108"><dt><strong>XPS_E_ALREADY_OWNED</strong></dt> <dt>0x80520503</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-109">У интерфейса уже есть владелец.</span><span class="sxs-lookup"><span data-stu-id="3720f-109">The interface already has an owner.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC"></span><span id="xps_e_bleed_box_page_dimensions_not_in_sync"></span><dl> <span data-ttu-id="3720f-110"><dt><strong>XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC</strong></dt> <dt>0x80520509</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-110"><dt><strong>XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC</strong></dt> <dt>0x80520509</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-111">Размеры поля с выходом за обрез несовместимы с размерами страницы.</span><span class="sxs-lookup"><span data-stu-id="3720f-111">The bleed box dimensions are not compatible with the page dimensions.</span></span><br/> <span data-ttu-id="3720f-112">Значение ширины рамки выпусков, которое должно быть больше или равно ширине страницы, а также абсолютное значение координаты x исходного окна.</span><span class="sxs-lookup"><span data-stu-id="3720f-112">The bleed box width value must be greater than or equal to the page width plus the absolute value of the x-coordinate of the bleed box origin.</span></span> <span data-ttu-id="3720f-113">Значение высоты рамки выпуска от края должно быть больше или равно высоте страницы плюс абсолютное значение координат по оси y исходного окна.</span><span class="sxs-lookup"><span data-stu-id="3720f-113">The bleed box height value must be greater than or equal to the page height plus the absolute value of the y-coordinate of the bleed box origin.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT"></span><span id="xps_e_both_pathfigure_and_abbr_syntax_present"></span><dl> <span data-ttu-id="3720f-114"><dt><strong>XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT</strong></dt> <dt>0x80520507</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-114"><dt><strong>XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT</strong></dt> <dt>0x80520507</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-115">Элемент <strong>PathGeometry</strong> содержит набор рисунков пути, указанных либо с помощью атрибута <strong>Figures</strong> , либо с дочерним элементом <strong>PathFigure</strong> .</span><span class="sxs-lookup"><span data-stu-id="3720f-115">A <strong>PathGeometry</strong> element contains a set of path figures that are specified either with the <strong>Figures</strong> attribute or with a child <strong>PathFigure</strong> element.</span></span> <span data-ttu-id="3720f-116">Контуры геометрии не могут одновременно иметь атрибут <strong>Figures</strong> и дочерний элемент <strong>PathFigure</strong> .</span><span class="sxs-lookup"><span data-stu-id="3720f-116">The path figures of a geometry cannot have both the <strong>Figures</strong> attribute and a child <strong>PathFigure</strong> element.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT"></span><span id="xps_e_both_resource_and_sourceattr_present"></span><dl> <span data-ttu-id="3720f-117"><dt><strong>XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT</strong></dt> <dt>0x80520508</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-117"><dt><strong>XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT</strong></dt> <dt>0x80520508</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-118">Элемент <strong>ResourceDictionary</strong> , указывающий удаленный словарь ресурсов в его <strong>исходном</strong> атрибуте, не должен содержать дочерних элементов определения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3720f-118">A <strong>ResourceDictionary</strong> element that specifies a remote resource dictionary in its <strong>Source</strong> attribute MUST NOT contain any resource definition children.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_CARET_OUT_OF_ORDER"></span><span id="xps_e_caret_out_of_order"></span><dl> <span data-ttu-id="3720f-119"><dt><strong>XPS_E_CARET_OUT_OF_ORDER</strong></dt> <dt>0x80520306</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-119"><dt><strong>XPS_E_CARET_OUT_OF_ORDER</strong></dt> <dt>0x80520306</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-120">Неупорядоченное значение положения курсора.</span><span class="sxs-lookup"><span data-stu-id="3720f-120">A caret location value is out of order.</span></span> <span data-ttu-id="3720f-121">Значения расположения должны быть отсортированы в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="3720f-121">The location values must be sorted in ascending order.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_CARET_OUTSIDE_STRING"></span><span id="xps_e_caret_outside_string"></span><dl> <span data-ttu-id="3720f-122"><dt><strong>XPS_E_CARET_OUTSIDE_STRING</strong></dt> <dt>0x80520305</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-122"><dt><strong>XPS_E_CARET_OUTSIDE_STRING</strong></dt> <dt>0x80520305</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-123">Для пустой строки были указаны остановки курсора; или индекс перехода курсора превысил длину строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="3720f-123">Caret stops were specified for an empty string; or, the caret jump index has exceeded the length of the Unicode string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_COLOR_COMPONENT_OUT_OF_RANGE"></span><span id="xps_e_color_component_out_of_range"></span><dl> <span data-ttu-id="3720f-124"><dt><strong>XPS_E_COLOR_COMPONENT_OUT_OF_RANGE</strong></dt> <dt>0x80520506</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-124"><dt><strong>XPS_E_COLOR_COMPONENT_OUT_OF_RANGE</strong></dt> <dt>0x80520506</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-125">Значение цвета выходит за пределы допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="3720f-125">A color value is out of range.</span></span><br/> <span data-ttu-id="3720f-126">Для <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_SCRGB</strong></a> типов цветов значение альфа-канала должно быть больше или равно 0,0 и меньше или равно + 1,0.</span><span class="sxs-lookup"><span data-stu-id="3720f-126">For <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_SCRGB</strong></a> color types, the alpha channel value must be greater than or equal to 0.0 and less than or equal to +1.0.</span></span><br/> <span data-ttu-id="3720f-127">Для <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a> типов цветов <strong>чаннелвалуес [0]</strong> , представляющий значение альфа-канала, должно быть больше или равно 0,0 и меньше или равно + 1,0.</span><span class="sxs-lookup"><span data-stu-id="3720f-127">For <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a> color types, the <strong>channelValues[0]</strong> that represents the alpha channel value must be greater than or equal to 0.0 and less than or equal to +1.0.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_DICTIONARY_ITEM_NAMED"></span><span id="xps_e_dictionary_item_named"></span><dl> <span data-ttu-id="3720f-128"><dt><strong>XPS_E_DICTIONARY_ITEM_NAMED</strong></dt> <dt>0x80520401</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-128"><dt><strong>XPS_E_DICTIONARY_ITEM_NAMED</strong></dt> <dt>0x80520401</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-129">Визуальный элемент в словаре ресурсов имеет атрибут <strong>Name</strong> , который не может быть указан ни для каких потомков элемента <strong>ResourceDictionary</strong> .</span><span class="sxs-lookup"><span data-stu-id="3720f-129">A visual in a resource dictionary has the <strong>Name</strong> attribute, which may not be specified on any children of a <strong>ResourceDictionary</strong> element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_DUPLICATE_NAMES"></span><span id="xps_e_duplicate_names"></span><dl> <span data-ttu-id="3720f-130"><dt><strong>XPS_E_DUPLICATE_NAMES</strong></dt> <dt>0x80520209</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-130"><dt><strong>XPS_E_DUPLICATE_NAMES</strong></dt> <dt>0x80520209</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-131">Объект с таким именем уже существует в словаре.</span><span class="sxs-lookup"><span data-stu-id="3720f-131">An object with this name already exists in the dictionary.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_DUPLICATE_RESOURCE_KEYS"></span><span id="xps_e_duplicate_resource_keys"></span><dl> <span data-ttu-id="3720f-132"><dt><strong>XPS_E_DUPLICATE_RESOURCE_KEYS</strong></dt> <dt>0x80520200</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-132"><dt><strong>XPS_E_DUPLICATE_RESOURCE_KEYS</strong></dt> <dt>0x80520200</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-133">Объект с таким именем ключа уже существует в словаре.</span><span class="sxs-lookup"><span data-stu-id="3720f-133">An object with this key name already exists in the dictionary.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INDEX_OUT_OF_RANGE"></span><span id="xps_e_index_out_of_range"></span><dl> <span data-ttu-id="3720f-134"><dt><strong>XPS_E_INDEX_OUT_OF_RANGE</strong></dt> <dt>0x80520500</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-134"><dt><strong>XPS_E_INDEX_OUT_OF_RANGE</strong></dt> <dt>0x80520500</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-135">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="3720f-135">Reserved.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_BLEED_BOX"></span><span id="xps_e_invalid_bleed_box"></span><dl> <span data-ttu-id="3720f-136"><dt><strong>XPS_E_INVALID_BLEED_BOX</strong></dt> <dt>0x80520004</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-136"><dt><strong>XPS_E_INVALID_BLEED_BOX</strong></dt> <dt>0x80520004</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-137">Прямоугольник в поле выпуска за обрез содержит одно или несколько недопустимых значений.</span><span class="sxs-lookup"><span data-stu-id="3720f-137">The bleed box rectangle contains one or more values that are not valid.</span></span> <span data-ttu-id="3720f-138">Допустимые значения см. в описании параметра.</span><span class="sxs-lookup"><span data-stu-id="3720f-138">See the parameter description for the valid values.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_CONTENT_BOX"></span><span id="xps_e_invalid_content_box"></span><dl> <span data-ttu-id="3720f-139"><dt><strong>XPS_E_INVALID_CONTENT_BOX</strong></dt> <dt>0x8052000b</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-139"><dt><strong>XPS_E_INVALID_CONTENT_BOX</strong></dt> <dt>0x8052000b</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-140">Прямоугольник поля содержимого содержит одно или несколько недопустимых значений.</span><span class="sxs-lookup"><span data-stu-id="3720f-140">The content box rectangle contains one or more values that are not valid.</span></span> <span data-ttu-id="3720f-141">Допустимые значения см. в описании параметра.</span><span class="sxs-lookup"><span data-stu-id="3720f-141">See the parameter description for the valid values.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_CONTENT_TYPE"></span><span id="xps_e_invalid_content_type"></span><dl> <span data-ttu-id="3720f-142"><dt><strong>XPS_E_INVALID_CONTENT_TYPE</strong></dt> <dt>0x8052000e</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-142"><dt><strong>XPS_E_INVALID_CONTENT_TYPE</strong></dt> <dt>0x8052000e</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-143">Недопустимая строка типа содержимого.</span><span class="sxs-lookup"><span data-stu-id="3720f-143">The content type string is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_FLOAT"></span><span id="xps_e_invalid_float"></span><dl> <span data-ttu-id="3720f-144"><dt><strong>XPS_E_INVALID_FLOAT</strong></dt> <dt>0x80520007</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-144"><dt><strong>XPS_E_INVALID_FLOAT</strong></dt> <dt>0x80520007</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-145">Недопустимое значение <strong>float</strong> .</span><span class="sxs-lookup"><span data-stu-id="3720f-145">A <strong>FLOAT</strong> value is not valid.</span></span> <span data-ttu-id="3720f-146">Это либо бесконечное, либо нечисловое значение (NAN).</span><span class="sxs-lookup"><span data-stu-id="3720f-146">It is either an infinite or not a number (NAN).</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_FONT_URI"></span><span id="xps_e_invalid_font_uri"></span><dl> <span data-ttu-id="3720f-147"><dt><strong>XPS_E_INVALID_FONT_URI</strong></dt> <dt>0x8052000a</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-147"><dt><strong>XPS_E_INVALID_FONT_URI</strong></dt> <dt>0x8052000a</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-148">Недопустимый URI шрифта, возможно, из-за того, что он содержит пустой фрагмент или символы, которые являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="3720f-148">The font URI is not valid, possibly because it contains an empty fragment or characters that are not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_LANGUAGE"></span><span id="xps_e_invalid_language"></span><dl> <span data-ttu-id="3720f-149"><dt><strong>XPS_E_INVALID_LANGUAGE</strong></dt> <dt>0x80520000</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-149"><dt><strong>XPS_E_INVALID_LANGUAGE</strong></dt> <dt>0x80520000</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-150">Указанный язык недопустим или имеет неправильный формат.</span><span class="sxs-lookup"><span data-stu-id="3720f-150">The specified language is either not valid or not correctly formatted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_LOOKUP_TYPE"></span><span id="xps_e_invalid_lookup_type"></span><dl> <span data-ttu-id="3720f-151"><dt><strong>XPS_E_INVALID_LOOKUP_TYPE</strong></dt> <dt>0x80520006</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-151"><dt><strong>XPS_E_INVALID_LOOKUP_TYPE</strong></dt> <dt>0x80520006</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-152">Имя ключа поиска ссылается на объект, который не является правильным типом для вызова; Например, если метод возвращает кисть, но имя ключа уточняющего запроса ссылается на объект Geometry.</span><span class="sxs-lookup"><span data-stu-id="3720f-152">The lookup key name references an object that is not the correct type for the call; for example, if the method returns a brush but the lookup key name refers to a geometry object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_MARKUP"></span><span id="xps_e_invalid_markup"></span><dl> <span data-ttu-id="3720f-153"><dt><strong>XPS_E_INVALID_MARKUP</strong></dt> <dt>0x8052000c</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-153"><dt><strong>XPS_E_INVALID_MARKUP</strong></dt> <dt>0x8052000c</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-154">Разметка для чтения содержит элемент или атрибут, который не соответствует <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">спецификации формата XML</a>.</span><span class="sxs-lookup"><span data-stu-id="3720f-154">The markup being read contains an element or an attribute that does not conform to the <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3720f-155">Для представления значений с плавающей запятой модель XPS использует тип данных <strong>float</strong> вместо <strong>Double</strong>.</span><span class="sxs-lookup"><span data-stu-id="3720f-155">To represent floating-point values, the XPS OM uses the <strong>FLOAT</strong> data type instead of <strong>DOUBLE</strong>.</span></span> <span data-ttu-id="3720f-156">Если документ XPS содержит элемент с данными с плавающей запятой, не попадающие в значение <strong>float</strong> , эта ошибка будет возвращена при обнаружении этого значения во время десериализации.</span><span class="sxs-lookup"><span data-stu-id="3720f-156">If an XPS document has an element with floating-point data that does not fit into a <strong>FLOAT</strong> value, this error will be returned when that value is encountered during deserialization.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_NAME"></span><span id="xps_e_invalid_name"></span><dl> <span data-ttu-id="3720f-157"><dt><strong>XPS_E_INVALID_NAME</strong></dt> <dt>0x80520001</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-157"><dt><strong>XPS_E_INVALID_NAME</strong></dt> <dt>0x80520001</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-158">Переданная строка не является допустимым именем в соответствии со спецификацией XML Paper.</span><span class="sxs-lookup"><span data-stu-id="3720f-158">The string that was passed is not a valid name, according to the XML Paper Specification.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_OBFUSCATED_FONT_URI"></span><span id="xps_e_invalid_obfuscated_font_uri"></span><dl> <span data-ttu-id="3720f-159"><dt><strong>XPS_E_INVALID_OBFUSCATED_FONT_URI</strong></dt> <dt>0x8052000f</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-159"><dt><strong>XPS_E_INVALID_OBFUSCATED_FONT_URI</strong></dt> <dt>0x8052000f</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-160">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="3720f-160">Reserved.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_PAGE_SIZE"></span><span id="xps_e_invalid_page_size"></span><dl> <span data-ttu-id="3720f-161"><dt><strong>XPS_E_INVALID_PAGE_SIZE</strong></dt> <dt>0x80520003</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-161"><dt><strong>XPS_E_INVALID_PAGE_SIZE</strong></dt> <dt>0x80520003</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-162">Размеры страницы содержат недопустимое значение размера страницы.</span><span class="sxs-lookup"><span data-stu-id="3720f-162">The page dimensions contain a page size value that is not valid.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_RESOURCE_KEY"></span><span id="xps_e_invalid_resource_key"></span><dl> <span data-ttu-id="3720f-163"><dt><strong>XPS_E_INVALID_RESOURCE_KEY</strong></dt> <dt>0x80520002</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-163"><dt><strong>XPS_E_INVALID_RESOURCE_KEY</strong></dt> <dt>0x80520002</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-164">В соответствии со <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">спецификацией XML Paper</a>строка ключа поиска недопустима.</span><span class="sxs-lookup"><span data-stu-id="3720f-164">According to the <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>, the lookup key string is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE"></span><span id="xps_e_invalid_thumbnail_image_type"></span><dl> <span data-ttu-id="3720f-165"><dt><strong>XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE</strong></dt> <dt>0x80520005</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-165"><dt><strong>XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE</strong></dt> <dt>0x80520005</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-166">Тип изображения эскиза не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3720f-166">The thumbnail image type is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_XML_ENCODING"></span><span id="xps_e_invalid_xml_encoding"></span><dl> <span data-ttu-id="3720f-167"><dt><strong>XPS_E_INVALID_XML_ENCODING</strong></dt> <dt>0x8052000d</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-167"><dt><strong>XPS_E_INVALID_XML_ENCODING</strong></dt> <dt>0x8052000d</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-168">Обнаружена неправильная или неправильно отформатированная XML-разметка.</span><span class="sxs-lookup"><span data-stu-id="3720f-168">Found improper or incorrectly formatted XML markup.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MAPPING_OUT_OF_ORDER"></span><span id="xps_e_mapping_out_of_order"></span><dl> <span data-ttu-id="3720f-169"><dt><strong>XPS_E_MAPPING_OUT_OF_ORDER</strong></dt> <dt>0x80520302</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-169"><dt><strong>XPS_E_MAPPING_OUT_OF_ORDER</strong></dt> <dt>0x80520302</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-170">В одной или нескольких структурах <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping"><strong>XPS_GLYPH_MAPPING</strong></a> элемент находится вне последовательности.</span><span class="sxs-lookup"><span data-stu-id="3720f-170">In one or more <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping"><strong>XPS_GLYPH_MAPPING</strong></a> structures, an element is out of sequence.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MAPPING_OUTSIDE_INDICES"></span><span id="xps_e_mapping_outside_indices"></span><dl> <span data-ttu-id="3720f-171"><dt><strong>XPS_E_MAPPING_OUTSIDE_INDICES</strong></dt> <dt>0x80520304</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-171"><dt><strong>XPS_E_MAPPING_OUTSIDE_INDICES</strong></dt> <dt>0x80520304</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-172">Сопоставления глифов превышают число индексов глифов.</span><span class="sxs-lookup"><span data-stu-id="3720f-172">The glyph mappings exceed the number of glyph indices.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MAPPING_OUTSIDE_STRING"></span><span id="xps_e_mapping_outside_string"></span><dl> <span data-ttu-id="3720f-173"><dt><strong>XPS_E_MAPPING_OUTSIDE_STRING</strong></dt> <dt>0x80520303</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-173"><dt><strong>XPS_E_MAPPING_OUTSIDE_STRING</strong></dt> <dt>0x80520303</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-174">Ошибка в сопоставлении глифов.</span><span class="sxs-lookup"><span data-stu-id="3720f-174">Error in the glyph mappings.</span></span><br/> <span data-ttu-id="3720f-175">Если строка Юникода пуста, эта ошибка означает, что также было определено сопоставление глифов.</span><span class="sxs-lookup"><span data-stu-id="3720f-175">If the Unicode string is empty, this error means that a glyph mapping was also defined.</span></span> <span data-ttu-id="3720f-176">Сопоставления глифов не должны быть определены, если строка Юникода пуста.</span><span class="sxs-lookup"><span data-stu-id="3720f-176">Glyph mappings must not be defined if the Unicode string is empty.</span></span><br/> <span data-ttu-id="3720f-177">Если строка Юникода не пуста, эта ошибка означает, что для глифов за пределами строки Юникода было определено сопоставление глифов.</span><span class="sxs-lookup"><span data-stu-id="3720f-177">If the Unicode string is not empty, this error means that a glyph mapping was defined for glyphs outside of the Unicode string.</span></span> <span data-ttu-id="3720f-178">Сопоставления глифов не могут быть определены для глифов, которые выходят за пределы длины строки Юникода.</span><span class="sxs-lookup"><span data-stu-id="3720f-178">Glyph mappings cannot be defined for glyphs that fall outside the length of the Unicode string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_COLORPROFILE"></span><span id="xps_e_missing_colorprofile"></span><dl> <span data-ttu-id="3720f-179"><dt><strong>XPS_E_MISSING_COLORPROFILE</strong></dt> <dt>0x80520104</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-179"><dt><strong>XPS_E_MISSING_COLORPROFILE</strong></dt> <dt>0x80520104</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-180">Параметр цветового профиля имеет <strong>значение NULL</strong>, но ожидается цветовой профиль.</span><span class="sxs-lookup"><span data-stu-id="3720f-180">The color profile parameter is <strong>NULL</strong>, but a color profile is expected.</span></span> <span data-ttu-id="3720f-181">Если тип цвета — XPS_COLOR_TYPE_CONTEXT, требуется цветовой профиль.</span><span class="sxs-lookup"><span data-stu-id="3720f-181">A color profile is required when the color type is XPS_COLOR_TYPE_CONTEXT.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_DISCARDCONTROL"></span><span id="xps_e_missing_discardcontrol"></span><dl> <span data-ttu-id="3720f-182"><dt><strong>XPS_E_MISSING_DISCARDCONTROL</strong></dt> <dt>0x80520112</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-182"><dt><strong>XPS_E_MISSING_DISCARDCONTROL</strong></dt> <dt>0x80520112</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-183">Страница ссылается на отклоненные ресурсы, но не указывает имя части Дискардконтрол.</span><span class="sxs-lookup"><span data-stu-id="3720f-183">A page refers to discardable resources but does not specify a DiscardControl part name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_DOCUMENT"></span><span id="xps_e_missing_document"></span><dl> <span data-ttu-id="3720f-184"><dt><strong>XPS_E_MISSING_DOCUMENT</strong></dt> <dt>0x80520109</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-184"><dt><strong>XPS_E_MISSING_DOCUMENT</strong></dt> <dt>0x80520109</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-185"><a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage"><strong>Икспсомпаккажевритер:: addPage</strong></a> вызывался до <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>Икспсомпаккажевритер:: стартневдокумент</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3720f-185"><a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage"><strong>IXpsOMPackageWriter::AddPage</strong></a> was called before <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter::StartNewDocument</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP"></span><span id="xps_e_missing_documentsequence_relationship"></span><dl> <span data-ttu-id="3720f-186"><dt><strong>XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP</strong></dt> <dt>0x80520108</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-186"><dt><strong>XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP</strong></dt> <dt>0x80520108</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-187">Пакет не содержит FixedDocumentSequence.</span><span class="sxs-lookup"><span data-stu-id="3720f-187">The package does not contain a FixedDocumentSequence.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_FONTURI"></span><span id="xps_e_missing_fonturi"></span><dl> <span data-ttu-id="3720f-188"><dt><strong>XPS_E_MISSING_FONTURI</strong></dt> <dt>0x80520107</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-188"><dt><strong>XPS_E_MISSING_FONTURI</strong></dt> <dt>0x80520107</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-189">Интерфейсу <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>икспсомглифс</strong></a> требуется URI шрифта, но он не указан.</span><span class="sxs-lookup"><span data-stu-id="3720f-189">The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> interface requires a font URI, but one is not specified.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_GLYPHS"></span><span id="xps_e_missing_glyphs"></span><dl> <span data-ttu-id="3720f-190"><dt><strong>XPS_E_MISSING_GLYPHS</strong></dt> <dt>0x80520102</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-190"><dt><strong>XPS_E_MISSING_GLYPHS</strong></dt> <dt>0x80520102</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-191">Интерфейс <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>икспсомглифс</strong></a> без строки Юникода не указывает индексы глифов.</span><span class="sxs-lookup"><span data-stu-id="3720f-191">The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> interface without a Unicode string does not specify any glyph indices.</span></span> <span data-ttu-id="3720f-192">Интерфейс <strong>икспсомглифс</strong> должен указывать либо строку в Юникоде, либо массив индексов глифов.</span><span class="sxs-lookup"><span data-stu-id="3720f-192">An <strong>IXpsOMGlyphs</strong> interface must specify either a Unicode string or an array of glyph indices.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH"></span><span id="xps_e_missing_image_in_imagebrush"></span><dl> <span data-ttu-id="3720f-193"><dt><strong>XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH</strong></dt> <dt>0x8052010e</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-193"><dt><strong>XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH</strong></dt> <dt>0x8052010e</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-194">Не удалось найти ресурс изображения для кисти изображения.</span><span class="sxs-lookup"><span data-stu-id="3720f-194">An image resource could not be located for the image brush.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_LOOKUP"></span><span id="xps_e_missing_lookup"></span><dl> <span data-ttu-id="3720f-195"><dt><strong>XPS_E_MISSING_LOOKUP</strong></dt> <dt>0x80520101</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-195"><dt><strong>XPS_E_MISSING_LOOKUP</strong></dt> <dt>0x80520101</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-196">Удаленный ресурс имеет непредвиденный объект.</span><span class="sxs-lookup"><span data-stu-id="3720f-196">The remote resource has an unexpected object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_NAME"></span><span id="xps_e_missing_name"></span><dl> <span data-ttu-id="3720f-197"><dt><strong>XPS_E_MISSING_NAME</strong></dt> <dt>0x80520100</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-197"><dt><strong>XPS_E_MISSING_NAME</strong></dt> <dt>0x80520100</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-198">Страница не имеет имени; Состояние целевого объекта гиперссылки может быть задано только в том случае, если у страницы есть имя.</span><span class="sxs-lookup"><span data-stu-id="3720f-198">The page has not been named; the hyperlink target status can only be set if the page has a name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_PAGE_IN_DOCUMENT"></span><span id="xps_e_missing_page_in_document"></span><dl> <span data-ttu-id="3720f-199"><dt><strong>XPS_E_MISSING_PAGE_IN_DOCUMENT</strong></dt> <dt>0x8052010c</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-199"><dt><strong>XPS_E_MISSING_PAGE_IN_DOCUMENT</strong></dt> <dt>0x8052010c</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-200">FixedDocument не содержит ни одной части FixedPage.</span><span class="sxs-lookup"><span data-stu-id="3720f-200">The FixedDocument does not contain any FixedPage parts.</span></span> <span data-ttu-id="3720f-201">Документ XPS должен содержать по крайней мере один элемент FixedPage.</span><span class="sxs-lookup"><span data-stu-id="3720f-201">An XPS document must contain at least one FixedPage part.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_PAGE_IN_PAGEREFERENCE"></span><span id="xps_e_missing_page_in_pagereference"></span><dl> <span data-ttu-id="3720f-202"><dt><strong>XPS_E_MISSING_PAGE_IN_PAGEREFERENCE</strong></dt> <dt>0x8052010d</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-202"><dt><strong>XPS_E_MISSING_PAGE_IN_PAGEREFERENCE</strong></dt> <dt>0x8052010d</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-203">Ссылка на страницу не имеет соответствующей страницы.</span><span class="sxs-lookup"><span data-stu-id="3720f-203">The page reference does not have a corresponding page.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_PART_REFERENCE"></span><span id="xps_e_missing_part_reference"></span><dl> <span data-ttu-id="3720f-204"><dt><strong>XPS_E_MISSING_PART_REFERENCE</strong></dt> <dt>0x80520110</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-204"><dt><strong>XPS_E_MISSING_PART_REFERENCE</strong></dt> <dt>0x80520110</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-205">Не указана ссылка на обязательный целевой элемент.</span><span class="sxs-lookup"><span data-stu-id="3720f-205">A required target part was not referenced.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_PART_STREAM"></span><span id="xps_e_missing_part_stream"></span><dl> <span data-ttu-id="3720f-206"><dt><strong>XPS_E_MISSING_PART_STREAM</strong></dt> <dt>0x80520113</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-206"><dt><strong>XPS_E_MISSING_PART_STREAM</strong></dt> <dt>0x80520113</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-207">Для ресурса не был указан поток.</span><span class="sxs-lookup"><span data-stu-id="3720f-207">A stream was not specified for the resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_REFERRED_DOCUMENT"></span><span id="xps_e_missing_referred_document"></span><dl> <span data-ttu-id="3720f-208"><dt><strong>XPS_E_MISSING_REFERRED_DOCUMENT</strong></dt> <dt>0x8052010a</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-208"><dt><strong>XPS_E_MISSING_REFERRED_DOCUMENT</strong></dt> <dt>0x8052010a</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-209">Не удалось найти часть FixedDocument, на которую ссылается FixedDocumentSequence.</span><span class="sxs-lookup"><span data-stu-id="3720f-209">The FixedDocument part that is referenced by the FixedDocumentSequence could not be found.</span></span> <span data-ttu-id="3720f-210">Документ XPS должен содержать по крайней мере один FixedDocument.</span><span class="sxs-lookup"><span data-stu-id="3720f-210">An XPS document must contain at least one FixedDocument.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_REFERRED_PAGE"></span><span id="xps_e_missing_referred_page"></span><dl> <span data-ttu-id="3720f-211"><dt><strong>XPS_E_MISSING_REFERRED_PAGE</strong></dt> <dt>0x8052010b</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-211"><dt><strong>XPS_E_MISSING_REFERRED_PAGE</strong></dt> <dt>0x8052010b</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-212">Не удалось найти часть FixedPage, на которую ссылается FixedDocument.</span><span class="sxs-lookup"><span data-stu-id="3720f-212">The FixedPage part that is referenced by the FixedDocument could not be found.</span></span> <span data-ttu-id="3720f-213">Документ XPS должен содержать по крайней мере один элемент FixedPage.</span><span class="sxs-lookup"><span data-stu-id="3720f-213">An XPS document must contain at least one FixedPage part.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_RELATIONSHIP_TARGET"></span><span id="xps_e_missing_relationship_target"></span><dl> <span data-ttu-id="3720f-214"><dt><strong>XPS_E_MISSING_RELATIONSHIP_TARGET</strong></dt> <dt>0x80520105</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-214"><dt><strong>XPS_E_MISSING_RELATIONSHIP_TARGET</strong></dt> <dt>0x80520105</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-215">Часть целевого объекта связи отсутствует в связи пакета.</span><span class="sxs-lookup"><span data-stu-id="3720f-215">The relationship target part is not present in the package relationship.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_RESOURCE_KEY"></span><span id="xps_e_missing_resource_key"></span><dl> <span data-ttu-id="3720f-216"><dt><strong>XPS_E_MISSING_RESOURCE_KEY</strong></dt> <dt>0x8052010f</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-216"><dt><strong>XPS_E_MISSING_RESOURCE_KEY</strong></dt> <dt>0x8052010f</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-217">Для ресурса не указан атрибут <strong>x:Key</strong> .</span><span class="sxs-lookup"><span data-stu-id="3720f-217">No <strong>x:Key</strong> attribute was specified for the resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_RESOURCE_RELATIONSHIP"></span><span id="xps_e_missing_resource_relationship"></span><dl> <span data-ttu-id="3720f-218"><dt><strong>XPS_E_MISSING_RESOURCE_RELATIONSHIP</strong></dt> <dt>0x80520106</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-218"><dt><strong>XPS_E_MISSING_RESOURCE_RELATIONSHIP</strong></dt> <dt>0x80520106</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-219">Ресурс, на который ссылается страница или удаленное содержимое словаря, не существует как связь между страницами.</span><span class="sxs-lookup"><span data-stu-id="3720f-219">The resource referred to by the page or remote dictionary content does not exist as a page relationship.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP"></span><span id="xps_e_missing_restricted_font_relationship"></span><dl> <span data-ttu-id="3720f-220"><dt><strong>XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520111</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-220"><dt><strong>XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520111</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-221">Указанный в ссылке шрифт с ограничением не был указан в вызове <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>икспсомпаккажевритер:: стартневдокумент</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3720f-221">The referenced restricted font was not specified in the call to <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter::StartNewDocument</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_SEGMENT_DATA"></span><span id="xps_e_missing_segment_data"></span><dl> <span data-ttu-id="3720f-222"><dt><strong>XPS_E_MISSING_SEGMENT_DATA</strong></dt> <dt>0x80520103</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-222"><dt><strong>XPS_E_MISSING_SEGMENT_DATA</strong></dt> <dt>0x80520103</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-223">Массив данных сегмента содержит меньше записей, чем массив типов сегментов.</span><span class="sxs-lookup"><span data-stu-id="3720f-223">The segment data array has fewer entries than the segment types array.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS"></span><span id="xps_e_multiple_documentsequence_relationships"></span><dl> <span data-ttu-id="3720f-224"><dt><strong>XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS</strong></dt> <dt>0x80520202</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-224"><dt><strong>XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS</strong></dt> <dt>0x80520202</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-225">Предпринята попытка добавить FixedDocumentSequence в пакет, который уже содержит его.</span><span class="sxs-lookup"><span data-stu-id="3720f-225">An attempt was made to add a FixedDocumentSequence to a package that already has one.</span></span> <span data-ttu-id="3720f-226">Документ XPS должен содержать одну и только одну часть FixedDocumentSequence.</span><span class="sxs-lookup"><span data-stu-id="3720f-226">An XPS document must contain one and only one FixedDocumentSequence part.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT"></span><span id="xps_e_multiple_printtickets_on_document"></span><dl> <span data-ttu-id="3720f-227"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT</strong></dt> <dt>0x80520206</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-227"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT</strong></dt> <dt>0x80520206</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-228">Предпринята попытка добавить билет печати на уровне документа в FixedDocument, у которого уже есть такой запрос.</span><span class="sxs-lookup"><span data-stu-id="3720f-228">An attempt was made to add a document-level print ticket to a FixedDocument that already has one.</span></span> <span data-ttu-id="3720f-229">FixedDocument в документе XPS может содержать только один билет печати на уровне документа.</span><span class="sxs-lookup"><span data-stu-id="3720f-229">A FixedDocument in an XPS document can contain only one document-level print ticket.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE"></span><span id="xps_e_multiple_printtickets_on_documentsequence"></span><dl> <span data-ttu-id="3720f-230"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE</strong></dt> <dt>0x80520207</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-230"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE</strong></dt> <dt>0x80520207</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-231">Предпринята попытка добавить билет печати на уровне задания в FixedDocumentSequence, у которого уже есть.</span><span class="sxs-lookup"><span data-stu-id="3720f-231">An attempt was made to add a job-level print ticket to a FixedDocumentSequence that already has one.</span></span> <span data-ttu-id="3720f-232">FixedDocumentSequence в документе XPS может содержать только один билет на печать на уровне задания.</span><span class="sxs-lookup"><span data-stu-id="3720f-232">The FixedDocumentSequence in an XPS document can contain only one job-level print ticket.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE"></span><span id="xps_e_multiple_printtickets_on_page"></span><dl> <span data-ttu-id="3720f-233"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE</strong></dt> <dt>0x80520205</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-233"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE</strong></dt> <dt>0x80520205</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-234">Предпринята попытка добавить билет печати на уровне страницы в FixedPage, которая уже содержит такой запрос.</span><span class="sxs-lookup"><span data-stu-id="3720f-234">An attempt was made to add a page-level print ticket to a FixedPage that already has one.</span></span> <span data-ttu-id="3720f-235">Элемент FixedPage в документе XPS может содержать только один билет на печать на уровне страницы.</span><span class="sxs-lookup"><span data-stu-id="3720f-235">A FixedPage in an XPS document can contain only one page-level print ticket.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_REFERENCES_TO_PART"></span><span id="xps_e_multiple_references_to_part"></span><dl> <span data-ttu-id="3720f-236"><dt><strong>XPS_E_MULTIPLE_REFERENCES_TO_PART</strong></dt> <dt>0x80520208</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-236"><dt><strong>XPS_E_MULTIPLE_REFERENCES_TO_PART</strong></dt> <dt>0x80520208</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-237">Коллекция ограниченных шрифтов содержит запись ограниченного шрифта, которая была повторена.</span><span class="sxs-lookup"><span data-stu-id="3720f-237">The restricted font collection contained a restricted font entry that was repeated.</span></span> <span data-ttu-id="3720f-238">Каждая запись шрифта может находиться в коллекции только один раз.</span><span class="sxs-lookup"><span data-stu-id="3720f-238">Each font entry can occur in the collection only once.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_RESOURCES"></span><span id="xps_e_multiple_resources"></span><dl> <span data-ttu-id="3720f-239"><dt><strong>XPS_E_MULTIPLE_RESOURCES</strong></dt> <dt>0x80520201</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-239"><dt><strong>XPS_E_MULTIPLE_RESOURCES</strong></dt> <dt>0x80520201</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-240">Ресурс с таким именем части уже существует.</span><span class="sxs-lookup"><span data-stu-id="3720f-240">A resource by that part name already exists.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE"></span><span id="xps_e_multiple_thumbnails_on_package"></span><dl> <span data-ttu-id="3720f-241"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE</strong></dt> <dt>0x80520204</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-241"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE</strong></dt> <dt>0x80520204</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-242">Предпринята попытка добавить эскиз в пакет, который уже содержит изображение.</span><span class="sxs-lookup"><span data-stu-id="3720f-242">An attempt was made to add a thumbnail image to a package that already has one.</span></span> <span data-ttu-id="3720f-243">Документ XPS может содержать только одно изображение в виде эскиза на уровне пакета.</span><span class="sxs-lookup"><span data-stu-id="3720f-243">An XPS document can contain only one package-level thumbnail image.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE"></span><span id="xps_e_multiple_thumbnails_on_page"></span><dl> <span data-ttu-id="3720f-244"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE</strong></dt> <dt>0x80520203</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-244"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE</strong></dt> <dt>0x80520203</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-245">Предпринята попытка добавить изображение эскиза на уровне страницы в FixedPage, у которой уже есть эскиз.</span><span class="sxs-lookup"><span data-stu-id="3720f-245">An attempt was made to add a page-level thumbnail image to a FixedPage that already has one.</span></span> <span data-ttu-id="3720f-246">Элемент FixedPage в документе XPS может содержать только одно изображение на уровне страницы.</span><span class="sxs-lookup"><span data-stu-id="3720f-246">A FixedPage in an XPS document can contain only one page-level thumbnail image.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_NEGATIVE_FLOAT"></span><span id="xps_e_negative_float"></span><dl> <span data-ttu-id="3720f-247"><dt><strong>XPS_E_NEGATIVE_FLOAT</strong></dt> <dt>0x8052030a</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-247"><dt><strong>XPS_E_NEGATIVE_FLOAT</strong></dt> <dt>0x8052030a</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-248">Запись содержит отрицательное значение, но не должна содержать отрицательное значение.</span><span class="sxs-lookup"><span data-stu-id="3720f-248">An entry contains a negative value, but it must contain a non-negative value.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_NESTED_REMOTE_DICTIONARY"></span><span id="xps_e_nested_remote_dictionary"></span><dl> <span data-ttu-id="3720f-249"><dt><strong>XPS_E_NESTED_REMOTE_DICTIONARY</strong></dt> <dt>0x80520402</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-249"><dt><strong>XPS_E_NESTED_REMOTE_DICTIONARY</strong></dt> <dt>0x80520402</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-250">Предпринята попытка добавить ссылку на удаленный словарь в удаленный словарь.</span><span class="sxs-lookup"><span data-stu-id="3720f-250">An attempt was made to add a remote dictionary reference to a remote dictionary.</span></span> <span data-ttu-id="3720f-251">Удаленный словарь не может ссылаться на другой удаленный словарь.</span><span class="sxs-lookup"><span data-stu-id="3720f-251">A remote dictionary cannot reference another remote dictionary.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_NO_CUSTOM_OBJECTS"></span><span id="xps_e_no_custom_objects"></span><dl> <span data-ttu-id="3720f-252"><dt><strong>XPS_E_NO_CUSTOM_OBJECTS</strong></dt> <dt>0x80520502</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-252"><dt><strong>XPS_E_NO_CUSTOM_OBJECTS</strong></dt> <dt>0x80520502</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-253">Указатель интерфейса не указывает на распознанную реализацию интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3720f-253">An interface pointer does not point to a recognized interface implementation.</span></span> <span data-ttu-id="3720f-254">Пользовательская реализация интерфейсов API документов XPS не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3720f-254">Custom implementation of XPS Document API interfaces is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_NOT_ENOUGH_GRADIENT_STOPS"></span><span id="xps_e_not_enough_gradient_stops"></span><dl> <span data-ttu-id="3720f-255"><dt><strong>XPS_E_NOT_ENOUGH_GRADIENT_STOPS</strong></dt> <dt>0x8052050b</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-255"><dt><strong>XPS_E_NOT_ENOUGH_GRADIENT_STOPS</strong></dt> <dt>0x8052050b</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-256">Коллекция ограничителей градиента имеет менее двух остановок.</span><span class="sxs-lookup"><span data-stu-id="3720f-256">The gradient stop collection has fewer than two stops.</span></span> <span data-ttu-id="3720f-257">Коллекция ограничителей градиента должна иметь по крайней мере две остановки градиента.</span><span class="sxs-lookup"><span data-stu-id="3720f-257">A gradient stop collection must have at least two gradient stops.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_ODD_BIDILEVEL"></span><span id="xps_e_odd_bidilevel"></span><dl> <span data-ttu-id="3720f-258"><dt><strong>XPS_E_ODD_BIDILEVEL</strong></dt> <dt>0x80520307</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-258"><dt><strong>XPS_E_ODD_BIDILEVEL</strong></dt> <dt>0x80520307</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-259">Текстовая строка была указана как ориентированная на сторону и справа налево.</span><span class="sxs-lookup"><span data-stu-id="3720f-259">The text string was specified as being oriented sideways and right-to-left.</span></span> <span data-ttu-id="3720f-260">Если текст ориентирован на уровни, он не может иметь нечетное значение (справа налево).</span><span class="sxs-lookup"><span data-stu-id="3720f-260">If the text is oriented sideways, it cannot have a bidi level that is an odd value (right-to-left).</span></span> <span data-ttu-id="3720f-261">Аналогично, если уровень bidi имеет нечетное значение, текст не может быть ориентирован в сторону.</span><span class="sxs-lookup"><span data-stu-id="3720f-261">Likewise, if the bidi level is an odd value, the text cannot be oriented sideways.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_ONE_TO_ONE_MAPPING_EXPECTED"></span><span id="xps_e_one_to_one_mapping_expected"></span><dl> <span data-ttu-id="3720f-262"><dt><strong>XPS_E_ONE_TO_ONE_MAPPING_EXPECTED</strong></dt> <dt>0x80520308</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-262"><dt><strong>XPS_E_ONE_TO_ONE_MAPPING_EXPECTED</strong></dt> <dt>0x80520308</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-263">Сопоставления глифов не соответствуют содержимому строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="3720f-263">The glyph mappings do not match the Unicode string contents.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_PACKAGE_WRITER_NOT_CLOSED"></span><span id="xps_e_package_writer_not_closed"></span><dl> <span data-ttu-id="3720f-264"><dt><strong>XPS_E_PACKAGE_WRITER_NOT_CLOSED</strong></dt> <dt>0x8052050c</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-264"><dt><strong>XPS_E_PACKAGE_WRITER_NOT_CLOSED</strong></dt> <dt>0x8052050c</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-265">Модуль записи пакета не был закрыт до его освобождения.</span><span class="sxs-lookup"><span data-stu-id="3720f-265">The package writer was not closed before it was released.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_RELATIONSHIP_EXTERNAL"></span><span id="xps_e_relationship_external"></span><dl> <span data-ttu-id="3720f-266"><dt><strong>XPS_E_RELATIONSHIP_EXTERNAL</strong></dt> <dt>0x8052050a</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-266"><dt><strong>XPS_E_RELATIONSHIP_EXTERNAL</strong></dt> <dt>0x8052050a</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-267">Связь относится к части, которая находится за пределами документа XPS.</span><span class="sxs-lookup"><span data-stu-id="3720f-267">A relationship refers to a part that is outside of the XPS document.</span></span> <span data-ttu-id="3720f-268">Все содержимое, отображаемое в документе XPS, должно содержаться в документе XPS.</span><span class="sxs-lookup"><span data-stu-id="3720f-268">All content to be rendered in an XPS document must be contained in the XPS document.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_RESOURCE_NOT_OWNED"></span><span id="xps_e_resource_not_owned"></span><dl> <span data-ttu-id="3720f-269"><dt><strong>XPS_E_RESOURCE_NOT_OWNED</strong></dt> <dt>0x80520504</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-269"><dt><strong>XPS_E_RESOURCE_NOT_OWNED</strong></dt> <dt>0x80520504</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-270">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="3720f-270">Reserved.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED"></span><span id="xps_e_restricted_font_not_obfuscated"></span><dl> <span data-ttu-id="3720f-271"><dt><strong>XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED</strong></dt> <dt>0x80520309</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-271"><dt><strong>XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED</strong></dt> <dt>0x80520309</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-272"><em>Зарезервировано</em>.</span><span class="sxs-lookup"><span data-stu-id="3720f-272"><em>Reserved</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_STRING_TOO_LONG"></span><span id="xps_e_string_too_long"></span><dl> <span data-ttu-id="3720f-273"><dt><strong>XPS_E_STRING_TOO_LONG</strong></dt> <dt>0x80520300</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-273"><dt><strong>XPS_E_STRING_TOO_LONG</strong></dt> <dt>0x80520300</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-274">При попытке скопировать строку в новый буфер произошло переполнение <strong>size_t</strong> .</span><span class="sxs-lookup"><span data-stu-id="3720f-274">A <strong>size_t</strong> overflow occurred during an attempt to copy a string into a new buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_TOO_MANY_INDICES"></span><span id="xps_e_too_many_indices"></span><dl> <span data-ttu-id="3720f-275"><dt><strong>XPS_E_TOO_MANY_INDICES</strong></dt> <dt>0x80520301</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-275"><dt><strong>XPS_E_TOO_MANY_INDICES</strong></dt> <dt>0x80520301</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-276">Количество индексов глифов больше, чем кодовые точки Юникода.</span><span class="sxs-lookup"><span data-stu-id="3720f-276">There were more glyph indices than Unicode code points.</span></span> <span data-ttu-id="3720f-277">Если сопоставления глифов отсутствуют, число индексов глифов должно быть меньше или равно числу кодовых позиций Юникода.</span><span class="sxs-lookup"><span data-stu-id="3720f-277">If there are no glyph mappings, the number of glyph indices must be less than or equal to the number of Unicode code points.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNAVAILABLE_PACKAGE"></span><span id="xps_e_unavailable_package"></span><dl> <span data-ttu-id="3720f-278"><dt><strong>XPS_E_UNAVAILABLE_PACKAGE</strong></dt> <dt>0x80520114</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-278"><dt><strong>XPS_E_UNAVAILABLE_PACKAGE</strong></dt> <dt>0x80520114</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-279">Произошла серьезная ошибка, и содержимое объектной модели XPS может быть невосстанавливаемым.</span><span class="sxs-lookup"><span data-stu-id="3720f-279">A severe error occurred and the contents of the XPS OM might be unrecoverable.</span></span> <span data-ttu-id="3720f-280">Некоторые компоненты объектной модели XPS по-прежнему можно использовать, но их необходимо проверить, прежде чем использовать их дальше.</span><span class="sxs-lookup"><span data-stu-id="3720f-280">Some components of the XPS OM might still be usable, but they will need to be verified before being used further.</span></span> <span data-ttu-id="3720f-281">Так как состояние модели XPS не может быть предсказано после возврата этой ошибки, все компоненты модели XPS должны быть освобождены и удалены.</span><span class="sxs-lookup"><span data-stu-id="3720f-281">Because the state of the XPS OM cannot be predicted after this error is returned, all components of the XPS OM should be released and discarded.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_UNEXPECTED_COLORPROFILE"></span><span id="xps_e_unexpected_colorprofile"></span><dl> <span data-ttu-id="3720f-282"><dt><strong>XPS_E_UNEXPECTED_COLORPROFILE</strong></dt> <dt>0x80520505</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-282"><dt><strong>XPS_E_UNEXPECTED_COLORPROFILE</strong></dt> <dt>0x80520505</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-283">Имеется цветовой профиль, если он не ожидался.</span><span class="sxs-lookup"><span data-stu-id="3720f-283">A color profile was present when one was not expected.</span></span> <span data-ttu-id="3720f-284">Цветовой профиль разрешен только в том случае, если тип цвета — <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3720f-284">A color profile is only allowed when the color type is <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a>.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNEXPECTED_CONTENT_TYPE"></span><span id="xps_e_unexpected_content_type"></span><dl> <span data-ttu-id="3720f-285"><dt><strong>XPS_E_UNEXPECTED_CONTENT_TYPE</strong></dt> <dt>0x80520008</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-285"><dt><strong>XPS_E_UNEXPECTED_CONTENT_TYPE</strong></dt> <dt>0x80520008</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-286">Целевой объект связи не является типом, ожидаемым контекстом связи.</span><span class="sxs-lookup"><span data-stu-id="3720f-286">The target of a relationship is not the type expected by the context of the relationship.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_UNEXPECTED_RELATIONSHIP_TYPE"></span><span id="xps_e_unexpected_relationship_type"></span><dl> <span data-ttu-id="3720f-287"><dt><strong>XPS_E_UNEXPECTED_RELATIONSHIP_TYPE</strong></dt> <dt>0x80520010</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-287"><dt><strong>XPS_E_UNEXPECTED_RELATIONSHIP_TYPE</strong></dt> <dt>0x80520010</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-288">Тип связи не распознан.</span><span class="sxs-lookup"><span data-stu-id="3720f-288">The relationship type was not recognized.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP"></span><span id="xps_e_unexpected_restricted_font_relationship"></span><dl> <span data-ttu-id="3720f-289"><dt><strong>XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520011</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-289"><dt><strong>XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520011</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-290">Коллекция ограниченных шрифтов содержит неограниченный шрифт.</span><span class="sxs-lookup"><span data-stu-id="3720f-290">The restricted font collection contains an unrestricted font.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_VISUAL_CIRCULAR_REF"></span><span id="xps_e_visual_circular_ref"></span><dl> <span data-ttu-id="3720f-291"><dt><strong>XPS_E_VISUAL_CIRCULAR_REF</strong></dt> <dt>0x80520501</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-291"><dt><strong>XPS_E_VISUAL_CIRCULAR_REF</strong></dt> <dt>0x80520501</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-292">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="3720f-292">Reserved.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT"></span><span id="xps_e_xkey_attr_present_outside_res_dict"></span><dl> <span data-ttu-id="3720f-293"><dt><strong>XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT</strong></dt> <dt>0x80520400</dt> </span><span class="sxs-lookup"><span data-stu-id="3720f-293"><dt><strong>XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT</strong></dt> <dt>0x80520400</dt> </span></span></dl></td>
<td><span data-ttu-id="3720f-294">Для геометрии пути, который не находится в словаре ресурсов, указан атрибут <strong>x:Key</strong> .</span><span class="sxs-lookup"><span data-stu-id="3720f-294">A path geometry that is not in a resource dictionary has an <strong>x:Key</strong> attribute specified.</span></span> <span data-ttu-id="3720f-295">Геометрические пути, которые не находятся в словаре ресурсов, не могут иметь атрибут <strong>x:Key</strong> .</span><span class="sxs-lookup"><span data-stu-id="3720f-295">Path geometries that are not in a resource dictionary cannot have an <strong>x:Key</strong> attribute.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="3720f-296">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3720f-296">Remarks</span></span>

<span data-ttu-id="3720f-297">Некоторые методы API документа XPS выполняют вызовы к API [упаковки](/previous-versions/windows/desktop/opc/packaging) .</span><span class="sxs-lookup"><span data-stu-id="3720f-297">Some XPS document API methods make calls to the [Packaging](/previous-versions/windows/desktop/opc/packaging) API.</span></span> <span data-ttu-id="3720f-298">Дополнительные сведения о возвращаемых значениях API упаковки см. в разделе [ошибки упаковки](/previous-versions/windows/desktop/opc/packaging-errors).</span><span class="sxs-lookup"><span data-stu-id="3720f-298">For information about the Packaging API return values, see [Packaging Errors](/previous-versions/windows/desktop/opc/packaging-errors).</span></span>

## <a name="requirements"></a><span data-ttu-id="3720f-299">Требования</span><span class="sxs-lookup"><span data-stu-id="3720f-299">Requirements</span></span>



| <span data-ttu-id="3720f-300">Требование</span><span class="sxs-lookup"><span data-stu-id="3720f-300">Requirement</span></span> | <span data-ttu-id="3720f-301">Значение</span><span class="sxs-lookup"><span data-stu-id="3720f-301">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3720f-302">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3720f-302">Minimum supported client</span></span><br/> | <span data-ttu-id="3720f-303">Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы \[ только для настольных приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3720f-303">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3720f-304">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3720f-304">Minimum supported server</span></span><br/> | <span data-ttu-id="3720f-305">Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3720f-305">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3720f-306">Header</span><span class="sxs-lookup"><span data-stu-id="3720f-306">Header</span></span><br/>                   | <dl> <span data-ttu-id="3720f-307"><dt>Кспсобжектмодел. h</dt></span><span class="sxs-lookup"><span data-stu-id="3720f-307"><dt>Xpsobjectmodel.h</dt></span></span> </dl>                                       |
| <span data-ttu-id="3720f-308">IDL</span><span class="sxs-lookup"><span data-stu-id="3720f-308">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3720f-309"><dt>Кспсобжектмодел. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3720f-309"><dt>XpsObjectModel.idl</dt></span></span> </dl>                                     |



## <a name="see-also"></a><span data-ttu-id="3720f-310">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3720f-310">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3720f-311">Обработка ошибок в COM</span><span class="sxs-lookup"><span data-stu-id="3720f-311">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> </dl>

 

