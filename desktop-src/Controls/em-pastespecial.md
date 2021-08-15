---
title: Сообщение EM_PASTESPECIAL (RichEdit. h)
description: Замещает конкретный формат буфера обмена в элементе управления Rich Edit.
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- элементы управления Windows сообщений EM_PASTESPECIAL
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
ms.openlocfilehash: 2dc1af4dd0566cdf8e256b34f87fcc52ea855bc521c87cbe390e02b8b1cf7b06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412805"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**репастеспеЦиал**](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

