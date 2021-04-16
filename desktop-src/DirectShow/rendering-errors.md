---
description: Ошибки отрисовки
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Ошибки отрисовки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e106a55363bf50e49a4966600662e26b03b53307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495429"
---
# <a name="rendering-errors"></a><span data-ttu-id="bbabe-103">Ошибки отрисовки</span><span class="sxs-lookup"><span data-stu-id="bbabe-103">Rendering Errors</span></span>

> [!Note]  
> <span data-ttu-id="bbabe-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="bbabe-104">\[Deprecated.</span></span> <span data-ttu-id="bbabe-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bbabe-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bbabe-106">Microsoft® DirectShow® Editing Services (DES) определяет различные коды ошибок, используемые для регистрации ошибок отрисовки.</span><span class="sxs-lookup"><span data-stu-id="bbabe-106">Microsoft® DirectShow® Editing Services (DES) defines various error codes used to log rendering errors.</span></span> <span data-ttu-id="bbabe-107">Если проект не отображается правильно, модуль визуализации вызывает метод [**иамеррорлог:: LogError**](iamerrorlog-logerror.md) .</span><span class="sxs-lookup"><span data-stu-id="bbabe-107">If a project does not render correctly, the render engine calls the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method.</span></span> <span data-ttu-id="bbabe-108">В следующей таблице перечислены параметры, заданные для **LogError**.</span><span class="sxs-lookup"><span data-stu-id="bbabe-108">The following table summarizes the parameters given to **LogError**:</span></span>

-   <span data-ttu-id="bbabe-109">Код ошибки содержится в параметре *ErrorCode* .</span><span class="sxs-lookup"><span data-stu-id="bbabe-109">The error code is contained in the *ErrorCode* parameter.</span></span>
-   <span data-ttu-id="bbabe-110">Описание содержится в параметре ErrorString.</span><span class="sxs-lookup"><span data-stu-id="bbabe-110">The description is contained in the ErrorString parameter.</span></span>
-   <span data-ttu-id="bbabe-111">Описание содержится в параметре *ErrorString* .</span><span class="sxs-lookup"><span data-stu-id="bbabe-111">The description is contained in the *ErrorString* parameter.</span></span>
-   <span data-ttu-id="bbabe-112">При наличии дополнительной информации тип **Variant** содержится в элементе **VT** объекта **Variant** , на который указывает *пекстраинфо*.</span><span class="sxs-lookup"><span data-stu-id="bbabe-112">If there is extra information, the **VARIANT** type is contained in the **vt** member of the **VARIANT** pointed to by *pExtraInfo*.</span></span>

