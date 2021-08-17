---
title: Сообщение EM_GETOLEINTERFACE (RichEdit. h)
description: Извлекает объект Иричедитоле, который клиент может использовать для доступа к функциональным возможностям модели COM в элементе управления "поле ввода".
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- элементы управления Windows сообщений EM_GETOLEINTERFACE
topic_type:
- apiref
api_name:
- EM_GETOLEINTERFACE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4e1799039081ed8250cb062aa3d1348a2fe8a8dbdcfa768fab74855d18d8e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831675"
---
# <a name="em_getoleinterface-message"></a>\_Сообщение ЖЕТОЛЕИНТЕРФАЦЕ EM

Извлекает объект [**иричедитоле**](/windows/desktop/api/Richole/nn-richole-iricheditole) , который клиент может использовать для доступа к функциональным ВОЗМОЖНОСТЯМ модели COM в элементе управления "поле ввода".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется; оно должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на указатель, который получает объект [**иричедитоле**](/windows/desktop/api/Richole/nn-richole-iricheditole) . Перед возвратом элемент управления вызывает метод [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) для объекта, поэтому вызывающее приложение должно вызвать метод [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) , когда он завершит работу с объектом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если операция завершилась удачно, возвращаемое значение будет ненулевым.

Если операция завершается ошибкой, возвращаемое значение равно нулю.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иричедитоле**](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 

