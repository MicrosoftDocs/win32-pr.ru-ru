---
title: Объект AxWindowsMediaPlayer (VB и C)
description: Объект Аксвиндовсмедиаплайер (VB и C)
ms.assetid: d7eeac20-1afa-4e73-9af6-9772fbb65516
keywords:
- Проигрыватель Windows Media, объект Аксвиндовсмедиаплайер
- Проигрыватель Windows Media Mobile, объект Аксвиндовсмедиаплайер
- Объектная модель проигрывателя Windows Media, объект Аксвиндовсмедиаплайер
- Объектная модель, объект Аксвиндовсмедиаплайер
- Элемент управления ActiveX, объект Аксвиндовсмедиаплайер
- Элемент управления ActiveX проигрывателя Windows Media, объект Аксвиндовсмедиаплайер
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, объект Аксвиндовсмедиаплайер
- Справочник по объектной модели, объекту Аксвиндовсмедиаплайер
- Объект Аксвиндовсмедиаплайер
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32f814560c8b6eb13dc5abb8736378432ec4565e
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "104487372"
---
# <a name="axwindowsmediaplayer-object-vb-and-c"></a>Объект Аксвиндовсмедиаплайер (VB и C#)

Объект Аксвиндовсмедиаплайер является корневым объектом для элемента управления проигрывателя Windows Media. Он поддерживает свойства, методы и события, перечисленные в следующих таблицах.

Объект Аксвиндовсмедиаплайер поддерживает следующие свойства:



| Свойство                                                                             | Описание                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [кдромколлектион](axwmplib-axwindowsmediaplayer-cdromcollection--vb-and-c.md)       | Возвращает интерфейс **ивмпкдромколлектион** .                                                                                         |
| [клоседкаптион](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md)           | Возвращает интерфейс Ивмпклоседкаптион.                                                                                               |
| [ктлконтролс](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md)               | Возвращает интерфейс Ивмпконтролс.                                                                                                    |
| [ктленаблед](axwmplib-axwindowsmediaplayer-ctlenabled--vb-and-c.md)                 | Возвращает или задает значение, указывающее, включен ли элемент управления проигрывателя Windows Media.                                               |
| [куррентмедиа](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)             | Возвращает или задает интерфейс Ивмпмедиа, соответствующий текущему элементу мультимедиа.                                                   |
| [куррентплайлист](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)       | Возвращает или задает текущий интерфейс **ивмпплайлист** .                                                                               |
| [оптически](axwmplib-axwindowsmediaplayer-dvd--vb-and-c.md)                               | Возвращает интерфейс ИВМПДВД.                                                                                                         |
| [енаблеконтекстмену](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)   | Возвращает или задает значение, указывающее, следует ли включать контекстное меню, которое появляется при нажатии правой кнопки мыши.          |
| [Ошибка](axwmplib-axwindowsmediaplayer-error--vb-and-c.md)                           | Возвращает интерфейс Ивмперрор.                                                                                                       |
| [fullScreen](axwmplib-axwindowsmediaplayer-fullscreen--vb-and-c.md)                 | Возвращает или задает значение, указывающее, воспроизводится ли содержимое видео в полноэкранном режиме.                                          |
| [Подключение к Интернету](axwmplib-axwindowsmediaplayer-isonline--vb-and-c.md)                     | Возвращает значение, указывающее, подключен ли пользователь к сети.                                                                |
| Удаленный                                                                             | Не поддерживается для программирования .NET.                                                                                                |
| [медиаколлектион](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)       | Возвращает интерфейс Ивмпмедиаколлектион.                                                                                             |
| [сети](axwmplib-axwindowsmediaplayer-network--vb-and-c.md)                       | Возвращает интерфейс Ивмпнетворк.                                                                                                     |
| [опенстате](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)                   | Возвращает значение, указывающее состояние источника содержимого.                                                                           |
| плайераппликатион                                                                    | Не поддерживается для программирования .NET.                                                                                                |
| [плайлистколлектион](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) | Возвращает интерфейс Ивмпплайлистколлектион.                                                                                          |
| [плайстате](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)                   | Возвращает значение, указывающее состояние операции проигрывателя Windows Media.                                                           |
| [параметры](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)                     | Возвращает интерфейс Ивмпсеттингс.                                                                                                    |
| [status](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)                         | Возвращает значение, указывающее текущее состояние проигрывателя Windows Media.                                                                |
| [стретчтофит](axwmplib-axwindowsmediaplayer-stretchtofit--vb-and-c.md)             | Возвращает или задает значение, указывающее, будет ли видео растягиваться по размеру экрана элемента управления проигрывателя Windows Media.          |
| [uiMode](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)                         | Возвращает или задает значение, указывающее, какие элементы управления отображаются в пользовательском интерфейсе при внедрении проигрывателя Windows Media на веб-страницу. |
| [URL-адрес](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)                               | Возвращает или задает имя клипа для воспроизведения.                                                                                         |
| [versionInfo](axwmplib-axwindowsmediaplayer-versioninfo--vb-and-c.md)               | Возвращает значение, указывающее версию проигрывателя Windows Media.                                                               |
| [виндовлессвидео](axwmplib-axwindowsmediaplayer-windowlessvideo--vb-and-c.md)       | Возвращает или задает значение, указывающее, визуализирует ли элемент управления проигрывателем Windows Media видео в режиме без окон.                         |



 

