---
title: Сообщение LVM_GETEMPTYTEXT (Коммктрл. h)
description: Получает текст, предназначенный для отображения, когда элемент управления "список" отображается пустым. Отправьте это сообщение явным образом или с помощью \_ макроса Жетемптитекст ListView.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- элементы управления Windows сообщений LVM_GETEMPTYTEXT
topic_type:
- apiref
api_name:
- LVM_GETEMPTYTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dd1dc1df7b0a558adda37938849b5383bbfee304d807a22a329e4f7301889b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411473"
---
# <a name="lvm_getemptytext-message"></a>\_Сообщение LVM жетемптитекст

Получает текст, предназначенный для отображения, когда элемент управления "список" отображается пустым. Отправьте это сообщение явным образом или с помощью макроса [**\_ жетемптитекст ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

Размер буфера, на который указывает *lParam*, включая завершающее **значение NULL**.

</dd> <dt>

*lParam* \[ в, out\]
</dt> <dd>

Указатель на заканчивающийся нулем буфер размером в Юникоде, заданный параметром *wParam* для получения текста. Вызывающий объект отвечает за выделение буфера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





