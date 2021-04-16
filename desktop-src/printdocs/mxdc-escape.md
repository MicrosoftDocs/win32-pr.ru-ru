---
description: Escape- \_ функция мксдк-принтера позволяет приложениям записывать документы в файл или на принтер в формате XPS с помощью конвертера документов XPS Microsoft (мксдк).
ms.assetid: 79aeb32e-94b1-4806-8ebf-a9d0956f4667
title: Функция MXDC_ESCAPE (Мксдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 08b5ae7e44f7b9c35d6a395b78ce514aee050e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650794"
---
# <a name="mxdc_escape-function"></a><span data-ttu-id="cbe6e-103">\_Escape-функция мксдк</span><span class="sxs-lookup"><span data-stu-id="cbe6e-103">MXDC\_ESCAPE function</span></span>

<span data-ttu-id="cbe6e-104">Escape-функция **мксдк \_** -принтера позволяет приложениям записывать документы в файл или на принтер в формате XPS с помощью конвертера документов XPS Microsoft (мксдк).</span><span class="sxs-lookup"><span data-stu-id="cbe6e-104">The **MXDC\_ESCAPE** printer escape function enables applications to write documents to a file or to a printer in XML Paper Specification (XPS) format by means of the Microsoft XPS Document Converter (MXDC).</span></span>

<span data-ttu-id="cbe6e-105">Чтобы выполнить эту операцию, вызовите функцию [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-105">To perform this operation, call the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function with the following parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbe6e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbe6e-106">Syntax</span></span>


```C++
int MXDC_ESCAPE(
    hdc,
    cbInput,
    lpszInData,
    cbOutput,
    lpszOutData
);
```



## <a name="parameters"></a><span data-ttu-id="cbe6e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbe6e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbe6e-108">*HDC*</span><span class="sxs-lookup"><span data-stu-id="cbe6e-108">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="cbe6e-109">Маркер контекста устройства принтера.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-109">A handle to the printer device context.</span></span>

</dd> <dt>

<span data-ttu-id="cbe6e-110">*кбинпут*</span><span class="sxs-lookup"><span data-stu-id="cbe6e-110">*cbInput*</span></span> 
</dt> <dd>

<span data-ttu-id="cbe6e-111">Размер (в байтах) данных, на которые указывает параметр *лпсзиндата* .</span><span class="sxs-lookup"><span data-stu-id="cbe6e-111">The size, in bytes, of the data pointed to by the *lpszInData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cbe6e-112">*лпсзиндата*</span><span class="sxs-lookup"><span data-stu-id="cbe6e-112">*lpszInData*</span></span> 
</dt> <dd>

<span data-ttu-id="cbe6e-113">Указатель на буфер, содержащий входные данные, которые всегда хранятся в одной из следующих структур.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-113">A pointer to a buffer containing the input data, which is always stored in one of the following structures.</span></span>

<dl> <dd><span data-ttu-id="cbe6e-114"><a href="mxdcescapeheader.md">**мксдцескапехеадер**</a></span><span class="sxs-lookup"><span data-stu-id="cbe6e-114"><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></span></span></dd> <dd><span data-ttu-id="cbe6e-115"><a href="mxdcprintticketescape.md">**мксдкпринттиккетескапе**</a></span><span class="sxs-lookup"><span data-stu-id="cbe6e-115"><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></span></span></dd> <dd><span data-ttu-id="cbe6e-116"><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></span><span class="sxs-lookup"><span data-stu-id="cbe6e-116"><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></span></span></dd> <dd><span data-ttu-id="cbe6e-117"><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></span><span class="sxs-lookup"><span data-stu-id="cbe6e-117"><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></span></span></dd> </dl>

<span data-ttu-id="cbe6e-118">Каждая из этих структур имеет элемент кода операции, указывающий, что именно должно выполняться МКСДК.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-118">Each of these structures has an opcode member that specifies what the MXDC is supposed to do.</span></span> <span data-ttu-id="cbe6e-119">Подробные замечания об этих кодах см. в разделе Мксдцескапехеадер.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-119">See MxdcEscapeHeader for detailed remarks about these codes.</span></span>



| <span data-ttu-id="cbe6e-120">Код операции (код операции)</span><span class="sxs-lookup"><span data-stu-id="cbe6e-120">Operations code (opcode)</span></span>                                                                                                                                                                                                  | <span data-ttu-id="cbe6e-121">Действие</span><span class="sxs-lookup"><span data-stu-id="cbe6e-121">Action</span></span>                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MXDCOP_GET_FILENAME"></span><span id="mxdcop_get_filename"></span><dl> <span data-ttu-id="cbe6e-122"><dt>**МКСДКОП \_ получить \_ имя файла**</dt></span><span class="sxs-lookup"><span data-stu-id="cbe6e-122"><dt>**MXDCOP\_GET\_FILENAME**</dt></span></span> </dl>                                          | <span data-ttu-id="cbe6e-123">Задает для параметра *лпсзаутдата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) значение, либо полный путь к выходному файлу в виде строки, завершающейся нулем, либо другой размер строки.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-123">Sets the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function to, either the full path of the output file as a zero-terminated string or else the size of that string.</span></span><br/>                               |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC_SEQ"></span><span id="mxdcop_printticket_fixed_doc_seq"></span><dl> <span data-ttu-id="cbe6e-124"><dt>**\_ \_ фиксированная \_ последовательность документов мксдкоп PRINTTICKET \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cbe6e-124"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**</dt></span></span> </dl> | <span data-ttu-id="cbe6e-125">Связывает билет на печать с фиксированной последовательностью документов XPS.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-125">Associates a print ticket with an XPS fixed document sequence.</span></span><br/>                                                                                                                                                         |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC"></span><span id="mxdcop_printticket_fixed_doc"></span><dl> <span data-ttu-id="cbe6e-126"><dt>**\_ \_ фиксированный документ мксдкоп PRINTTICKET \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cbe6e-126"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_DOC**</dt></span></span> </dl>              | <span data-ttu-id="cbe6e-127">Связывает билет печати с документом XPS.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-127">Associates a print ticket with an XPS document.</span></span><br/>                                                                                                                                                                        |
| <span id="MXDCOP_PRINTTICKET_FIXED_PAGE"></span><span id="mxdcop_printticket_fixed_page"></span><dl> <span data-ttu-id="cbe6e-128"><dt>**\_ \_ фиксированная страница мксдкоп PRINTTICKET \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cbe6e-128"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_PAGE**</dt></span></span> </dl>           | <span data-ttu-id="cbe6e-129">Связывает билет на печать со страницей XPS.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-129">Associates a print ticket with an XPS page.</span></span><br/>                                                                                                                                                                            |
| <span id="MXDCOP_SET_S0PAGE"></span><span id="mxdcop_set_s0page"></span><dl> <span data-ttu-id="cbe6e-130"><dt>**МКСДКОП \_ Set \_ S0PAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="cbe6e-130"><dt>**MXDCOP\_SET\_S0PAGE**</dt></span></span> </dl>                                                | <span data-ttu-id="cbe6e-131">Отправляет в выходные данные разметку XPS текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-131">Sends the XPS markup of the current page to the output.</span></span><br/>                                                                                                                                                                |
| <span id="MXDCOP_SET_S0PAGE_RESOURCE"></span><span id="mxdcop_set_s0page_resource"></span><dl> <span data-ttu-id="cbe6e-132"><dt>**МКСДКОП \_ задать \_ S0PAGE \_ ресурс**</dt></span><span class="sxs-lookup"><span data-stu-id="cbe6e-132"><dt>**MXDCOP\_SET\_S0PAGE\_RESOURCE**</dt></span></span> </dl>                    | <span data-ttu-id="cbe6e-133">Отправляет на выход на страницу ресурс, например изображение или шрифт.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-133">Sends a resource on the page, such as an image or font, to the output.</span></span><br/>                                                                                                                                                 |
| <span id="MXDCOP_SET_XPSPASSTHRU_MODE"></span><span id="mxdcop_set_xpspassthru_mode"></span><dl> <span data-ttu-id="cbe6e-134"><dt>**МКСДКОП \_ Set \_ кспспасссру \_ mode**</dt></span><span class="sxs-lookup"><span data-stu-id="cbe6e-134"><dt>**MXDCOP\_SET\_XPSPASSTHRU\_MODE**</dt></span></span> </dl>                 | <span data-ttu-id="cbe6e-135">Помещает МКСДК в состояние сквозной передачи, позволяя приложению записывать XPS непосредственно в выходной файл без какой-либо обработки МКСДК.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-135">Puts the MXDC into a pass through state, enabling an application to write XPS directly to the output file without any processing by the MXDC.</span></span> <span data-ttu-id="cbe6e-136">Таким образом может быть написан весь документ или даже последовательность документов.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-136">An entire document or even document sequence can be written in this way.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cbe6e-137">*кбаутпут*</span><span class="sxs-lookup"><span data-stu-id="cbe6e-137">*cbOutput*</span></span> 
</dt> <dd>

<span data-ttu-id="cbe6e-138">Размер (в байтах) данных, на которые указывает параметр *лпсзаутдата* .</span><span class="sxs-lookup"><span data-stu-id="cbe6e-138">The size, in bytes, of the data pointed to by the *lpszOutData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cbe6e-139">*лпсзаутдата*</span><span class="sxs-lookup"><span data-stu-id="cbe6e-139">*lpszOutData*</span></span> 
</dt> <dd>

<span data-ttu-id="cbe6e-140">Указатель на буфер, содержащий выходные данные.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-140">A pointer to a buffer containing the output data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbe6e-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbe6e-141">Return value</span></span>

<span data-ttu-id="cbe6e-142">Если функция выполнена удачно, возвращаемое значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-142">If the function succeeds, the return value is greater than zero.</span></span> <span data-ttu-id="cbe6e-143">Если функция завершается ошибкой или не поддерживается, возвращаемое значение меньше или равно нулю.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-143">If the function fails or is not supported, the return value is less than or equal to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbe6e-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cbe6e-144">Remarks</span></span>

<span data-ttu-id="cbe6e-145">Эта escape-последовательность поддерживается МКСДК и XPSDrv, но не GDI.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-145">This escape is supported by MXDC and XPSDrv, but not by GDI.</span></span>

<span data-ttu-id="cbe6e-146">Чтобы определить, является ли драйвер принтера МКСДК, вызовите [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) с помощью [**escape-**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) последовательности.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-146">To determine if the printer driver is the MXDC, call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) escape.</span></span> <span data-ttu-id="cbe6e-147">Если драйвер является МКСДК, **екстескапе** вернет строку, завершающуюся нулем, " http://schemas.microsoft.com/xps/2005/06 ".</span><span class="sxs-lookup"><span data-stu-id="cbe6e-147">If the driver is the MXDC, the **ExtEscape** will return the zero-terminated string, "http://schemas.microsoft.com/xps/2005/06".</span></span> <span data-ttu-id="cbe6e-148">Убедитесь, что буфер, на который ссылается параметр *лпсзаутдата* , достаточно велик, чтобы вместить эту строку.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-148">Be sure the buffer referenced by the *lpszOutData* parameter is large enough to hold this string.</span></span>

<span data-ttu-id="cbe6e-149">Чтобы определить, является ли драйвер принтера Windows встроенным драйвером для записи XPS-документов (Microsoft), убедитесь, что драйвер принтера является МКСДК, а затем определите, что имя драйвера принтера — "Microsoft XPS Document Writer".</span><span class="sxs-lookup"><span data-stu-id="cbe6e-149">To determine if the printer driver is the Windows in-box Microsoft XPS Document Writer driver, confirm that the printer driver is the MXDC, and then determine whether the name of the printer driver is "Microsoft XPS Document Writer".</span></span>

<span data-ttu-id="cbe6e-150">Чтобы получить имя драйвера принтера, используйте один из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-150">To get the printer driver name, use one of the following techniques.</span></span> <dl> <span data-ttu-id="cbe6e-151">Вызовите [**жетпринтердривер**](getprinterdriver.md) с параметром *Level* , имеющим значение 1.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-151">Call [**GetPrinterDriver**](getprinterdriver.md) with the *Level* parameter value set to 1.</span></span> <span data-ttu-id="cbe6e-152">Имя драйвера принтера возвращается в элементе **pName** структуры [**драйвера \_ \_ 1**](driver-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="cbe6e-152">The printer driver name is returned in the **pName** member of the [**DRIVER\_INFO\_1**](driver-info-1.md) structure.</span></span>  
<span data-ttu-id="cbe6e-153">или</span><span class="sxs-lookup"><span data-stu-id="cbe6e-153">or</span></span>  
<span data-ttu-id="cbe6e-154">Вызовите [**метод установки, указав**](getprinter.md) для параметра *уровня* значение 2.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-154">Call [**GetPrinter**](getprinter.md) with the *Level* parameter value set to 2.</span></span> <span data-ttu-id="cbe6e-155">Имя драйвера принтера возвращается в элементе **пдривернаме** структуры " [**\_ сведения \_ о принтере**](printer-info-2.md) ".</span><span class="sxs-lookup"><span data-stu-id="cbe6e-155">The printer driver name is returned in the **pDriverName** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>  
</dl>

<span data-ttu-id="cbe6e-156">В следующей таблице показано, где будут записаны различные объекты в XPS-файле различных типов.</span><span class="sxs-lookup"><span data-stu-id="cbe6e-156">The following table shows where to find various objects in the XPS file various types of objects will be written.</span></span>



| <span data-ttu-id="cbe6e-157">Объект</span><span class="sxs-lookup"><span data-stu-id="cbe6e-157">Object</span></span>       | <span data-ttu-id="cbe6e-158">Расположение в выходном файле</span><span class="sxs-lookup"><span data-stu-id="cbe6e-158">Location in the output file</span></span>    |
|--------------|--------------------------------|
| <span data-ttu-id="cbe6e-159">Фиксированная страница</span><span class="sxs-lookup"><span data-stu-id="cbe6e-159">Fixed Page</span></span>   | <span data-ttu-id="cbe6e-160">/Documents/1/Pages/Esc%d.fpage</span><span class="sxs-lookup"><span data-stu-id="cbe6e-160">/Documents/1/Pages/Esc%d.fpage</span></span> |
| <span data-ttu-id="cbe6e-161">Thumbnail</span><span class="sxs-lookup"><span data-stu-id="cbe6e-161">Thumbnail</span></span>    | <span data-ttu-id="cbe6e-162">/Documents/1/Metadata</span><span class="sxs-lookup"><span data-stu-id="cbe6e-162">/Documents/1/Metadata</span></span>          |
| <span data-ttu-id="cbe6e-163">Билет на печать</span><span class="sxs-lookup"><span data-stu-id="cbe6e-163">Print Ticket</span></span> | <span data-ttu-id="cbe6e-164">/Documents/1/Metadata</span><span class="sxs-lookup"><span data-stu-id="cbe6e-164">/Documents/1/Metadata</span></span>          |
| <span data-ttu-id="cbe6e-165">Шрифт</span><span class="sxs-lookup"><span data-stu-id="cbe6e-165">Font</span></span>         | <span data-ttu-id="cbe6e-166">/Documents/1/Resources/Fonts</span><span class="sxs-lookup"><span data-stu-id="cbe6e-166">/Documents/1/Resources/Fonts</span></span>   |
| <span data-ttu-id="cbe6e-167">Образ</span><span class="sxs-lookup"><span data-stu-id="cbe6e-167">Image</span></span>        | <span data-ttu-id="cbe6e-168">/Documents/1/Resources/Images</span><span class="sxs-lookup"><span data-stu-id="cbe6e-168">/Documents/1/Resources/Images</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="cbe6e-169">Требования</span><span class="sxs-lookup"><span data-stu-id="cbe6e-169">Requirements</span></span>



| <span data-ttu-id="cbe6e-170">Требование</span><span class="sxs-lookup"><span data-stu-id="cbe6e-170">Requirement</span></span> | <span data-ttu-id="cbe6e-171">Значение</span><span class="sxs-lookup"><span data-stu-id="cbe6e-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cbe6e-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cbe6e-172">Minimum supported client</span></span><br/> | <span data-ttu-id="cbe6e-173">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cbe6e-173">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cbe6e-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cbe6e-174">Minimum supported server</span></span><br/> | <span data-ttu-id="cbe6e-175">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cbe6e-175">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cbe6e-176">Header</span><span class="sxs-lookup"><span data-stu-id="cbe6e-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbe6e-177"><dt>Мксдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbe6e-177"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbe6e-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbe6e-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbe6e-179">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="cbe6e-179">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

<span data-ttu-id="cbe6e-180">[Escape-функции принтера](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cbe6e-180">[Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cbe6e-181">**екстескапе**</span><span class="sxs-lookup"><span data-stu-id="cbe6e-181">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> </dl>

 

