---
title: Сообщение TB_GETINSERTMARK (Коммктрл. h)
description: Извлекает текущую метку вставки для панели инструментов.
ms.assetid: b22770a4-e859-451d-a726-279bbc49b984
keywords:
- Элементы управления Windows для TB_GETINSERTMARK сообщений
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
ms.openlocfilehash: b45a4cafbd49c709e9ca5b8e9afeda51323de491
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071248"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_СЕТИНСЕРТМАРК ТБ**](tb-setinsertmark.md)
</dt> </dl>

 

 





