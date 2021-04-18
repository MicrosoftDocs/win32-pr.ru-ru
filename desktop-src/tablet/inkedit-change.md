---
description: Происходит при изменении содержимого элемента управления InkEdit.
ms.assetid: 6c65fcca-c84a-414c-a4e5-c5fdffb13e51
title: Событие InkEdit. Change (with. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1ad11ef335a397070001f1ae6be785d60fe9cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693468"
---
# <a name="inkeditchange-event"></a>Событие InkEdit. Change

Происходит при изменении содержимого элемента управления [InkEdit](inkedit-control-reference.md) .

## <a name="syntax"></a>Синтаксис


```C++
void Change();
```



## <a name="parameters"></a>Параметры

У этого события нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Это событие возникает при каждом изменении любого свойства, влияющего на содержимое элемента управления [InkEdit](inkedit-control-reference.md) .

Этот метод события определен в интерфейсе **\_ иинкедитевентс** . Интерфейс **\_ иинкедитевентс** реализует интерфейс IDispatch с идентификатором **DISPID \_ иичанже**.

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

 

 




