---
description: 'Эта справочная информация по программированию для пакета Audio SDK включает следующие интерфейсы:'
ms.assetid: b18e2094-e974-4c23-b70b-ace5a168132d
title: Основные интерфейсы аудиоподсистемы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 330bb620b48b865db3db2ab5ea5625b7859588bd8e53e1addbcd8fd8ec9bda6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109474"
---
# <a name="core-audio-interfaces"></a>Основные интерфейсы аудиоподсистемы

Эта справочная информация по программированию для пакета Audio SDK включает следующие интерфейсы:

## <a name="mmdevice-api"></a>API Ммдевице

API Windows мультимедиа-устройства (ммдевице) позволяет клиентам аудио находить [устройства конечных точек аудио](audio-endpoint-devices.md), определять их возможности и создавать экземпляры драйверов для этих устройств. Файл заголовка Ммдевицеапи. h определяет интерфейсы в API Ммдевице. Дополнительные сведения см. в разделе [About ММДЕВИЦЕ API](mmdevice-api.md).

в следующей таблице перечислены интерфейсы ммдевице, доступные в ядре Audio SDK для Windows Vista.



| Интерфейс                                              | Описание                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                         | Представляет звуковое устройство.                                                                                                                                                                    |
| [**иммдевицеколлектион**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)     | Представляет коллекцию звуковых устройств.                                                                                                                                                      |
| [**иммдевицеенумератор**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)     | Предоставляет методы для перечисления звуковых устройств.                                                                                                                                                |
| [**иммендпоинт**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                     | Представляет устройство звуковой конечной точки.                                                                                                                                                           |
| [**иммнотификатионклиент**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Предоставляет уведомления при добавлении или удалении устройства конечной точки аудио, при изменении состояния или свойств устройства, а также при изменении роли по умолчанию, назначенной устройству. |



 

## <a name="wasapi"></a>васапи

API Windows Audio Session (васапи) позволяет клиентским приложениям управлять потоком звуковых данных между приложением и [устройством конечной точки аудио](audio-endpoint-devices.md). Файлы заголовков Аудиоклиент. h и Аудиополици. h определяют интерфейсы ВАСАПИ. Дополнительные сведения см. в разделе [About васапи](wasapi.md).

в следующей таблице перечислены интерфейсы васапи, доступные в ядре Audio SDK для Windows Vista и более поздних версий.



| Интерфейс                                                                                    | Описание                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иактиватеаудиоинтерфацеасинкоператион**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation)       | Представляет асинхронную операцию активации интерфейса [васапи](wasapi.md) и предоставляет метод для получения результатов активации.<br/> Применяется, начиная с Windows 8.<br/> |
| [**иактиватеаудиоинтерфацекомплетионхандлер**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfacecompletionhandler) | Предоставляет обратный вызов для указания того, что активация интерфейса [васапи](wasapi.md) завершена.<br/> Применяется, начиная с Windows 8.<br/>                                                  |
| [**иаудиокаптуреклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)                                           | Позволяет клиенту считывать входные данные из буфера конечной точки записи.                                                                                                                                       |
| [**иаудиоклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                                                         | Позволяет клиенту создавать и инициализировать аудио-поток между звуковым приложением и обработчиком аудио или аппаратным буфером устройства конечной точки аудио.                                           |
| [**иаудиоклокк**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                                                           | Позволяет клиенту отслеживать скорость передачи данных в потоке и текущую точку в потоке.                                                                                                                  |
| [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)<br/>                                              | Позволяет клиенту получить текущее расположение устройства.<br/>                                                                                                                                           |
| [**иаудиоклоккаджустмент**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)<br/>                            | Позволяет клиенту задать частоту дискретизации потока.<br/>                                                                                                                                           |
| [**иаудиорендерклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)                                             | Позволяет клиенту записывать выходные данные в буфер конечной точки отрисовки.                                                                                                                                     |
| [**иаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)                                         | Позволяет клиенту настраивать параметры управления для сеанса аудио и отслеживать события в сеансе.                                                                                           |
| [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)<br/>                            | Позволяет клиенту получать сведения о сеансе аудио.<br/>                                                                                                                                   |
| [**иаудиосессионманажер**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager)                                         | Позволяет клиенту получать доступ к элементам управления сеансом и элементам управления томами как для межпроцессных, так и для отдельных процессов.                                                                           |
| [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)<br/>                            | Управляет всеми поднаборами, в том числе перечислением и уведомлением для поднаборов. Он также обеспечивает поддержку уведомлений дуккинг.<br/>                                                                   |
| [**иаудиосессионенумератор**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)<br/>                        | Позволяет клиенту перечислять звуковые сеансы.<br/>                                                                                                                                                  |
| [**иаудиостреамволуме**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)                                             | Позволяет клиенту контролировать и отслеживать уровни громкости для всех каналов в аудиопотока.                                                                                                     |
| [**ичаннелаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)                                           | Позволяет клиенту управлять уровнями громкости для всех каналов в сеансе звука, к которому принадлежит поток.                                                                                    |
| [**исимплеаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)                                             | Позволяет клиенту управлять основным уровнем громкости звукового сеанса.                                                                                                                                  |
| [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)                                           | Предоставляет уведомления о событиях, связанных с сеансом, таких как изменения на уровне тома, отображаемое имя и состояние сеанса.                                                                                    |
| [**иаудиосессионнотификатион**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)<br/>                    | Отправляет уведомления, когда происходят изменения сеанса. <br/>                                                                                                                                               |
| [**иаудиоволумедуккнотификатион**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)<br/>              | Отправляет уведомления о незавершенных изменениях системных дуккинг.<br/>                                                                                                                                      |



 

## <a name="devicetopology-api"></a>API Девицетопологи

API Девицетопологи предоставляет клиентским приложениям возможность перемещаться по функциональным топологиям аппаратного обеспечения для отрисовки аудио-данных и устройств записи. Файл заголовка Девицетопологи. h определяет интерфейсы в API Девицетопологи. Дополнительные сведения см. в статье [топологии устройств](device-topologies.md) и [**API девицетопологи**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology).

в следующей таблице перечислены интерфейсы девицетопологи, доступные в ядре Audio SDK для Windows Vista и более поздних версий.



| Интерфейс                                                           | Описание                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иаудиоаутогаинконтрол**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)              | Предоставляет доступ к оборудованию автоматического усиления контроля (АГК).                                                                                                                                                               |
| [**иаудиобасс**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                                    | Предоставляет доступ к аппаратному контролю уровня басов.                                                                                                                                                                         |
| [**иаудиочаннелконфиг**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)                  | Предоставляет доступ к элементу управления конфигурацией аппаратного канала.                                                                                                                                                              |
| [**иаудиоинпутселектор**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)                  | Предоставляет доступ к элементу управления аппаратным мультиплексором (селектор ввода).                                                                                                                                                       |
| [**иаудиолауднесс**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                            | Предоставляет доступ к элементу управления компенсацией "громкости".                                                                                                                                                                     |
| [**иаудиомидранже**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                            | Предоставляет доступ к аппаратному управлению на уровне средний уровень.                                                                                                                                                                     |
| [**иаудиомуте**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                                    | Предоставляет доступ к аппаратному отключению управления.                                                                                                                                                                               |
| [**иаудиуутпутселектор**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)                | Предоставляет доступ к элементу управления аппаратным средством демультиплексирования (Селектор вывода).                                                                                                                                                    |
| [**иаудиопеакметер**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                          | Предоставляет доступ к оборудованию с пиковым контролем использования оборудования.                                                                                                                                                                         |
| [**иаудиотребле**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                                | Предоставляет доступ к аппаратному контролю уровня высоких частот.                                                                                                                                                                       |
| [**иаудиоволумелевел**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)                      | Предоставляет доступ к аппаратному регулятору громкости.                                                                                                                                                                             |
| [**иконнектор**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                                    | Представляет точку соединения между компонентами.                                                                                                                                                                      |
| [**иконтролинтерфаце**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)                      | Представляет интерфейс элемента управления в части (подединице или соединителе).                                                                                                                                                          |
| [**идевицеспеЦификпроперти**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)          | Представляет свойство соединителя или подединицы для конкретного устройства.                                                                                                                                                          |
| [**идевицетопологи**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                          | Предоставляет доступ к топологии звукового устройства.                                                                                                                                                                       |
| [**иксформатсуппорт**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)                        | Предоставляет сведения о форматах звуковых данных, поддерживаемых программно настроенным подключением ввода-вывода (обычно это канал DMA) между звуковым устройством и системной памятью.                                        |
| [**иксжаккдескриптион**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)                    | Содержит сведения о гнездах или внутренних соединителях, обеспечивающих физическое подключение между устройством на звуковом адаптере и внешним или внутренним устройством конечной точки (например, микрофон или проигрыватель компакт-дисков). |
| [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)<br/>       | Предоставляет удобный доступ к свойству **\_ \_ DESCRIPTION2 кспроперти** соединителя для устройства конечной точки.<br/>                                                                                            |
| [**иксжакксинкинформатион**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)<br/> | Предоставляет сведения о приемнике разъема, если гнездо поддерживается оборудованием.<br/>                                                                                                                             |
| [**ипарт**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                              | Представляет часть (соединитель или подединицу) топологии устройства.                                                                                                                                                            |
| [**ипартслист**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                                    | Представляет список частей (соединителей и подразделений).                                                                                                                                                                     |
| [**иперчаннелдблевел**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)                    | Представляет универсальный интерфейс управления подединицей, который обеспечивает управление на уровне громкости для каждого канала (в децибел) звукового потока или частотной полосы в потоке аудио.                                        |
| [**исубунит**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                                        | Представляет подразделение оборудования (например, управление на уровне тома), которое находится в пути данных между клиентом и устройством конечной точки аудио.                                                                             |
| [**иконтролчанженотифи**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify)                | Предоставляет уведомления при изменении состояния части (соединителя или подединицы).                                                                                                                                          |



 

## <a name="endpointvolume-api"></a>API Ендпоинтволуме

API Ендпоинтволуме позволяет специализированным клиентам управлять уровнями громкости [конечных точек аудио](audio-endpoint-devices.md)и отслеживать их. Файл заголовка Ендпоинтволуме. h определяет интерфейсы в API Ендпоинтволуме. Дополнительные сведения см. в разделе [**API ендпоинтволуме**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) .

в следующей таблице перечислены интерфейсы ендпоинтволуме, доступные в ядре Audio SDK для Windows Vista.



| **Интерфейс**                                                        | **Описание**                                                                                   |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**иаудиоендпоинтволуме**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)                 | Представляет элементы управления громкостью в звуковом потоке на устройстве конечной точки аудио.           |
| [**иаудиоендпоинтволумикс**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)<br/>  | Предоставляет регуляторы громкости в потоке аудио в конечную точку устройства или из нее.<br/>             |
| [**иаудиометеринформатион**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation)             | Представляет пиковый счетчик звукового потока, на устройство конечной точки аудио.                  |
| [**иаудиоендпоинтволумекаллбакк**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Предоставляет уведомления при изменении уровня громкости или выключения звука устройства конечной точки. |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по программированию](programming-reference.md)
</dt> </dl>

 

