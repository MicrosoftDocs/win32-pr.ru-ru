---
title: Сообщение EM_SETOPTIONS (RichEdit. h)
description: Задает параметры для элемента управления Rich Edit.
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- элементы управления Windows сообщений EM_SETOPTIONS
topic_type:
- apiref
api_name:
- EM_SETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5d5c4b7fd9e92261cedaf0681523ad0a3e25a37aa2814f6c00d0d9460e94bb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672613"
---
# <a name="em_setoptions-message"></a>\_Сообщение СЕТОПТИОНС EM

Задает параметры для элемента управления Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает операцию, которая может принимать одно из следующих значений.



| Значение                                                                                                                                             | Значение                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**\_набор екуп**</dt> </dl> | Задает параметры, заданные параметром *lParam*.<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ЕКУП \_ или**</dt> </dl>    | Объединяет указанные параметры с текущими параметрами.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ЕКУП \_ и**</dt> </dl> | Сохраняются только текущие параметры, которые также задаются параметром *lParam*.<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**ЕКУП \_ XOR**</dt> </dl> | Логически исключающие или текущие параметры с параметрами, указанными как *lParam*.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Задает одно или несколько из следующих значений.



| Значение                                                                                                                                                                                 | Значение                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="ECO_AUTOWORDSELECTION"></span><span id="eco_autowordselection"></span><dl> <dt>**ЭКОНОМИЧный \_ аутовордселектион**</dt> </dl> | Автоматический выбор слова при двойном щелчке.<br/>                                                                           |
| <span id="ECO_AUTOVSCROLL"></span><span id="eco_autovscroll"></span><dl> <dt>**ЭКОНОМИЧный \_ аутовскролл**</dt> </dl>                   | Аналогично [**\_ аутовскролл**](rich-edit-control-styles.md) стилю.<br/>                                      |
| <span id="ECO_AUTOHSCROLL"></span><span id="eco_autohscroll"></span><dl> <dt>**ЭКОНОМИЧный \_ аутохскролл**</dt> </dl>                   | Аналогично [**\_ аутохскролл**](rich-edit-control-styles.md) стилю.<br/>                                      |
| <span id="ECO_NOHIDESEL"></span><span id="eco_nohidesel"></span><dl> <dt>**ЭКОНОМИЧный \_ нохидесел**</dt> </dl>                         | Аналогично [**\_ нохидесел**](rich-edit-control-styles.md) стилю.<br/>                                          |
| <span id="ECO_READONLY"></span><span id="eco_readonly"></span><dl> <dt>**ЭКОНОМИЧное \_ чтение**</dt> </dl>                            | То же, что и стиль [**\_ только для чтения**](rich-edit-control-styles.md) .<br/>                                            |
| <span id="ECO_WANTRETURN"></span><span id="eco_wantreturn"></span><dl> <dt>**ЭКОНОМИЧный \_ вантретурн**</dt> </dl>                      | Аналогично [**\_ вантретурн**](rich-edit-control-styles.md) стилю.<br/>                                        |
| <span id="ECO_SELECTIONBAR"></span><span id="eco_selectionbar"></span><dl> <dt>**ЭКОНОМИЧный \_ селектионбар**</dt> </dl>                | Аналогично [**\_ селектионбар**](rich-edit-control-styles.md) стилю.<br/>                                    |
| <span id="ECO_VERTICAL"></span><span id="eco_vertical"></span><dl> <dt>**ЭКОНОМИЧный \_ по вертикали**</dt> </dl>                            | То же, что и [**\_ вертикальный стиль ES**](rich-edit-control-styles.md) . Доступно только в версиях для азиатских языков.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение возвращает текущие параметры элемента управления "поле ввода".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Стили элемента управления Rich Edit**](rich-edit-control-styles.md)
</dt> </dl>

 

 





