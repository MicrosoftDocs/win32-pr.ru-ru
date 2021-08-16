---
title: Сообщение PSM_SETNEXTTEXT (Пршт. h)
description: Задает текст кнопки "Далее" в мастере. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит сетнексттекст.
ms.assetid: 4608425e-1724-4d0b-b0f6-9fec147a85f6
keywords:
- элементы управления Windows сообщений PSM_SETNEXTTEXT
topic_type:
- apiref
api_name:
- PSM_SETNEXTTEXT
- PSM_SETNEXTTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d177acb2f2c96e12f5dc4b460ee88149ad81f9b4f79cc3505f776d8f1f92551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410084"
---
# <a name="psm_setnexttext-message"></a>\_Сообщение ПСМ сетнексттекст

Задает текст кнопки " **Далее** " в мастере. Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ сетнексттекст**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на буфер, содержащий текст.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет осмысленных возвращаемых значений.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ПСМ \_ СЕТНЕКСТТЕКСТВ** (Юникод)<br/>                                         |



 

 





