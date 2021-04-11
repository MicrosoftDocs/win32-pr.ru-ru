---
title: Сообщение TB_INSERTBUTTON (Коммктрл. h)
description: Вставляет кнопку на панель инструментов.
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- Элементы управления Windows для TB_INSERTBUTTON сообщений
topic_type:
- apiref
api_name:
- TB_INSERTBUTTON
- TB_INSERTBUTTONA
- TB_INSERTBUTTONW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e08eed328a99d4a8927a7e09084bf122f2e4e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135575"
---
# <a name="tb_insertbutton-message"></a>\_Сообщение ИНСЕРТБУТТОН ТБ

Вставляет кнопку на панель инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс кнопки. Сообщение вставляет кнопку Создать слева от этой кнопки.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) , содержащую сведения о вставляемой кнопке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТБ \_ ИНСЕРТБУТТОНВ** (Юникод) и **ТБ \_ инсертбуттона** (ANSI)<br/>           |



 

 





