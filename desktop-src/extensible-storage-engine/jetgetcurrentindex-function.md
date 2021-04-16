---
description: Дополнительные сведения о функции Жетжеткуррентиндекс
title: Функция Жетжеткуррентиндекс
TOCTitle: JetGetCurrentIndex Function
ms:assetid: 9db3b875-0b95-4027-9742-c36d2d7e64cf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294041(v=EXCHG.10)
ms:contentKeyID: 32765642
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCurrentIndexW
- JetGetCurrentIndex
- JetGetCurrentIndexA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3337ddaefbea803a137ad8366d2e3df665bacd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712417"
---
# <a name="jetgetcurrentindex-function"></a>Функция Жетжеткуррентиндекс


_**Применимо к:** Windows | Windows Server_

## <a name="jetgetcurrentindex-function"></a>Функция Жетжеткуррентиндекс

Функция **жетжеткуррентиндекс** определяет имя текущего индекса данного курсора. Это имя также используется для повторного выбора этого индекса в качестве текущего индекса с помощью [жетсеткуррентиндекс](./jetsetcurrentindex-function.md). Его также можно использовать для обнаружения свойств этого индекса с помощью [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md).

```cpp
    JET_ERR JET_API JetGetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_PSTR szIndexName,
      __in          unsigned long cchIndexName
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*сзиндекснаме*

Выходной буфер, который получает имя текущего индекса курсора.

*кчиндекснаме*

Максимальный размер в символах выходного буфера.

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>Операция успешно завершена, но выходной буфер слишком мал для получения полного имени индекса.</p>
<p>Выходной буфер заполнен как часть имени индекса, которая будет соответствовать. Если выходной буфер имеет длину по крайней мере один символ, то строка в этом выходном буфере будет завершаться нулем.</p>
<p><strong>Примечание  </strong> . Эта ошибка не будет возвращена, если Кчиндекснаме равен нулю. Дополнительные сведения см. в разделе "Примечания".</p></td>
</tr>
</tbody>
</table>


В случае успешного выполнения в выходном буфере будет возвращено имя текущего индекса данного курсора. Если возвращается значение JET_wrnBufferTruncated, то выходной буфер будет содержать столько имен индексов, сколько будет помещаться в предоставленное пространство. Если выходной буфер имеет длину по крайней мере один символ, то строка, возвращаемая в этом буфере, будет завершаться нулем. Изменение состояния базы данных не выполняется.

В случае сбоя состояние выходного буфера будет не определено. Изменение состояния базы данных не выполняется.

#### <a name="remarks"></a>Комментарии

Если текущий индекс для курсора отсутствует, возвращается пустая строка. Это может произойти, если курсор находится на кластеризованном индексе таблицы, а первичный индекс не определен. Этот индекс известен как последовательный индекс таблицы и не имеет определения. В любом случае установка текущего индекса в пустую строку с помощью [жетсеткуррентиндекс](./jetsetcurrentindex-function.md) выберет кластеризованный индекс независимо от наличия первичного определения индекса.

В этой функции есть важная ошибка, которая присутствует во всех выпусках. Если выходной буфер слишком мал для получения всего имени индекса, а выходной буфер является по крайней мере одним символом длиной, то JET_wrnBufferTruncated не будет возвращен. Вместо этого будет возвращено JET_errSuccess. Чтобы избежать этой проблемы, выходной буфер должен всегда иметь длину не менее JET_cbNameMost + 1 (65) символов.

#### <a name="requirements"></a>Требования

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
<td><p>Реализуется как <strong>жетжеткуррентиндексв</strong> (Юникод) и <strong>жетжеткуррентиндекса</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md)  
[жетсеткуррентиндекс](./jetsetcurrentindex-function.md)
