---
title: Сообщение EM_SETBKGNDCOLOR (RichEdit. h)
description: В \_ сообщении EM сетбкгндколор задается цвет фона для элемента управления Rich Edit.
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- Элементы управления Windows для EM_SETBKGNDCOLOR сообщений
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
ms.openlocfilehash: 091f04909e2660498f1380628439c067b5438b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892485"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Другие ресурсы**
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

