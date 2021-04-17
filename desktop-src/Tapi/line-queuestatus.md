---
description: Сообщение LINE \_ QUEUESTATUS отправляется при изменении состояния ACD-очереди в обработчике агента, для которого приложение в настоящий момент имеет открытую строку. Это сообщение создается с помощью функции Линепроксимессаже.
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: Сообщение LINE_QUEUESTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a89785b92009a7531ae693545febaf153cf19bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688925"
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
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**линепроксимессаже**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




