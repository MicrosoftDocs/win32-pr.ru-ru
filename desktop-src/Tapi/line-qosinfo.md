---
description: Сообщение ТСПИ LINE \_ косинфо заставляет TAPI запустить событие QoS. Дополнительные сведения см. в разделе Иткосевент.
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: Сообщение LINE_QOSINFO (Тспи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35ff19601ab6acd9a3d8e8aebf1e59b06a4f17e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675678"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,2<br/>                                                      |
| Header<br/>       | <dl> <dt>Тспи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**событие качества обслуживания \_**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[**иткосевент**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

