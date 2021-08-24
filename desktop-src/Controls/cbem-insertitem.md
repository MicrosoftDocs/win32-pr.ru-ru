---
title: Сообщение CBEM_INSERTITEM (Коммктрл. h)
description: Вставляет новый элемент в элемент управления ComboBoxEx.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- элементы управления Windows сообщений CBEM_INSERTITEM
topic_type:
- apiref
api_name:
- CBEM_INSERTITEM
- CBEM_INSERTITEMA
- CBEM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4d9627efef4796554dfdbe1d7263747cc6b1c32b2cc00d5619a7cb7953024cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699313"
---
# <a name="cbem_insertitem-message"></a>\_Сообщение кбем INSERTITEM

Вставляет новый элемент в элемент управления ComboBoxEx.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**комбобоксекситем**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) , содержащую сведения о вставляемом элементе. При отправке сообщения элемент **Член iItem** должен быть установлен в значение, указывающее на Отсчитываемый от нуля индекс, по которому нужно вставить элемент. Чтобы вставить элемент в конец списка, установите для элемента **Член iItem** значение-1.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс, по которому новый элемент был вставлен в случае успеха, или значение-1 в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Кбем \_ ИНСЕРТИТЕМВ** (Юникод) и **кбем \_ инсертитема** (ANSI)<br/>           |



 

 





