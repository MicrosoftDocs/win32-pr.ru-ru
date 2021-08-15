---
description: 'Дополнительные сведения: структура JET_DBINFOMISC'
title: Структура JET_DBINFOMISC
TOCTitle: JET_DBINFOMISC Structure
ms:assetid: ff287087-35b8-495e-9922-418ec2439e19
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294147(v=EXCHG.10)
ms:contentKeyID: 32765761
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
ms.openlocfilehash: 6c7684fe69cff252d75ea2cceb0872044e8a011b39e88375d6eb576cb1b5360e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118486337"
---
# <a name="jet_dbinfomisc-structure"></a>Структура JET_DBINFOMISC


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_dbinfomisc-structure"></a>Структура JET_DBINFOMISC

Структура **JET_DBINFOMISC** содержит различные сведения о базе данных. Это сведения, содержащиеся в заголовке базы данных.

```cpp
    typedef struct {
      unsigned long ulVersion;
      unsigned long ulUpdate;
      JET_SIGNATURE signDb;
      unsigned long dbstate;
      JET_LGPOS lgposConsistent;
      JET_LOGTIME logtimeConsistent;
      JET_LOGTIME logtimeAttach;
      JET_LGPOS lgposAttach;
      JET_LOGTIME logtimeDetach;
      JET_LGPOS lgposDetach;
      JET_SIGNATURE signLog;
      JET_BKINFO bkinfoFullPrev;
      JET_BKINFO bkinfoIncPrev;
      JET_BKINFO bkinfoFullCur;
      unsigned long fShadowingDisabled;
      unsigned long fUpgradeDb;
      unsigned long dwMajorVersion;
      unsigned long dwMinorVersion;
      unsigned long dwBuildNumber;
      long lSPNumber;
      unsigned long cbPageSize;
    } JET_DBINFOMISC;
```

### <a name="members"></a>Элементы

**улверсион**

Собственная версия ядра СУБД, создавшая базу данных. См. раздел [жетжетверсион](./jetgetversion-function.md) to получение собственной версии для текущего ядра СУБД.

**улупдате**

Отслеживает добавочные обновления формата базы данных с обратной совместимостью.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Улверсион, Улупдате =</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0x620, 0</p></td>
<td><p>Исходный формат бета-версии операционной системы (4/22/97).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 1</p></td>
<td><p>Добавление столбцов в каталог для условного индексирования и старых (5/29/97).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 2</p></td>
<td><p>Добавьте флаг Флокализедтекст в IDB (6/5/97).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 3</p></td>
<td><p>Добавьте SPLIT_BUFFER корневые страницы дерева пространства (10/30/97).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 2</p></td>
<td><p>Отмените изменения, чтобы ESE97 оставалась совместимыми с прямыми (1/28/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 3</p></td>
<td><p>Добавьте новые столбцы с тегами в каталог ( &quot; каллбаккдата &quot; и &quot; каллбаккдепенденЦиес &quot; ).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 4</p></td>
<td><p>Поддержка SLV: Сигнслв, Фслвексистс в заголовке базы данных (5/5/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 5</p></td>
<td><p>Новое дерево пространства SLV (5/29/98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 6</p></td>
<td><p>Схема пространства SLV (10/12/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 7</p></td>
<td><p>4-байтовый ИДКССЕГ (12/10/98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 8</p></td>
<td><p>Новый формат столбца шаблона (1/25/99).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 9</p></td>
<td><p>Отсортированные столбцы шаблона (6/24/99).</p></td>
</tr>
<tr class="odd">
<td><p>0x623, 0</p></td>
<td><p>Новый диспетчер пространства (5/15/99).</p></td>
</tr>
</tbody>
</table>


**сигндб**

Подпись базы данных (включая время создания). Эта структура составляет 28 байт.

**дбстате**

Это состояние базы данных.

Для этого элемента доступны следующие параметры.

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
<td><p>JET_dbstateJustCreated<br />
1</p></td>
<td><p>База данных была только что создана.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbstateDirtyShutdown<br />
2</p></td>
<td><p>Для использования или перемещаемой базы данных необходимо выполнить жесткое или мягкое восстановление. Одна из них не должна пытаться переместить базы данных в этом состоянии.</p></td>
</tr>
<tr class="odd">
<td><p>JET_dbstateCleanShutdown<br />
3</p></td>
<td><p>База данных находится в чистом состоянии. База данных может быть присоединена без каких бы то ни было файлов журнала.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbstateBeingConverted<br />
4</p></td>
<td><p>Выполняется обновление базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_dbstateForceDetach<br />
5</p></td>
<td><p>Внутренний.</p></td>
</tr>
</tbody>
</table>


**лгпосконсистент**

Значение null, если база данных находится в состоянии "грязный". Это расположение журнала, использованное при последнем переключении базы данных в состояние чистого отключения.

**логтимеконсистент**

Значение null, если база данных находится в состоянии "грязный". Это время последнего перевода базы данных в состояние чистого отключения.

**логтимеаттач**

Время последнего подключения базы данных к [жетаттачдатабасе](./jetattachdatabase-function.md).

**лгпосаттач**

Расположение журнала, которое использовалось в последний раз при присоединении базы данных с помощью [жетаттачдатабасе](./jetattachdatabase-function.md).

**логтимедетач**

Время последней отсоединения базы данных с [жетдетачдатабасе](./jetdetachdatabase-function.md).

**лгпосдетач**

Расположение журнала, которое использовалось в последний раз при отсоединении базы данных с [жетдетачдатабасе](./jetdetachdatabase-function.md).

**сигнлог**

Поддерживает инфраструктуру ESE и не может использоваться в коде.

**бкинфофуллпрев**

Поддерживает инфраструктуру ESE и не может использоваться в коде.

**бкинфоинкпрев**

Поддерживает инфраструктуру ESE и не может использоваться в коде.

**бкинфофуллкур**

Поддерживает инфраструктуру ESE и не может использоваться в коде.

**фшадовингдисаблед**

Поддерживает инфраструктуру ESE и не может использоваться в коде.

**фупградедб**

Поддерживает инфраструктуру ESE и не может использоваться в коде.

**двмажорверсион**

представляет Windows NT номера версий при обновлении индексов баз данных. Используется для обновления индексов.

**двминорверсион**

представляет Windows NT номера версий при обновлении индексов баз данных. Используется для обновления индексов.

**двбуилднумбер**

представляет Windows NT номера версий при обновлении индексов баз данных. Используется для обновления индексов.

**лспнумбер**

представляет Windows NT номера версий при обновлении индексов баз данных. Используется для обновления индексов.

**кбпажесизе**

Размер страницы базы данных. 0 означает, что размер страницы равен 4 КБ.

Это значение извлекается, только если JET_DbInfoMisc передано в [жетжетдатабасеинфо](./jetgetdatabaseinfo-function.md) или [жетжетдатабасефилеинфо](./jetgetdatabasefileinfo-function.md).

### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Сервер</strong></p></td>
<td><p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[жетжетдатабасеинфо](./jetgetdatabaseinfo-function.md)  
[жетжетдатабасефилеинфо](./jetgetdatabasefileinfo-function.md)
