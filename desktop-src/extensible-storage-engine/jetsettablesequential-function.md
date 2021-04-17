---
description: Дополнительные сведения о функции Жетсеттаблесекуентиал
title: Функция Жетсеттаблесекуентиал
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b633b348b712e446535054c5a39d2768236b7705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710932"
---
# <a name="jetsettablesequential-function"></a>Функция Жетсеттаблесекуентиал


_**Применимо к:** Windows | Windows Server_

## <a name="jetsettablesequential-function"></a>Функция Жетсеттаблесекуентиал

Функция **жетсеттаблесекуентиал** уведомляет ядро СУБД о том, что приложение сканирует весь текущий индекс, содержащий данный курсор. Следовательно, методы, используемые для доступа к данным индекса, будут настроены таким образом, чтобы сделать этот сценарий максимально быстрым.

**Windows XP:**  **Жетсеттаблесекуентиал** появился в Windows XP.

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*грбит*

Группа битов, задающих ноль или более следующих параметров.

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
<td><p>JET_bitPrereadForward</p></td>
<td><p>Этот параметр используется для индексирования в прямом направлении.</p>
<p><strong>Windows 7:</strong>  <strong>JET_bitPrereadForward</strong> введен в Windows 7.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitPrereadBackward</p></td>
<td><p>Этот параметр используется для индексации в обратном направлении.</p>
<p><strong>Windows 7:</strong>  <strong>JET_bitPrereadBackward</strong> введен в Windows 7.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были заморожены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p>
<p><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
</tbody>
</table>


Если эта функция выполнена, текущий индекс курсора оптимизирован для последовательного просмотра всего индекса. Изменение состояния базы данных не выполняется.

Если эта функция завершается неудачно, не выполняется никаких изменений в конфигурации курсора. Изменение состояния базы данных не выполняется.

#### <a name="remarks"></a>Комментарии

Если приложению требуется эффективно сканировать известное подмножество индекса, подобная оптимизация также выполняется при каждом создании диапазона индексов с помощью [жетсетиндексранже](./jetsetindexrange-function.md). Эта оптимизация доступна только в Windows XP и более поздних версиях.

Если приложению нужно эффективно сканировать неизвестное подмножество индекса, никакие действия не выполняются. Подсистема может автоматически обнаружить поведение при сканировании и будет получать данные заранее. Однако это поведение не так агрессивно.

Эта оптимизация обеспечит эффективную проверку первичного индекса и сделает проверку данных записи индекса вторичным индексом эффективной. При этом не выполняется проверка вторичного индекса при получении данных о неэффективном доступе к записям. Это обусловлено тем, что модуль не выполняет упреждающее чтение данных записи.

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista или Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008 или Windows Server 2003.</p></td>
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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетсетиндексранже](./jetsetindexrange-function.md)  
[жетстопсервице](./jetstopservice-function.md)
