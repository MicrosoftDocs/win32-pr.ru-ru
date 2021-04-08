---
title: Сообщение EM_PASTESPECIAL (RichEdit. h)
description: Замещает конкретный формат буфера обмена в элементе управления Rich Edit.
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- Элементы управления Windows для EM_PASTESPECIAL сообщений
topic_type:
- apiref
api_name:
- EM_PASTESPECIAL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9375dd4a333f0e29d5e8f2721409244cf80f1233
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892169"
---
# <a name="em_pastespecial-message"></a>\_Сообщение PASTESPECIAL EM

Замещает конкретный формат буфера обмена в элементе управления Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает [форматы буфера обмена](/windows/desktop/dataxchg/clipboard-formats).

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**репастеспеЦиал**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) или **значение NULL**. Если объект вставляется, структура **репастеспеЦиал** заполняется требуемым аспектом дисплея. Если параметр *lParam* имеет **значение NULL** или элемент **дваспект** равен нулю, то используемый аспект изображения будет содержимым дескриптора объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**репастеспеЦиал**](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

