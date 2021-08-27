---
title: Сообщение TDM_SET_ELEMENT_TEXT (Коммктрл. h)
description: TDM_SET_ELEMENT_TEXT сообщение — обновляет текстовый элемент в диалоговом окне задачи.
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- элементы управления Windows сообщений TDM_SET_ELEMENT_TEXT
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
ms.openlocfilehash: 7bb0f81867bcff4fd5f7d533c156c8af17d0f4a761b6f8560aa584a85c62b7c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060774"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ \_ текст элемента обновления \_ TDM**](tdm-update-element-text.md)
</dt> </dl>

 

 





