---
title: Сообщение CBEM_SETITEM (Коммктрл. h)
description: Задает атрибуты элемента в элементе управления ComboBoxEx.
ms.assetid: 752df8ea-fd5e-47fa-b729-d019bdde0904
keywords:
- элементы управления Windows сообщений CBEM_SETITEM
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
ms.openlocfilehash: 7b1010c090283a47404ee93ef5f3bc1cf2d5ffe71a646d6d734cb443152bdd64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527934"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Кбем \_ СЕТИТЕМВ** (Юникод) и **кбем \_ сетитема** (ANSI)<br/>                 |



 

 





