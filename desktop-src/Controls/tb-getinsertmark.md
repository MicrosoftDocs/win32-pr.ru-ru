---
title: Сообщение TB_GETINSERTMARK (Коммктрл. h)
description: Извлекает текущую метку вставки для панели инструментов.
ms.assetid: b22770a4-e859-451d-a726-279bbc49b984
keywords:
- элементы управления Windows сообщений TB_GETINSERTMARK
topic_type:
- apiref
api_name:
- TB_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ee4a51d3110a99013ed26ccb1f2c102e7821873e63dd419b33e92636a1b655
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918754"
---
# <a name="tb_getinsertmark-message"></a>\_Сообщение ЖЕТИНСЕРТМАРК ТБ

Извлекает текущую метку вставки для панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**тбинсертмарк**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) , которая получает метку вставки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Всегда возвращает **значение true**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_СЕТИНСЕРТМАРК ТБ**](tb-setinsertmark.md)
</dt> </dl>

 

 





