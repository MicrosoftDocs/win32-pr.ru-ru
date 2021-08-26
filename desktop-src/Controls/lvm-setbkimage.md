---
title: Сообщение LVM_SETBKIMAGE (Коммктрл. h)
description: Задает фоновое изображение в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Сетбкимаже ListView.
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- элементы управления Windows сообщений LVM_SETBKIMAGE
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
ms.openlocfilehash: 4f00fbf02d4e354115c01af637251782adb9f95b11923d12cba4bc9f1a0f9e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919974"
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

## <a name="remarks"></a>Remarks

Так как элемент управления "представление списка" использует OLE COM для работы с фоновыми изображениями, вызывающее приложение должно вызвать [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) или [**олеинитиализе**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) перед отправкой этого сообщения. Рекомендуется вызывать одну из этих функций при инициализации приложения и вызывать [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) или [**олеунинитиализе**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) при завершении работы приложения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **LVM \_ СЕТБКИМАЖЕВ** (Юникод) и **LVM \_ сетбкимажеа** (ANSI)<br/>             |



## <a name="see-also"></a>См. также

<dl> <dt>

[**LVM \_ жетбкимаже**](lvm-getbkimage.md)
</dt> </dl>

 

