---
title: Сообщение EM_INSERTIMAGE (RichEdit. h)
description: Заменяет выделенный BLOB-объект, который отображает изображение.
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- Элементы управления Windows для EM_INSERTIMAGE сообщений
topic_type:
- apiref
api_name:
- EM_INSERTIMAGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9ff1e0fd355cf5dd8d43d211c44fda6417c638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489450"
---
# <a name="em_insertimage-message"></a>\_Сообщение ИНСЕРТИМАЖЕ EM

Заменяет выделенный BLOB-объект, который отображает изображение.


```C++
#define EM_INSERTIMAGE       (WM_USER + 314)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**\_ \_ параметров изображения RichEdit**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) , содержащую большой двоичный объект изображения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

\_При успешном выполнении или один из следующих кодов ошибок возвращает значение ОК.



| Код возврата                                                                                    | Описание                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**Д \_ Не пройден**</dt> </dl>        | Не удается вставить изображение. <br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Параметр *lParam* имеет значение null или указывает на недопустимое изображение. |
| <dl> <dt>**Д \_ OUTOFMEMORY**</dt> </dl> | Недостаточно свободной памяти.<br/>                  |



 

## <a name="remarks"></a>Комментарии

Если выделение является точкой вставки, большой двоичный объект изображения вставляется в позицию курсора.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ инсерттабле**](em-inserttable.md)
</dt> </dl>

 

 