> [!Note]  
> <span data-ttu-id="bbabe-113">Описанные здесь коды ошибок не являются значениями **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bbabe-113">The error codes described here are not **HRESULT** values.</span></span> <span data-ttu-id="bbabe-114">Список возвращаемых значений **HRESULT** , характерных для DES, см. в разделе [коды ошибок и успешности](error-and-success-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bbabe-114">For a list of **HRESULT** return values specific to DES, see [Error and Success Codes](error-and-success-codes.md).</span></span>

 



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bbabe-115">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="bbabe-115">Error code</span></span></th>
<th><span data-ttu-id="bbabe-116">Описание</span><span class="sxs-lookup"><span data-stu-id="bbabe-116">Description</span></span></th>
<th><span data-ttu-id="bbabe-117">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="bbabe-117">Extra information</span></span></th>
<th><span data-ttu-id="bbabe-118">Тип Variant </span><span class="sxs-lookup"><span data-stu-id="bbabe-118">Variant type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bbabe-119">DEX_IDS_BAD_SOURCE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbabe-119">DEX_IDS_BAD_SOURCE_NAME</span></span></td>
<td><span data-ttu-id="bbabe-120">Имя файла не существует, или DirectShow не распознает расширение файла.</span><span class="sxs-lookup"><span data-stu-id="bbabe-120">File name doesn't exist, or DirectShow doesn't recognize the file extension.</span></span></td>
<td><span data-ttu-id="bbabe-121">Имя файла</span><span class="sxs-lookup"><span data-stu-id="bbabe-121">File name</span></span></td>
<td><span data-ttu-id="bbabe-122"><strong>ОСВОБОЖДАЕМОЙ</strong></span><span class="sxs-lookup"><span data-stu-id="bbabe-122"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbabe-123">DEX_IDS_BAD_SOURCE_NAME2</span><span class="sxs-lookup"><span data-stu-id="bbabe-123">DEX_IDS_BAD_SOURCE_NAME2</span></span></td>
<td><span data-ttu-id="bbabe-124">Тип файла не соответствует расширению файла, или файл поврежден.</span><span class="sxs-lookup"><span data-stu-id="bbabe-124">File type does not match the file extension or the file is corrupt.</span></span></td>
<td><span data-ttu-id="bbabe-125">Имя файла</span><span class="sxs-lookup"><span data-stu-id="bbabe-125">File name</span></span></td>
<td><span data-ttu-id="bbabe-126"><strong>ОСВОБОЖДАЕМОЙ</strong></span><span class="sxs-lookup"><span data-stu-id="bbabe-126"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbabe-127">DEX_IDS_MISSING_SOURCE_NAME</span><span class="sxs-lookup"><span data-stu-id="bbabe-127">DEX_IDS_MISSING_SOURCE_NAME</span></span></td>
<td><span data-ttu-id="bbabe-128">Имя файла является обязательным, но не было задано.</span><span class="sxs-lookup"><span data-stu-id="bbabe-128">File name was required, but wasn't given.</span></span></td>
<td><span data-ttu-id="bbabe-129">Нет</span><span class="sxs-lookup"><span data-stu-id="bbabe-129">None</span></span></td>
<td><span data-ttu-id="bbabe-130">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="bbabe-130">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbabe-131">DEX_IDS_UNKNOWN_SOURCE</span><span class="sxs-lookup"><span data-stu-id="bbabe-131">DEX_IDS_UNKNOWN_SOURCE</span></span></td>
<td><span data-ttu-id="bbabe-132">Не удается проанализировать источник данных, предоставленный этим источником.</span><span class="sxs-lookup"><span data-stu-id="bbabe-132">Cannot parse data source provided by this source.</span></span></td>
<td><span data-ttu-id="bbabe-133">Нет</span><span class="sxs-lookup"><span data-stu-id="bbabe-133">None</span></span></td>
<td><span data-ttu-id="bbabe-134">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="bbabe-134">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbabe-135">DEX_IDS_INSTALL_PROBLEM</span><span class="sxs-lookup"><span data-stu-id="bbabe-135">DEX_IDS_INSTALL_PROBLEM</span></span></td>
<td><span data-ttu-id="bbabe-136">Непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="bbabe-136">Unexpected error.</span></span> <span data-ttu-id="bbabe-137">Некоторые компоненты DirectShow установлены неправильно.</span><span class="sxs-lookup"><span data-stu-id="bbabe-137">Some DirectShow component is not installed properly.</span></span></td>
<td><span data-ttu-id="bbabe-138">Нет</span><span class="sxs-lookup"><span data-stu-id="bbabe-138">None</span></span></td>
<td><span data-ttu-id="bbabe-139">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="bbabe-139">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbabe-140">DEX_IDS_NO_SOURCE_NAMES</span><span class="sxs-lookup"><span data-stu-id="bbabe-140">DEX_IDS_NO_SOURCE_NAMES</span></span></td>
<td><span data-ttu-id="bbabe-141">Фильтр источника не принимает имена файлов.</span><span class="sxs-lookup"><span data-stu-id="bbabe-141">Source filter does not accept file names.</span></span></td>
<td><span data-ttu-id="bbabe-142">Нет</span><span class="sxs-lookup"><span data-stu-id="bbabe-142">None</span></span></td>
<td><span data-ttu-id="bbabe-143">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="bbabe-143">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbabe-144">DEX_IDS_BAD_MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="bbabe-144">DEX_IDS_BAD_MEDIATYPE</span></span></td>
<td><span data-ttu-id="bbabe-145">Тип носителя группы не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bbabe-145">Group's media type is not supported.</span></span></td>
<td><span data-ttu-id="bbabe-146">Номер группы</span><span class="sxs-lookup"><span data-stu-id="bbabe-146">Group number</span></span></td>
<td><span data-ttu-id="bbabe-147"><strong>int</strong></span><span class="sxs-lookup"><span data-stu-id="bbabe-147"><strong>int</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbabe-148">DEX_IDS_STREAM_NUMBER</span><span class="sxs-lookup"><span data-stu-id="bbabe-148">DEX_IDS_STREAM_NUMBER</span></span></td>
<td><span data-ttu-id="bbabe-149">Недопустимый номер потока для этого источника.</span><span class="sxs-lookup"><span data-stu-id="bbabe-149">Invalid stream number for this source.</span></span></td>
<td><span data-ttu-id="bbabe-150">Номер потока</span><span class="sxs-lookup"><span data-stu-id="bbabe-150">Stream number</span></span></td>
<td><span data-ttu-id="bbabe-151"><strong>int</strong></span><span class="sxs-lookup"><span data-stu-id="bbabe-151"><strong>int</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbabe-152">DEX_IDS_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="bbabe-152">DEX_IDS_OUTOFMEMORY</span></span></td>
<td><span data-ttu-id="bbabe-153">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="bbabe-153">Out of memory.</span></span></td>
<td><span data-ttu-id="bbabe-154">Нет</span><span class="sxs-lookup"><span data-stu-id="bbabe-154">None</span></span></td>
<td><span data-ttu-id="bbabe-155">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="bbabe-155">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbabe-156">DEX_IDS_DIBSEQ_NOTALLSAME</span><span class="sxs-lookup"><span data-stu-id="bbabe-156">DEX_IDS_DIBSEQ_NOTALLSAME</span></span></td>
<td><span data-ttu-id="bbabe-157">Одно растровое изображение в последовательности не совпадает с типом других.</span><span class="sxs-lookup"><span data-stu-id="bbabe-157">One bitmap in the sequence was not the same type as the others.</span></span></td>
<td><span data-ttu-id="bbabe-158">Имя точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="bbabe-158">Bitmap name</span></span></td>
<td><span data-ttu-id="bbabe-159"><strong>ОСВОБОЖДАЕМОЙ</strong></span><span class="sxs-lookup"><span data-stu-id="bbabe-159"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbabe-160">DEX_IDS_CLIPTOOSHORT</span><span class="sxs-lookup"><span data-stu-id="bbabe-160">DEX_IDS_CLIPTOOSHORT</span></span></td>
<td><span data-ttu-id="bbabe-161">Время воспроизведения клипа недопустимо, или последовательность независимых устройств (DIB) слишком мала.</span><span class="sxs-lookup"><span data-stu-id="bbabe-161">Clip's media times are invalid, or the device-independent bitmap (DIB) sequence is too short.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="bbabe-162">При возникновении других ошибок отрисовки эта ошибка может возникать, несмотря на допустимость времени передачи.</span><span class="sxs-lookup"><span data-stu-id="bbabe-162">If other rendering errors occur, this error might occur even though the media times are valid.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="bbabe-163">Нет</span><span class="sxs-lookup"><span data-stu-id="bbabe-163">None</span></span></td>
<td><span data-ttu-id="bbabe-164">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="bbabe-164">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbabe-165">DEX_IDS_INVALID_DXT</span><span class="sxs-lookup"><span data-stu-id="bbabe-165">DEX_IDS_INVALID_DXT</span></span></td>
<td><span data-ttu-id="bbabe-166">Недопустимый идентификатор класса (CLSID) действия или перехода.</span><span class="sxs-lookup"><span data-stu-id="bbabe-166">Class identifier (CLSID) of the effect or transition is not valid.</span></span></td>
<td><span data-ttu-id="bbabe-167">CLSID</span><span class="sxs-lookup"><span data-stu-id="bbabe-167">CLSID</span></span></td>
<td><span data-ttu-id="bbabe-168"><strong>ОСВОБОЖДАЕМОЙ</strong></span><span class="sxs-lookup"><span data-stu-id="bbabe-168"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbabe-169">DEX_IDS_INVALID_DEFAULT_DXT</span><span class="sxs-lookup"><span data-stu-id="bbabe-169">DEX_IDS_INVALID_DEFAULT_DXT</span></span></td>
<td><span data-ttu-id="bbabe-170">Недопустимый идентификатор CLSID для действия по умолчанию или перехода.</span><span class="sxs-lookup"><span data-stu-id="bbabe-170">The CLSID of the default effect or transition is not valid.</span></span></td>
<td><span data-ttu-id="bbabe-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="bbabe-171">CLSID</span></span></td>
<td><span data-ttu-id="bbabe-172"><strong>ОСВОБОЖДАЕМОЙ</strong></span><span class="sxs-lookup"><span data-stu-id="bbabe-172"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbabe-173">DEX_IDS_NO_3D</span><span class="sxs-lookup"><span data-stu-id="bbabe-173">DEX_IDS_NO_3D</span></span></td>
<td><span data-ttu-id="bbabe-174">Ваша версия DirectX не поддерживает трехмерные переходы.</span><span class="sxs-lookup"><span data-stu-id="bbabe-174">Your version of DirectX does not support three-dimensional transitions.</span></span></td>
<td><span data-ttu-id="bbabe-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="bbabe-175">CLSID</span></span></td>
<td><span data-ttu-id="bbabe-176"><strong>ОСВОБОЖДАЕМОЙ</strong></span><span class="sxs-lookup"><span data-stu-id="bbabe-176"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbabe-177">DEX_IDS_BROKEN_DXT</span><span class="sxs-lookup"><span data-stu-id="bbabe-177">DEX_IDS_BROKEN_DXT</span></span></td>
<td><span data-ttu-id="bbabe-178">Этот результат неверного типа или нарушен.</span><span class="sxs-lookup"><span data-stu-id="bbabe-178">This effect is not the right kind, or is broken.</span></span></td>
<td><span data-ttu-id="bbabe-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="bbabe-179">CLSID</span></span></td>
<td><span data-ttu-id="bbabe-180"><strong>ОСВОБОЖДАЕМОЙ</strong></span><span class="sxs-lookup"><span data-stu-id="bbabe-180"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbabe-181">DEX_IDS_NO_SUCH_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="bbabe-181">DEX_IDS_NO_SUCH_PROPERTY</span></span></td>
<td><span data-ttu-id="bbabe-182">Такое свойство для объекта не существует.</span><span class="sxs-lookup"><span data-stu-id="bbabe-182">No such property exists on the object.</span></span></td>
<td><span data-ttu-id="bbabe-183">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="bbabe-183">Property name</span></span></td>
<td><span data-ttu-id="bbabe-184"><strong>ОСВОБОЖДАЕМОЙ</strong></span><span class="sxs-lookup"><span data-stu-id="bbabe-184"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbabe-185">DEX_IDS_ILLEGAL_PROPERTY_VAL</span><span class="sxs-lookup"><span data-stu-id="bbabe-185">DEX_IDS_ILLEGAL_PROPERTY_VAL</span></span></td>
<td><span data-ttu-id="bbabe-186">Недопустимое значение для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="bbabe-186">Illegal value for this property.</span></span></td>
<td><span data-ttu-id="bbabe-187">Указанное значение</span><span class="sxs-lookup"><span data-stu-id="bbabe-187">Value specified</span></span></td>
<td><span data-ttu-id="bbabe-188"><strong>ЗНАЧЕНИЕ</strong></span><span class="sxs-lookup"><span data-stu-id="bbabe-188"><strong>VARIANT</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbabe-189">DEX_IDS_INVALID_XML</span><span class="sxs-lookup"><span data-stu-id="bbabe-189">DEX_IDS_INVALID_XML</span></span></td>
<td><span data-ttu-id="bbabe-190">Синтаксическая ошибка в XML-файле.</span><span class="sxs-lookup"><span data-stu-id="bbabe-190">Syntax error in XML file.</span></span></td>
<td><span data-ttu-id="bbabe-191">Номер строки</span><span class="sxs-lookup"><span data-stu-id="bbabe-191">Line number</span></span></td>
<td><span data-ttu-id="bbabe-192">VT_I4 (4-байтное целое число)</span><span class="sxs-lookup"><span data-stu-id="bbabe-192">VT_I4 (4-byte integer)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbabe-193">DEX_IDS_CANT_FIND_FILTER</span><span class="sxs-lookup"><span data-stu-id="bbabe-193">DEX_IDS_CANT_FIND_FILTER</span></span></td>
<td><span data-ttu-id="bbabe-194">Не удалось найти фильтр, указанный в XML, по категории и экземпляру.</span><span class="sxs-lookup"><span data-stu-id="bbabe-194">Cannot find filter specified in XML by category and instance.</span></span></td>
<td><span data-ttu-id="bbabe-195">Понятное имя (экземпляр)</span><span class="sxs-lookup"><span data-stu-id="bbabe-195">Friendly name (instance)</span></span></td>
<td><span data-ttu-id="bbabe-196"><strong>ОСВОБОЖДАЕМОЙ</strong></span><span class="sxs-lookup"><span data-stu-id="bbabe-196"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbabe-197">DEX_IDS_DISK_WRITE_ERROR</span><span class="sxs-lookup"><span data-stu-id="bbabe-197">DEX_IDS_DISK_WRITE_ERROR</span></span></td>
<td><span data-ttu-id="bbabe-198">Ошибка записи XML-файла на диск.</span><span class="sxs-lookup"><span data-stu-id="bbabe-198">Error writing XML file to disk.</span></span></td>
<td><span data-ttu-id="bbabe-199">Нет</span><span class="sxs-lookup"><span data-stu-id="bbabe-199">None</span></span></td>
<td><span data-ttu-id="bbabe-200">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="bbabe-200">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbabe-201">DEX_IDS_INVALID_AUDIO_FX</span><span class="sxs-lookup"><span data-stu-id="bbabe-201">DEX_IDS_INVALID_AUDIO_FX</span></span></td>
<td><span data-ttu-id="bbabe-202">CLSID не является допустимым фильтром звукового эффекты DirectShow.</span><span class="sxs-lookup"><span data-stu-id="bbabe-202">CLSID not a valid DirectShow audio effect filter.</span></span></td>
<td><span data-ttu-id="bbabe-203">CLSID</span><span class="sxs-lookup"><span data-stu-id="bbabe-203">CLSID</span></span></td>
<td><span data-ttu-id="bbabe-204"><strong>ОСВОБОЖДАЕМОЙ</strong></span><span class="sxs-lookup"><span data-stu-id="bbabe-204"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbabe-205">DEX_IDS_CANT_FIND_COMPRESSOR</span><span class="sxs-lookup"><span data-stu-id="bbabe-205">DEX_IDS_CANT_FIND_COMPRESSOR</span></span></td>
<td><span data-ttu-id="bbabe-206">Не удается найти программу сжатия для создания указанного формата сжатия.</span><span class="sxs-lookup"><span data-stu-id="bbabe-206">Cannot find a compressor to produce the specified compression format.</span></span></td>
<td><span data-ttu-id="bbabe-207">Нет</span><span class="sxs-lookup"><span data-stu-id="bbabe-207">None</span></span></td>
<td><span data-ttu-id="bbabe-208">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="bbabe-208">Not applicable</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bbabe-209">Следующие ошибки не должны возникать.</span><span class="sxs-lookup"><span data-stu-id="bbabe-209">The following errors should never occur.</span></span> <span data-ttu-id="bbabe-210">Если возникла одна из этих ошибок, отправьте отчет об ошибках в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="bbabe-210">If you encounter one of these errors, please send a bug report to Microsoft.</span></span>



