---
title: Внедрение элемента управления проигрывателя Windows Media в решение C
description: Внедрение элемента управления проигрывателя Windows Media в решение C \
ms.assetid: 0889cfd8-ed1f-4d0c-aff8-bff2f55ffccb
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX, внедрение
- Проигрыватель Windows Media, C
- Объектная модель проигрывателя Windows Media, C
- Объектная модель, C
- Проигрыватель Windows Media Mobile, C
- Элемент управления ActiveX проигрывателя Windows Media, C
- Элемент управления ActiveX проигрывателя Windows Media Mobile, C
- Элемент управления ActiveX, C
- внедрение, программы на языке C
- Внедрение программ на C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c950bed9812cea0aa6ce28995fd6998bb8417ac
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2019
ms.locfileid: "105691396"
---
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a>Внедрение элемента управления проигрывателя Windows Media в решение C#

Чтобы использовать функциональные возможности проигрывателя Windows Media в приложении C#, сначала добавьте компонент в форму, как описано в статье [использование элемента управления проигрывателя Windows Media с Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

В следующих разделах описывается создание приложения, которое воспроизводит видео, и использование настраиваемых кнопок воспроизведения и отключения.

## <a name="add-the-video-window"></a>Добавление окна видео

Добавление элемента управления ActiveX проигрывателя Windows Media в форму. Измените размер элемента управления, а затем поместите его там, где должно отображаться окно видео.

Выберите элемент управления проигрывателя Windows Media, а затем измените значение свойства **uiMode** на "нет". Этот параметр скрывает элементы управления пользовательского интерфейса. Когда пользователь воспроизводит видео, он появляется в окне. Для содержимого, поддерживающего только звук, отображается визуализация.

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



В предыдущем примере кода "axWindowsMediaPlayer1" — это имя элемента управления проигрывателя Windows Media по умолчанию, а "c: \\ mediafile. wmv" — это имя элемента мультимедиа, который необходимо воспроизвести. Можно использовать любой допустимый путь к файлу. Символ @ указывает компилятору не интерпретировать обратные косые черты как escape-символы.

Если вы добавили цифровое мультимедийное содержимое из пакета SDK проигрывателя Windows Media в библиотеку в проигрывателе Windows Media Player, можно использовать следующий код:


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



Поскольку свойство **автозапуска** по умолчанию имеет значение true, проигрыватель Windows Media начнет играть при установке свойства **куррентплайлист** или **URL** .

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
> Оболочка управляемого кода для элемента управления проигрывателя Windows Media предоставляет объект **Controls** как **ктлконтролс** , чтобы избежать конфликта со свойством **Controls** , унаследованным от **System. Windows. Forms. Control**.

 

## <a name="add-error-handling"></a>Добавление обработки ошибок

Элемент управления проигрывателя Windows Media не вызывает исключение, если возникает ошибка, например недопустимый URL-адрес. Вместо этого он сигнализирует о событии. Приложение должно поддерживать события ошибок, отправленные проигрывателем.

Чтобы создать обработчик событий, сначала откройте окно свойств для элемента управления проигрывателя Windows Media. В списке событий дважды щелкните **медиаеррор**. Отобразится следующий код:


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Внедрение элемента управления проигрывателя Windows Media в платформа .NET Framework решение**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




