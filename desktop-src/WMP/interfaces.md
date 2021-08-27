---
title: SDK-интерфейсы WMP
description: SDK-интерфейсы WMP
ms.assetid: 68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd
keywords:
- проигрыватель Windows Media, интерфейсы
- проигрыватель Windows Media Мобильные устройства, интерфейсы
- объектная модель проигрыватель Windows Media, интерфейсы
- Объектная модель, интерфейсы
- элемент управления ActiveX, интерфейсы
- проигрыватель Windows Media ActiveX элемент управления, интерфейсы
- проигрыватель Windows Media мобильный ActiveX элемент управления, интерфейсы
- Справочник по объектной модели, интерфейсам
- Справочник по объектной модели интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7db8e5ebe29e38da9f92370f60a622fad70f36395b271eb7bd86ef49f49a3d49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123504"
---
# <a name="wmp-sdk-interfaces"></a>SDK-интерфейсы WMP

в этом разделе описываются COM-интерфейсы, предоставляемые элементом управления проигрыватель Windows Media ActiveX и элементом управления проигрыватель Windows Media Mobile ActiveX.

Методы доступа к интерфейсу **ивмпкоре** или **ивмпплайер** используются для получения конкретных интерфейсов. Эти интерфейсы, в свою очередь, могут иметь методы доступа для получения дополнительных интерфейсов. Вызов **QueryInterface** на одном из этих интерфейсов необходим только при извлечении базовой версии интерфейса и необходимости вызова метода в более поздней версии того же интерфейса.

> [!Note]  
> все методы и события полностью поддерживаются в проигрыватель Windows Media 10 Mobile и более поздних версиях, если явно не указано иное.

элемент управления проигрыватель Windows Media предоставляет следующие интерфейсы.

