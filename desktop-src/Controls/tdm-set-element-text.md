---
title: Сообщение TDM_SET_ELEMENT_TEXT (Коммктрл. h)
description: TDM_SET_ELEMENT_TEXT сообщение — обновляет текстовый элемент в диалоговом окне задачи.
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- Элементы управления Windows для TDM_SET_ELEMENT_TEXT сообщений
topic_type:
- apiref
api_name:
- TDM_SET_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d0c8830a6d8a1057ab283a9e096434a6184151
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104032"
---
# <a name="tdm_set_element_text-message"></a>\_ \_ Текстовое сообщение для элемента набора TDM \_

Обновляет текстовый элемент в диалоговом окне задачи.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

Указывает обновляемый элемент. (Иллюстрация см. в разделе [о диалоговых окнах задач](task-dialogs-overview.md).) Этот параметр должен иметь одно из следующих значений.



| Значение                                                                                                                                                                                           | Значение                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**TDE \_ содержимое**</dt> </dl>                                         | Содержимое.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**TDE \_ Расширенная \_ информация**</dt> </dl> | Расширенная информация.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**\_Нижний КОЛОНТИТУЛ TDE**</dt> </dl>                                            | Текст нижнего колонтитула.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**\_Основная \_ инструкция TDE**</dt> </dl>             | Основная инструкция.<br/>     |



 

</dd> <dt>

*lParam* \[ окне\]
</dt> <dd>

Новый текст для использования.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="remarks"></a>Remarks

Размер или структура диалогового окна задачи может измениться для размещения нового текста.

## <a name="examples"></a>Примеры

В следующем примере кода показано, как задать текст нижнего колонтитула в диалоговом окне задачи, представленном *HWND*.


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ \_ текст элемента обновления \_ TDM**](tdm-update-element-text.md)
</dt> </dl>

 

 





