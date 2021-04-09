---
title: Сообщение EM_SETHYPHENATEINFO (RichEdit. h)
description: Задает способ расстановки переносов в элементе управления Rich Edit.
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- Элементы управления Windows для EM_SETHYPHENATEINFO сообщений
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
ms.openlocfilehash: b8369d463ae03e9410347ab58a50346625e3de47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892481"
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

## <a name="remarks"></a>Комментарии

> [!Note]  
> Чтобы включить расстановку переносов, клиент должен вызвать [**EM \_ сеттипографйоптионс**](em-settypographyoptions.md), указав для \_ адванцедтипографи.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 1 \[\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ жесифенатеинфо**](em-gethyphenateinfo.md)
</dt> </dl>

 

 





