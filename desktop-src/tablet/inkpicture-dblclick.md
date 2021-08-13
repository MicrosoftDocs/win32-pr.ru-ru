---
description: Происходит при двойном щелчке элемента управления InkPicture.
ms.assetid: 5b2a6413-d415-4bf1-a291-35f4c3c5a0dc
title: Событие InkPicture. DblClick (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 515d16d16fb585771a8e2e06e642476b6be7a29851b750add4d6de2ca1a89bda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717333"
---
# <a name="inkpicturedblclick-event"></a>Событие InkPicture. DblClick

Происходит при двойном щелчке элемента управления [InkPicture](inkpicture-control-reference.md) .

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

Следует ли отменять событие для родительского элемента управления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

> [!Note]  
> Чтобы различать левую, правую и среднюю кнопки мыши, используйте события [**MouseDown**](inkpicture-mousedown.md) и [**MouseUp**](inkpicture-mouseup.md) . Если в событии [**Click**](inkpicture-click.md) есть код, событие **DblClick** не запустится.

 

Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** . Интерфейс **\_ иинкпиктуривентс** реализует интерфейс IDispatch с идентификатором **DISPID \_ ипедблкликк**.

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

 

 




