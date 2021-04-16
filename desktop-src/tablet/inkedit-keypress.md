---
description: Происходит, когда пользователь нажимает и отпускает ключ, когда элемент управления InkEdit имеет фокус.
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: Событие InkEdit. KeyPress (с. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e49264f82b2cfe3c6998666339f08340a540791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712219"
---
# <a name="inkeditkeypress-event"></a>Событие InkEdit. KeyPress

Происходит, когда пользователь нажимает и отпускает ключ, когда элемент управления [InkEdit](inkedit-control-reference.md) имеет фокус.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT KeyPress(
   Long *Char
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Char* 
</dt> <dd>

Целое число, возвращающее стандартное числовое значение ANSI KeyCode. Параметр *char* передается по ссылке; При изменении он отправляет элементу управления другой символ. Изменение параметра *char* на 0 отменяет событие.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если это событие завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод события определен в интерфейсе **\_ иинкедитевентс** . Интерфейс **\_ иинкедитевентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ иикэйпресс.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>«С». h (также требует \_ ввода i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**\[Элемент управления InkEdit события KeyDown\]**](inkedit-keydown.md)
</dt> <dt>

[**\[Элемент управления InkEdit для события KeyUp\]**](inkedit-keyup.md)
</dt> </dl>

 

