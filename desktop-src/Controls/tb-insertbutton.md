---
title: Сообщение TB_INSERTBUTTON (Коммктрл. h)
description: Вставляет кнопку на панель инструментов.
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- элементы управления Windows сообщений TB_INSERTBUTTON
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
ms.openlocfilehash: 909a4e039450e001757cd054cf27a15d24af392d6a55841c2857e2312252145c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829655"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТБ \_ ИНСЕРТБУТТОНВ** (Юникод) и **ТБ \_ инсертбуттона** (ANSI)<br/>           |



 

 





