---
title: Реализация поведения устройства
description: Поведение устройства определяется предоставляемыми им службами.
ms.assetid: 5b352870-6de1-42f2-a178-ed7036b7afc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce2857c11a02ef5eeebe7b2cd5e75ee76138929e5bd95a2e3bdfa7ffd2c71dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137267"
---
# <a name="implementing-device-behavior"></a>Реализация поведения устройства

Поведение устройства определяется предоставляемыми им службами. Каждая служба имеет описание службы, в котором перечислены ее действия и переменные состояния. Вместе эти описания служб составляют интерфейс службы, который определяет способ, которым точка управления может взаимодействовать со службой. Каждая служба должна иметь по крайней мере одно действие.

Для реализации службы размещенное устройство должно предоставлять объект модели COM, предоставляющий интерфейс для службы. В описании службы интерфейсы служб указываются на языке шаблона UPnP (УТЛ). Однако интерфейсы объектов COM обычно задаются в языке определения интерфейса (IDL). Можно также указать COM-интерфейс в файле библиотеки типов или заголовка. Пакет средств разработки программного обеспечения платформы (SDK) включает средство Utl2idl, которое преобразует описание службы в УТЛ в COM-интерфейс в IDL.

В следующих примерах иллюстрируется процесс преобразования. Описание службы предоставляется разработчиком устройства и написано на УТЛ.

``` syntax
<?xml version="1.0" ?> 
  <scpd xmlns="urn:schemas-upnp-org:service-1-0">

    <specVersion>
      <major>1</major> 
      <minor>0</minor> 
    </specVersion>

    <serviceStateTable>
      <stateVariable>
        <name>Power</name> 
        <dataType>Boolean</dataType> 
        <defaultValue>0</defaultValue> 
      </stateVariable>

      <stateVariable>
        <name>Level</name> 
        <dataType>i4</dataType> 
        <allowedValueRange>
          <minimum>0</minimum> 
            <maximum>10</maximum> 
            <step>1</step> 
        </allowedValueRange>
        <defaultValue>0</defaultValue> 
      </stateVariable>

      <stateVariable>
        <name>State</name> 
        <dataType>string</dataType> 
        <allowedValueList>
          <allowedValue>ON</allowedValue> 
          <allowedValue>OFF</allowedValue> 
          <allowedValue>DIMMED</allowedValue> 
        </allowedValueList>
        <defaultValue>OFF</defaultValue> 
      </stateVariable>
    </serviceStateTable>

    <actionList>
      <action>
        <name>PowerOn</name> 
      </action>

      <action>
        <name>PowerOff</name> 
      </action>

      <action>
        <name>SetLevel</name> 
        <argumentList>
          <argument>
            <name>NewLevel</name> 
            <relatedStateVariable>Level</relatedStateVariable> 
            <direction>in</direction> 
          </argument>
          <argument>
            <name>NewState</name> 
            <relatedStateVariable>State</relatedStateVariable> 
            <direction>out</direction> 
          </argument>
        </argumentList>
      </action>

      <action>
        <name>IncreaseLevel</name> 
      </action>

      <action>
        <name>DecreaseLevel</name> 
      </action>
    </actionList>
</scpd>
```

Следующим шагом является запуск средства Utl2idl. Он создает IDL-файл, содержащий интерфейс COM. Дополнительные сведения о IDL-файлах и ключевом слове **Interface** см. в разделе [файл определения интерфейса (IDL)](/windows/desktop/Midl/interface-definition-idl-file) и [**интерфейс**](/windows/desktop/Midl/interface) в справочнике по MIDL.

``` syntax
#include <windows.h>
typedef [v1_enum] enum SCPD_DISPIDS
{
     DISPID_POWER = 1,
     DISPID_LEVEL,
     DISPID_STATE,
     DISPID_POWERON,
     DISPID_POWEROFF,
     DISPID_SETLEVEL,
     DISPID_INCREASELEVEL,
     DISPID_DECREASELEVEL
} SCPD_DISPIDS;

[
     uuid(68369839-960d-4c8c-8d0d-c319c69e73be),
     oleautomation,
     pointer_default(unique)
]
interface IUPnPService_scpd : IUnknown 
{
     [propget, id(DISPID_POWER), helpstring("Property Power")]
     HRESULT Power(
          [out, retval] VARIANT_BOOL *pPower);

     [propget, id(DISPID_LEVEL), helpstring("Property Level")]
     HRESULT Level(
          [out, retval] long *pLevel);

     [propget, id(DISPID_STATE), helpstring("Property State")]
     HRESULT State(
          [out, retval] BSTR *pState);

     [ id(DISPID_POWERON), helpstring("Method PowerOn")]
     HRESULT PowerOn();

     [ id(DISPID_POWEROFF), helpstring("Method PowerOff")]
     HRESULT PowerOff();

     [ id(DISPID_SETLEVEL), helpstring("Method SetLevel")]
     HRESULT SetLevel(
          [in] long NewLevel,
          [in, out] BSTR *pNewState;
                                
     [ id(DISPID_INCREASELEVEL), helpstring("Method IncreaseLevel")]
     HRESULT IncreaseLevel();

     [ id(DISPID_DECREASELEVEL), helpstring("Method DecreaseLevel")]
     HRESULT DecreaseLevel();
};
```

