---
description: Сообщение ТСПИ LINE \_ косинфо заставляет TAPI запустить событие QoS. Дополнительные сведения см. в разделе Иткосевент.
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: Сообщение LINE_QOSINFO (Тспи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f0e6273eb31447f0e0c9543dfa191a25869fa08f05be8a5c639ceb101deff47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873324"
---
# <a name="line_qosinfo-message"></a>Строка \_ сообщения косинфо

Сообщение ТСПИ **Line \_ КОСИНФО** заставляет TAPI запустить событие QoS. Дополнительные сведения см. в разделе [**иткосевент**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) .


```C++
        
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хтлине* 
</dt> <dd>

Маркер TAPI для линии.

</dd> <dt>

*хткалл* 
</dt> <dd>

Маркер TAPI для вызова.

</dd> <dt>

*двмсг* 
</dt> <dd>

Строка значения \_ косинфо.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Член перечислителя [**\_ событий QoS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) , определяющий тип события.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Константа [типа мультимедиа](./tapiprotocol--constants.md) , определяющая носитель вызова, связанного с этим событием.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,2<br/>                                                      |
| Заголовок<br/>       | <dl> <dt>Тспи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**событие качества обслуживания \_**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[**иткосевент**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

