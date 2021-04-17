---
description: Происходит, когда пользователь щелкает элемент управления InkEdit.
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: InkEdit. Click, событие (с. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55df62807ee78e0f083a301c83a756b4cffb729d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684206"
---
# <a name="inkeditclick-event"></a>Событие InkEdit. Click

Происходит, когда пользователь щелкает элемент управления [InkEdit](inkedit-control-reference.md) .

## <a name="syntax"></a>Синтаксис


```C++
void Click();
```



## <a name="parameters"></a>Параметры

У этого события нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

При щелчке элемента управления создаются события [**MouseDown**](inkedit-mousedown.md) и [**MouseUp**](inkedit-mouseup.md) в дополнение к событию Click.

> [!Note]  
> Чтобы различать левую, правую и среднюю кнопки мыши, используйте события [**MouseDown**](inkedit-mousedown.md) и [**MouseUp**](inkedit-mouseup.md) .

 

Если в событии **Click** есть код, событие [**DblClick**](inkedit-dblclick.md) никогда не запустится, так как событие **Click** является первым событием для активации между двумя. В результате нажатие кнопки мыши перехватывается событием **нажатия** , поэтому событие **DblClick** не возникает.

Этот метод события определен в интерфейсе **\_ иинкедитевентс** . Интерфейс **\_ иинкедитевентс** реализует интерфейс IDispatch с идентификатором **DISPID \_ иикликк**.

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
</dt> </dl>

 

 




