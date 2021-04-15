---
title: Интерфейс IWMPControls2 (VB и C) (Wmp.h)
description: Предоставляет метод, который дополняет интерфейс Ивмпконтролс.
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- IWMPControls2 (VB и C) интерфейс проигрывателя Windows Media
- IWMPControls2 (VB и C) интерфейс проигрывателя Windows Media, описание
topic_type:
- apiref
api_name:
- IWMPControls2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955ee2a8b18f1629427dfe45da802759901ab00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688846"
---
# <a name="iwmpcontrols2-vb-and-c-interface"></a>Интерфейс IWMPControls2 (VB и C#)

Предоставляет метод, который дополняет интерфейс [**ивмпконтролс**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) .

## <a name="members"></a>Элементы

Интерфейс **IWMPControls2 (VB и C#)** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IWMPControls2 (VB и C#)** содержит следующие методы.



| Метод                                                           | Описание                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**первом**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md) | Перемещает текущий элемент мультимедиа в следующий кадр или предыдущий кадр и закрепляет воспроизведение.<br/> |



 

В следующем примере кода показано, как получить доступ к интерфейсу [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) . В примере кода приведено значение [**ивмпконтролс**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) , которое свойство [**аксвиндовсмедиаплайер. Ктлконтролс**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) возвращает значение **IWMPControls2** .

Для **C#**:


```CSharp
IWMPControls2 Ctlcontrols2 = (IWMPControls2)AxWindowsMediaPlayer.Ctlcontrols;
```



Для **VB**:


```VB
Dim Ctlcontrols As WMPLib.IWMPControls = Me.AxWindowsMediaPlayer1.Ctlcontrols
Dim Ctlcontrols2 As WMPLib.IWMPControls2 = DirectCast(Ctlcontrols, WMPLib.IWMPControls2)
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмпконтролс**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)
</dt> <dt>

[**Интерфейсы для Visual Basic .NET и C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпконтролс (VB и C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Интерфейс IWMPControls3 (VB и C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





