---
description: Отображает сообщение об ошибке в всплывающей подсказке, связанной с элементом управления "сетевой адрес".
title: Сообщение NCM_DISPLAYERRORTIP (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5ECAB6C3-69FC-4f2a-A9E6-80BC37ED3119
api_name:
- NCM_DISPLAYERRORTIP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 046119c93ec6a80fcfcedbd562d04665d5642fd832f2385bab914cc732499e5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111474"
---
# <a name="ncm_displayerrortip-message"></a>\_Сообщение НКМ дисплайеррортип

Отображает сообщение об ошибке в всплывающей подсказке, связанной с элементом управления "сетевой адрес".


```C++
NCM_DISPLAYERRORTIP

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если это сообщение завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Отправка этого сообщения для вывода сообщения об ошибке, когда адрес, введенный в элементе управления, не проверяется по разрешенным типам сетевых адресов, заданным с помощью сообщения [**НКМ \_ сеталловтипе**](ncm-setallowtype.md) . Чтобы проверить адрес, используйте сообщение [**НКМ \_**](ncm-getaddress.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Шеллапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Нетаддр \_ дисплайеррортип**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)
</dt> </dl>

 

 




