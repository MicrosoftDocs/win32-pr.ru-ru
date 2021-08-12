---
title: Событие Player. Стрингколлектиончанже
description: Событие Стрингколлектиончанже возникает при изменении коллекции строк. | Событие Player. Стрингколлектиончанже
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- проигрыватель Windows Media событий стрингколлектиончанже
- проигрыватель Windows Media событий стрингколлектиончанже, класс Player
- класс проигрывателя проигрыватель Windows Media, событие стрингколлектиончанже
topic_type:
- apiref
api_name:
- Player.StringCollectionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5012cd94c14532eb94eb452c9c7aa20d50ffb8a447c2d14f56e8c6df02456849
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572422"
---
# <a name="playerstringcollectionchange-event"></a>Событие Player. Стрингколлектиончанже

Событие Стрингколлектиончанже возникает при изменении коллекции строк.

## <a name="syntax"></a>Синтаксис


```JScript
Player.StringCollectionChange(
  pdispStringCollection,
  change,
  lCollectionIndex
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдиспстрингколлектион* 
</dt> <dd>

Измененный объект **StringCollection** .

</dd> <dt>

*change* 
</dt> <dd>

Число (Long), указывающее тип изменения, произошедшего в коллекции строк. Включает одно из следующих значений.



| Число | Описание                        |
|--------|------------------------------------|
| 0      | Неизвестно. (Недопустимое значение)       |
| 1      | Элемент был вставлен.              |
| 2      | Изменена коллекция строк.     |
| 3      | Элемент удален.               |
| 4      | Коллекция строк была удалена. |
| 5      | Начинается групповое обновление.        |
| 6      | Групповые обновления завершены.           |



 

</dd> <dt>

*лколлектиониндекс* 
</dt> <dd>

Число (Long), содержащее индекс измененного элемента коллекции строк.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

**проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Объект StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





