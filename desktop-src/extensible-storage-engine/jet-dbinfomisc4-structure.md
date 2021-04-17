---
description: 'Дополнительные сведения: структура JET_DBINFOMISC4'
title: Структура JET_DBINFOMISC4
TOCTitle: JET_DBINFOMISC4 Structure
ms:assetid: 63f446bc-98b7-4a60-9575-d6b4757fb0fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269269(v=EXCHG.10)
ms:contentKeyID: 32765571
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
ms.openlocfilehash: 1e2242b1e419c4834a2a1843165e1c9a2ad1f2de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682443"
---
# <a name="jet_dbinfomisc4-structure"></a>Структура JET_DBINFOMISC4


_**Применимо к:** Windows | Windows Server_

## <a name="jet_dbinfomisc4-structure"></a>Структура JET_DBINFOMISC4

Структура **JET_DBINFOMISC4** содержит различные сведения о базе данных. Это сведения, содержащиеся в заголовке базы данных.

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
      unsigned long genMinRequired;
      unsigned long genMaxRequired;
      JET_LOGTIME logtimeGenMaxCreate;
      unsigned long ulRepairCount;
      JET_LOGTIME logtimeRepair;
      unsigned long ulRepairCountOld;
      unsigned long ulECCFixSuccess;
      JET_LOGTIME logtimeECCFixSuccess;
      unsigned long ulECCFixSuccessOld;
      unsigned long ulECCFixFail;
      JET_LOGTIME logtimeECCFixFail;
      unsigned long ulECCFixFailOld;
      unsigned long ulBadChecksum;
      JET_LOGTIME logtimeBadChecksum;
      unsigned long ulBadChecksumOld;
      unsigned long genCommitted;
      JET_BKINFO bkinfoCopyPrev;
      JET_BKINFO bkinfoDiffPrev;
    } JET_DBINFOMISC4;
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
<td><p>0x620,</p></td>
<td><p>Основа Объединенного кода (3/26/2003).</p></td>
</tr>
<tr class="even">
<td><p>0x620, B</p></td>
<td><p>Новый формат контрольной суммы (1/08/2004).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, C</p></td>
<td><p>Увеличена максимальная длина ключа до 1000/2000 байт для 4/8 КБ страниц (1/15/2004).</p></td>
</tr>
<tr class="even">
<td><p>0x620, г</p></td>
<td><p>Указания пространства каталога, space_header. v2 (7/15/2007).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, E</p></td>
<td><p>Добавьте новый формат узла или экстента в диспетчер пространства, используйте его для зарезервированных пулов пространства (8/9/2007).</p></td>
</tr>
<tr class="even">
<td><p>0x620, F</p></td>
<td><p>Сжатие для внутренних значений long (10/30/2007).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 10</p></td>
<td><p>Сжатие для отдельных длинных значений (12/05/2007).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 11</p></td>
<td><p>Новый размер фрагмента LV для больших страниц (12/29/2007).</p></td>
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

Представляет номера версий Windows NT при обновлении индексов баз данных. Используется для обновления индексов.

**двминорверсион**

Представляет номера версий Windows NT при обновлении индексов баз данных. Используется для обновления индексов.

**двбуилднумбер**

Представляет номера версий Windows NT при обновлении индексов баз данных. Используется для обновления индексов.

**лспнумбер**

Представляет номера версий Windows NT при обновлении индексов баз данных. Используется для обновления индексов.

**кбпажесизе**

Размер страницы базы данных. 0 означает, что размер страницы равен 4 КБ.

Это значение извлекается, только если JET_DbInfoMisc передано в [жетжетдатабасеинфо](./jetgetdatabaseinfo-function.md) или [жетжетдатабасефилеинфо](./jetgetdatabasefileinfo-function.md).

**женминрекуиред**

Представляет минимальное поколение журналов, необходимое для воспроизведения журналов. Обычно это используется в качестве создания контрольной точки.

**женмаксрекуиред**

Представляет максимальное создание журнала, необходимое для воспроизведения журналов.

**логтимеженмакскреате**

Представляет дату и время создания файла журнала Женмакс.

**улрепаиркаунт**

Количество раз, когда в этой базе данных было вызвано восстановление.

**логтимерепаир**

Представляет дату и время выполнения последнего восстановления.

**улрепаиркаунтолд**

Количество выполнений восстановления в этой базе данных до последней дефрагментации.

**улеккфикссукцесс**

Количество случаев, когда одна разрядная ошибка была исправлена и привела к хорошей странице.

**логтимиккфикссукцесс**

Представляет дату и время исправления последней ошибки в битах, что привело к хорошей странице.

**улеккфикссукцессолд**

Представляет количество случаев, когда одна разрядная ошибка была исправлена и привела к хорошей странице до последнего восстановления.

**улеккфиксфаил**

Количество случаев, когда одна разрядная ошибка была исправлена и привела к поврежденной странице.

**логтимиккфиксфаил**

Представляет дату и время исправления последней битовой ошибки, которая привела к поврежденной странице.

**улеккфиксфаилолд**

Количество случаев, когда одна разрядная ошибка была исправлена и привела к поврежденной странице до последнего восстановления.

**улбадчекксум**

Количество случаев, когда обнаружена Неисправимая ошибка ECC/CHECKSUM.

**логтимебадчекксум**

Представляет дату и время обнаружения последней неисправимой ошибки ECC/CHECKSUM.

**улбадчекксумолд**

Количество случаев, когда ошибка неисправимой ошибки/контрольной суммы была обнаружена перед последним восстановлением.

**женкоммиттед**

Максимальное число поколений журналов, зафиксированных в базе данных. Обычно создается текущая версия журнала.

**бкинфокопипрев**

Последняя успешная резервная копия копии.

**бкинфодиффпрев**

Последняя успешная разностная резервная копия. Это значение сбрасывается при установке Бкинфофуллпрев.

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

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[жетжетдатабасеинфо](./jetgetdatabaseinfo-function.md)  
[жетжетдатабасефилеинфо](./jetgetdatabasefileinfo-function.md)
