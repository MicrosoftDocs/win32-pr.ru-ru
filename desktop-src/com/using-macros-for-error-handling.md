---
title: Использование макросов для обработки ошибок
description: COM определяет ряд макросов, упрощающих работу со значениями HRESULT.
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6605ecc05f2d24d3671d28becd770b15d56e1413
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793968"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="73c06-103">Использование макросов для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="73c06-103">Using Macros for Error Handling</span></span>

<span data-ttu-id="73c06-104">COM определяет ряд макросов, упрощающих работу со значениями **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="73c06-104">COM defines a number of macros that make it easier to work with **HRESULT** values.</span></span>

<span data-ttu-id="73c06-105">Макросы обработки ошибок описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="73c06-105">The error handling macros are described in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="73c06-106">Макрос</span><span class="sxs-lookup"><span data-stu-id="73c06-106">Macro</span></span></th>
<th><span data-ttu-id="73c06-107">Описание</span><span class="sxs-lookup"><span data-stu-id="73c06-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73c06-108"><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a></span><span class="sxs-lookup"><span data-stu-id="73c06-108"><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a></span></span><br/></td>
<td><span data-ttu-id="73c06-109">Возвращает <strong>значение HRESULT</strong> по заданному биту серьезности, коду устройства и коду ошибки, составляющему <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="73c06-109">Returns an <strong>HRESULT</strong> given the severity bit, facility code, and error code that comprise the <strong>HRESULT</strong>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="73c06-110">Вызов <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> для проверки S_OK приводит к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="73c06-110">Calling <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> for S_OK verification carries a performance penalty.</span></span> <span data-ttu-id="73c06-111">Не следует часто использовать <strong>MAKE_HRESULT</strong> для успешных результатов.</span><span class="sxs-lookup"><span data-stu-id="73c06-111">You should not routinely use <strong>MAKE_HRESULT</strong> for successful results.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73c06-112"><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="73c06-112"><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="73c06-113">Возвращает <strong>SCODE</strong> с заданным битом серьезности, кодом устройства и кодом ошибки, составляющими <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="73c06-113">Returns an <strong>SCODE</strong> given the severity bit, facility code, and error code that comprise the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73c06-114"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="73c06-114"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="73c06-115">Извлекает часть кода ошибки <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="73c06-115">Extracts the error code portion of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73c06-116"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="73c06-116"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="73c06-117">Извлекает код устройства <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="73c06-117">Extracts the facility code of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73c06-118"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="73c06-118"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="73c06-119">Извлекает бит серьезности <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="73c06-119">Extracts the severity bit of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73c06-120"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="73c06-120"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="73c06-121">Извлекает код ошибки из <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="73c06-121">Extracts the error code portion of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73c06-122"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="73c06-122"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="73c06-123">Извлекает код устройства <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="73c06-123">Extracts the facility code of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73c06-124"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="73c06-124"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="73c06-125">Извлекает поле степени серьезности <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="73c06-125">Extracts the severity field of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73c06-126"><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>УСПЕШНО</strong></a></span><span class="sxs-lookup"><span data-stu-id="73c06-126"><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>SUCCEEDED</strong></a></span></span><br/></td>
<td><span data-ttu-id="73c06-127">Проверяет бит серьезности <strong>SCODE</strong> или <strong>HRESULT</strong>; Возвращает <strong>значение true</strong> , если уровень серьезности равен нулю, и <strong>значение false</strong> , если это один.</span><span class="sxs-lookup"><span data-stu-id="73c06-127">Tests the severity bit of the <strong>SCODE</strong> or <strong>HRESULT</strong>; returns <strong>TRUE</strong> if the severity is zero and <strong>FALSE</strong> if it is one.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73c06-128"><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>ОШИБОК</strong></a></span><span class="sxs-lookup"><span data-stu-id="73c06-128"><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>FAILED</strong></a></span></span><br/></td>
<td><span data-ttu-id="73c06-129">Проверяет бит серьезности <strong>SCODE</strong> или <strong>HRESULT</strong>; Возвращает <strong>значение true</strong> , если уровень серьезности равен единице, и <strong>значение false</strong> , если оно равно нулю.</span><span class="sxs-lookup"><span data-stu-id="73c06-129">Tests the severity bit of the <strong>SCODE</strong> or <strong>HRESULT</strong>; returns <strong>TRUE</strong> if the severity is one and <strong>FALSE</strong> if it is zero.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73c06-130"><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a></span><span class="sxs-lookup"><span data-stu-id="73c06-130"><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a></span></span><br/></td>
<td><span data-ttu-id="73c06-131">Предоставляет универсальный тест для ошибок любого значения состояния.</span><span class="sxs-lookup"><span data-stu-id="73c06-131">Provides a generic test for errors on any status value.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73c06-132"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a></span><span class="sxs-lookup"><span data-stu-id="73c06-132"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a></span></span><br/></td>
<td><span data-ttu-id="73c06-133">Сопоставляет <a href="/windows/desktop/Debug/system-error-codes">код системной ошибки</a> со значением <strong>HRESULT</strong> .</span><span class="sxs-lookup"><span data-stu-id="73c06-133">Maps a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> to an <strong>HRESULT</strong> value.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73c06-134"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a></span><span class="sxs-lookup"><span data-stu-id="73c06-134"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a></span></span><br/></td>
<td><span data-ttu-id="73c06-135">Сопоставляет значение состояния NT со значением <strong>HRESULT</strong> .</span><span class="sxs-lookup"><span data-stu-id="73c06-135">Maps an NT status value to an <strong>HRESULT</strong> value.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="73c06-136">См. также</span><span class="sxs-lookup"><span data-stu-id="73c06-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73c06-137">Обработка ошибок в COM</span><span class="sxs-lookup"><span data-stu-id="73c06-137">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

