---
description: Топологии устройств
ms.assetid: 5ac421e5-74a4-40e8-af6f-a99a05ebc3e0
title: Топологии устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e0af267bb4a0fa924ee23d36a2a615ac5ae7fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539344"
---
# <a name="device-topologies"></a>Топологии устройств

[API девицетопологи](devicetopology-api.md) предоставляет клиентам возможности управления различными внутренними функциями звуковых адаптеров, которые не могут получить доступ через [API ммдевице](mmdevice-api.md), [васапи](wasapi.md)или [API ендпоинтволуме](endpointvolume-api.md).

Как упоминалось ранее, [API ммдевице](mmdevice-api.md), [Васапи](wasapi.md)и [API ендпоинтволуме](endpointvolume-api.md) представляют микрофоны, динамики, наушники, а также другие входные и выходные устройства в качестве [звуковых конечных](audio-endpoint-devices.md)устройств. Модель устройства конечной точки предоставляет клиентам удобный доступ к тому и звуковые элементы управления в звуковых устройствах. Клиенты, которым требуются только эти простые элементы управления, могут избежать обхода внутренних топологий аппаратных устройств в звуковых адаптерах.

В Windows Vista механизм аудио автоматически настраивает топологии звуковых устройств для использования в приложениях аудио. Таким же приложениям редко приходится использовать API Девицетопологи для этой цели. Например, предположим, что звуковой адаптер содержит мультиплексор ввода, который может записывать поток из входного или микрофона, но не может одновременно записывать потоки из обеих конечных устройств. Предположим, что пользователь включил приложения с монопольным режимом для прерывания использования устройства "Звуковая конечная точка" приложениями общего режима, как описано в разделе [потоки с монопольным режимом](exclusive-mode-streams.md). Если приложение общего режима записывает поток из входных данных во время записи потока из микрофона приложением с монопольным режимом, обработчик звука автоматически переключает мультиплексор из входных данных в микрофон. В более ранних версиях Windows, включая Windows XP, приложение с монопольным режимом в этом примере использовало функции **миксеркскскс** в API мультимедиа Windows для обхода топологий устройств адаптеров, обнаружения мультиплексора и настройки мультиплексора для выбора входных данных с микрофона. В Windows Vista эти действия больше не требуются.

Однако некоторым клиентам может потребоваться явный контроль над типами элементов управления звуком, которые недоступны через API Ммдевице, ВАСАПИ или API Ендпоинтволуме. Для этих клиентов API Девицетопологи предоставляет возможность обхода топологий устройств адаптеров для обнаружения и управления звуковыми элементами на устройствах. Приложения, использующие API Девицетопологи, должны быть разработаны с осторожностью, чтобы избежать помех в работе политики Windows Audio и нарушения внутренних конфигураций звуковых устройств, используемых совместно с другими приложениями. Дополнительные сведения о политике Windows Audio см. в разделе [звуковые компоненты пользовательского режима](user-mode-audio-components.md).

API Девицетопологи предоставляет интерфейсы для обнаружения следующих типов элементов управления звуком в топологии устройства и управления ими:

-   Автоматическое усиление контроля
-   Элемент управления басов
-   Селектор ввода (мультиплексор)
-   Элемент управления громкостью
-   Элемент управления "средний"
-   Отключить контроль
-   Селектор выходных данных (демультиплексор)
-   Счетчик пиковой нагрузки
-   Элемент управления "ВЧ"
-   Элемент управления громкостью

Кроме того, API Девицетопологи позволяет клиентам запрашивать устройства адаптеров для получения сведений о поддерживаемых ими форматах потока. В файле заголовка Девицетопологи. h определяются интерфейсы в API Девицетопологи.

На следующей схеме показан пример нескольких топологий подключенных устройств для части адаптера PCI, которая захватывает звук с микрофона, линейного входа и ЛАЗЕРного проигрывателя.

