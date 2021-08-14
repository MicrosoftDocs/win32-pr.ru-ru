---
title: Сообщение EM_SETBKGNDCOLOR (RichEdit. h)
description: В \_ сообщении EM сетбкгндколор задается цвет фона для элемента управления Rich Edit.
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- элементы управления Windows сообщений EM_SETBKGNDCOLOR
topic_type:
- apiref
api_name:
- EM_SETBKGNDCOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1173c2da9f3c04e49211224bd269d79c0634e1cb3f8ea959f6b58e354fdf0dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412658"
---
# <a name="em_setbkgndcolor-message"></a>\_Сообщение СЕТБКГНДКОЛОР EM

В сообщении **EM \_ сетбкгндколор** задается цвет фона для элемента управления Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает, следует ли использовать системный цвет. Если этот параметр имеет ненулевое значение, для фона задается цвет системы фона окна. В противном случае для фона задается указанный цвет.

</dd> <dt>

*lParam* 
</dt> <dd>

Структура [**COLORREF**](/windows/desktop/gdi/colorref) , указывающая цвет, если параметр *wParam* равен нулю. Чтобы создать **COLORREF**, используйте макрос [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение возвращает исходный цвет фона.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Другие ресурсы**
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

