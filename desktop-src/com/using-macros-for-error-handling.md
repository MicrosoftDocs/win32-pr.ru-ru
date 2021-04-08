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
# <a name="using-macros-for-error-handling"></a>Использование макросов для обработки ошибок

COM определяет ряд макросов, упрощающих работу со значениями **HRESULT** .

Макросы обработки ошибок описаны в следующей таблице.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Макрос</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a><br/></td>
<td>Возвращает <strong>значение HRESULT</strong> по заданному биту серьезности, коду устройства и коду ошибки, составляющему <strong>HRESULT</strong>.<br/>
<blockquote>
[!Note]<br />
Вызов <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> для проверки S_OK приводит к снижению производительности. Не следует часто использовать <strong>MAKE_HRESULT</strong> для успешных результатов.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a><br/></td>
<td>Возвращает <strong>SCODE</strong> с заданным битом серьезности, кодом устройства и кодом ошибки, составляющими <strong>SCODE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a><br/></td>
<td>Извлекает часть кода ошибки <strong>HRESULT</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a><br/></td>
<td>Извлекает код устройства <strong>HRESULT</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a><br/></td>
<td>Извлекает бит серьезности <strong>HRESULT</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a><br/></td>
<td>Извлекает код ошибки из <strong>SCODE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a><br/></td>
<td>Извлекает код устройства <strong>SCODE</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a><br/></td>
<td>Извлекает поле степени серьезности <strong>SCODE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>УСПЕШНО</strong></a><br/></td>
<td>Проверяет бит серьезности <strong>SCODE</strong> или <strong>HRESULT</strong>; Возвращает <strong>значение true</strong> , если уровень серьезности равен нулю, и <strong>значение false</strong> , если это один.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>ОШИБОК</strong></a><br/></td>
<td>Проверяет бит серьезности <strong>SCODE</strong> или <strong>HRESULT</strong>; Возвращает <strong>значение true</strong> , если уровень серьезности равен единице, и <strong>значение false</strong> , если оно равно нулю.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a><br/></td>
<td>Предоставляет универсальный тест для ошибок любого значения состояния. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a><br/></td>
<td>Сопоставляет <a href="/windows/desktop/Debug/system-error-codes">код системной ошибки</a> со значением <strong>HRESULT</strong> . <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a><br/></td>
<td>Сопоставляет значение состояния NT со значением <strong>HRESULT</strong> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Обработка ошибок в COM](error-handling-in-com.md)
</dt> </dl>

 

