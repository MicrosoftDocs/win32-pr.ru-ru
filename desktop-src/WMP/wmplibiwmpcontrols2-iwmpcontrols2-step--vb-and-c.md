---
title: Метод шага IWMPControls2
description: Метод Step заставляет текущий элемент мультимедиа перейти к следующему кадру или предыдущему кадру и заморозить воспроизведение.
ms.assetid: c5cb720f-527f-45b6-ae8a-4da0e3e34618
keywords:
- проигрыватель Windows Media метода step
- проигрыватель Windows Media метода step, интерфейс IWMPControls2
- проигрыватель Windows Media интерфейса IWMPControls2, метод step
topic_type:
- apiref
api_name:
- IWMPControls2.step
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 310094a0b41381d729db3c5e5ef2f530a93b7da88c4a3116df8440e4ad3830c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930226"
---
# <a name="iwmpcontrols2step-method"></a>Метод IWMPControls2:: Step

Метод **Step** заставляет текущий элемент мультимедиа перейти к следующему кадру или предыдущему кадру и заморозить воспроизведение.

## <a name="syntax"></a>Синтаксис


```CSharp
public void step(
  System.Int32 lStep
);
```


```VB

Public Sub step( _
  ByVal lStep As System.Int32 _
)
Implements IWMPControls2.step
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*лстеп* \[ окне\]
</dt> <dd>

Значение **System. Int32** , указывающее, сколько кадров необходимо выполнить перед замораживанием. Необходимо задать значение 1 или-1.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

В настоящее время этот метод поддерживает только параметры 1 или-1, поэтому можно пошаговым образом выполнять только один кадр.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс IWMPControls2 (VB и C#)**](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[**Интерфейс ИВМПДВД (VB и C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





