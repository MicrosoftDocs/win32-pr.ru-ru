---
title: Сообщение EM_SETOPTIONS (RichEdit. h)
description: Задает параметры для элемента управления Rich Edit.
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- Элементы управления Windows для EM_SETOPTIONS сообщений
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
ms.openlocfilehash: 0c43dda8268b42dc264a86600826d2a6b550e35c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135726"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Стили элемента управления Rich Edit**](rich-edit-control-styles.md)
</dt> </dl>

 

 