![Пример четырех топологий подключенных устройств](images/fig2.jpg)

На предыдущей схеме показаны пути к данным, ведущие от аналоговых входов в системную шину. Каждое из следующих устройств представлено в виде объекта топологии устройства с интерфейсом [**идевицетопологи**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) :

-   Устройство записи звука
-   Устройство для ввода мультиплексора
-   Устройство A конечной точки
-   Устройство в конечной точке B

Обратите внимание, что схема топологии объединяет устройства адаптеров (устройства для записи звука и мультиплексора ввода) с устройствами конечных точек. Благодаря подключениям между устройствами звуковые данные передаются с одного устройства на другое. На каждой стороне соединения находится соединитель (с меткой Con на схеме), с помощью которого данные перемещаются или попадают в устройство.

На левой границе диаграммы сигналы от входных и микрофонных разъемов поступают в конечные устройства.

Устройство для записи волнового сигнала и устройство мультиплексора ввода являются функциями потоковой обработки, которые в терминологии API Девицетопологи называются подразделениями. На предыдущей схеме отображаются следующие типы подразделений.

-   Элемент управления "Громкость&quot; (с меткой &quot;Громкость")
-   Отключить контроль (с меткой)
-   Мультиплексор (или селектор ввода; помеченный МУЛЬТИПЛЕКСОР)
-   Аналоговый для цифрового преобразователя (под названием ADC)

Параметры в подразделениях тома, звука и мультиплексора могут управляться клиентами, а API Девицетопологи предоставляет клиентам управляющие интерфейсы для управления ими. В этом примере подмодуль ADC не имеет параметров управления. Таким же Девицетопологи API не предоставляет интерфейс управления для ADC.

В терминологии API Девицетопологи соединители и подединицы принадлежат к одной общей категории — частям. Все части, независимо от того, являются ли они соединителями или подразделениями, предоставляют общий набор функций. API Девицетопологи реализует интерфейс [**ипарт**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) для представления универсальных функций, общих для соединителей и подразделений. API реализует интерфейсы [**иконнектор**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) и [**исубунит**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) для представления конкретных аспектов соединителей и подразделений.

API Девицетопологи создает топологии устройства записи звука и устройства мультиплексирования ввода из фильтров потоковой передачи (KS), которые драйвер аудиоподсистемы предоставляет операционной системе для представления этих устройств. (Драйвер адаптера аудиоподсистемы реализует интерфейсы **иминипортвавекскскс** и **иминипорттопологи** , которые представляют зависимые от оборудования части этих фильтров; дополнительные сведения об этих интерфейсах и о фильтрах KS см. в документации по Windows DDK.)

API Девицетопологи конструирует тривиальные топологии для представления конечных устройств A и B на предыдущей схеме. Топология устройства конечной точки состоит из одного соединителя. Эта топология является просто заполнителем для устройства конечной точки и не содержит подразделений для обработки звуковых данных. На самом деле адаптеры устройств содержат все подединицы, используемые клиентскими приложениями для управления обработкой аудио. Топология устройства конечной точки в основном используется в качестве отправной точки для изучения топологий устройств адаптеров.

Внутренние соединения между двумя частями в топологии устройства называются ссылками. API Девицетопологи предоставляет методы для обхода ссылок из одной части в другую в топологии устройства. API также предоставляет методы для обхода соединений между топологиями устройств.

Чтобы приступить к исследованию набора топологий подключенных устройств, клиентское приложение активирует интерфейс **идевицетопологи** устройства конечной точки аудио. Соединитель на устройстве конечной точки подключается к соединителю в звуковом адаптере или в сети. Если конечная точка подключается к устройству на звуковом адаптере, методы в API Девицетопологи позволяют приложению выполнять шаг через подключение от конечной точки к адаптеру, получая ссылку на интерфейс **идевицетопологи** устройства адаптера на другой стороне соединения. Сеть, с другой стороны, не имеет топологии устройства. Сетевое подключение передает звуковой поток клиенту, который обращается к системе удаленно.

