---
title: Интерфейс IWMPControls2 (VB и C) (Wmp.h)
description: Предоставляет метод, который дополняет интерфейс Ивмпконтролс.
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- проигрыватель Windows Media интерфейса IWMPControls2 (VB и C)
- проигрыватель Windows Media интерфейса IWMPControls2 (VB и C), описание
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
ms.openlocfilehash: 9757471526eb385168a10c505254b5a418ea7f9811576de95266c06817c73109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575924"
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
| Заголовок<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмпконтролс**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)
</dt> <dt>

[**интерфейсы для Visual Basic .net и C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпконтролс (VB и C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Интерфейс IWMPControls3 (VB и C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





