---
title: Использование макросов для обработки ошибок
description: COM определяет ряд макросов, упрощающих работу со значениями HRESULT.
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f31280ec2076f8ece1fcf15dd6e27629a3016e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480540"
---
# <a name="using-macros-for-error-handling"></a>Использование макросов для обработки ошибок

COM определяет ряд макросов, упрощающих работу со значениями **HRESULT** .

Макросы обработки ошибок описаны в следующей таблице.




| Макрос | Описание | 
|-------|-------------|
| <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a><br /> | Возвращает <strong>значение HRESULT</strong> по заданному биту серьезности, коду устройства и коду ошибки, составляющему <strong>HRESULT</strong>.<br /><blockquote>[!Note]<br />Вызов <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> для проверки S_OK приводит к снижению производительности. Не следует часто использовать <strong>MAKE_HRESULT</strong> для успешных результатов.</blockquote><br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a><br /> | Возвращает <strong>SCODE</strong> с заданным битом серьезности, кодом устройства и кодом ошибки, составляющими <strong>SCODE</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a><br /> | Извлекает часть кода ошибки <strong>HRESULT</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a><br /> | Извлекает код устройства <strong>HRESULT</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a><br /> | Извлекает бит серьезности <strong>HRESULT</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a><br /> | Извлекает код ошибки из <strong>SCODE</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a><br /> | Извлекает код устройства <strong>SCODE</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a><br /> | Извлекает поле степени серьезности <strong>SCODE</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>УСПЕШНО</strong></a><br /> | Проверяет бит серьезности <strong>SCODE</strong> или <strong>HRESULT</strong>; Возвращает <strong>значение true</strong> , если уровень серьезности равен нулю, и <strong>значение false</strong> , если это один.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>ОШИБОК</strong></a><br /> | Проверяет бит серьезности <strong>SCODE</strong> или <strong>HRESULT</strong>; Возвращает <strong>значение true</strong> , если уровень серьезности равен единице, и <strong>значение false</strong> , если оно равно нулю.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a><br /> | Предоставляет универсальный тест для ошибок любого значения состояния. <br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a><br /> | Карты <a href="/windows/desktop/Debug/system-error-codes">код системной ошибки</a> в значение <strong>HRESULT</strong> . <br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a><br /> | Карты значение состояния NT в значение <strong>HRESULT</strong> .<br /> | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Обработка ошибок в COM](error-handling-in-com.md)
</dt> </dl>

 