API Девицетопологи предоставляет доступ только к топологиям аппаратных устройств в аудио адаптере. Внешние устройства на левой границе схемы и программные компоненты на правом крае выходят за рамки API. Пунктирные линии на обеих сторонах диаграммы представляют ограничения API Девицетопологи. Клиент может использовать API для просмотра пути к данным, который растягивается от розетки ввода к системной шине, но API не может проникнуть за пределы этих границ.

Каждый соединитель на предыдущей схеме имеет связанный тип соединения, указывающий тип соединения, создаваемого соединителем. Таким же соединители на двух сторонах соединения всегда имеют одинаковые типы соединения. Тип соединения указывается значением перечисления [**коннектортипе**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) — физическим \_ внешним, физическим \_ внутренним, фиксированным программным обеспечением, \_ программным \_ вводом или сетью. Соединения между устройством и конечными устройствами входного мультиплексора A и B имеют тип физических внешних. это \_ означает, что соединение представляет физическое подключение к внешнему устройству (иными словами, звуковой разъем, доступный пользователю). Подключение к аналоговому сигналу от внутреннего проигрывателя компакт-диска имеет тип физический \_ внутренний, что означает физическое подключение к вспомогательному устройству, установленному в системном корпусе. Подключение между устройством записи Wave и устройством мультиплексора ввода имеет фиксированное программное обеспечение \_ , которое указывает на постоянное фиксированное подключение и не может быть настроено в разделе Управление программным обеспечением. Наконец, соединение с системной шиной в правой части схемы относится к типу программного \_ ввода-вывода, что означает, что данные ввода/вывода для подключения реализуются модулем DMA в разделе Управление программным обеспечением. (Схема не включает пример типа сетевого подключения.)

Клиент начинает прохождение пути к данным на устройстве конечной точки. Сначала клиент получает интерфейс [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) , представляющий устройство конечной точки, как описано в подразделе [перечисление звуковых устройств](enumerating-audio-devices.md). Чтобы получить интерфейс **идевицетопологи** для устройства конечной точки, клиент вызывает метод [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) с параметром *IID* , равным рефиид IID \_ идевицетопологи.

В примере на предыдущей схеме устройство мультиплексора ввода содержит все аппаратные элементы управления (громкость, звук и мультиплексор) для потоков записи из гнезд ввода и микрофона. В следующем примере кода показано, как получить интерфейс **идевицетопологи** для устройства входного мультиплексора из интерфейса **иммдевице** для устройства конечной точки для линейного входа или микрофона:


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface of an endpoint device. The function
// outputs a pointer (counted reference) to the
// IDeviceTopology interface of the adapter device that
// connects to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);

HRESULT GetHardwareDeviceTopology(
            IMMDevice *pEndptDev,
            IDeviceTopology **ppDevTopo)
{
    HRESULT hr = S_OK;
    IDeviceTopology *pDevTopoEndpt = NULL;
    IConnector *pConnEndpt = NULL;
    IConnector *pConnHWDev = NULL;
    IPart *pPartConn = NULL;

    // Get the endpoint device's IDeviceTopology interface.

    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL,
                      NULL, (void**)&pDevTopoEndpt);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).

    hr = pDevTopoEndpt->GetConnector(0, &pConnEndpt);
    EXIT_ON_ERROR(hr)

    // Use the connector in the endpoint device to get the
    // connector in the adapter device.

    hr = pConnEndpt->GetConnectedTo(&pConnHWDev);
    EXIT_ON_ERROR(hr)

    // Query the connector in the adapter device for
    // its IPart interface.

    hr = pConnHWDev->QueryInterface(
                         IID_IPart, (void**)&pPartConn);
    EXIT_ON_ERROR(hr)

    // Use the connector's IPart interface to get the
    // IDeviceTopology interface for the adapter device.

    hr = pPartConn->GetTopologyObject(ppDevTopo);

