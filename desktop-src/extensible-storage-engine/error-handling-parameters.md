---
description: 'Дополнительные сведения: обработка ошибок параметров'
title: Параметры обработки ошибок
TOCTitle: Error Handling Parameters
ms:assetid: 014996a1-5674-40c7-9538-54cae1681fec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269173(v=EXCHG.10)
ms:contentKeyID: 32765476
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb225d7dbb67655286635320352060bcf2cb8a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913352"
---
# <a name="error-handling-parameters"></a>Параметры обработки ошибок


_**Применимо к:** Windows | Windows Server_

## <a name="error-handling-parameters"></a>Параметры обработки ошибок

Этот раздел содержит параметры, используемые для обработки ошибок.

*JET_paramErrorToString* 70  

Этот параметр можно использовать для преобразования [JET_ERR](./jet-err.md) в строку. Это делается с помощью специального вызова [жетжетсистемпараметер](./jetgetsystemparameter-function.md) , где выходной буфер выходных данных содержит [JET_ERR](./jet-err.md) значение для преобразования (в качестве входного параметра), а строковый выходной буфер возвращает соответствующую строку ошибки. Строка будет выглядеть примерно следующим образом: "JET_errSuccess, успешная операция". Строка состоит из символьного имени строки, затем запятой, а затем простого текстового описания ошибки. Строка описания может содержать запятые. Если ошибка не распознана, строка будет иметь значение "Неизвестная ошибка, неизвестная ошибка".

**Примечание**  .  Этот параметр доступен только для чтения.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>Специальные функции</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Специальные функции</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>Специальные функции</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Глобальный</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Все</p></td>
</tr>
</tbody>
</table>

*JET_paramExceptionAction*  
98  

Этот параметр определяет, что происходит при возникновении исключения ядром СУБД или кодом, который вызывается ядром СУБД. Если задано значение JET_ExceptionMsgBox, в фильтр необработанных исключений Windows будет создано любое исключение. Это приведет к тому, что исключение будет обработано как сбой приложения. Цель состоит в том, чтобы предотвратить ошибочную попытку перехвата и игнорирования исключения, созданного ядром СУБД. Это не может быть разрешено, так как может произойти повреждение базы данных. Если приложение должно правильно обрабатывать эти исключения, можно отключить защиту, присвоив этому параметру значение JET_ExceptionNone.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>JET_ExceptionMsgBox</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>JET_ExceptionMsgBox, JET_ExceptionNone</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Глобальный</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Windows <strong>2000, Windows XP и Windows Server 2003:</strong>  Нет</p>
<p><strong>Windows Vista:</strong>  Да</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Windows <strong>2000, Windows XP и Windows Server 2003:</strong>  Нет</p>
<p><strong>Windows Vista:</strong>  Да</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Все</p></td>
</tr>
</tbody>
</table>

### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>

### <a name="see-also"></a>См. также:

[Константы обработки ошибок](./error-handling-constants.md)  
[Коды ошибок расширенного подсистемы хранилища](./extensible-storage-engine-error-codes.md)  
[жеткреатеинстанце](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[жетинит](./jetinit-function.md)
