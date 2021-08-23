---
description: Не рекомендуется. Пенинпутпанел был заменен панелью ввода текста (TIP). Происходит при отображении или скрытии объекта Пенинпутпанел.
ms.assetid: bf4651f4-2cf4-4952-a93e-3c6ba4846722
title: Событие Пенинпутпанел. Висиблечанжед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc917f34c09ef0d4f079fd55e476bbbc4cea266e1b1c436a62b20d6c08ed1b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596613"
---
# <a name="peninputpanelvisiblechanged-event"></a>Пенинпутпанел. Висиблечанжед, событие

Не рекомендуется. [**Пенинпутпанел**](peninputpanel-class.md) был заменен [панелью ввода текста (TIP)](text-input-panel-reference.md).

Происходит при отображении или скрытии объекта [**пенинпутпанел**](peninputpanel-class.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT VisibleChanged(
  [in] VARIANT_BOOL NewVisibility
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Неввисибилити* \[ окне\]
</dt> <dd>

**Вариант \_ Значение TRUE** , чтобы объект [**пенинпутпанел**](peninputpanel-class.md) стал видимым; в противном случае — **\_ значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если это событие завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Событие **висиблечанжед** применяется к нацеливанию на панель ввода Tablet PC. Однако он не вызывается, когда нацеливание наводится на панель ввода для отображения всей панели вводов Tablet PC.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Заголовок<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**пенинпутпанел**](peninputpanel-class.md)
</dt> </dl>

 

 




