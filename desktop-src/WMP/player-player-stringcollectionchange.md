---
title: Событие Player. Стрингколлектиончанже
description: Событие Стрингколлектиончанже возникает при изменении коллекции строк. | Событие Player. Стрингколлектиончанже
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- Проигрыватель Windows Media Event Стрингколлектиончанже
- Проигрыватель Windows Media Event Стрингколлектиончанже, класс Player
- Класс проигрывателя Windows Media Player, событие Стрингколлектиончанже
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
ms.openlocfilehash: e6a61b8e1e09e749579f323d506371138b0d9b59
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424094"
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
| 0      | Неизвестна. (Недопустимое значение)       |
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

## <a name="remarks"></a>Комментарии

**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Объект StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





