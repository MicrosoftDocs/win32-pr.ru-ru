---
title: Сообщение PSM_SETBUTTONTEXT (Пршт. h)
description: Задает текст на кнопке в мастере Aero. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит сетбуттонтекст.
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- элементы управления Windows сообщений PSM_SETBUTTONTEXT
topic_type:
- apiref
api_name:
- PSM_SETBUTTONTEXT
- PSM_SETBUTTONTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feac193beef3149140447a38c0be00b7f4fa0c1c1b28e10a5d7de2203ba21cec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088594"
---
# <a name="psm_setbuttontext-message"></a>\_Сообщение ПСМ сетбуттонтекст

Задает текст на кнопке в мастере Aero. Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ сетбуттонтекст**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Одно из следующих значений, задающее кнопку, для которой задан текст.



| Значение                                                                                                                                                                                 | Значение                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**ПСВИЗБ \_ назад**</dt> </dl>                               | Кнопка " **назад** ".<br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**ПСВИЗБ \_ Отмена**</dt> </dl>                         | Кнопка **Отмена** .<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**ПСВИЗБ \_ дисабледфиниш**</dt> </dl> | Кнопка **"Готово"** .<br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**\_Завершение псвизб**</dt> </dl>                         | Кнопка **"Готово"** .<br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**ПСВИЗБ \_ Далее**</dt> </dl>                               | Кнопка **Далее** .<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Заданный текст.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ПСМ \_ СЕТБУТТОНТЕКСТВ** (Юникод)<br/>                                       |



 

 





