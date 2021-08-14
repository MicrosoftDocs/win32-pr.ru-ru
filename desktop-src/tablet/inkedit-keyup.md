---
description: Происходит, когда пользователь отпускает ключ, когда элемент управления InkEdit имеет фокус.
ms.assetid: 973d99f2-df09-4315-aaab-72877272100b
title: Событие InkEdit. KeyUp (с. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60ac908202a22fc1f564c3f21da4cc3cce2e79e2f093ec93b65ff56066f94510
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220771"
---
# <a name="inkeditkeyup-event"></a>Событие InkEdit. KeyUp

Происходит, когда пользователь отпускает ключ, когда элемент управления [InkEdit](inkedit-control-reference.md) имеет фокус.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT KeyUp(
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

## <a name="remarks"></a>Remarks

Этот метод события определен в интерфейсе **\_ иинкедитевентс** . Интерфейс **\_ иинкедитевентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ иикэйуп.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>«С». h (также требует \_ ввода i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Перечисление Инкшифткэймодифиерфлагс**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**\[Элемент управления InkEdit события KeyDown\]**](inkedit-keydown.md)
</dt> <dt>

[**\[Элемент управления InkEdit события KeyPress\]**](inkedit-keypress.md)
</dt> </dl>

 