| <span data-ttu-id="bbabe-211">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="bbabe-211">Error code</span></span>                 | <span data-ttu-id="bbabe-212">Описание</span><span class="sxs-lookup"><span data-stu-id="bbabe-212">Description</span></span>                                 |
|----------------------------|---------------------------------------------|
| <span data-ttu-id="bbabe-213">\_ \_ Анализ временной шкалы ИДЕНТИФИКАТОРов DEX \_</span><span class="sxs-lookup"><span data-stu-id="bbabe-213">DEX\_IDS\_TIMELINE\_PARSE</span></span>  | <span data-ttu-id="bbabe-214">Непредвиденная ошибка при синтаксическом анализе временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="bbabe-214">Unexpected error parsing the timeline.</span></span>      |
| <span data-ttu-id="bbabe-215">\_ \_ Ошибка графа ИДЕНТИФИКАТОРов DEX \_</span><span class="sxs-lookup"><span data-stu-id="bbabe-215">DEX\_IDS\_GRAPH\_ERROR</span></span>     | <span data-ttu-id="bbabe-216">Непредвиденная ошибка при построении графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="bbabe-216">Unexpected error building the filter graph.</span></span> |
| <span data-ttu-id="bbabe-217">\_Ошибка сетки идентификаторов DEX \_ \_</span><span class="sxs-lookup"><span data-stu-id="bbabe-217">DEX\_IDS\_GRID\_ERROR</span></span>      | <span data-ttu-id="bbabe-218">Произошла непредвиденная ошибка во внутренней сетке.</span><span class="sxs-lookup"><span data-stu-id="bbabe-218">Unexpected error with the internal grid.</span></span>    |
| <span data-ttu-id="bbabe-219">\_ \_ Ошибка интерфейса DEX \_ ID</span><span class="sxs-lookup"><span data-stu-id="bbabe-219">DEX\_IDS\_INTERFACE\_ERROR</span></span> | <span data-ttu-id="bbabe-220">Непредвиденная ошибка при получении интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bbabe-220">Unexpected error getting an interface.</span></span>      |



 

 

 




