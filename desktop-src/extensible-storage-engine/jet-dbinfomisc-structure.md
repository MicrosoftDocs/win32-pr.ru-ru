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
ms.openlocfilehash: 7d7861e558bbf6a1938d252a52e7bb781068a331
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476870"
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


| <p>Улверсион, Улупдате =</p> | <p>Значение</p> | 
|------------------------------|----------------|
| <p>0x620, 0</p> | <p>Исходный формат бета-версии операционной системы (4/22/97).</p> | 
| <p>0x620, 1</p> | <p>Добавление столбцов в каталог для условного индексирования и старых (5/29/97).</p> | 
| <p>0x620, 2</p> | <p>Добавьте флаг Флокализедтекст в IDB (6/5/97).</p> | 
| <p>0x620, 3</p> | <p>Добавьте SPLIT_BUFFER корневые страницы дерева пространства (10/30/97).</p> | 
| <p>0x620, 2</p> | <p>Отмените изменения, чтобы ESE97 оставалась совместимыми с прямыми (1/28/98).</p> | 
| <p>0x620, 3</p> | <p>Добавьте новые столбцы с тегами в каталог ("Каллбаккдата" и "КаллбаккдепенденЦиес").</p> | 
| <p>0x620, 4</p> | <p>Поддержка SLV: Сигнслв, Фслвексистс в заголовке базы данных (5/5/98).</p> | 
| <p>0x620, 5</p> | <p>Новое дерево пространства SLV (5/29/98).</p> | 
| <p>0x620, 6</p> | <p>Схема пространства SLV (10/12/98).</p> | 
| <p>0x620, 7</p> | <p>4-байтовый ИДКССЕГ (12/10/98).</p> | 
| <p>0x620, 8</p> | <p>Новый формат столбца шаблона (1/25/99).</p> | 
| <p>0x620, 9</p> | <p>Отсортированные столбцы шаблона (6/24/99).</p> | 
| <p>0x623, 0</p> | <p>Новый диспетчер пространства (5/15/99).</p> | 



**сигндб**

Подпись базы данных (включая время создания). Эта структура составляет 28 байт.

**дбстате**

Это состояние базы данных.

Для этого элемента доступны следующие параметры.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_dbstateJustCreated<br />1</p> | <p>База данных была только что создана.</p> | 
| <p>JET_dbstateDirtyShutdown<br />2</p> | <p>Для использования или перемещаемой базы данных необходимо выполнить жесткое или мягкое восстановление. Одна из них не должна пытаться переместить базы данных в этом состоянии.</p> | 
| <p>JET_dbstateCleanShutdown<br />3</p> | <p>База данных находится в чистом состоянии. База данных может быть присоединена без каких бы то ни было файлов журнала.</p> | 
| <p>JET_dbstateBeingConverted<br />4</p> | <p>Выполняется обновление базы данных.</p> | 
| <p>JET_dbstateForceDetach<br />5</p> | <p>Внутренний.</p> | 



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


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[жетжетдатабасеинфо](./jetgetdatabaseinfo-function.md)  
[жетжетдатабасефилеинфо](./jetgetdatabasefileinfo-function.md)
