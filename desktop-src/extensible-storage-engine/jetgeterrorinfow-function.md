---
description: Дополнительные сведения о функции Жетжетерроринфов
title: Функция Жетжетерроринфов
TOCTitle: JetGetErrorInfoW Function
ms:assetid: 7a84f937-7a16-434e-896d-789f316ee833
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475859(v=EXCHG.10)
ms:contentKeyID: 37033565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetErrorInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f459d98ee2cc3c0bb1b57eb5cd4fb630d076836b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468981"
---
# <a name="jetgeterrorinfow-function"></a>Функция Жетжетерроринфов


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetgeterrorinfow-function"></a>Функция Жетжетерроринфов

Функция **жетжетерроринфов** BAS_ ядра СУБД.

примечание. эта документация основана на предварительном выпуске расширяемого механизма служба хранилища. Эта информация может быть изменена.

```cpp
JET_ERR JET_API JetGetErrorInfoW( 
    _In_opt_ void *                      pvContext, 
    _Out_writes_bytes_( cbMax ) void *   pvResult, 
    _In_ unsigned long                   cbMax, 
    _In_ unsigned long                   InfoLevel, 
    _In_ JET_GRBIT                       grbit );
```

### <a name="parameters"></a>Параметры

*пвконтекст*

Контекст или значение ошибки, для которого требуются расширенные сведения об ошибке. Передаваемое значение зависит от значения параметра *инфолевел* .

*пвресулт*

Указатель на буфер, который будет принимать сведения. Тип буфера зависит от значения параметра *инфолевел* . Вызывающий объект должен быть настроен для правильного согласования буфера.

*кбмакс*

Максимальный размер передаваемой структуры *пвресулт* .

*инфолевел*

Тип сведений, которые будут получены для сведений об ошибке или контекста, задается параметром *пвконтекст* . Формат данных, хранящихся в *пвресулт* , зависит от *инфолевел*.

В следующей таблице перечислены возможные значения для этого параметра.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_ErrorInfoSpecificErr</p> | <p><em>пвконтекст</em> интерпретируется как код/Error <a href="gg269297(v=exchg.10).md">JET_ERR</a>, <em>пвресулт</em> интерпретируется как <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>, а поля структуры <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> заполняются соответствующим образом.</p> | 



*грбит*

Зарезервировано.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./extensible-storage-engine-error-codes.md) тип данных с одним из кодов возврата, перечисленных в следующей таблице. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра. Это может произойти для <strong>жетжетерроринфо</strong> , когда происходит следующее:</p><ul><li><p>Указано недопустимое значение параметра <em>инфолевел</em> .</p></li><li><p>Указано недопустимое значение <em>грбит</em> .</p></li><li><p>Указанное значение <em>кбмакс</em> буфера параметра <em>пвресулт</em> меньше, чем требуемый размер для выходных данных этого параметра <em>инфолевел</em> .</p></li><li><p>Для <em>инфолевел</em> = JET_ErrorInfoSpecificErr переданное значение <a href="gg294092(v=exchg.10).md">JET_ERR</a> неизвестно подсистеме.</p></li></ul> | 
| <p>JET_errDisabledFunctionality</p> | <p>Если этот номер SKU Windows не поддерживает эту функцию, будет возвращена эта ошибка.</p> | 



При успешном завершении для выходного буфера, соответствующего запрошенному контексту или значению ошибки, будут установлены запрошенные расширенные сведения об ошибке.

В случае сбоя состояние выходных буферов будет не определено.

### <a name="remarks"></a>Комментарии

Функция [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) и [JET_ERRCAT](./jet-errcat.md) группы констант содержат документацию о расширенных сведениях об ошибках, возвращаемых для *инфолевел* = JET_ErrorInfoSpecificErr.

### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>Требуется Windows 8.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows 8 Server.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | | <p><strong>Юникод</strong></p> | <p>Примечание. реализуется только <strong>жетжетерроринфов</strong> (Unicode). Этот API не имеет версию A (ANSI).</p> | 

