---
title: SDK-интерфейсы WMP
description: SDK-интерфейсы WMP
ms.assetid: 68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd
keywords:
- Проигрыватель Windows Media, интерфейсы
- Проигрыватель Windows Media Mobile, интерфейсы
- Объектная модель проигрывателя Windows Media, интерфейсы
- Объектная модель, интерфейсы
- Элемент управления ActiveX, интерфейсы
- Элемент управления ActiveX проигрывателя Windows Media, интерфейсы
- Элемент управления ActiveX проигрывателя Windows Media для мобильных устройств, интерфейсы
- Справочник по объектной модели, интерфейсам
- Справочник по объектной модели интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffff5a4c609d13d84972989ac32dae1600f5f02d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414433"
---
# <a name="wmp-sdk-interfaces"></a>SDK-интерфейсы WMP

В этом разделе описываются COM-интерфейсы, предоставляемые элементом управления ActiveX проигрывателя Windows Media и мобильным элементом управления ActiveX проигрывателя Windows Media.

Методы доступа к интерфейсу **ивмпкоре** или **ивмпплайер** используются для получения конкретных интерфейсов. Эти интерфейсы, в свою очередь, могут иметь методы доступа для получения дополнительных интерфейсов. Вызов **QueryInterface** на одном из этих интерфейсов необходим только при извлечении базовой версии интерфейса и необходимости вызова метода в более поздней версии того же интерфейса.

> [!Note]  
> Все методы и события полностью поддерживаются в проигрывателе Windows Media 10 Mobile и более поздних версиях, если явно не указано иное.

Элемент управления проигрывателя Windows Media предоставляет следующие интерфейсы.

