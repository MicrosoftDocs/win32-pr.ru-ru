---
description: Происходит, когда пользователь щелкает элемент управления InkPicture.
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: Событие InkPicture. Click (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ebde47609a36a92eca211f597345a9784fca03f66076ebb4db6f04ee6f5936
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218543"
---
# <a name="inkpictureclick-event"></a>Событие InkPicture. Click

Происходит, когда пользователь щелкает элемент управления [InkPicture](inkpicture-control-reference.md) .

## <a name="syntax"></a>Синтаксис


```C++
void Click();
```



## <a name="parameters"></a>Параметры

У этого события нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

При щелчке элемента управления создаются события [**MouseDown**](inkpicture-mousedown.md) и [**MouseUp**](inkpicture-mouseup.md) в дополнение к событию Click.

> [!Note]  
> Чтобы различать левую, правую и среднюю кнопки мыши, используйте события [**MouseDown**](inkpicture-mousedown.md) и [**MouseUp**](inkpicture-mouseup.md) .

 

Если в событии **Click** есть код, событие [**DblClick**](inkpicture-dblclick.md) никогда не запустится, так как событие **Click** является первым событием для активации между двумя. В результате нажатие кнопки мыши перехватывается событием **нажатия** , поэтому событие **DblClick** не возникает.

Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** . Интерфейс **\_ иинкпиктуривентс** реализует интерфейс IDispatch с идентификатором **DISPID \_ ипекликк**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

 




