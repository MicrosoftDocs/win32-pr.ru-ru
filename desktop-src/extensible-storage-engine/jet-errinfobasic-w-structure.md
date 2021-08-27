---
description: 'Дополнительные сведения: структура JET_ERRINFOBASIC_W'
title: Структура JET_ERRINFOBASIC_W
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: c02d9f8081040293bd154137163e13cc9d313a32
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984037"
---
# <a name="jet_errinfobasic_w-structure"></a>Структура JET_ERRINFOBASIC_W


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_errinfobasic_w-structure"></a>Структура JET_ERRINFOBASIC_W

Структура **JET_ERRINFOBASIC_W** определяет данные, возвращаемые методом [жетжетерроринфо ()](./jetgeterrorinfow-function.md) при передаче JET_ErrorInfoSpecificErr инфолевел.

примечание. эта документация основана на предварительном выпуске расширяемого механизма служба хранилища. Эта информация может быть изменена.

```cpp
typedef struct { 
    unsigned long cbStruct; 
    JET_ERR errValue; 
    JET_ERRCAT errcatMostSpecific; 
    unsigned char rgCategoricalHierarchy[8]; 
    unsigned long lSourceLine; 
    WCHAR rgszSourceFile[64]; 
} JET_ERRINFOBASIC_W;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер структуры в байтах. Он должен иметь значение sizeof (JET_ERRINFOBASIC).

**еррвалуе**

Вычисленное значение ошибки, переданное для аргумента *пвресулт* в [жетжетерроринфо ()](./jetgeterrorinfow-function.md).

**ерркатмостспеЦифик**

Константа нижнего уровня [JET_ERRCAT](./jet-errcat.md) , связанная с ошибкой; Это значит, что категория конечного уровня в иерархии категорий задокументирована в [JET_ERRCAT](./jet-errcat.md).

**Ргкатегорикалхиерарчи \[ 8\]**

Иерархия категорий ошибок, связанных с ошибкой. Расположение 0 является самым высоким уровнем в иерархии [JET_ERRCAT](./jet-errcat.md), а остальные являются подкатегориями до тех пор, пока не будет задана наиболее конкретная категория, после чего все категории будут JET_errcatUnknownы.

**лсаурцелине**

Зарезервировано.

**Ргсзсаурцефиле \[ 64\]**

Зарезервировано.

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>Требуется Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows 8 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 