Exit:
    SAFE_RELEASE(pDevTopoEndpt)
    SAFE_RELEASE(pConnEndpt)
    SAFE_RELEASE(pConnHWDev)
    SAFE_RELEASE(pPartConn)

    return hr;
}
```



Функция Жесардваредевицетопологи в предыдущем примере кода выполняет следующие действия, чтобы получить интерфейс **идевицетопологи** для устройства входного мультиплексора:

1.  Вызовите метод **иммдевице:: Activate** , чтобы получить интерфейс **идевицетопологи** для устройства конечной точки.
2.  С помощью интерфейса **идевицетопологи** , полученного на предыдущем шаге, вызовите метод [**идевицетопологи::-Connect**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) , чтобы получить интерфейс **иконнектор** для одного соединителя (номер соединителя 0) на устройстве конечной точки.
3.  С помощью интерфейса **иконнектор** , полученного на предыдущем шаге, вызовите метод [**Иконнектор:: жетконнектедто**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) , чтобы получить интерфейс **иконнектор** соединителя на устройстве входного мультиплексора.
4.  Запросите интерфейс **иконнектор** , полученный на предыдущем шаге, для своего интерфейса **ипарт** .
5.  С помощью интерфейса **ипарт** , полученного на предыдущем шаге, вызовите метод [**Ипарт:: жеттопологйобжект**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) , чтобы получить интерфейс **идевицетопологи** для устройства входного мультиплексора.

Прежде чем пользователь сможет записать данные с микрофона на предыдущей схеме, клиентское приложение должно убедиться, что мультиплексор выбирает входные микрофона. В следующем примере кода показано, как клиент может перемещаться по пути к данным с микрофона, пока не обнаружит мультиплексор, который затем программирует на выбор входного микрофона:


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface for a capture endpoint device. The
// function traverses the data path that extends from the
// endpoint device to the system bus (for example, PCI)
// or external bus (USB). If the function discovers a MUX
// (input selector) in the path, it selects the MUX input
// that connects to the stream from the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);
const IID IID_IConnector = __uuidof(IConnector);
const IID IID_IAudioInputSelector = __uuidof(IAudioInputSelector);

HRESULT SelectCaptureDevice(IMMDevice *pEndptDev)
{
    HRESULT hr = S_OK;
    DataFlow flow;
    IDeviceTopology *pDeviceTopology = NULL;
    IConnector *pConnFrom = NULL;
    IConnector *pConnTo = NULL;
    IPart *pPartPrev = NULL;
    IPart *pPartNext = NULL;
    IAudioInputSelector *pSelector = NULL;

    if (pEndptDev == NULL)
    {
        EXIT_ON_ERROR(hr = E_POINTER)
    }

    // Get the endpoint device's IDeviceTopology interface.
    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL, NULL,
                      (void**)&pDeviceTopology);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).
    hr = pDeviceTopology->GetConnector(0, &pConnFrom);
    SAFE_RELEASE(pDeviceTopology)
    EXIT_ON_ERROR(hr)

    // Make sure that this is a capture device.
    hr = pConnFrom->GetDataFlow(&flow);
    EXIT_ON_ERROR(hr)

    if (flow != Out)
    {
        // Error -- this is a rendering device.
        EXIT_ON_ERROR(hr = AUDCLNT_E_WRONG_ENDPOINT_TYPE)
    }

    // Outer loop: Each iteration traverses the data path
    // through a device topology starting at the input
    // connector and ending at the output connector.
    while (TRUE)
    {
        BOOL bConnected;
        hr = pConnFrom->IsConnected(&bConnected);
        EXIT_ON_ERROR(hr)

        // Does this connector connect to another device?
        if (bConnected == FALSE)
        {
            // This is the end of the data path that
            // stretches from the endpoint device to the
            // system bus or external bus. Verify that
            // the connection type is Software_IO.
            ConnectorType  connType;
            hr = pConnFrom->GetType(&connType);
            EXIT_ON_ERROR(hr)

            if (connType == Software_IO)
            {
                break;  // finished
            }
            EXIT_ON_ERROR(hr = E_FAIL)
        }

        // Get the connector in the next device topology,
        // which lies on the other side of the connection.
        hr = pConnFrom->GetConnectedTo(&pConnTo);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnFrom)

        // Get the connector's IPart interface.
        hr = pConnTo->QueryInterface(
                        IID_IPart, (void**)&pPartPrev);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnTo)

        // Inner loop: Each iteration traverses one link in a
        // device topology and looks for input multiplexers.
        while (TRUE)
        {
            PartType parttype;
            UINT localId;
            IPartsList *pParts;

            // Follow downstream link to next part.
            hr = pPartPrev->EnumPartsOutgoing(&pParts);
            EXIT_ON_ERROR(hr)

            hr = pParts->GetPart(0, &pPartNext);
            pParts->Release();
            EXIT_ON_ERROR(hr)

            hr = pPartNext->GetPartType(&parttype);
            EXIT_ON_ERROR(hr)

            if (parttype == Connector)
            {
                // We've reached the output connector that
                // lies at the end of this device topology.
                hr = pPartNext->QueryInterface(
                                  IID_IConnector,
                                  (void**)&pConnFrom);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pPartPrev)
                SAFE_RELEASE(pPartNext)
                break;
            }

            // Failure of the following call means only that
            // the part is not a MUX (input selector).
            hr = pPartNext->Activate(
                              CLSCTX_ALL,
                              IID_IAudioInputSelector,
                              (void**)&pSelector);
            if (hr == S_OK)
            {
                // We found a MUX (input selector), so select
                // the input from our endpoint device.
                hr = pPartPrev->GetLocalId(&localId);
                EXIT_ON_ERROR(hr)

                hr = pSelector->SetSelection(localId, NULL);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pSelector)
            }

            SAFE_RELEASE(pPartPrev)
            pPartPrev = pPartNext;
            pPartNext = NULL;
        }
    }

Exit:
    SAFE_RELEASE(pConnFrom)
    SAFE_RELEASE(pConnTo)
    SAFE_RELEASE(pPartPrev)
    SAFE_RELEASE(pPartNext)
    SAFE_RELEASE(pSelector)
    return hr;
}
```



