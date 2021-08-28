---
title: Сообщение PSM_ENABLEWIZBUTTONS (Пршт. h)
description: Включает или отключает любые стандартные кнопки в мастере Aero. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ енаблевизбуттонс.
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- элементы управления Windows сообщений PSM_ENABLEWIZBUTTONS
topic_type:
- apiref
api_name:
- PSM_ENABLEWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a677b596e57a55271224f5b22baac5d979e2806c20676065457aa47b8a66e527
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825877"
---
# <a name="psm_enablewizbuttons-message"></a>\_Сообщение ПСМ енаблевизбуттонс

Включает или отключает любые стандартные кнопки в мастере Aero. Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ енаблевизбуттонс**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Одно или несколько из следующих значений, указывающих, какие кнопки страницы свойств должны быть включены. Если значение кнопки включено и для этого параметра, и для *lParam*, оно включено.



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

Одно или несколько из тех же значений, которые используются в параметре *wParam*, указывая, какие кнопки затрагиваются этим вызовом. Если значение кнопки отображается в этом параметре, но не в *wParam*, это означает, что кнопка должна быть отключена.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



 

 





