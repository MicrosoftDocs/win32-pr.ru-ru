---
title: Сообщение LVM_GETBKIMAGE (Коммктрл. h)
description: Возвращает фоновое изображение в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Жетбкимаже ListView.
ms.assetid: db0e8f31-746a-4a16-b689-68da696e3657
keywords:
- Элементы управления Windows для LVM_GETBKIMAGE сообщений
topic_type:
- apiref
api_name:
- LVM_GETBKIMAGE
- LVM_GETBKIMAGEA
- LVM_GETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e178bae10b9bed880213ca4a4ab2a1b4e07239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801120"
---
# <a name="lvm_getbkimage-message"></a>\_Сообщение LVM жетбкимаже

Возвращает фоновое изображение в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью макроса [**\_ жетбкимаже ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**лвбкимаже**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) , которая получит сведения о фоновом изображении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **LVM \_ ЖЕТБКИМАЖЕВ** (Юникод) и **LVM \_ жетбкимажеа** (ANSI)<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**LVM \_ сетбкимаже**](lvm-setbkimage.md)
</dt> </dl>

 

 





