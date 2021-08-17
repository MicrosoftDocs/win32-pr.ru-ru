---
description: API Девицетопологи
ms.assetid: 051311ef-dd29-4014-bb9c-4cdccf7ce7de
title: API Девицетопологи
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 3b79def9f1cb1f5ec9342074b813e50993cbc37e7a7af2a9e0b577c730156247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406759"
---
# <a name="devicetopology-api"></a>API Девицетопологи

см. [пример с высококачественным речевым захватом майкрософт DMO](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/audio/aecmicarray).

API Девицетопологи предоставляет клиентским приложениям возможность перемещаться по функциональным топологиям аппаратного обеспечения для отрисовки аудио-данных и устройств записи. С помощью интерфейсов и методов в API Девицетопологи клиенты могут обнаруживать функциональные подединицы (например, регулятор громкости), которые находятся в путях данных, ведущих к [устройствам конечных точек аудио](audio-endpoint-devices.md). Клиенты могут перемещаться по внутренним топологиям устройств звуковых адаптеров и устройств аудио конечных точек, а также выполнять по шагам подключения, связывающие одно устройство с другим. Дополнительные сведения см. в разделе [топологии устройств](device-topologies.md).

Файл заголовка Девицетопологи. h определяет интерфейсы в API Девицетопологи.

Чтобы получить доступ к интерфейсам API Девицетопологи, клиент сначала получает ссылку на интерфейс [**идевицетопологи**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) для устройства конечной точки аудио, выполнив следующие действия.

1.  Используя один из методов, описанных в [**интерфейсе иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice), получите ссылку на интерфейс **иммдевице** для устройства конечной точки аудио.
2.  Вызовите метод [**иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) с параметром *IID* , равным **рефиид** IID \_ идевицетопологи.

Клиент может получить ссылки на другие интерфейсы в API Девицетопологи, вызвав методы в интерфейсе [**идевицетопологи**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) .

API Девицетопологи реализует следующие интерфейсы.



| Интерфейс                                                  | Описание                                                                                                                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иаудиоаутогаинконтрол**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | Предоставляет доступ к оборудованию автоматического усиления контроля (АГК).                                                                                                                                                               |
| [**иаудиобасс**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | Предоставляет доступ к аппаратному контролю уровня басов.                                                                                                                                                                         |
| [**иаудиочаннелконфиг**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | Предоставляет доступ к элементу управления конфигурацией аппаратного канала.                                                                                                                                                              |
| [**иаудиоинпутселектор**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | Предоставляет доступ к элементу управления аппаратным мультиплексором (селектор ввода).                                                                                                                                                       |
| [**иаудиолауднесс**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | Предоставляет доступ к элементу управления компенсацией "громкости".                                                                                                                                                                     |
| [**иаудиомидранже**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | Предоставляет доступ к аппаратному управлению на уровне средний уровень.                                                                                                                                                                     |
| [**иаудиомуте**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | Предоставляет доступ к аппаратному отключению управления.                                                                                                                                                                               |
| [**иаудиуутпутселектор**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | Предоставляет доступ к элементу управления аппаратным средством демультиплексирования (Селектор вывода).                                                                                                                                                    |
| [**иаудиопеакметер**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | Предоставляет доступ к оборудованию с пиковым контролем использования оборудования.                                                                                                                                                                         |
| [**иаудиотребле**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | Предоставляет доступ к аппаратному контролю уровня высоких частот.                                                                                                                                                                       |
| [**иаудиоволумелевел**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | Предоставляет доступ к аппаратному регулятору громкости.                                                                                                                                                                             |
| [**иконнектор**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                           | Представляет точку соединения между компонентами.                                                                                                                                                                      |
| [**иконтролинтерфаце**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)             | Представляет интерфейс элемента управления в части (подединице или соединителе).                                                                                                                                                          |
| [**идевицеспеЦификпроперти**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | Представляет свойство соединителя или подединицы для конкретного устройства.                                                                                                                                                          |
| [**идевицетопологи**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                 | Предоставляет доступ к топологии звукового устройства.                                                                                                                                                                       |
| [**иксформатсуппорт**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)               | Предоставляет сведения о форматах звуковых данных, поддерживаемых программно настроенным подключением ввода-вывода (обычно это канал DMA) между звуковым устройством и системной памятью.                                        |
| [**иксжаккдескриптион**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)           | Содержит сведения о гнездах или внутренних соединителях, обеспечивающих физическое подключение между устройством на звуковом адаптере и внешним или внутренним устройством конечной точки (например, микрофон или проигрыватель компакт-дисков). |
| [**ипарт**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                     | Представляет часть (соединитель или подединицу) топологии устройства.                                                                                                                                                            |
| [**ипартслист**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                           | Представляет список частей (соединителей и подразделений).                                                                                                                                                                     |
| [**иперчаннелдблевел**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)           | Представляет универсальный интерфейс управления подединицей, который обеспечивает управление на уровне громкости для каждого канала (в децибел) звукового потока или частотной полосы в потоке аудио.                                        |
| [**исубунит**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                               | Представляет подразделение оборудования (например, управление на уровне тома), которое находится в пути данных между клиентом и устройством конечной точки аудио.                                                                             |



 

Клиенты API Девицетопологи, которым требуются уведомления о событиях управления изменениями в соединителях и подразделениях, должны реализовать следующий интерфейс.



| Интерфейс                                            | Описание                                                                      |
|------------------------------------------------------|----------------------------------------------------------------------------------|
| [**иконтролчанженотифи**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify) | Предоставляет уведомления при изменении состояния части (соединителя или подединицы). |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Топологии устройств](device-topologies.md)
</dt> <dt>

[**Справочник по программированию**](programming-reference.md)
</dt> </dl>

 

 
