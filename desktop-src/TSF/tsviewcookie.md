---
title: Тсвиевкукие (Текстстор. h)
description: Тип данных Тсвиевкукие определяет представление контекста.
ms.assetid: e649b799-d0d6-4f2d-b9f1-28070eea9b16
keywords:
- тсвиевкукие
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb43f888f76410e83e89d037f39ea665ca548ec9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681819"
---
# <a name="tsviewcookie"></a>тсвиевкукие

Тип данных **тсвиевкукие** определяет представление контекста.


```C++
typedef DWORD TsViewCookie;
```



## <a name="remarks"></a>Комментарии

Приложение должно предоставить уникальное значение **тсвиевкукие** для каждого создаваемого представления.

Диспетчер TSF получает это значение из приложения путем вызова [ITextStoreACP:: жетактивевиев](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) или [Итекстстореанчор:: жетактивевиев](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview). Диспетчер TSF использует это значение для обнаружения представления при вызове различных методов [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) или [итекстстореанчор](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Приложения Windows 2000 Professional \[ классические приложения \| UWP\]<br/>                       |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows 2000 \|\]<br/>                             |
| Распространяемые компоненты<br/>          | TSF 1,0 в Windows 2000 профессиональная<br/>                                         |
| Header<br/>                   | <dl> <dt>Текстстор. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Текстстор. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ITextStoreACP**](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[**ITextStoreACP:: Жетактивевиев**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview)
</dt> <dt>

[**Итекстстореанчор:: Жетактивевиев**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview)
</dt> </dl>

 

 





