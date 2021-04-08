---
title: Сообщение EM_GETSTORYTYPE (RichEdit. h)
description: Возвращает тип истории.
ms.assetid: 06D87AA1-5AA3-4235-AC1D-045CE9975384
keywords:
- Элементы управления Windows для EM_GETSTORYTYPE сообщений
topic_type:
- apiref
api_name:
- EM_GETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fed85183f292bd1c69e3bbebdadb4b38f9f3bdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891837"
---
# <a name="em_getstorytype-message"></a>\_Сообщение ЖЕТСТОРИТИПЕ EM

Возвращает тип истории.


```C++
#define EM_GETSTORYTYPE       (WM_USER + 290)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс истории.

</dd> <dt>

*lParam* 
</dt> <dd>

Процессу значение должно быть равно 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает тип истории, который может быть определяемым клиентом пользовательским значением или одним из следующих значений:

<dl> <dt>

**[**томкомментсстори**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**томенднотесстори**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**томевенпажесфутерстори**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**томевенпажешеадерстори**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**томфиндстори**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**томфирстпажефутерстори**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**томфирстпажехеадерстори**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**томфутнотесстори**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**томмаинтекстстори**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**томпримарифутерстори**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**томпримарихеадерстори**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**томреплацестори**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**томскратчстори**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**томтекстфраместори**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**томункновнстори**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ сетсторитипе**](em-setstorytype.md)
</dt> <dt>

[**Итекстсториранжес:: Item**](/windows/desktop/api/Tom/nf-tom-itextstoryranges-item)
</dt> </dl>

 

 





