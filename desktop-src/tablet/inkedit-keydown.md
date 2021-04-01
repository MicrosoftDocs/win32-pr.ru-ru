---
description: Происходит, когда пользователь нажимает клавишу, когда элемент управления InkEdit имеет фокус.
ms.assetid: 14b05b72-ae5d-416a-8ea5-9d9716c0967f
title: Событие InkEdit. KeyDown (с. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cee260d4c902534b9b234e0e30d0b60645c579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999432"
---
# <a name="inkeditkeydown-event"></a>Событие InkEdit. KeyDown

Происходит, когда пользователь нажимает клавишу, когда элемент управления [InkEdit](inkedit-control-reference.md) имеет фокус.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT KeyDown(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pKey* 
</dt> <dd>

Код виртуального ключа для клавиши, нажатой пользователем.

</dd> <dt>

*шифткэй* 
</dt> <dd>

Член перечисления [**инкшифткэймодифиерфлагс**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) , указывающий, какие клавиши-модификаторы следует отменять во время события.



| Значение                                                                                                                                                                                     | Значение                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**ИКМ \_ SHIFT**</dt> </dl>             | Указывает, что клавиша SHIFT использовалась как модификатор. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**ИКМ \_ Элемент управления**</dt> </dl> | Указывает, что клавиша CTRL использовалась как модификатор. <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**ИКМ \_ Alt**</dt> </dl>                 | Указывает, что клавиша ALT использовалась как модификатор. <br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если это событие завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод события определен в интерфейсе **\_ иинкедитевентс** . Интерфейс **\_ иинкедитевентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ иикэйдовн.

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

[**Перечисление Инкшифткэймодифиерфлагс**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**\[Элемент управления InkEdit события KeyPress\]**](inkedit-keypress.md)
</dt> <dt>

[**\[Элемент управления InkEdit для события KeyUp\]**](inkedit-keyup.md)
</dt> </dl>

 

