---
title: Сообщение LVM_SETBKIMAGE (Коммктрл. h)
description: Задает фоновое изображение в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Сетбкимаже ListView.
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- Элементы управления Windows для LVM_SETBKIMAGE сообщений
topic_type:
- apiref
api_name:
- LVM_SETBKIMAGE
- LVM_SETBKIMAGEA
- LVM_SETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e22bebdcb36faff56dfabab721731acb55fdec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491457"
---
# <a name="lvm_setbkimage-message"></a>\_Сообщение LVM сетбкимаже

Задает фоновое изображение в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью макроса [**\_ сетбкимаже ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**лвбкимаже**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) , содержащую новые сведения о фоновом изображении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае. Возвращает нуль, если элемент **улфлагс** структуры [**Лвбкимаже**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) имеет значение **лвбкиф \_ source \_ None**.

## <a name="remarks"></a>Комментарии

Так как элемент управления "представление списка" использует OLE COM для работы с фоновыми изображениями, вызывающее приложение должно вызвать [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) или [**олеинитиализе**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) перед отправкой этого сообщения. Рекомендуется вызывать одну из этих функций при инициализации приложения и вызывать [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) или [**олеунинитиализе**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) при завершении работы приложения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **LVM \_ СЕТБКИМАЖЕВ** (Юникод) и **LVM \_ сетбкимажеа** (ANSI)<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**LVM \_ жетбкимаже**](lvm-getbkimage.md)
</dt> </dl>

 

