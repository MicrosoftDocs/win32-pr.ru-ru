---
title: внедрение элемента управления проигрыватель Windows Media в решение C
description: внедрение элемента управления проигрыватель Windows Media в решение C \
ms.assetid: 0889cfd8-ed1f-4d0c-aff8-bff2f55ffccb
keywords:
- проигрыватель Windows Media, встраивание ActiveX элемента управления
- проигрыватель Windows Media объектная модель, встраивание ActiveX элемента управления
- объектная модель, встраивание элемента управления ActiveX
- проигрыватель Windows Media мобильный, внедренный элемент управления ActiveX
- проигрыватель Windows Media элемент управления ActiveX, внедрение
- проигрыватель Windows Media управление мобильными ActiveXми, внедрение
- элемент управления ActiveX, встраивание
- проигрыватель Windows Media, C
- объектная модель проигрыватель Windows Media, C
- Объектная модель, C
- проигрыватель Windows Media Mobile, C
- проигрыватель Windows Media ActiveX элемент управления, C
- проигрыватель Windows Media мобильный ActiveX элемент управления, C
- элемент управления ActiveX, C
- внедрение, программы на языке C
- Внедрение программ на C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a067a407fccdd78d71d9e60bc00d1eae6950e3fdaf204f886c5e96edf372eb07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901984"
---
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a>внедрение элемента управления проигрыватель Windows Media в решение C#

чтобы использовать функциональные возможности проигрыватель Windows Media в приложении C#, сначала добавьте компонент в форму, как описано в разделе [использование элемента управления проигрыватель Windows Media с Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

В следующих разделах описывается создание приложения, которое воспроизводит видео, и использование настраиваемых кнопок воспроизведения и отключения.

## <a name="add-the-video-window"></a>Добавление окна видео

добавьте элемент управления ActiveX проигрыватель Windows Media в форму. Измените размер элемента управления, а затем поместите его там, где должно отображаться окно видео.

выберите элемент управления проигрыватель Windows Media, а затем измените значение свойства **uiMode** на «none». Этот параметр скрывает элементы управления пользовательского интерфейса. Когда пользователь воспроизводит видео, он появляется в окне. Для содержимого, поддерживающего только звук, отображается визуализация.

## <a name="add-two-buttons-and-adjust-the-form"></a>Добавление двух кнопок и настройка формы

Теперь добавьте две кнопки в форму. Нажмите первую кнопку и измените свойство **Text** на Play. Нажмите вторую кнопку и измените ее свойство **Text** на «останавливаться».

## <a name="add-the-play-code"></a>Добавление кода воспроизведения

Дважды щелкните кнопку **Воспроизведение** , чтобы открыть окно кода. В C# отобразится следующий код:


```CSharp
private void button1_Click(object sender, System.EventArgs e)
{

}

```



Добавьте следующую строку между двумя фигурными скобками:


```CSharp
axWindowsMediaPlayer1.URL = @"c:\mediafile.wmv";

```



в предыдущем примере кода «axWindowsMediaPlayer1» является именем по умолчанию для элемента управления проигрыватель Windows Media, а «c: \\ mediafile. wmv» — заполнитель имени элемента мультимедиа, который требуется воспроизвести. Можно использовать любой допустимый путь к файлу. Символ @ указывает компилятору не интерпретировать обратные косые черты как escape-символы.

если вы добавили цифровое мультимедийное содержимое из пакета SDK для проигрыватель Windows Media в библиотеку в проигрыватель Windows Media, вы можете использовать этот код.


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



поскольку свойство **автозапуска** по умолчанию имеет значение true, проигрыватель Windows Media начнет воспроизводиться при установке свойства **куррентплайлист** или **URL** .

## <a name="add-the-stop-code"></a>Добавление кода завершения

Дважды щелкните кнопку " **Закрыть** ", чтобы открыть окно кода. В C# отобразится следующий код:


```CSharp
private void button2_Click(object sender, System.EventArgs e)
{

}

```



Добавьте следующую строку между двумя фигурными скобками:


```CSharp
axWindowsMediaPlayer1.Ctlcontrols.stop();

```



> [!Note]  
> оболочка управляемого кода для элемента управления проигрыватель Windows Media предоставляет объект **controls** как **ктлконтролс** , чтобы избежать конфликта со свойством **controls** , унаследованным от **System. Windows. Forms. Control**.

 

## <a name="add-error-handling"></a>Добавление обработки ошибок

элемент управления проигрыватель Windows Media не создает исключение, если возникает ошибка, например недопустимый URL-адрес. Вместо этого он сигнализирует о событии. Приложение должно поддерживать события ошибок, отправленные проигрывателем.

чтобы создать обработчик событий, сначала откройте окно свойств для элемента управления проигрыватель Windows Media. В списке событий дважды щелкните **медиаеррор**. Отобразится следующий код:


```CSharp
private void Player_MediaError(object sender, _WMPOCXEvents_MediaErrorEvent e)
{
}

```



Следующий код можно вставить в метод, чтобы обеспечить минимальную возможность обработки ошибок. Обратите внимание, что сведения об ошибке можно получить из аргумента **\_ \_ медиаерроревент вмпокксевентс** .


```CSharp
try
// If the Player encounters a corrupt or missing file, 
// show the hexadecimal error code and URL.
{
    IWMPMedia2 errSource = e.pMediaObject as IWMPMedia2;
    IWMPErrorItem errorItem = errSource.Error;
    MessageBox.Show("Error " + errorItem.errorCode.ToString("X") 
                    + " in " + errSource.sourceURL);
}
catch(InvalidCastException)
// In case pMediaObject is not an IWMPMedia item.
{
    MessageBox.Show("Error.");
} 

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**внедрение элемента управления проигрыватель Windows Media в платформа .NET Framework решение**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




