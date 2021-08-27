---
description: 'Дополнительные сведения: структура JET_ENUMCOLUMNID'
title: Структура JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID Structure
ms:assetid: 5480ebf1-4fc9-49b5-bbb3-12542b86c8f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269251(v=EXCHG.10)
ms:contentKeyID: 32765553
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be9b25f989998450808ea78d99a5b96c2d4c4dc2
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984187"
---
# <a name="jet_enumcolumnid-structure"></a>Структура JET_ENUMCOLUMNID


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_enumcolumnid-structure"></a>Структура JET_ENUMCOLUMNID

Структура **JET_ENUMCOLUMNID** перечисляет конкретный набор столбцов и, при необходимости, конкретный набор нескольких значений для этих столбцов при использовании функции [жетенумератеколумнс](./jetenumeratecolumns-function.md) . [Жетенумератеколумнс](./jetenumeratecolumns-function.md) возвращает массив структур **JET_ENUMCOLUMNID** .

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      unsigned long ctagSequence;
      unsigned long* rgtagSequence;
    } JET_ENUMCOLUMNID;
```

### <a name="members"></a>Элементы

**columnid**

Идентификатор столбца для перечисления.

Если идентификатор столбца равен 0 (нулю), то перечисление этого столбца пропускается, а соответствующая область в выходном массиве [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) структур будет создана с состоянием столбца JET_wrnColumnSkipped.

**ктагсекуенце**

При необходимости определяет массив значений столбца (по одному индексу) для перечисления по указанному ИДЕНТИФИКАТОРу столбца.

Если **ктагсекуенце** имеет значение 0 (ноль), то **ргтагсекуенце** игнорируется и все значения столбцов для указанного идентификатора столбца будут перечислены.

Если элемент **ргтагсекуенце** имеет значение 0 (ноль), то перечисление этого значения столбца (с помощью индекса, начинающегося с единицы) будет пропущено. Соответствующий слот в выходном массиве структуры **JET_ENUMCOLUMNID** будет создан со значением состояния столбца JET_wrnColumnSkipped.

**ргтагсекуенце**

Массив индексов, отсчитываемый от единицы, в массиве значений столбцов для данного столбца. Единственный элемент — это **итагсекуенце** , который определен в [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md). **Итагсекуенце** 0 (ноль) означает "Skip". **Итагсекуенце** 1 означает возврат значения первого столбца столбца, 2 — второй и т. д.

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_COLUMNID](./jet-columnid.md)  
[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNID]()  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[жетенумератеколумнс](./jetenumeratecolumns-function.md)
