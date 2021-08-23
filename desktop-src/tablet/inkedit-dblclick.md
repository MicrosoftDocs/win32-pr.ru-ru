---
description: Происходит при двойном щелчке элемента управления InkEdit.
ms.assetid: 380499e4-8697-4823-8153-29f24b2f234c
title: Событие InkEdit. DblClick (с. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2f1cf2a7b7d7d699af5cd8a148e5c54a2879ad5eb879bd34af7531025748e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032092"
---
# <a name="inkeditdblclick-event"></a>Событие InkEdit. DblClick

Происходит при двойном щелчке элемента управления [InkEdit](inkedit-control-reference.md) .

## <a name="syntax"></a>Синтаксис


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Отмена* \[ в, out\]
</dt> <dd>

**Вариант \_ Значение TRUE** , чтобы отменить событие для родительского элемента управления; в противном случае — **\_ значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

> [!Note]  
> Чтобы различать левую, правую и среднюю кнопки мыши, используйте события [**MouseDown**](inkedit-mousedown.md) и [**MouseUp**](inkedit-mouseup.md) . Если в событии [**Click**](inkedit-click.md) есть код, событие **DblClick** не запустится.

 

Этот метод события определен в интерфейсе **\_ иинкедитевентс** . Интерфейс **\_ иинкедитевентс** реализует интерфейс IDispatch с идентификатором **DISPID \_ иидблкликк**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>«С». h (также требует \_ ввода i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




