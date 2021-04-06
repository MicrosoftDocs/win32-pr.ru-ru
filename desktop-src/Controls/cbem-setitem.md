---
title: Сообщение CBEM_SETITEM (Коммктрл. h)
description: Задает атрибуты элемента в элементе управления ComboBoxEx.
ms.assetid: 752df8ea-fd5e-47fa-b729-d019bdde0904
keywords:
- Элементы управления Windows для CBEM_SETITEM сообщений
topic_type:
- apiref
api_name:
- CBEM_SETITEM
- CBEM_SETITEMA
- CBEM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ae19287e3e30810b1d8c558be9b6153a86ab6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803700"
---
# <a name="cbem_setitem-message"></a>\_Сообщение кбем сетитем

Задает атрибуты элемента в элементе управления ComboBoxEx.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**комбобоксекситем**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) , содержащую сведения об элементе, которые необходимо задать. При отправке сообщения элемент **маски** структуры должен быть установлен, чтобы указать, какие атрибуты являются допустимыми, а элемент **Член iItem** должен указывать Отсчитываемый от нуля индекс изменяемого элемента. Установка элемента **Член iItem** в значение-1 приведет к изменению элемента, отображаемого в элементе управления "поле ввода".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Кбем \_ СЕТИТЕМВ** (Юникод) и **кбем \_ сетитема** (ANSI)<br/>                 |



 

 





