---
title: Сообщение EM_SETHYPHENATEINFO (RichEdit. h)
description: Задает способ расстановки переносов в элементе управления Rich Edit.
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- элементы управления Windows сообщений EM_SETHYPHENATEINFO
topic_type:
- apiref
api_name:
- EM_SETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5551aace3ab054c1c6fa322242ae06386ff19f5a44775bd6dcc6887d19c65c62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437564"
---
# <a name="em_sethyphenateinfo-message"></a>\_Сообщение СЕСИФЕНАТЕИНФО EM

Задает способ расстановки переносов в элементе управления Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указатель на структуру [**хифенатеинфо**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) .

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется, должно быть равно нулю.

</dd> </dl>

## <a name="remarks"></a>Remarks

> [!Note]  
> Чтобы включить расстановку переносов, клиент должен вызвать [**EM \_ сеттипографйоптионс**](em-settypographyoptions.md), указав для \_ адванцедтипографи.

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 1 (SP1), \[ только классические приложения\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ жесифенатеинфо**](em-gethyphenateinfo.md)
</dt> </dl>

 

 





