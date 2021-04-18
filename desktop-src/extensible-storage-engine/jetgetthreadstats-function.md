---
description: Дополнительные сведения о функции Жетжетсреадстатс
title: Функция Жетжетсреадстатс
TOCTitle: JetGetThreadStats Function
ms:assetid: 1b8df8cd-fc61-44fe-a15c-a166f7097c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269196(v=EXCHG.10)
ms:contentKeyID: 32765499
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetThreadStats
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85d45021910f818f297cd0bc9829580a18b7a296
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701357"
---
# <a name="jetgetthreadstats-function"></a>Функция Жетжетсреадстатс


_**Применимо к:** Windows | Windows Server_

## <a name="jetgetthreadstats-function"></a>Функция Жетжетсреадстатс

Функция **жетжетсреадстатс** извлекает сведения о производительности из ядра СУБД для текущего потока. Для сбора статистики, отражающей активность ядра СУБД в этом потоке между этими вызовами, можно использовать несколько вызовов.

**Windows Vista:**  **Жетжетсреадстатс** появился в Windows Vista.

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>Параметры

*пвресулт*

Выходной буфер, который получает данные статистики потока. После успешного вызова буфер содержит структуру [JET_THREADSTATS](./jet-threadstats-structure.md) .

*кбмакс*

Максимальный размер выходного буфера в байтах.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).

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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Не удалось выполнить операцию, так как указанный выходной буфер слишком мал для размещения запрошенных данных. Функция <strong>жетжетсреадстатс</strong> возвращает эту ошибку, если выходной буфер слишком мал для хранения наименьшей версии структуры <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> , поддерживаемой ядром СУБД.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении выходной буфер будет содержать структуру [JET_THREADSTATS](./jet-threadstats-structure.md) , содержащую статистику ядра СУБД для текущего потока.

В случае сбоя состояние выходного буфера не определено.

#### <a name="remarks"></a>Комментарии

Сведения, предоставляемые двумя последовательными вызовами этого API, предназначены для расчета расходов на любые другие операции ядра СУБД в текущем потоке. Как правило, это делается до и после считывания статистики и вычитания из счетчика Before, чтобы получить общее количество выполненных операций.

Например, приложение может вызвать **жетжетсреадстатс** один раз, чтобы получить начальное считывание статистики для текущего потока. Затем можно вызвать функцию [жетмове](./jetmove-function.md) с параметром *CRowset* , имеющим значение JET_MoveNext, чтобы перейти к следующей записи индекса в индексе. Затем можно вызвать **жетжетсреадстатс** еще раз, чтобы получить еще одно считывание статистики потока. Затем можно вычесть счетчик Кпажереференцед из второго считывания из первого. Результатом будет число страниц базы данных, на которые ссылается ядро СУБД для выполнения операции [жетмове](./jetmove-function.md) .

Статистика для каждого потока накапливается в течение времени существования этого потока. Статистика сбрасывается, если библиотека DLL ядра СУБД выгружается из хост-процесса.

Структура [JET_THREADSTATS](./jet-threadstats-structure.md) , скорее всего, будет расширена в будущем, чтобы она содержала больше статистики. Новая статистика будет добавлена в конец структуры и может быть извлечена с увеличением размера выходного буфера. Наличие дополнительной статистики может быть выведено с помощью большего значения Кбструкт.

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008.</p></td>
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
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_THREADSTATS](./jet-threadstats-structure.md)  
[жетмове](./jetmove-function.md)
