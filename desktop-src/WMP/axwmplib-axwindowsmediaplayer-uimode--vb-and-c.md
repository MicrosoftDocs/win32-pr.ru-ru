---
title: Аксвиндовсмедиаплайер. uiMode, свойство
description: Свойство uiMode получает или задает значение, указывающее, какие элементы управления отображаются в пользовательском интерфейсе.
ms.assetid: 01034418-be70-44f3-8812-e529c747c9e4
keywords:
- проигрыватель Windows Media свойства uiMode
- проигрыватель Windows Media свойства uiMode, класс аксвиндовсмедиаплайер
- проигрыватель Windows Media класса аксвиндовсмедиаплайер, свойство uiMode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.uiMode
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f1d716d36aafbd3625ae1144e0adde1abf0898bee4cbe6831d627cea97bb9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618774"
---
# <a name="axwindowsmediaplayeruimode-property"></a>Аксвиндовсмедиаплайер. uiMode, свойство

Свойство uiMode получает или задает значение, указывающее, какие элементы управления отображаются в пользовательском интерфейсе.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String uiMode {get; set;}
```


```VB

Public Property uiMode As System.String
```





## <a name="property-value"></a>Значение свойства

Строка System. String, которая является одним из следующих значений.



| Значение     | Описание                                                                                                                                                                                                     | Пример звука                                                   | Пример видео                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------|
| невидимые | проигрыватель Windows Media внедряется без видимого пользовательского интерфейса (элементы управления, видео или окна визуализации).                                                                                                  | (Ничего не отображается.)                                         | (Ничего не отображается.)                                         |
| нет      | проигрыватель Windows Media внедряется без элементов управления и только с отображением окна видео или визуализации.                                                                                                   | ![UIMODE = "нет" с аудио](images/uimode-none-audio-v11.png) | ![UIMODE = "нет" с видео](images/uimode-none-video-v11.png) |
| Mini      | проигрыватель Windows Media внедряется в окно состояния, воспроизведение/пауза, остановка, отключение звука и элементы управления громкостью, отображаемые в дополнение к окну видео или визуализации.                                                    | ![UIMODE = ' Мини ' с аудио](images/uimode-mini-audio-v11.png) | ![UIMODE = ' Мини ' с видео](images/uimode-mini-video-v11.png) |
| переполненные      | По умолчанию. в дополнение к окну видео или визуализации проигрыватель Windows Media внедряется в окно состояния, строку поиска, воспроизведение/пауза, остановить, выключить звук, далее, назад, вперед, назад, а также элементы управления громкостью. | ![UIMODE = ' Full ' с аудио](images/uimode-full-audio-v11.png) | ![UIMODE = ' Full ' с видео](images/uimode-full-video-v11.png) |
| пользовательский    | проигрыватель Windows Media внедряется с настраиваемым пользовательским интерфейсом. Может использоваться только в программах на C++.                                                                                                                | (Отображается настраиваемый пользовательский интерфейс.)                           | (Отображается настраиваемый пользовательский интерфейс.)                           |



 

## <a name="remarks"></a>Remarks

это свойство определяет внешний вид внедренного проигрыватель Windows Media. Если для **uiMode** задано значение "нет", "Мини-" или "полная", то для отображения видеороликов и визуализаций звука имеется окно. Это окно можно скрыть в свернутом или полном режиме, установив атрибут **Height** тега **объекта** равным 40, который измеряется снизу, и оставляет часть элементов управления видимой. Если внедренный интерфейс не нужен, задайте для атрибутов **Width** и **Height** нулевое значение.

Если для **uiMode** задано значение "Невидимый", Пользовательский интерфейс не отображается, но пространство на странице все еще зарезервировано, как указано **шириной** и **высотой**. Это полезно для того, чтобы хранить макет страницы, когда **uiMode** может измениться. Кроме того, зарезервированное пространство прозрачно, поэтому все элементы, расположенные позади элемента управления, будут видимы.

если для **uiMode** задано значение full или mini, проигрыватель Windows Media отображает элементы управления передачей в полноэкранном режиме. Если для **uiMode** задано значение "нет", никакие элементы управления не отображаются в полноэкранном режиме.

если окно является видимым и воспроизводится звуковое содержимое, отображаемая визуализация будет последней в проигрыватель Windows Media.

Если для **uiMode** задано значение Custom в программе C++, которая реализует **ивмпремотемедиасервицес**, отображается файл обложки, указанный в **ивмпремотемедиасервицес. жеткустомуимоде** .

во время воспроизведения в полноэкранном режиме проигрыватель Windows Media скрывает курсор мыши, когда **енаблеконтекстмену** равняется false, а **uiMode** равно "none".

## <a name="examples"></a>Примеры

в следующем примере создается список, позволяющий пользователю изменить режим пользовательского интерфейса для внедренного объекта проигрыватель Windows Media. Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.


```CSharp
// Load the list box with the four UI mode options.
uiModeOptions.Items.Add("invisible");
uiModeOptions.Items.Add("none");
uiModeOptions.Items.Add("mini");
uiModeOptions.Items.Add("full");


private void uiModeOptions_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Get the selected UI mode in the list box as a string.
    string newMode = (string)(((System.Windows.Forms.ListBox)sender).SelectedItem);
     
    // Set the UI mode that the user selected.
    player.uiMode = newMode;            
}
```


```VB

' Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible&quot;)
uiModeOptions.Items.Add(&quot;none&quot;)
uiModeOptions.Items.Add(&quot;mini&quot;)
uiModeOptions.Items.Add(&quot;full&quot;)


Public Sub uiModeOptions_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles uiModeOptions.SelectedIndexChanged

    &#39; Get the selected UI mode in the list box as a string.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim newMode As String = lb.SelectedItem

    &#39; Set the UI mode that the user selected.
    player.uiMode = newMode

End Sub
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media версии 7,0 или более поздней. проигрыватель Windows Media 9 Series или более поздней версии для "невидимый" или "пользовательский"<br/>   |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Аксвиндовсмедиаплайер. Енаблеконтекстмену (VB и C#)**](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)
</dt> </dl>

 

 