| Интерфейс                                                    | Описание                                                                                                                                                                               |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_вмпокксевентс](-wmpocxevents-interface.md)                | Предоставляет события, происходящие из элемента управления проигрывателя Windows Media, на который может ответить программа внедрения.                                                                              |
| [ивмпкдром](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)                                   | Доступ к компакт-диску или DVD-диску на диске.                                                                                                                                                          |
| [ивмпкдромбурн](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)                           | Предоставляет методы для управления созданием звуковых компакт-дисков.                                                                                                                                            |
| [ивмпкдромколлектион](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)               | Обращается к коллекции дисководов компакт-дисков или дисков DVD.                                                                                                                                                |
| [ивмпкдромрип](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)                             | Предоставляет методы для управления копированием дорожек с аудио компакт-диска.                                                                                                                               |
| [ивмпклоседкаптион](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption)                   | Включает субтитры с клипом мультимедиа.                                                                                                                                                      |
| [IWMPClosedCaption2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption2)                 | Предоставляет дополнительные методы закрытой подписи.                                                                                                                                            |
| [ивмпконтролс](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)                             | Представляет элементы управления транспорта Windows Media Player, такие как воспроизведение, остановка и пауза.                                                                                                 |
| [IWMPControls2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2)                           | Предоставляет дополнительные методы управления.                                                                                                                                                      |
| [IWMPControls3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3)                           | Предоставляет дополнительные методы управления.                                                                                                                                                      |
| [ивмпкоре](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore)                                     | Получает указатели на другие интерфейсы и обращается к основным функциям элемента управления. Это корневой интерфейс для объектной модели проигрывателя Windows Media.                                  |
| [IWMPCore2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore2)                                   | Предоставляет дополнительные основные методы.                                                                                                                                                         |
| [IWMPCore3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore3)                                   | Предоставляет дополнительные основные методы.                                                                                                                                                         |
| [ивмпдвд](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpdvd)                                       | Доступ к меню содержимого DVD-диска.                                                                                                                                                       |
| [ивмперрор](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperror)                                   | Обращается к коллекции указателей [ивмперроритем](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem) .                                                                                                                     |
| [ивмперроритем](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem)                           | Предоставляет сведения об ошибках.                                                                                                                                                        |
| [IWMPErrorItem2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem2)                         | Предоставляет дополнительные методы ошибочных элементов.                                                                                                                                                   |
| [ивмпевентс](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)                       | Предоставляет события, происходящие из элемента управления проигрывателя Windows Media, на который может ответить программа внедрения.                                                                            |
| [IWMPEvents2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)                     | Предоставляет события, происходящие из элемента управления проигрывателя Windows Media 10, на который может ответить программа внедрения. Эти события специально используются для программ синхронизации устройств. |
| [IWMPEvents3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)                               | Предоставляет события, связанные с копированием компакт-дисков, записью компакт-дисков, мониторингом папок и удаленными службами библиотек.                                                                                        |
| [ивмпфолдермониторсервицес](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)   | Предоставляет методы для перечисления, просмотра и изменения файловых папок, которые проигрыватель Windows Media отслеживает для цифрового мультимедийного содержимого.                                                                |
| [ивмпграфкреатион](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)                   | Управляет графом DirectShow.                                                                                                                                                             |
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
| [ивмпнетворк](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpnetwork)                               | Задает и получает свойства сетевого подключения, используемого проигрывателем Windows Media.                                                                                                 |
| [ивмпплайер](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer)                                 | Управляет поведением пользовательского интерфейса элемента управления проигрывателя Windows Media.                                                                                                                 |
| [IWMPPlayer2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer2)                               | Предоставляет дополнительные методы управления проигрывателем Windows Media.                                                                                                                         |
| [IWMPPlayer3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer3)                               | Предоставляет дополнительные методы управления проигрывателем Windows Media.                                                                                                                         |
| [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4)                               | Предоставляет дополнительные методы управления проигрывателем Windows Media.                                                                                                                         |
| [ивмпплайераппликатион](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication)           | Переключение между удаленным элементом управления проигрывателя Windows Media и полноэкранным режимом проигрывателя. Предназначен для использования программами C++, которые внедряют элемент управления в удаленный режим.                          |
| [ивмпплайерсервицес](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)                 | Используется узлом удаленного элемента управления для управления полным режимом проигрывателя Windows Media. Предназначен для использования с C++.                                                                     |
| [IWMPPlayerServices2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)               | Задает приоритет фоновой обработки.                                                                                                                                                  |
| [ивмпплайлист](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)                             | Создает списки воспроизведения и управляет ими.                                                                                                                                                            |
| [ивмпплайлистаррай](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray)                   | Обращается к коллекции указателей [ивмпплайлист](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) по номеру индекса.                                                                                                       |
| [ивмпплайлистколлектион](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection)         | Управляет указателями [ивмпплайлист](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) и [ивмпплайлистаррай](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray) .                                                                                     |
| [ивмпкуери](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)                                   | Представляет составной запрос.                                                                                                                                                              |
| [ивмпремотемедиасервицес](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)       | Предоставляет службы для проигрывателя Windows Media из программы, в которой размещается элемент управления проигрывателя. Предназначен для использования с C++.                                                                        |
| [ивмпрендерконфиг](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)                     | Предоставляет методы для указания или получения значения, указывающего, происходит ли воспроизведение только в текущем процессе.                                                                          |
| [ивмпсеттингс](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings)                             | Задает или получает параметры проигрывателя Windows Media.                                                                                                                                          |
| [IWMPSettings2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2)                           | Задает или получает параметры проигрывателя Windows Media.                                                                                                                                          |
| [ивмпскинманажер](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)                       | Указывает обложку, используемую с проигрывателем Windows Media.                                                                                                                                        |
| [ивмпстрингколлектион](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)             | Обращается к коллекции строк.                                                                                                                                                         |
| [IWMPStringCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)           | Предоставляет методы, дополняют интерфейс **ивмпстрингколлектион** .                                                                                                                  |
| [ивмпсинкдевице](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)                         | Представляет устройство, которое может синхронизировать цифровые файлы мультимедиа с проигрывателем Windows Media 10.                                                                                                |
| [IWMPSyncDevice2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)                       | Предоставляет метод, который дополняет интерфейс **ивмпсинкдевице** .                                                                                                                      |
| [ивмпсинксервицес](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)                     | Перечисляет доступные устройства, которые могут синхронизировать цифровые файлы мультимедиа с проигрывателем Windows Media 10.                                                                                       |
| [ивмптранскодеполици](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmptranscodepolicy)               | Предоставляет метод, реализованный фильтрами источников DirectShow для управления изменением формата цифровых файлов мультимедиа.                                                                          |
| [ивмпвидеорендерконфиг](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)           | Предоставляет метод, который настраивает Расширенный модуль обработки видео, используемый проигрывателем Windows Media.                                                                                               |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Справочник по объектной модели для C++**](object-model-reference-for-c.md)
</dt> </dl>

 

 




