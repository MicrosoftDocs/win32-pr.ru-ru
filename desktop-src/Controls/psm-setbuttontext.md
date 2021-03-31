---
title: Сообщение PSM_SETBUTTONTEXT (Пршт. h)
description: Задает текст на кнопке в мастере Aero. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит сетбуттонтекст.
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- Элементы управления Windows для PSM_SETBUTTONTEXT сообщений
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
ms.openlocfilehash: 41a0b55f73fc7084e89f54c1e741d12000b0f949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071516"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ПСМ \_ СЕТБУТТОНТЕКСТВ** (Юникод)<br/>                                       |



 

 





