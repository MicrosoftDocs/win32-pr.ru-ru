---
title: Сообщение CBEM_INSERTITEM (Коммктрл. h)
description: Вставляет новый элемент в элемент управления ComboBoxEx.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- Элементы управления Windows для CBEM_INSERTITEM сообщений
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
ms.openlocfilehash: 23e6cb26a575472e53703d65e407a94a024dcfac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654707"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Кбем \_ ИНСЕРТИТЕМВ** (Юникод) и **кбем \_ инсертитема** (ANSI)<br/>           |



 

 