API Девицетопологи реализует интерфейс [**иаудиоинпутселектор**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) для инкапсуляции мультиплексора, например, на предыдущей схеме. (Интерфейс [**иаудиуутпутселектор**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) инкапсулирует демультиплексор.) В предыдущем примере кода внутренний цикл функции Селекткаптуредевице запрашивает каждую найденную подединицу, чтобы определить, является ли подединица мультиплексором. Если подединица является мультиплексором, то функция вызывает метод [**иаудиоинпутселектор:: сетселектион**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) , чтобы выбрать входные данные, которые подключаются к потоку с устройства конечной точки.

В предыдущем примере кода каждая итерация внешнего цикла проходит по одной топологии устройства. При просмотре топологий устройств на предыдущей схеме первая итерация проходит по устройству входного мультиплексора, а вторая итерация проходит по устройству записи звука. Функция будет завершена при достижении соединителя на правой границе схемы. Завершение происходит, когда функция обнаруживает соединитель с типом соединения с программным обеспечением \_ ввода-вывода. Этот тип подключения определяет точку, в которой устройство адаптера подключается к системной шине.

Вызов метода [**ипарт:: жетпарттипе**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) в предыдущем примере кода получает значение перечисления **ипарттипе** , указывающее, является ли текущая часть соединителем или подединицей обработки звука.

