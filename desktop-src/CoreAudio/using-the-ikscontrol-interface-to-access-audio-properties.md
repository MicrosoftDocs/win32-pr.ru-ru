---
description: Использование интерфейса Иксконтрол для доступа к свойствам аудио
ms.assetid: 72bf9164-96c6-4543-b858-19480b032fdb
title: Использование интерфейса Иксконтрол для доступа к свойствам аудио
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a67639a0e51334da80b7bff88293414a58bb204c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262683"
---
# <a name="using-the-ikscontrol-interface-to-access-audio-properties"></a>Использование интерфейса Иксконтрол для доступа к свойствам аудио

В редких случаях специализированному звуковому приложению может потребоваться использовать интерфейс [**иксконтрол**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) для доступа к определенным аппаратным возможностям звукового адаптера, которые не предоставляются [API Девицетопологи](devicetopology-api.md) или [API ммдевице](mmdevice-api.md). Интерфейс **иксконтрол** делает свойства, события и методы устройств потоковой передачи (KS) доступными для приложений пользовательского режима. Основным интересом к звуковым приложениям являются свойства KS. Интерфейс **иксконтрол** можно использовать совместно с API ДЕВИЦЕТОПОЛОГИ и API ммдевице для доступа к свойствам KS звуковых адаптеров.

Интерфейс [**иксконтрол**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) предназначен главным образом для использования поставщиками оборудования, которые пишут приложения панели управления для управления звуковым оборудованием. **Иксконтрол** менее удобен для звуковых приложений общего назначения, которые не привязаны к определенным аппаратным устройствам. Это связано с тем, что поставщики оборудования часто реализуют собственные механизмы для доступа к свойствам аудио своих устройств. В отличие от API Девицетопологи, который скрывает особенности аппаратно-зависимых драйверов и предоставляет сравнительно единообразный интерфейс для доступа к свойствам аудио, приложения используют **иксконтрол** для непосредственного взаимодействия с драйверами. Дополнительные сведения о **иксконтрол** см. в документации по Windows DDK.

Как обсуждалось в разделе [топологии устройств](device-topologies.md), подразделение в топологии устройства адаптера может поддерживать один или несколько интерфейсов элементов управления, зависящих от функции, показанных в левом столбце следующей таблицы. Каждая запись в правом столбце таблицы — это свойство KS, соответствующее интерфейсу элемента управления слева. Интерфейс элемента управления предоставляет удобный доступ к свойству. Большинство аудио-драйверов используют свойства KS для представления возможностей обработки, характерных для функций подразделений (также называемых узлами KS) в топологиях своих звуковых адаптеров. Дополнительные сведения о свойствах KS и узлах KS см. в документации по Windows DDK.



