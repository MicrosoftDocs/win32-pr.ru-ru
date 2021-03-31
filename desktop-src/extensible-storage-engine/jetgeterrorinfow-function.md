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
ms.openlocfilehash: 1bf4db5d8d34a741e57f72e8f237f1497de0bacf
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104157282"
---
# <a name="jetgeterrorinfow-function"></a>Функция Жетжетерроринфов


_**Применимо к:** Windows | Windows Server_

## <a name="jetgeterrorinfow-function"></a>Функция Жетжетерроринфов

Функция **жетжетерроринфов** BAS_ ядра СУБД.

Примечание. Эта документация основана на предварительном выпуске расширяемой подсистемы хранилища. Эта информация может быть изменена.

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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_ErrorInfoSpecificErr</p></td>
<td><p><em>пвконтекст</em> интерпретируется как код/Error <a href="gg269297(v=exchg.10).md">JET_ERR</a>, <em>пвресулт</em> интерпретируется как <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>, а поля структуры <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> заполняются соответствующим образом.</p></td>
</tr>
</tbody>
</table>


*грбит*

Зарезервировано.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./extensible-storage-engine-error-codes.md) тип данных с одним из кодов возврата, перечисленных в следующей таблице. Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Код возврата</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Операция выполнена успешно.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра. Это может произойти для <strong>жетжетерроринфо</strong> , когда происходит следующее:</p>
<ul>
<li><p>Указано недопустимое значение параметра <em>инфолевел</em> .</p></li>
<li><p>Указано недопустимое значение <em>грбит</em> .</p></li>
<li><p>Указанное значение <em>кбмакс</em> буфера параметра <em>пвресулт</em> меньше, чем требуемый размер для выходных данных этого параметра <em>инфолевел</em> .</p></li>
<li><p>Для <em>инфолевел</em> = JET_ErrorInfoSpecificErr переданное значение <a href="gg294092(v=exchg.10).md">JET_ERR</a> неизвестно подсистеме.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errDisabledFunctionality</p></td>
<td><p>Если этот номер SKU Windows не поддерживает эту функцию, будет возвращена эта ошибка.</p></td>
</tr>
</tbody>
</table>


При успешном завершении для выходного буфера, соответствующего запрошенному контексту или значению ошибки, будут установлены запрошенные расширенные сведения об ошибке.

В случае сбоя состояние выходных буферов будет не определено.

### <a name="remarks"></a>Комментарии

Функция [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) и [JET_ERRCAT](./jet-errcat.md) группы констант содержат документацию о расширенных сведениях об ошибках, возвращаемых для *инфолевел* = JET_ErrorInfoSpecificErr.

### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows 8 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Библиотека</strong></p></td>
<td><p>Используйте ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>КОМПОНОВКИ</strong></p></td>
<td><p>Требуется ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Юникод</strong></p></td>
<td><p>Примечание. реализуется только <strong>жетжетерроринфов</strong> (Unicode). Этот API не имеет версию A (ANSI).</p></td>
</tr>
</tbody>
</table>
