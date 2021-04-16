---
title: Сообщение LVM_GETEMPTYTEXT (Коммктрл. h)
description: Получает текст, предназначенный для отображения, когда элемент управления "список" отображается пустым. Отправьте это сообщение явным образом или с помощью \_ макроса Жетемптитекст ListView.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- Элементы управления Windows для LVM_GETEMPTYTEXT сообщений
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
ms.openlocfilehash: 7549081ef7f158a6a6a061bcee9669ea62d52f68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489060"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





