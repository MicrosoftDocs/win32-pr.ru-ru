---
title: Сообщение HDM_CLEARFILTER (Коммктрл. h)
description: Очищает фильтр для данного элемента управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса клеарфилтер.
ms.assetid: 74c0265e-68d1-4414-8fd9-20f5f041d4b4
keywords:
- Элементы управления Windows для HDM_CLEARFILTER сообщений
topic_type:
- apiref
api_name:
- HDM_CLEARFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b1184432517761a567cd76bdd488e4593b1e999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136439"
---
# <a name="hdm_clearfilter-message"></a>\_Сообщение КЛЕАРФИЛТЕР HDM

Очищает фильтр для данного элемента управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ клеарфилтер**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Значение столбца, указывающее, какой фильтр следует очистить.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает целое число. **LResult** преобразуется в целое число, которое указывает **true**(1) или **false**(0).

## <a name="remarks"></a>Комментарии

Если значение столбца указано как-1, удаляются все фильтры, а уведомление [ХДН \_ филтерчанже](hdn-filterchange.md) отправляется только один раз.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Клеараллфилтерс заголовка**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)
</dt> </dl>

 

 





