---
title: Ивмпконтролс. доступ (VB и C)
description: Свойство Available (метод Get- \_ Available в C \) получает значение, указывающее, доступен ли указанный тип сведений, или может быть выполнено указанное действие.
ms.assetid: 00812d5c-513e-49d5-93ba-750b81a852dd
keywords:
- Проигрыватель Windows Media Ивмпконтролс. Available (VB и C)
topic_type:
- apiref
api_name:
- IWMPControls.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d5d9ffcd6cad6eefb7cdff25fd2cf34b76ccc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688847"
---
# <a name="iwmpcontrolsisavailable-vb-and-c"></a>Ивмпконтролс. доступ (VB и C#)

Свойство **Available** (метод Get- **\_ Available** в C#) получает значение, указывающее, доступен ли указанный тип сведений или может быть выполнено указанное действие.


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
bool get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a>Параметры

*бстритем*

Строка System. String, которая является одним из следующих значений.



| Значение           | Описание                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| currentItem     | Обнаруживает, может ли пользователь задать свойство **ивмпконтролс. currentItem** .                                                                                     |
| куррентмаркер   | Обнаруживает, может ли пользователь перейти к определенному маркеру.                                                                                                         |
| currentPosition | Обнаруживает, может ли пользователь перейти к определенной должности в файле. Некоторые файлы не поддерживают поиск.                                                        |
| фастфорвард     | Обнаруживает, поддерживает ли файл быструю пересылку и можно ли вызывать эту функцию. Многие типы файлов (и динамические потоки) не поддерживают Фастфорвард. |
| фастреверсе     | Обнаруживает, поддерживает ли файл Фастреверсе и можно ли вызывать эту функцию. Многие типы файлов (и динамические потоки) не поддерживают Фастреверсе.     |
| Далее            | Обнаруживает, может ли пользователь перейти к следующей записи списка воспроизведения.                                                                                              |
| pause           | Обнаруживает, доступен ли метод **ивмпконтролс. Pause** .                                                                                                 |
| играть            | Обнаруживает, доступен ли метод **ивмпконтролс. Play** .                                                                                                  |
| Предыдущее время        | Обнаруживает, может ли пользователь перейти к предыдущей записи списка воспроизведения.                                                                                          |
| Шаг            | Обнаруживает, доступен ли метод **IWMPControls2. Step** во время воспроизведения.                                                                                 |
| stop            | Обнаруживает, доступен ли метод **ивмпконтролс. останавливаться** .                                                                                                  |



 

## <a name="property-value"></a>Значение свойства

**System.Boolean**

Значение **System. Boolean** , указывающее, доступен ли указанный тип сведений, или может быть выполнено указанное действие.

## <a name="remarks"></a>Комментарии

**Ивмпконтролс. Available** — это свойство в Visual Basic, которое принимает параметр. В C# он называется методом **ивмпконтролс. Get- \_ Available** .

## <a name="examples"></a>Примеры

В следующем примере используется свойство **Available** (метод Get- **\_ Available** в C#), чтобы убедиться, что текущий элемент мультимедиа поддерживает свойство **CurrentPosition** . Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// If the currentPosition property is supported, seek to position 0.
if (player.Ctlcontrols.get_isAvailable("currentPosition"))
{
    player.Ctlcontrols.currentPosition = 0;
}
```


```VB

' If the currentPosition property is supported, seek to position 0.
If (player.Ctlcontrols.isAvailable(&quot;currentPosition&quot;)) Then

    player.Ctlcontrols.currentPosition = 0

End If
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпконтролс (VB и C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. currentItem (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. Pause (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. Play (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. останавливаться (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPControls2. Step (VB и C#)**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md)
</dt> </dl>

 

 





