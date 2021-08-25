---
description: Сообщение TAPI LINE \_ аппневкаллхуб отправляется для информирования приложения о создании нового концентратора вызовов.
ms.assetid: cf693d95-9abb-4999-81b6-7d2aa06d0f58
title: Сообщение LINE_APPNEWCALLHUB (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bf413f16270ba54fd7447cc0c41c040759edd699c995eac79314b9961486ce5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905911"
---
# <a name="line_appnewcallhub-message"></a>Строка \_ сообщения аппневкаллхуб

Сообщение TAPI **Line \_ аппневкаллхуб** отправляется для информирования приложения о создании нового концентратора вызовов.


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

Уровень отслеживания в новом концентраторе, как определено одной из [**\_ констант линекаллхубтраккинг**](linecallhubtracking--constants.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Это сообщение исходит от TAPI, а не от поставщика услуг, поэтому соответствующее сообщение ТСПИ отсутствует.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,2<br/>                                                      |
| Заголовок<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