| Интерфейс управления                                          | KS, свойство                        |
|------------------------------------------------------------|------------------------------------|
| [**иаудиоаутогаинконтрол**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | КСПРОПЕРТИ \_ Audio \_ АГК             |
| [**иаудиобасс**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | КСПРОПЕРТИ \_ Audio \_ НЧ            |
| [**иаудиочаннелконфиг**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | \_ \_ Конфигурация канала кспроперти \_ Audio |
| [**иаудиоинпутселектор**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | \_ \_ источник мультиплексора кспроперти Audio \_     |
| [**иаудиолауднесс**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | КСПРОПЕРТИ \_ \_ громкости звука        |
| [**иаудиомидранже**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | КСПРОПЕРТИ \_ аудио \_ середина             |
| [**иаудиомуте**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | \_Выключить звук \_ кспроперти            |
| [**иаудиуутпутселектор**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | \_приемник кспроперти Audio \_ демультиплексирование \_     |
| [**иаудиопеакметер**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | КСПРОПЕРТИ \_ Audio \_ пеакметер       |
| [**иаудиотребле**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | КСПРОПЕРТИ \_ аудио \_ ВЧ          |
| [**иаудиоволумелевел**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | КСПРОПЕРТИ \_ Audio \_ волумелевел     |
| [**идевицеспеЦификпроперти**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | КСПРОПЕРТИ \_ для \_ разработки \_ аудио   |



 

Топологии некоторых звуковых адаптеров могут содержать подединицы, имеющие свойства KS, которых нет в приведенной выше таблице. Например, предположим, что вызов метода [**ипарт:: жетсубтипе**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) для определенной подединицы получает значение GUID кснодетипе \_ тон. Этот тип GUID этого подтипа указывает, что подединица поддерживает одно или несколько следующих свойств KS:

-   КСПРОПЕРТИ \_ Audio \_ НЧ
-   КСПРОПЕРТИ \_ аудио \_ середина
-   КСПРОПЕРТИ \_ аудио \_ ВЧ
-   \_ \_ усиление кспроперти звука басов \_

Первые три свойства в этом списке можно получить с помощью интерфейсов элементов управления, которые отображаются в предыдущей таблице, но свойство КСПРОПЕРТИ \_ Audio \_ басов \_ Boost не имеет соответствующего интерфейса управления в API девицетопологи. Однако приложение может использовать интерфейс [**иксконтрол**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) для доступа к этому свойству, если подединица поддерживает свойство.

Чтобы получить доступ к \_ свойству кспроперти Audio басов для \_ \_ подединицы подтипа кснодетипе тон, необходимо выполнить следующие действия \_ :

1.  Вызовите метод [**иконнектор:: жетдевицеидконнектедто**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getdeviceidconnectedto) или [**Идевицетопологи:: GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) , чтобы получить строку идентификатора устройства, идентифицирующее устройство адаптера. Эта строка похожа на [строку идентификатора конечной точки](endpoint-id-strings.md), за исключением того, что она определяет устройство адаптера вместо устройства конечной точки. Дополнительные сведения о различиях между устройством адаптера и конечным устройством см. в статье [устройства конечных точек аудио](audio-endpoint-devices.md).
2.  Получите интерфейс [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) устройства адаптера, вызвав метод [**иммдевицеенумератор::**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) GetString с идентификатором устройства. Этот интерфейс **иммдевице** тот же, что и интерфейс, описанный в **интерфейсе иммдевице**, но он представляет устройство адаптера вместо устройства конечной точки.
3.  Получите интерфейс [**иксконтрол**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) в подразделении, вызвав метод [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) с параметром *IID* , равным **рефиид** IID \_ иксконтрол. Обратите внимание, что интерфейсы, поддерживаемые этим методом **активации** , предназначенным для устройства адаптера, отличаются от интерфейсов, поддерживаемых методом **Activate** для устройства конечной точки. В частности, метод **Activate** для устройства адаптера поддерживает **иксконтрол**.
4.  Вызовите метод [**ипарт:: жетлокалид**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getlocalid) , чтобы получить локальный идентификатор подединицы.
5.  Создание запроса свойства KS. Идентификатор узла KS, необходимый для запроса, содержится в 16-значащих битах локального идентификатора, полученного на предыдущем шаге.
6.  Отправьте запрос свойства KS в звуковой драйвер, вызвав метод [**иксконтрол:: кспроперти**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) . Дополнительные сведения об этом методе см. в документации по Windows DDK.

В следующем примере кода извлекается значение \_ Свойства Boost кспроперти Audio \_ басов \_ из подединицы подтипа \_ тон кснодетипе:


```C++
//-----------------------------------------------------------
// This function calls the IKsControl::Property method to get
// the value of the KSPROPERTY_AUDIO_BASS_BOOST property of
// a subunit. Parameter pPart should point to a part that is
// a subunit with a subtype GUID value of KSNODETYPE_TONE.
//-----------------------------------------------------------
#define PARTID_MASK 0x0000ffff
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IKsControl = __uuidof(IKsControl);

HRESULT GetBassBoost(IMMDeviceEnumerator *pEnumerator,
                     IPart *pPart, BOOL *pbValue)
{
    HRESULT hr;
    IDeviceTopology *pTopology = NULL;
    IMMDevice *pPnpDevice = NULL;
    IKsControl *pKsControl = NULL;
    LPWSTR pwszDeviceId = NULL;

    if (pEnumerator == NULL || pPart == NULL || pbValue == NULL)
    {
        return E_INVALIDARG;
    }

    // Get the topology object for the adapter device that contains
    // the subunit represented by the IPart interface.
    hr = pPart->GetTopologyObject(&pTopology);
    EXIT_ON_ERROR(hr)

    // Get the device ID string that identifies the adapter device.
    hr = pTopology->GetDeviceId(&pwszDeviceId);
    EXIT_ON_ERROR(hr)

    // Get the IMMDevice interface of the adapter device object.
    hr = pEnumerator->GetDevice(pwszDeviceId, &pPnpDevice);
    EXIT_ON_ERROR(hr)

    // Activate an IKsControl interface on the adapter device object.
    hr = pPnpDevice->Activate(IID_IKsControl, CLSCTX_ALL, NULL, (void**)&pKsControl);
    EXIT_ON_ERROR(hr)

    // Get the local ID of the subunit (contains the KS node ID).
    UINT localId = 0;
    hr = pPart->GetLocalId(&localId);
    EXIT_ON_ERROR(hr)

    KSNODEPROPERTY_AUDIO_CHANNEL ksprop;
    ZeroMemory(&ksprop, sizeof(ksprop));
    ksprop.NodeProperty.Property.Set = KSPROPSETID_Audio;
    ksprop.NodeProperty.Property.Id = KSPROPERTY_AUDIO_BASS_BOOST;
    ksprop.NodeProperty.Property.Flags = KSPROPERTY_TYPE_GET | KSPROPERTY_TYPE_TOPOLOGY;
    ksprop.NodeProperty.NodeId = localId & PARTID_MASK;
    ksprop.Channel = 0;

    // Send the property request.to the device driver.
    BOOL bValue = FALSE;
    ULONG valueSize;
    hr = pKsControl->KsProperty(
                         &ksprop.NodeProperty.Property, sizeof(ksprop),
                         &bValue, sizeof(bValue), &valueSize);
    EXIT_ON_ERROR(hr)

    *pbValue = bValue;

Exit:
    SAFE_RELEASE(pTopology)
    SAFE_RELEASE(pPnpDevice)
    SAFE_RELEASE(pKsControl)
    CoTaskMemFree(pwszDeviceId);
    return hr;
}

```



В предыдущем примере кода функция Жетбассбуст принимает следующие три параметра:

-   `pEnumerator` Указывает на интерфейс [**иммдевицеенумератор**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) перечислителя конечной точки аудио.
-   `pPart` Указывает на интерфейс [**ипарт**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) подразделении с подтипом \_ тонового кснодетипе.
-   `pbValue` Указывает на переменную **bool** , в которую функция записывает значение свойства.

Программа вызывает Жетбассбуст только после вызова [**ипарт:: жетсубтипе**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) и определяет, что подединица подразделений кснодетипе \_ . Значение свойства равно **true** , если включено усиление басов. **Значение false** , если усиление басов отключено.

В начале функции Жетбассбуст вызов метода [**ипарт:: жеттопологйобжект**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) получает интерфейс [**идевицетопологи**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) устройства адаптера, который содержит \_ подединицу тонового блока. Вызов метода [**идевицетопологи:: GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) ИЗВЛЕКАЕТ строку идентификатора устройства, идентифицирующее устройство адаптера. Вызов метода [**иммдевицеенумератор::**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) GetString принимает строку идентификатора устройства в качестве входного параметра и получает интерфейс [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) устройства адаптера. Затем вызов метода [**иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) получает интерфейс [**иксконтрол**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) подразделений. Дополнительные сведения об интерфейсе **иксконтрол** см. в документации по Windows DDK.

Затем в предыдущем примере кода создается структура [**кснодепроперти \_ Audio \_ Channel**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) , описывающая свойство басов-Boost. Пример кода передает указатель на структуру методу [**иксконтрол:: кспроперти**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) , который использует сведения в структуре для получения значения свойства. Дополнительные сведения о структуре **кснодепроперти \_ Audio \_ Channel** и методе **иксконтрол:: кспроперти** см. в документации по Windows DDK.

Звуковые аппаратные устройства обычно присваивают каждому каналу звукового потока отдельное состояние басов-Boost. В принципе, усиление басов можно включить для некоторых каналов и отключить для других. Структура [**\_ звукового \_ канала Кснодепроперти**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) содержит элемент **Channel** , указывающий номер канала. Если поток содержит *N* каналов, каналы нумеруются от 0 до *N*— 1. Предыдущий пример кода получает значение свойства басов-Boost только для канала 0. Эта реализация неявно предполагает, что свойства басов-Boost для всех каналов устанавливаются единообразно в одно и то же состояние. Поэтому, чтобы определить значение свойства для потока, достаточно прочесть свойство басов-Boost для канала 0. Чтобы обеспечить соответствие этому предположении, соответствующая функция, устанавливающая свойство басов-Boost, задаст всем каналам одно значение свойства басов-Boost. Это разумные соглашения, но не все поставщики оборудования должны следовать им. Например, поставщик может предоставить приложение панели управления, которое обеспечивает увеличение басов только для каналов, которые могут использовать динамики с полным диапазоном. (Динамик с полным диапазоном может воспроизводить звуки в пределах от басов до высоких частот.) В этом случае значение свойства, полученное в предыдущем примере кода, может не точно представлять состояние потока с частотой басов.

Клиенты, использующие интерфейсы управления, перечисленные в предыдущей таблице, могут вызывать метод [**ипарт:: регистерконтролчанжекаллбакк**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-registercontrolchangecallback) для регистрации уведомлений при изменении значения параметра элемента управления. Обратите внимание, что интерфейс [**иксконтрол**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) не предоставляет клиентам аналогичные средства для регистрации уведомлений при изменении значения свойства. Если **иксконтрол** поддерживал уведомления об изменениях свойств, оно может сообщить приложению, когда другое приложение изменило значение свойства. Однако в отличие от наиболее часто используемых элементов управления, которые отслеживаются через [**ипарт**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) уведомления, свойства, управляемые **иксконтрол** , предназначены главным образом для использования поставщиками оборудования, и эти свойства, скорее всего, будут изменены только приложениями панели управления, написанными поставщиками. Если приложение должно обнаруживать изменения свойств, внесенные другим приложением, оно может обнаружить изменения, периодически опрашивая значение свойства через **иксконтрол**.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Руководство по программированию](programming-guide.md)
</dt> </dl>

 

 