Внутренний цикл в предыдущем примере кода выполняет шаги по ссылке из одной части в другую путем вызова метода [**ипарт:: енумпартсаутгоинг**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) . (Существует также метод [**ипарт:: енумпартсинкоминг**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) для пошагового выполнения в обратном направлении.) Этот метод извлекает объект [**ипартслист**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) , содержащий список всех исходящих частей. Однако любая часть, которую функция Селекткаптуредевице должна столкнуться на устройстве записи, всегда будет содержать только одну исходящую часть. Таким образом, последующий вызов [**ипартслист::-Part**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) всегда запрашивает первую часть в списке, часть номер 0, поскольку функция предполагает, что это единственная часть в списке.

Если функция Селекткаптуредевице встречает топологию, для которой это допущение является недопустимым, функция может не настроить устройство должным образом. Чтобы избежать такого сбоя, более универсальная версия функции может выполнять следующие действия:

-   Вызовите метод [**ипартслист:: NOCOUNT**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) , чтобы определить количество исходящих частей.
-   Для каждой исходящей части вызовите **ипартслист::** , чтобы начать проход по пути к данным, который ведет от части.

Некоторые, но не обязательно все компоненты имеют связанные элементы управления оборудованием, которые клиенты могут устанавливать или получать. Конкретная часть может иметь ноль, один или несколько аппаратных элементов управления. Аппаратный элемент управления представлен следующей парой интерфейсов:

-   Универсальный интерфейс элемента управления [**иконтролинтерфаце**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface), который содержит методы, общие для всех элементов управления оборудования.
-   Интерфейс, зависящий от функции (например, [**иаудиоволумелевел**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)), который предоставляет параметры управления для конкретного типа аппаратного управления (например, регулятора громкости).

Чтобы перечислить аппаратные элементы управления для части, клиент сначала вызывает метод [**ипарт:: жетконтролинтерфацекаунт**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) , чтобы определить количество аппаратных элементов управления, связанных с частью. Затем клиент выполняет ряд вызовов метода [**ипарт:: жетконтролинтерфаце**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) , чтобы получить интерфейс **иконтролинтерфаце** для каждого аппаратного управления. Наконец, клиент получает интерфейс функции для каждого аппаратного управления, вызывая метод [**иконтролинтерфаце:: жетиид**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) для получения идентификатора интерфейса. Клиент вызывает метод [**ипарт:: Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) с этим идентификатором для получения интерфейса, зависящего от функции.

Часть, которая является соединителем, может поддерживать один из следующих интерфейсов элементов управления, зависящих от функции:

-   [**иксформатсуппорт**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)
-   [**иксжаккдескриптион**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)

Часть, которая является подединицей, может поддерживать один или несколько следующих интерфейсов элементов управления, зависящих от функции:

-   [**иаудиоаутогаинконтрол**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)
-   [**иаудиобасс**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)
-   [**иаудиочаннелконфиг**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)
-   [**иаудиоинпутселектор**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)
-   [**иаудиолауднесс**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)
-   [**иаудиомидранже**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)
-   [**иаудиомуте**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)
-   [**иаудиуутпутселектор**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)
-   [**иаудиопеакметер**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)
-   [**иаудиотребле**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)
-   [**иаудиоволумелевел**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)
-   [**идевицеспеЦификпроперти**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)

Часть поддерживает интерфейс **идевицеспеЦификпроперти** , только если базовый аппаратный элемент управления имеет зависящее от устройства значение элемента управления, и элемент управления не может быть адекватно представлен каким-либо другим интерфейсом, зависящим от функции, в приведенном выше списке. Как правило, свойство для конкретного устройства удобно использовать только для клиента, который может определить значение свойства из таких сведений, как тип части, подтип части и имя части. Клиент может получить эти сведения, вызвав методы [**ипарт:: жетпарттипе**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**Ипарт:: жетсубтипе**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype)и [**ипарт:: Name**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Руководство по программированию](programming-guide.md)
</dt> </dl>

 

 