Объект Аксвиндовсмедиаплайер поддерживает следующие методы.



| Метод                                                       | Описание                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| [close](axwmplib-axwindowsmediaplayer-close.md)             | Освобождает ресурсы проигрывателя Windows Media.                  |
| [лаунчурл](axwmplib-axwindowsmediaplayer-launchurl.md)     | Отправляет URL-адрес браузера пользователя по умолчанию для подготовки к просмотру. |
| [невмедиа](axwmplib-axwindowsmediaplayer-newmedia.md)       | Возвращает интерфейс Ивмпмедиа для нового элемента мультимедиа.      |
| [невплайлист](axwmplib-axwindowsmediaplayer-newplaylist.md) | Возвращает интерфейс Ивмпплайлист для нового списка воспроизведения.     |
| [опенплайер](axwmplib-axwindowsmediaplayer-openplayer.md)   | Открывает проигрыватель Windows Media с использованием указанного URL-адреса.       |



 

Объект Аксвиндовсмедиаплайер поддерживает следующие события.



| Событие                                                                                                              | Описание                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [аудиолангуажечанже](axwmplib-axwindowsmediaplayer-audiolanguagechange.md)                                       | Происходит при изменении текущего звукового языка.                                                            |
| [ответов](axwmplib-axwindowsmediaplayer-buffering.md)                                                           | Происходит при начале или окончании буферизации элементом управления проигрывателя Windows Media.                                     |
| [кдромбурнеррор](axwmplib-axwindowsmediaplayer-cdromburnerror.md)                                                 | Происходит при возникновении общей ошибки во время операции записи на компакт-диск.                                         |
| [кдромбурнмедиаеррор](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)                                       | Происходит при возникновении ошибки при записи отдельного элемента мультимедиа на компакт-диск.                               |
| [кдромбурнстатечанже](axwmplib-axwindowsmediaplayer-cdromburnstatechange.md)                                     | Происходит при изменении состояния операции записи компакт-диска.                                                          |
| [кдроммедиачанже](axwmplib-axwindowsmediaplayer-cdrommediachange.md)                                             | Происходит, когда компакт-диск или DVD-диск вставлен или извлечен с компакт-диска или DVD-дисковода.                                |
| [кдромрипмедиаеррор](axwmplib-axwindowsmediaplayer-cdromripmediaerror.md)                                         | Происходит при возникновении ошибки при копировании отдельной дорожки с компакт-диска.                                  |
| [кдромрипстатечанже](axwmplib-axwindowsmediaplayer-cdromripstatechange.md)                                       | Происходит при изменении состояния операции копирования компакт-диска.                                                          |
| [Щелчок](axwmplib-axwindowsmediaplayer-click.md)                                                                   | Происходит, когда пользователь нажимает кнопку мыши.                                                                |
| креатепартнершипкомплете                                                                                          | Не поддерживается для программирования .NET.                                                                        |
| [куррентитемчанже](axwmplib-axwindowsmediaplayer-currentitemchange.md)                                           | Происходит при изменении [ивмпконтролс. currentItem](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md) . |
| [куррентмедиаитемаваилабле](axwmplib-axwindowsmediaplayer-currentmediaitemavailable.md)                           | Возникает, когда элемент метаданных в текущем элементе мультимедиа станет доступным.                           |
| [куррентплайлистчанже](axwmplib-axwindowsmediaplayer-currentplaylistchange.md)                                   | Происходит при изменении в текущем списке воспроизведения.                                                 |
| [куррентплайлиститемаваилабле](axwmplib-axwindowsmediaplayer-currentplaylistitemavailable.md)                     | Происходит, когда текущий элемент списка воспроизведения станет доступным.                                                   |
| DeviceConnect                                                                                                      | Не поддерживается для программирования .NET.                                                                        |
| девицедисконнект                                                                                                   | Не поддерживается для программирования .NET.                                                                        |
| девицестатусчанже                                                                                                 | Не поддерживается для программирования .NET.                                                                        |
| девицесинцеррор                                                                                                    | Не поддерживается для программирования .NET.                                                                        |
| девицесинкстатечанже                                                                                              | Не поддерживается для программирования .NET.                                                                        |
| [Отключение](axwmplib-axwindowsmediaplayer-disconnect.md)                                                         | Зарезервировано для последующего использования.                                                                                   |
| [домаинчанже](axwmplib-axwindowsmediaplayer-domainchange.md)                                                     | Происходит при изменении домена DVD.                                                                        |
| [DoubleClick](axwmplib-axwindowsmediaplayer-doubleclick.md)                                                       | Происходит, когда пользователь дважды щелкает кнопку мыши.                                                         |
| [дуратионунитчанже](axwmplib-axwindowsmediaplayer-durationunitchange.md)                                         | Зарезервировано для последующего использования.                                                                                   |
| [EndOfStream](axwmplib-axwindowsmediaplayer-endofstream.md)                                                       | Зарезервировано для последующего использования.                                                                                   |
| [Ошибка](axwmplib-axwindowsmediaplayer-error.md)                                                                   | Происходит, когда элемент управления проигрывателя Windows Media имеет условие ошибки.                                       |
| [фолдерсканстатечанже](axwmplib-axwindowsmediaplayer-folderscanstatechange.md)                                   | Происходит при изменении состояния операции наблюдения за папками.                                                   |
| [KeyDown](axwmplib-axwindowsmediaplayer-keydown.md)                                                               | Вызывается при нажатии клавиши.                                                                              |
| [Бытии](axwmplib-axwindowsmediaplayer-keypress.md)                                                             | Происходит при нажатии клавиши, а затем при ее освобождении.                                                            |
| [KeyUp](axwmplib-axwindowsmediaplayer-keyup.md)                                                                   | Вызывается при отпускании клавиши.                                                                             |
| [либрариконнект](axwmplib-axwindowsmediaplayer-libraryconnect.md)                                                 | Происходит, когда библиотека станет доступной.                                                                   |
| [либраридисконнект](axwmplib-axwindowsmediaplayer-librarydisconnect.md)                                           | Происходит, когда библиотека больше недоступна.                                                              |
| [маркерхит](axwmplib-axwindowsmediaplayer-markerhit.md)                                                           | Происходит при достижении маркера.                                                                           |
| [медиачанже](axwmplib-axwindowsmediaplayer-mediachange.md)                                                       | Происходит при изменении элемента мультимедиа.                                                                          |
| [медиаколлектионаттрибутестрингаддед](axwmplib-axwindowsmediaplayer-mediacollectionattributestringadded.md)       | Происходит при добавлении значения атрибута в библиотеку.                                                    |
| [медиаколлектионаттрибутестрингчанжед](axwmplib-axwindowsmediaplayer-mediacollectionattributestringchanged.md)   | Происходит при изменении значения атрибута в библиотеке.                                                  |
| [медиаколлектионаттрибутестрингремовед](axwmplib-axwindowsmediaplayer-mediacollectionattributestringremoved.md)   | Происходит при удалении значения атрибута из библиотеки.                                                |
| [медиаколлектиончанже](axwmplib-axwindowsmediaplayer-mediacollectionchange.md)                                   | Происходит при изменении коллекции носителей.                                                                  |
| [медиаколлектионмедиааддед](axwmplib-axwindowsmediaplayer-mediacollectionmediaadded.md)                           | Происходит при добавлении элемента мультимедиа в локальную библиотеку.                                                    |
| [медиаколлектионмедиаремовед](axwmplib-axwindowsmediaplayer-mediacollectionmediaremoved.md)                       | Происходит при удалении элемента мультимедиа из локальной библиотеки.                                                |
| [медиаеррор](axwmplib-axwindowsmediaplayer-mediaerror.md)                                                         | Происходит, когда объект **мультимедиа** имеет условие ошибки.                                                   |
| [модечанже](axwmplib-axwindowsmediaplayer-modechange.md)                                                         | Происходит при изменении режима проигрывателя Windows Media.                                                     |
| [Вниз](axwmplib-axwindowsmediaplayer-mousedown.md)                                                           | Происходит при нажатии кнопки мыши.                                                                     |
| [Событие](axwmplib-axwindowsmediaplayer-mousemove.md)                                                           | Происходит при перемещении указателя мыши.                                                                    |
| [Кнопка](axwmplib-axwindowsmediaplayer-mouseup.md)                                                               | Происходит при отпускании кнопки мыши.                                                                    |
| [невстреам](axwmplib-axwindowsmediaplayer-newstream.md)                                                           | Зарезервировано для последующего использования.                                                                                   |
| [опенплайлистсвитч](axwmplib-axwindowsmediaplayer-openplaylistswitch.md)                                         | Происходит, когда начинается воспроизведение заголовка DVD-диска.                                                               |
| [опенстатечанже](axwmplib-axwindowsmediaplayer-openstatechange.md)                                               | Происходит при изменении состояния элемента управления проигрывателя Windows Media.                                                |
| плайердоккедстатечанже                                                                                            | Не поддерживается для программирования .NET.                                                                        |
| плайерреконнект                                                                                                    | Не поддерживается для программирования .NET.                                                                        |
| [плайлистчанже](axwmplib-axwindowsmediaplayer-playlistchange.md)                                                 | Происходит при изменении списка воспроизведения.                                                                            |
| [плайлистколлектиончанже](axwmplib-axwindowsmediaplayer-playlistcollectionchange.md)                             | Происходит при внесении каких-либо изменений в коллекцию списков воспроизведения.                                                  |
| [плайлистколлектионплайлистаддед](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistadded.md)               | Происходит при добавлении списка воспроизведения в коллекцию списков воспроизведения.                                                |
| [плайлистколлектионплайлистремовед](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistremoved.md)           | Происходит при удалении списка воспроизведения из коллекции списков воспроизведения.                                            |
| [плайлистколлектионплайлистсетасделетед](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistsetasdeleted.md) | Зарезервировано для последующего использования.                                                                                   |
| [плайстатечанже](axwmplib-axwindowsmediaplayer-playstatechange.md)                                               | Происходит при изменении состояния воспроизведения элемента управления проигрывателя Windows Media.                                    |
| [поситиончанже](axwmplib-axwindowsmediaplayer-positionchange.md)                                                 | Происходит при изменении текущей позиции элемента мультимедиа.                                       |
| [ScriptCommand](axwmplib-axwindowsmediaplayer-scriptcommand.md)                                                   | Происходит при получении синхронизированной команды или URL-адреса.                                                     |
| [StatusChange](axwmplib-axwindowsmediaplayer-statuschange.md)                                                     | Происходит при изменении значения свойства **Status** .                                                         |
| [стрингколлектиончанже](axwmplib-axwindowsmediaplayer-stringcollectionchange.md)                                 | Происходит при изменении коллекции строк.                                                                   |
| свитчедтоконтрол                                                                                                  | Не поддерживается для программирования .NET.                                                                        |
| свитчедтоплайераппликатион                                                                                        | Не поддерживается для программирования .NET.                                                                        |
| [Предупреждение](axwmplib-axwindowsmediaplayer-warning.md)                                                               | Зарезервировано для последующего использования.                                                                                   |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейсы для Visual Basic .NET и C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпкдромколлектион (VB и C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпклоседкаптион (VB и C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпконтролс (VB и C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Интерфейс ИВМПДВД (VB и C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмперрор (VB и C#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпмедиаколлектион (VB и C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпнетворк (VB и C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпплайлист (VB и C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпплайлистколлектион (VB и C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпсеттингс (VB и C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Справочник по объектной модели для Visual Basic .NET и C #**](object-model-reference-for-visual-basic--net-and-c.md)
</dt> <dt>

[**вмпопенстате**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> <dt>

[**вмпплайстате**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 