> [!Note]
> Возвращаемое значение является первым \[ выходным \] параметром в списке аргументов в описании службы, однако он указан как последний параметр после перевода.
> 
> Все остальные параметры остаются в том же порядке.

 

Чтобы предоставить функциональные возможности службы, реализуйте этот COM-интерфейс.

## <a name="obtaining-information-about-an-endpoint"></a>Получение сведений о конечной точке

В инфраструктуре UPnP сведения о конечной точке включают сведения о запросе и его источнике. Устройство может проверить эти сведения, чтобы принять решение о запросе.

Сведения о конечной точке могут быть доступны для реализованной службы. Узел устройства имеет доступ к сведениям о конечной точке; Однако по умолчанию узел устройства не передает сведения в реализованную службу. Вы можете разрешить узлу устройства совместно использовать сведения о конечной точке с реализованной службой, изменив интерфейс COM в IDL-файле (созданном средством Utl2idl). \[В \] каждый метод, для которого требуются сведения о конечной точке, можно добавить параметр in. Дополнительный \[ параметр in \] должен быть первым в списке аргументов, указателем на интерфейс [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) и явно названным **пункремотиндпоинтинфо**. Изменения в XML-коде службы не являются обязательными и не рекомендуются. В следующем примере показано новое определение метода **поверон** при его дополнении для получения сведений о конечной точке:

"HRESULT Поверон ( \[ в \] IUnknown \* пункремотиндпоинтинфо);"

Указатель на объект сведений о конечной точке, интерфейс [**иупнпремотиндпоинтинфо**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) , передается через этот новый параметр узлом устройства. Интерфейс **иупнпремотиндпоинтинфо** предоставляет три метода для доступа к сведениям о конечной точке. Необходимо вызвать соответствующий метод, чтобы получить сведения о конечной точке, необходимые для реализации службы.

В качестве альтернативы ручному изменению COM-интерфейса можно использовать средство Utl2idl с параметром **-CI** . Этот параметр приводит к тому, что средство добавляет параметр сведений о конечной точке в каждый из методов в интерфейсе COM. Использование параметра **-CI** не облегчает изменение отдельных методов. Если сведения о конечной точке не требуются для всех методов интерфейса, следует добавить параметр вручную, чтобы получить наиболее эффективные реализации.

## <a name="implementing-a-service-object"></a>Реализация объекта службы

Для преобразования описания каждой службы устройства необходимо использовать средство Utl2idl.

Объект, предоставляющий функциональность для службы, называется [*объектом службы*](s-gly.md). Помимо предоставления функциональных возможностей службы, объекты службы обрабатывали ошибки с помощью интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Дополнительные сведения см. в разделе [Использование API узла устройства с технологией UPnP](using-the-device-host-api-with-upnp-technology.md).

чтобы обеспечить совместимость с Visual Basic, который не поддерживает \[ параметры out \] , параметры/директион **направления** в описании службы преобразуются в \[ выходные \] параметры в IDL. Сервер должен освободить эти \[ выходные \] Параметры.

## <a name="implementing-a-device-control-object"></a>Реализация объекта управления устройством

Помимо реализации объектов службы, необходимо реализовать [*объект управления устройством*](d-gly.md). Объект управления устройством является центральной точкой управления и контроля для объектов службы устройства. Во время регистрации объект управления устройством передается на узел устройства. При получении подписки на события или управляющего запроса для одной из служб устройства узел устройства вызывает этот объект управления устройством для получения соответствующего объекта службы. В этот момент объект управления устройством либо создает экземпляр объекта службы, либо возвращает интерфейс существующего экземпляра объекта службы.

Описание устройства можно зарегистрировать на нескольких компьютерах или несколько раз на одном компьютере. Так как уникальное имя устройства (УДН) должно отличаться для каждого экземпляра устройства, узел устройства создает уникальный УДН для каждого устройства и встроенного устройства каждый раз при регистрации устройства. Используйте УДН, указанный в шаблоне описания устройства, чтобы получить фактические УДН, созданные узлом устройства и связанные с устройством. Чтобы отменить регистрацию устройства, необходимо использовать идентификатор, предоставленный инфраструктурой UPnP при регистрации устройства.

Объекты управления устройствами должны реализовывать интерфейс [**иупнпдевицеконтрол**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) . Узел устройства вызывает метод [**иупнпдевицеконтрол:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) объекта управления устройством, передавая в нем описание устройства на основе UPnP, которое ранее было опубликовано узлом устройства, и строку инициализации, указанную во время регистрации (см. раздел [Регистрация размещенного устройства на узле устройства](registering-a-hosted-device-with-the-device-host.md)). В описании этого устройства объект управления устройством считывает Уднс, назначенный каждому устройству в дереве устройств. Для получения этих сведений можно также использовать метод [**иупнпрегистрар:: жетуникуедевиценаме**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) .

Когда узлу устройства требуется указатель на объект службы, реализующий определенную службу, он вызывает метод [**иупнпдевицеконтрол:: жетсервицеобжект**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) для объекта управления устройством. Узел устройства передает УДН и идентификатор службы, для которой он запрашивает объект службы, и адрес указателя [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , в котором метод должен вернуть указатель на объект службы. Параметр УДН необходим, так как управляющий объект устройства управляет службами для всего дерева устройств, включая вложенные устройства. Если узел устройства запрашивает вложенное устройство, **жетсервицеобжект** использует УДН для его обнаружения.

 

 