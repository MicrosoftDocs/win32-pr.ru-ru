---
title: Сообщение TTM_SETTITLE (Коммктрл. h)
description: Добавляет стандартный значок и строку заголовка в подсказку.
ms.assetid: e745a592-eef7-4e0d-8939-a48b52c4ab9f
keywords:
- элементы управления Windows сообщений TTM_SETTITLE
topic_type:
- apiref
api_name:
- TTM_SETTITLE
- TTM_SETTITLEA
- TTM_SETTITLEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e159ce522ea27361f93beaa96da06959fba6f92fedf5981dfd049ddc7f36cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166357"
---
# <a name="ttm_settitle-message"></a>\_Сообщение ТТМ сеттитле

Добавляет стандартный значок и строку заголовка в подсказку.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Задайте для параметра *wParam* одно из следующих значений, чтобы указать отображаемый значок. начиная с версии Windows XP SP2 и более поздних версий этот параметр также может содержать значение **хикон** . Значение, превышающее TTI \_ Error, считается **Хикон**.



| Значение                                                                                                                                                                      | Значение                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="TTI_NONE"></span><span id="tti_none"></span><dl> <dt>**TTI \_ None**</dt> </dl>                             | Нет значка.<br/>         |
| <span id="TTI_INFO"></span><span id="tti_info"></span><dl> <dt>**\_сведения о TTI**</dt> </dl>                             | Значок сведений.<br/>       |
| <span id="TTI_WARNING"></span><span id="tti_warning"></span><dl> <dt>**\_предупреждение TTI**</dt> </dl>                    | Значок предупреждения<br/>     |
| <span id="TTI_ERROR"></span><span id="tti_error"></span><dl> <dt>**TTI, \_ Ошибка**</dt> </dl>                          | Значок ошибки<br/>       |
| <span id="TTI_INFO_LARGE"></span><span id="tti_info_large"></span><dl> <dt>**TTI \_ сведения о \_ большом размере**</dt> </dl>          | Значок "крупные ошибки"<br/> |
| <span id="TTI_WARNING_LARGE"></span><span id="tti_warning_large"></span><dl> <dt>**\_предупреждение TTI \_ Large**</dt> </dl> | Значок "крупные ошибки"<br/> |
| <span id="TTI_ERROR_LARGE"></span><span id="tti_error_large"></span><dl> <dt>**TTI \_ Ошибка \_ большого размера**</dt> </dl>       | Значок "крупные ошибки"<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на строку заголовка. Необходимо присвоить значение *lParam*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха, в противном случае **false** .

## <a name="remarks"></a>Remarks

Заголовок всплывающей подсказки отображается над текстом в другом шрифте. Недостаточно иметь заголовок; подсказка должна содержать текст и не отображается.

Если параметр *wParam* содержит **Хикон**, то в окне подсказки создается копия значка.

При вызове **ТТМ \_ сеттитле** строка, на которую указывает *lParam* , не должна превышать 100 **тчарс** в длину, включая завершающее **значение NULL**.

## <a name="examples"></a>Примеры

В следующем примере показано, как добавить заголовок и системный значок в подсказку.


```C++
// hwndTip is the handle of the tooltip window.
HICON hIcon = LoadIcon(NULL, IDI_INFORMATION);
SendMessage(hwndTip, TTM_SETTITLE, (WPARAM)hIcon, L"Title text");
DestroyIcon(hIcon);
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТТМ \_ СЕТТИТЛЕВ** (Юникод) и **ТТМ \_ сеттитлеа** (ANSI)<br/>                 |



## <a name="see-also"></a>См. также

<dl> <dt>

[Сведения об элементах управления ToolTip](tooltip-controls.md)
</dt> </dl>

 

 





