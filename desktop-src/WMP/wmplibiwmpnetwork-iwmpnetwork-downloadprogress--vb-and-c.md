---
title: Ивмпнетворк Довнлоадпрогресс, свойство
description: Свойство Довнлоадпрогресс Возвращает процент завершенной загрузки.
ms.assetid: 40568c81-5bb5-45d9-b654-31072608663d
keywords:
- проигрыватель Windows Media свойства довнлоадпрогресс
- проигрыватель Windows Media свойства довнлоадпрогресс, интерфейс ивмпнетворк
- проигрыватель Windows Media интерфейса ивмпнетворк, свойство довнлоадпрогресс
topic_type:
- apiref
api_name:
- IWMPNetwork.downloadProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96c2b47895d595a570191d9aa66b90b1cdc53392f8f111d64307074e5689f2ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331983"
---
# <a name="iwmpnetworkdownloadprogress-property"></a>Ивмпнетворк: свойство Овнлоадпрогресс:d

Свойство **довнлоадпрогресс** Возвращает процент завершенной загрузки.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 downloadProgress {get; set;}
```


```VB

Public ReadOnly Property downloadProgress As System.Int32
```





## <a name="property-value"></a>Значение свойства

Объект **System. Int32** , который является процессом загрузки, выраженный в процентах.

## <a name="remarks"></a>Remarks

если элемент управления проигрыватель Windows Media подключен к цифровому файлу мультимедиа, который можно воспроизвести и скачать одновременно, свойство **довнлоадпрогресс** возвращает процент общего файла, который был скачан. В настоящее время эта функция поддерживается только для цифровых файлов мультимедиа, скачанных с веб-серверов. Файл любого из следующих форматов можно скачать и воспроизвести одновременно:

-   Advanced Systems Format (ASF)
-   Звуковые файлы в формате WMA
-   Видеофайлы в формате WMV
-   MP3
-   КОДИРОВЩИК
-   WAV

Кроме того, некоторые файлы AVI можно загружать и воспроизводить одновременно.

Используйте **аксвиндовсмедиаплайер. \_ Вмпокксевентс \_ буфферинжевент** , чтобы определить, когда буферизация начинается или останавливается.

## <a name="examples"></a>Примеры

В следующем примере кода используется **довнлоадпрогресс** для показа процента завершенной загрузки. Сведения отображаются в метке в ответ на событие **буферизации** . В примере для обновления экрана используется таймер с интервалом в 1 секунду. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Determine whether buffering has started or stopped.
    if (e.start == true)
    {
        // Set the timer interval at one second (1000 miliseconds).
        timer.Interval = 1000;
        
        // Start the timer.
        timer.Start();
    }
    else
    {
        // Buffering is complete. Stop the timer.
        timer.Stop();
    }
}

// Update the download progress in a timer event handler.
private void UpdateDownloadProgress(object sender, EventArgs e)
{
    downloadProgressLabel.Text = ("Download progress: " + player.network.downloadProgress + " percent complete");
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Test whether packets may be arriving.
    Select Case e.newState

    &#39; If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
    &#39; or Transitioning then stop the timer. 
        Case 1
        Case 2
        Case 4
        Case 5
        Case 7
        Case 8
        Case 9
            timer.Stop()

        &#39; If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        Case Else
            timer.Interval = 1000
            timer.Start()

    End Select

End Sub

&#39; Update the download progress in a timer event handler.
Public Sub UpdateDownloadProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    downloadProgressLabel.Text = (&quot;Download progress: &quot; + player.network.downloadProgress + &quot; percent complete&quot;)

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

[**Событие Аксвиндовсмедиаплайер. Buffering (VB и C#)**](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[**Интерфейс Ивмпнетворк (VB и C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





