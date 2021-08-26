---
title: Свойство Ивмпсеттингс Rate
description: Свойство Rate Возвращает или задает текущую скорость воспроизведения видео.
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- свойство rate проигрыватель Windows Media
- свойство rate проигрыватель Windows Media, интерфейс ивмпсеттингс
- интерфейс ивмпсеттингс проигрыватель Windows Media, свойство rate
topic_type:
- apiref
api_name:
- IWMPSettings.rate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc053861b9061df676455e10b011cd0ffe0fe9f06052b129ec163e00d4c8d71f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999704"
---
# <a name="iwmpsettingsrate-property"></a>Свойство Ивмпсеттингс:: Rate

Свойство **Rate** Возвращает или задает текущую скорость воспроизведения видео.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a>Значение свойства

Значение **System. Double** , которое является скоростью воспроизведения и значением по умолчанию 1,0.

## <a name="remarks"></a>Remarks

Значение, полученное этим свойством, выступает в качестве значения множителя, которое позволяет воспроизводить элемент мультимедиа с более высокой или низкой скоростью. Значение по умолчанию 1,0 указывает на созданную скорость.

Обратите внимание, что звуковая дорожка будет трудной для понимания на скорости ниже 0,5 или выше 1,5. Скорость воспроизведения 2 означает удвоенную нормальную скорость воспроизведения.

проигрыватель Windows Media попытается использовать наиболее эффективный из следующих четырех режимов воспроизведения.

-   Плавное воспроизведение видео с пошаговым сопровождением
-   Плавное воспроизведение видео с пошаговой звука не поддерживается
-   Плавное воспроизведение видео без звука
-   Воспроизведение видео опорного кадра без звука

режим, выбранный проигрыватель Windows Media, зависит от множества факторов, включая тип файла и расположение, операционную систему, сеть и сервер.

Кроме того, в зависимости от формата цифрового мультимедиа, используемого для создания содержимого, также применяются и другие соображения.

-   **Windows Мультимедиа-видео (WMV) и ASF.** Оптимальные значения для свойства **Rate** : от 1 до 10 или от 1 до 10 для обратного воспроизведения. Значения от 0,5 до 1,0 или от-0,5 до-1,0 могут также работать в случаях, когда может поддерживаться тон звука, например при воспроизведении файлов, расположенных на локальном компьютере. Значения с абсолютной величиной больше 10 допускаются, но не очень важны.
-   **Другие форматы видео.** Свойство **Rate** может принимать значения от 0 до 9. Отрицательные значения не допускаются. Значения меньше 1 представляют медленное движение. Значения, указанные выше 9, разрешены, но не очень важны.

Метод **ивмпконтролс. фастфорвард** изменяет значение **Rate** на 5,0, а метод **ивмпконтролс. фастреверсе** изменяет значение **Rate** на 5,0.

Скорость воспроизведения некоторых форматов мультимедиа не может быть изменена. Используйте свойство **ивмпсеттингс.** Ивмпсеттингс (в C# метод **. Get- \_ Available** ), чтобы определить, можно ли указать это свойство для конкретного элемента мультимедиа.

## <a name="examples"></a>Примеры

В следующем примере используется числовой элемент управления, который позволяет пользователю изменить скорость воспроизведения текущего носителя. Когда пользователь нажимает стрелки вверх или вниз элемента управления, свойству **Rate** присваивается новое значение. Возможный диапазон значений в элементе управления — 0,5 (половинная скорость) 2,0 (двойная скорость). Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void playbackRate_Click(object sender, System.EventArgs e)
{
    // Get the new value of the control, and cast it from decimal to double.
    double newRate = (double)((System.Windows.Forms.NumericUpDown)sender).Value;

    // Test whether playback rate can be set. 
    if( player.settings.get_isAvailable("Rate") )
    {
        // Set the playback rate to the new value.
        player.settings.rate = newRate;
    }
}
```


```VB

Public Sub playbackRate_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playbackRate.Click

    &#39;  Get the new value of the control as a double.
    Dim nUpDown As System.Windows.Forms.NumericUpDown = sender
    Dim newRate As Double = nUpDown.Value

    &#39;  Test whether playback rate can be set. 
    If (player.settings.isAvailable(&quot;Rate&quot;)) Then

        &#39;  Set the playback rate to the new value.
        player.settings.rate = newRate

    End If

End Sub
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ивмпконтролс. Фастфорвард (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. Фастреверсе (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпсеттингс (VB и C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. доступ (VB и C#)**](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. выкл. (VB и C#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 





