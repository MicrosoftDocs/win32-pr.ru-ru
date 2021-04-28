---
title: Сообщение TDM_UPDATE_ELEMENT_TEXT (Коммктрл. h)
description: TDM_UPDATE_ELEMENT_TEXT сообщение — обновляет текстовый элемент в диалоговом окне задачи.
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- Элементы управления Windows для TDM_UPDATE_ELEMENT_TEXT сообщений
topic_type:
- apiref
api_name:
- TDM_UPDATE_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c155b426b92645c0b9cdbabe00c44ffa722b89f3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085812"
---
# <a name="tdm_update_element_text-message"></a>\_ \_ Текстовое сообщение элемента обновления TDM \_

Обновляет текстовый элемент в диалоговом окне задачи.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

Указывает обновляемый элемент. (Иллюстрация элементов см. в разделе [о диалоговых окнах задач](task-dialogs-overview.md).) Этот параметр должен иметь одно из следующих значений:



| Значение                                                                                                                                                                                           | Значение                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**TDE \_ содержимое**</dt> </dl>                                         | Содержимое.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**TDE \_ Расширенная \_ информация**</dt> </dl> | Расширенная информация.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**\_Нижний КОЛОНТИТУЛ TDE**</dt> </dl>                                            | Текст нижнего колонтитула.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**\_Основная \_ инструкция TDE**</dt> </dl>             | Основная инструкция.<br/>     |



 

</dd> <dt>

*lParam* \[ окне\]
</dt> <dd>

Указатель на строку в Юникоде, содержащую новый текст.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="remarks"></a>Remarks

Чтобы избежать обрезки, новый текст должен быть больше, чем существующий текст. Установка более короткой строки текста не приводит к изменению размера диалогового окна.

Если элемент **псзекспандединформатион** структуры [**таскдиалогконфиг**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) , используемый для создания диалогового окна задачи, имел **значение NULL**, и вы отправляете ТЕКСТОВОЕ сообщение об **\_ обновлении \_ \_ TDM** с \_ TDE \_ информацией, ничего не произойдет.

Приведенные выше также применяются к нижнему колонтитулу и \_ нижнему колонтитулу TDE.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ \_ текст элемента набора \_ TDM**](tdm-set-element-text.md)
</dt> </dl>

 

 





