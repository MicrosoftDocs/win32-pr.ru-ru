---
title: Сообщение EM_GETSTORYTYPE (RichEdit. h)
description: Возвращает тип истории.
ms.assetid: 06D87AA1-5AA3-4235-AC1D-045CE9975384
keywords:
- элементы управления Windows сообщений EM_GETSTORYTYPE
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
ms.openlocfilehash: e4e6d501fffca857e1e283f2678c1b42e5d3d12e587e51a3a58585041489f8b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048784"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**EM \_ сетсторитипе**](em-setstorytype.md)
</dt> <dt>

[**Итекстсториранжес:: Item**](/windows/desktop/api/Tom/nf-tom-itextstoryranges-item)
</dt> </dl>

 

 





