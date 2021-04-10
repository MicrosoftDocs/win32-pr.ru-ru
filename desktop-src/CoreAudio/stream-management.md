---
description: Управление потоками
ms.assetid: 936d8d69-e86c-418b-b5b0-c4fbbfa1dd49
title: Управление потоками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07180d8b46f4d079c08f4b619cf4a7773a6104d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141851"
---
# <a name="stream-management"></a>Управление потоками

После перечисления [устройств конечных точек аудио](audio-endpoint-devices.md) в системе и определения подходящего устройства для отрисовки или записи, следующая задача для клиентского приложения будет открывать подключение к оконечному устройству и управлять потоком звуковых данных по этому соединению. [Васапи](wasapi.md) позволяет клиентам создавать звуковые потоки и управлять ими.

ВАСАПИ реализует несколько интерфейсов для предоставления службам управления потоками аудио клиентам. Основным интерфейсом является [**иаудиоклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient). Клиент получает интерфейс **иаудиоклиент** для устройства конечной точки аудио, вызывая метод [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (с параметром *IID* которого задано значение **рефиид** IID \_ иаудиоклиент) для объекта Endpoint.

Клиент вызывает методы в интерфейсе [**иаудиоклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) для следующих задач:

-   Узнайте, какие аудио форматы поддерживает устройство конечной точки.
-   Возвращает размер буфера конечной точки.
-   Получение формата потока и задержки.
-   Запускает, останавливает и сбрасывает поток, который проходит через устройство конечной точки.
-   Доступ к дополнительным службам аудио.

Чтобы создать поток, клиент вызывает метод [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) . С помощью этого метода клиент указывает формат данных для потока, размер буфера конечной точки и то, работает ли поток в общем или монопольном режиме.

Остальные методы в интерфейсе [**иаудиоклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) делятся на две группы:

-   Методы, которые могут вызываться только после открытия потока с помощью [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).
-   Методы, которые могут быть вызваны в любое время до или после вызова [**инициализации**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .

Следующие методы можно вызывать только после вызова [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize):

-   [**Иаудиоклиент:: Жетбуфферсизе**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)
-   [**Иаудиоклиент:: Жеткуррентпаддинг**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)
-   [**Иаудиоклиент:: "Услуга"**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
-   [**Иаудиоклиент:: Жетстреамлатенци**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getstreamlatency)
-   [**Иаудиоклиент:: Reset**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-reset)
-   [**Иаудиоклиент:: Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start)
-   [**Иаудиоклиент:: останавливаться**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop)

Следующие методы можно вызывать до или после вызова [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) :

-   [**Иаудиоклиент:: Жетдевицепериод**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)
-   [**Иаудиоклиент:: Жетмиксформат**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [**Иаудиоклиент:: Исформатсуппортед**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)

Для доступа к дополнительным службам аудио клиента клиент вызывает метод [**иаудиоклиент::**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) . С помощью этого метода клиент может получить ссылки на следующие интерфейсы:

-   [**иаудиорендерклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)

    Записывает данные отрисовки в буфер конечной точки отрисовки звука.

-   [**иаудиокаптуреклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)

    Считывает записанные данные из буфера конечной точки записи звука.

-   [**иаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)

    Взаимодействует с диспетчером сеансов аудио для настройки и управления сеансом звука, связанным с потоком.

-   [**исимплеаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)

    Управляет уровнем громкости звукового сеанса, связанного с потоком.

-   [**ичаннелаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)

    Управляет уровнями громкости отдельных каналов в сеансе звука, который связан с потоком.

-   [**иаудиоклокк**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)

    Отслеживает скорость потоковых данных и расположение потока.

Кроме того, клиенты ВАСАПИ, которым требуется уведомление о событиях, связанных с сеансом, должны реализовать следующий интерфейс:

-   [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)

    Чтобы получать уведомления о событиях, клиент передает указатель на интерфейс [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) в метод [**Иаудиосессионконтрол:: регистераудиосессионнотификатион**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) в качестве параметра вызова.

Наконец, клиент может использовать API более высокого уровня для создания звукового потока, но также требует доступа к элементам управления сеанса и элементам управления громкостью для сеанса, содержащего поток. Интерфейс API более высокого уровня обычно не предоставляет такой доступ. Клиент может получать элементы управления для определенного сеанса через интерфейс [**иаудиосессионманажер**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) . Этот интерфейс позволяет клиенту получать интерфейсы [**иаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) и [**исимплеаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) для сеанса, не требуя от клиента использования интерфейса [**иаудиоклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) для создания потока и назначения потока сеансу. Клиент получает интерфейс **иаудиосессионманажер** для устройства конечной точки аудио, вызывая метод [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (с параметром *IID* которого задано значение **рефиид** IID \_ иаудиосессионманажер) для объекта Endpoint.

Интерфейсы [**иаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)и [**Иаудиосессионманажер**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) определены в файле заголовка аудиополици. h. Все остальные интерфейсы ВАСАПИ определены в файле заголовка Аудиоклиент. h.

В следующих разделах описывается использование ВАСАПИ для управления звуковыми потоками.

-   [О ВАСАПИ](wasapi.md)
-   [Отрисовка потока](rendering-a-stream.md)
-   [Запись потока](capturing-a-stream.md)
-   [Запись замыкания на себя](loopback-recording.md)
-   [Потоки с монопольным режимом](exclusive-mode-streams.md)
-   [Восстановление после ошибки Invalid-Device](recovering-from-an-invalid-device-error.md)
-   [Использование коммуникационного устройства](using-the-communication-device.md)
-   [Потоковая маршрутизация](stream-routing.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Руководство по программированию](programming-guide.md)
</dt> </dl>

 

 



