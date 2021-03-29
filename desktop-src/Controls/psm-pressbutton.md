---
title: Сообщение PSM_PRESSBUTTON (Пршт. h)
description: Имитирует выбор кнопки страницы свойств. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит прессбуттон.
ms.assetid: 82a55a29-d916-47ee-b0a0-f685a3a386d9
keywords:
- Элементы управления Windows для PSM_PRESSBUTTON сообщений
topic_type:
- apiref
api_name:
- PSM_PRESSBUTTON
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b54b04dcc7b1263019f49ff8c1de0d2c21a12a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493302"
---
# <a name="psm_pressbutton-message"></a>\_Сообщение ПСМ прессбуттон

Имитирует выбор кнопки страницы свойств. Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ прессбуттон**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс кнопки для выбора. Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                            | Значение                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PSBTN_APPLYNOW"></span><span id="psbtn_applynow"></span><dl> <dt>**ПСБТН \_ апплинов**</dt> </dl> | Нажмите кнопку **Применить** . Это значение недопустимо при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).<br/> |
| <span id="PSBTN_BACK"></span><span id="psbtn_back"></span><dl> <dt>**ПСБТН \_ назад**</dt> </dl>             | Нажмите кнопку **назад** .<br/>                                                                                                         |
| <span id="PSBTN_CANCEL"></span><span id="psbtn_cancel"></span><dl> <dt>**ПСБТН \_ Отмена**</dt> </dl>       | Нажмите кнопку **Отмена** .<br/>                                                                                                       |
| <span id="PSBTN_FINISH"></span><span id="psbtn_finish"></span><dl> <dt>**\_Завершение псбтн**</dt> </dl>       | Выбирает кнопку **Готово** .<br/>                                                                                                       |
| <span id="PSBTN_HELP"></span><span id="psbtn_help"></span><dl> <dt>**\_Справка псбтн**</dt> </dl>             | Выбор кнопки " **Справка** ". Это значение недопустимо при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).<br/>  |
| <span id="PSBTN_NEXT"></span><span id="psbtn_next"></span><dl> <dt>**ПСБТН \_ Далее**</dt> </dl>             | Нажмите кнопку **Далее** .<br/>                                                                                                         |
| <span id="PSBTN_OK"></span><span id="psbtn_ok"></span><dl> <dt>**ПСБТН \_ ОК**</dt> </dl>                   | Нажмите кнопку **ОК** . Это значение недопустимо при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                               |
| Header<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



 

 