| Интерфейс                                                    | Описание                                                                                                                                                                               |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_вмпокксевентс](-wmpocxevents-interface.md)                | предоставляет события, происходящие из элемента управления проигрыватель Windows Media, к которому может реагировать программа внедрения.                                                                              |
| [ивмпкдром](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)                                   | Доступ к компакт-диску или DVD-диску на диске.                                                                                                                                                          |
| [ивмпкдромбурн](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)                           | Предоставляет методы для управления созданием звуковых компакт-дисков.                                                                                                                                            |
| [ивмпкдромколлектион](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)               | Обращается к коллекции дисководов компакт-дисков или дисков DVD.                                                                                                                                                |
| [ивмпкдромрип](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)                             | Предоставляет методы для управления копированием дорожек с аудио компакт-диска.                                                                                                                               |
| [ивмпклоседкаптион](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption)                   | Включает субтитры с клипом мультимедиа.                                                                                                                                                      |
| [IWMPClosedCaption2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption2)                 | Предоставляет дополнительные методы закрытой подписи.                                                                                                                                            |
| [ивмпконтролс](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)                             | представляет элементы управления транспорта для проигрыватель Windows Media, такие как воспроизведение, остановка и пауза.                                                                                                 |
| [IWMPControls2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2)                           | Предоставляет дополнительные методы управления.                                                                                                                                                      |
| [IWMPControls3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3)                           | Предоставляет дополнительные методы управления.                                                                                                                                                      |
| [ивмпкоре](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore)                                     | Получает указатели на другие интерфейсы и обращается к основным функциям элемента управления. это корневой интерфейс для проигрыватель Windows Media объектной модели.                                  |
| [IWMPCore2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore2)                                   | Предоставляет дополнительные основные методы.                                                                                                                                                         |
| [IWMPCore3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore3)                                   | Предоставляет дополнительные основные методы.                                                                                                                                                         |
| [ивмпдвд](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpdvd)                                       | Доступ к меню содержимого DVD-диска.                                                                                                                                                       |
| [ивмперрор](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperror)                                   | Обращается к коллекции указателей [ивмперроритем](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem) .                                                                                                                     |
| [ивмперроритем](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem)                           | Предоставляет сведения об ошибках.                                                                                                                                                        |
| [IWMPErrorItem2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem2)                         | Предоставляет дополнительные методы ошибочных элементов.                                                                                                                                                   |
| [ивмпевентс](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)                       | предоставляет события, происходящие из элемента управления проигрыватель Windows Media, к которому может реагировать программа внедрения.                                                                            |
| [IWMPEvents2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)                     | предоставляет события, происходящие из элемента управления проигрыватель Windows Media 10, на который может ответить программа внедрения. Эти события специально используются для программ синхронизации устройств. |
| [IWMPEvents3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)                               | Предоставляет события, связанные с копированием компакт-дисков, записью компакт-дисков, мониторингом папок и удаленными службами библиотек.                                                                                        |
| [ивмпфолдермониторсервицес](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)   | предоставляет методы для перечисления, просмотра и изменения папок файлов, которые проигрыватель Windows Media мониторы для цифрового мультимедийного содержимого.                                                                |
| [ивмпграфкреатион](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)                   | управляет графиком DirectShow.                                                                                                                                                             |
| [ивмплибрари](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)                               | Представляет библиотеку.                                                                                                                                                                     |
| [ивмплибрарисервицес](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)               | Предоставляет методы для перечисления библиотек.                                                                                                                                                  |
| [ивмплибраришарингсервицес](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices) | Предоставляет методы для управления совместным доступом к библиотеке.                                                                                                                                               |
| [ивмпмедиа](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)                                   | Задает и получает свойства элемента мультимедиа.                                                                                                                                        |
| [IWMPMedia2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia2)                                 | Предоставляет дополнительные методы для установки и получения свойств элемента мультимедиа.                                                                                                           |
| [IWMPMedia3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3)                                 | Предоставляет дополнительные методы для установки и получения свойств элемента мультимедиа.                                                                                                           |
| [ивмпмедиаколлектион](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)               | Обращается к коллекции указателей [ивмпмедиа](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) .                                                                                                                             |
| [IWMPMediaCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)             | Предоставляет методы, дополняют интерфейс **ивмпмедиаколлектион** .                                                                                                                   |
| [ивмпметадатапиктуре](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatapicture)               | Извлекает сведения об атрибуте метаданных **WM/Picture** .                                                                                                                        |
| [ивмпметадататекст](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatatext)                     | Извлекает сведения о сложных атрибутах текстовых метаданных.                                                                                                                          |
| [ивмпнетворк](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpnetwork)                               | задает и получает свойства сетевого подключения, используемого проигрыватель Windows Media.                                                                                                 |
| [ивмпплайер](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer)                                 | управляет поведением пользовательского интерфейса проигрыватель Windows Media элемента управления.                                                                                                                 |
| [IWMPPlayer2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer2)                               | предоставляет дополнительные методы для управления проигрыватель Windows Media.                                                                                                                         |
| [IWMPPlayer3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer3)                               | предоставляет дополнительные методы для управления проигрыватель Windows Media.                                                                                                                         |
| [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4)                               | предоставляет дополнительные методы для управления проигрыватель Windows Media.                                                                                                                         |
| [ивмпплайераппликатион](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication)           | переключение между удаленным проигрыватель Windows Mediaным элементом управления и полноэкранным режимом проигрывателя. Предназначен для использования программами C++, которые внедряют элемент управления в удаленный режим.                          |
| [ивмпплайерсервицес](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)                 | используется узлом удаленного элемента управления для управления полным режимом проигрыватель Windows Media. Предназначен для использования с C++.                                                                     |
| [IWMPPlayerServices2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)               | Задает приоритет фоновой обработки.                                                                                                                                                  |
| [ивмпплайлист](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)                             | Создает списки воспроизведения и управляет ими.                                                                                                                                                            |
| [ивмпплайлистаррай](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray)                   | Обращается к коллекции указателей [ивмпплайлист](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) по номеру индекса.                                                                                                       |
| [ивмпплайлистколлектион](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection)         | Управляет указателями [ивмпплайлист](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) и [ивмпплайлистаррай](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray) .                                                                                     |
| [ивмпкуери](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)                                   | Представляет составной запрос.                                                                                                                                                              |
| [ивмпремотемедиасервицес](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)       | предоставляет службы для проигрыватель Windows Media из программы, в которой размещается элемент управления проигрывателя. Предназначен для использования с C++.                                                                        |
| [ивмпрендерконфиг](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)                     | Предоставляет методы для указания или получения значения, указывающего, происходит ли воспроизведение только в текущем процессе.                                                                          |
| [ивмпсеттингс](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings)                             | задает или получает параметры проигрыватель Windows Media.                                                                                                                                          |
| [IWMPSettings2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2)                           | задает или получает параметры проигрыватель Windows Media.                                                                                                                                          |
| [ивмпскинманажер](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)                       | указывает обложку, используемую с проигрыватель Windows Media.                                                                                                                                        |
| [ивмпстрингколлектион](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)             | Обращается к коллекции строк.                                                                                                                                                         |
| [IWMPStringCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)           | Предоставляет методы, дополняют интерфейс **ивмпстрингколлектион** .                                                                                                                  |
| [ивмпсинкдевице](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)                         | представляет устройство, которое может синхронизировать цифровые файлы мультимедиа с проигрыватель Windows Media 10.                                                                                                |
| [IWMPSyncDevice2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)                       | Предоставляет метод, который дополняет интерфейс **ивмпсинкдевице** .                                                                                                                      |
| [ивмпсинксервицес](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)                     | перечисляет доступные устройства, которые могут синхронизировать цифровые файлы мультимедиа с проигрыватель Windows Media 10.                                                                                       |
| [ивмптранскодеполици](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmptranscodepolicy)               | предоставляет метод, реализуемый фильтрами источников DirectShow для управления изменением формата цифровых файлов мультимедиа.                                                                          |
| [ивмпвидеорендерконфиг](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)           | предоставляет метод, который настраивает расширенный модуль обработки видео, используемый проигрыватель Windows Media.                                                                                               |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Справочник по объектной модели для C++**](object-model-reference-for-c.md)
</dt> </dl>

 

 




