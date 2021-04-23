---
description: Определяет значения, указывающие свойства альтернативного распознавания. Интерфейс прикладного программирования (API) Tablet PC использует глобальные уникальные идентификаторы (GUID) для идентификации свойств пакетов, которые в автоматизации являются константными строками.
ms.assetid: 2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8
title: Константы Рекогнитионпроперти (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62971276b6348af3d8ac971851d70b03f7b003c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348635"
---
# <a name="recognitionproperty-constants"></a><span data-ttu-id="7561c-104">Константы Рекогнитионпроперти</span><span class="sxs-lookup"><span data-stu-id="7561c-104">RecognitionProperty Constants</span></span>

<span data-ttu-id="7561c-105">Определяет значения, указывающие свойства альтернативного распознавания.</span><span class="sxs-lookup"><span data-stu-id="7561c-105">Defines values that specify the properties of a recognition alternate.</span></span> <span data-ttu-id="7561c-106">Интерфейс прикладного программирования (API) Tablet PC использует глобальные уникальные идентификаторы (GUID) для идентификации свойств пакетов, которые в автоматизации являются константными строками.</span><span class="sxs-lookup"><span data-stu-id="7561c-106">The Tablet PC application programming interface (API) uses globally unique identifiers (GUIDs) to identify packet properties, which in Automation are constant strings.</span></span>

<span data-ttu-id="7561c-107">В следующей таблице перечислены доступные поля для альтернативного уникального идентификатора (GUID) распознавания альтернативных свойств.</span><span class="sxs-lookup"><span data-stu-id="7561c-107">The following table lists the available recognition alternate property globally unique identifier (GUID) fields.</span></span> <span data-ttu-id="7561c-108">Используйте эти идентификаторы GUID для доступа к свойствам объекта [**иинкрекогнитионалтернате**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) , вызвав метод [**жетпропертивалуе**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) .</span><span class="sxs-lookup"><span data-stu-id="7561c-108">Use these GUIDs to access properties of an [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) object by calling the [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) method.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="7561c-109">Имя константы</span><span class="sxs-lookup"><span data-stu-id="7561c-109">Constant Name</span></span></th>
<th style="text-align: left;"><span data-ttu-id="7561c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7561c-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINENUMBER_________"></span><span id="___________inkrecognitionproperty_linenumber_________"></span><dl> <span data-ttu-id="7561c-111"><dt><strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7561c-111"><dt> <strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7561c-112">Идентификатор GUID, определяющий свойство для номера строки объекта <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>иинкрекогнитионалтернате</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7561c-112">The GUID that identifies the property for the line number of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/> <span data-ttu-id="7561c-113">Номер_строки указывает варианты с определенным номером строки.</span><span class="sxs-lookup"><span data-stu-id="7561c-113">LineNumber specifies the alternates with a particular line number.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7561c-114">Это поле не поддерживается для распознавателей символов восточноазиатских языков.</span><span class="sxs-lookup"><span data-stu-id="7561c-114">This field is not supported for recognizers of East Asian characters.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_SEGMENTATION_________"></span><span id="___________inkrecognitionproperty_segmentation_________"></span><dl> <span data-ttu-id="7561c-115"><dt><strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7561c-115"><dt> <strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7561c-116">Идентификатор GUID, определяющий свойство для сегментации объекта <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>иинкрекогнитионалтернате</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7561c-116">The GUID that identifies the property for the segmentation of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/> <span data-ttu-id="7561c-117">Сегментация указывает основной фрагмент или единицу рукописного ввода, которую распознаватель использует для получения результата распознавания.</span><span class="sxs-lookup"><span data-stu-id="7561c-117">Segmentation specifies the basic ink fragment or unit that the recognizer uses to produce a recognition result.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7561c-118">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="7561c-118">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_HOTPOINT_________"></span><span id="___________inkrecognitionproperty_hotpoint_________"></span><dl> <span data-ttu-id="7561c-119"><dt><strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7561c-119"><dt> <strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7561c-120">Идентификатор GUID, определяющий свойство для горячей точки распознавания объекта <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>иинкрекогнитионалтернате</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7561c-120">The GUID that identifies the property for the recognition hot point of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT_________"></span><span id="___________inkrecognitionproperty_maximumstrokecount_________"></span><dl> <span data-ttu-id="7561c-121"><dt><strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7561c-121"><dt> <strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7561c-122">Идентификатор GUID, определяющий свойство для максимального числа штрихов для результата распознавания объекта <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>иинкрекогнитионалтернате</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7561c-122">The GUID that identifies the property for the maximum stroke count of the recognition result for the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7561c-123">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="7561c-123">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_POINTSPERINCH_________"></span><span id="___________inkrecognitionproperty_pointsperinch_________"></span><dl> <span data-ttu-id="7561c-124"><dt><strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7561c-124"><dt> <strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7561c-125">Идентификатор GUID, определяющий свойство для метрики объекта <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>иинкрекогнитионалтернате</strong></a> в точках на дюйм.</span><span class="sxs-lookup"><span data-stu-id="7561c-125">The GUID that identifies the property for the points-per-inch metric of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7561c-126">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="7561c-126">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_CONFIDENCELEVEL_________"></span><span id="___________inkrecognitionproperty_confidencelevel_________"></span><dl> <span data-ttu-id="7561c-127"><dt><strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7561c-127"><dt> <strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7561c-128">Идентификатор GUID, определяющий свойство для уровня достоверности, который распознаватель имеет в результате распознавания.</span><span class="sxs-lookup"><span data-stu-id="7561c-128">The GUID that identifies the property for the level of confidence that the recognizer has in the recognition result.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7561c-129">Оценка достоверности доступна только для США английского и всех распознавателей жестов в Microsoft Windows XP Tablet PC Edition и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7561c-129">Confidence evaluation is available only for United States English and all gesture recognizers in Microsoft Windows XP Tablet PC Edition and Windows Vista.</span></span> <span data-ttu-id="7561c-130">Методы, которые предоставляют свойство достоверности для любого другого распознавателя, возвращающего E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="7561c-130">Methods that provide the confidence property for any other recognizer return E_NOTIMPL.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINEMETRICS_________"></span><span id="___________inkrecognitionproperty_linemetrics_________"></span><dl> <span data-ttu-id="7561c-131"><dt><strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7561c-131"><dt> <strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7561c-132">Идентификатор GUID, определяющий свойство для метрик линии объекта <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>иинкрекогнитионалтернате</strong></a> , который является строкой, для которой извлекаются метрики.</span><span class="sxs-lookup"><span data-stu-id="7561c-132">The GUID that identifies the property for the line metrics of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object, which is the line for which to retrieve metrics.</span></span> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="7561c-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7561c-133">Remarks</span></span>

<span data-ttu-id="7561c-134">В C++ вы можете получить доступ к этим константам в файле заголовка Мсинкаут. h, который находится в папке <systemdrive> : \\ Program Files \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ include, если пакет SDK установлен в расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7561c-134">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Include directory if you installed the SDK in the default location.</span></span>

> [!Note]  
> <span data-ttu-id="7561c-135">В C++ эти константы являются Вчарс, а не BSTRs.</span><span class="sxs-lookup"><span data-stu-id="7561c-135">In C++, these constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="7561c-136">Преобразуйте их в BSTRs перед использованием.</span><span class="sxs-lookup"><span data-stu-id="7561c-136">Convert them into BSTRs before use.</span></span> <span data-ttu-id="7561c-137">Дополнительные сведения о типе данных BSTR см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="7561c-137">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7561c-138">Требования</span><span class="sxs-lookup"><span data-stu-id="7561c-138">Requirements</span></span>



| <span data-ttu-id="7561c-139">Требование</span><span class="sxs-lookup"><span data-stu-id="7561c-139">Requirement</span></span> | <span data-ttu-id="7561c-140">Значение</span><span class="sxs-lookup"><span data-stu-id="7561c-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7561c-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7561c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7561c-142">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7561c-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7561c-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7561c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7561c-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7561c-144">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7561c-145">Header</span><span class="sxs-lookup"><span data-stu-id="7561c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="7561c-146"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7561c-146"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7561c-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7561c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7561c-148">**Метод Алтернатесвисконстантпропертивалуес**</span><span class="sxs-lookup"><span data-stu-id="7561c-148">**AlternatesWithConstantPropertyValues Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues)
</dt> <dt>

[<span data-ttu-id="7561c-149">**Конфиденцеалтернатес, свойство**</span><span class="sxs-lookup"><span data-stu-id="7561c-149">**ConfidenceAlternates Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates)
</dt> <dt>

[<span data-ttu-id="7561c-150">**Линеалтернатес, свойство**</span><span class="sxs-lookup"><span data-stu-id="7561c-150">**LineAlternates Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates)
</dt> <dt>

[<span data-ttu-id="7561c-151">**Интерфейс Иинкрекогнитионалтернатес**</span><span class="sxs-lookup"><span data-stu-id="7561c-151">**IInkRecognitionAlternates Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates)
</dt> </dl>

 

 




