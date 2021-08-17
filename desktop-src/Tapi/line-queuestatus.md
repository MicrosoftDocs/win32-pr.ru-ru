---
description: Сообщение LINE \_ QUEUESTATUS отправляется при изменении состояния ACD-очереди в обработчике агента, для которого приложение в настоящий момент имеет открытую строку. Это сообщение создается с помощью функции Линепроксимессаже.
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: Сообщение LINE_QUEUESTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b336a8239e31e5c0bcc70de747cbb48a2028c85e67f44a3e45032f02b37065d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975534"
---
# <a name="line_queuestatus-message"></a>Строка \_ сообщения QUEUESTATUS

Сообщение **Line \_ QUEUESTATUS** отправляется при изменении состояния ACD-очереди в обработчике агента, для которого приложение в настоящий момент имеет открытую строку. Это сообщение создается с помощью функции [**линепроксимессаже**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .


```C++
        
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двдевице* 
</dt> <dd>

Маркер приложения для линейного устройства. Это связано с обработчиком агента.

</dd> <dt>

*двкаллбаккинстанце* 
</dt> <dd>

Экземпляр обратного вызова, указанный при открытии строки.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Идентификатор очереди, состояние которой изменилось.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Указывает состояние очереди, которое было изменено. Может быть одной или несколькими [**\_ константами линекуеуестатус**](linequeuestatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Зарезервировано. Задайте нулевое значение.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,2<br/>                                                      |
| Заголовок<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**линепроксимессаже**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




