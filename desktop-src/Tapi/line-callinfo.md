---
description: Сообщение TAPI LINE \_ каллинфо отправляется при изменении сведений о вызове указанного вызова. Приложение может вызвать Линежеткаллинфо для определения текущих сведений о вызовах.
ms.assetid: eb882409-6842-434e-9f93-61cf0c11d1d0
title: Сообщение LINE_CALLINFO (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6005ab5383816ead440f5a1a7d580bfaccb5c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688823"
---
# <a name="line_callinfo-message"></a>Строка \_ сообщения каллинфо

Сообщение TAPI **Line \_ каллинфо** отправляется при изменении сведений о вызове указанного вызова. Приложение может вызвать [**линежеткаллинфо**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) для определения текущих сведений о вызовах.


```C++
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдевице* 
</dt> <dd>

Маркер вызова.

</dd> <dt>

*двкаллбаккинстанце* 
</dt> <dd>

Экземпляр обратного вызова, указанный при открытии линии вызова.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Измененный элемент сведений о вызове. Может быть одной или несколькими [**\_ константами линекаллинфостате**](linecallinfostate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Не используется.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

**Строка сообщения \_ каллинфо** с указанием *нумовнерсинкр*, *нумовнерсдекр* и (или) *нуммониторсчанжед* отправляется в приложения, которые уже имеют обработчик для вызова. Это может быть результатом того, что другое приложение изменяет владельца или отслеживание на вызов с помощью [**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**линеклосе**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**линешутдовн**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**линесеткаллпривилеже**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**линежетневкаллс**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)и [**линежетконфрелатедкаллс**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls).

Эти **строки \_ каллинфо** сообщения не отправляются, если уведомление о новом вызове предоставляется в [**строке \_ каллстате**](line-callstate.md) , поскольку сведения о вызове уже отражают правильное количество владельцев и мониторов на момент \_ отправки строки каллстате сообщений. **Строка \_ Сообщения КАЛЛИНФО** также подавляются в случае, когда интерфейс TAPI предоставляет вызов для мониторинга через линекаллстате \_ неизвестный механизм.

> [!Note]  
> Приложение, которое вызывает изменение числа владельцев или мониторов (например, путем вызова [**линедеаллокатекалл**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) или [**линесеткаллпривилеже**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)), само по себе не получает сообщение о том, что изменение выполнено.

 

Сообщения **\_ каллинфо Line** не отправляются для вызова после того, как вызов перешел в состояние *простоя* . В частности, изменения в количестве владельцев и мониторов не отображаются, так как приложения отменяют выделение своих дескрипторов для неактивного вызова.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**линеклосе**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**линедеаллокатекалл**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[**линежеткаллинфо**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[**линежетконфрелатедкаллс**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[**линежетневкаллс**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)
</dt> <dt>

[**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**линесеткаллпривилеже**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)
</dt> <dt>

[**линешутдовн**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




