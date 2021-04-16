---
title: Реализация поведения устройства
description: Поведение устройства определяется предоставляемыми им службами.
ms.assetid: 5b352870-6de1-42f2-a178-ed7036b7afc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb702adf3ccb0f21bc71f08e98427cca15495f3b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105651246"
---
# <a name="implementing-device-behavior"></a><span data-ttu-id="97f2a-103">Реализация поведения устройства</span><span class="sxs-lookup"><span data-stu-id="97f2a-103">Implementing Device Behavior</span></span>

<span data-ttu-id="97f2a-104">Поведение устройства определяется предоставляемыми им службами.</span><span class="sxs-lookup"><span data-stu-id="97f2a-104">The behavior of a device is defined by the services it exposes.</span></span> <span data-ttu-id="97f2a-105">Каждая служба имеет описание службы, в котором перечислены ее действия и переменные состояния.</span><span class="sxs-lookup"><span data-stu-id="97f2a-105">Each service has a service description that lists its actions and state variables.</span></span> <span data-ttu-id="97f2a-106">Вместе эти описания служб составляют интерфейс службы, который определяет способ, которым точка управления может взаимодействовать со службой.</span><span class="sxs-lookup"><span data-stu-id="97f2a-106">Taken together, these service descriptions make up the service interface, which defines the way in which a control point can interact with a service.</span></span> <span data-ttu-id="97f2a-107">Каждая служба должна иметь по крайней мере одно действие.</span><span class="sxs-lookup"><span data-stu-id="97f2a-107">Each service must have at least one action.</span></span>

<span data-ttu-id="97f2a-108">Для реализации службы размещенное устройство должно предоставлять объект модели COM, предоставляющий интерфейс для службы.</span><span class="sxs-lookup"><span data-stu-id="97f2a-108">To implement a service, a hosted device must provide a Component Object Model (COM) object that exposes the interface for the service.</span></span> <span data-ttu-id="97f2a-109">В описании службы интерфейсы служб указываются на языке шаблона UPnP (УТЛ). Однако интерфейсы объектов COM обычно задаются в языке определения интерфейса (IDL).</span><span class="sxs-lookup"><span data-stu-id="97f2a-109">In the service description, the service interfaces are specified in UPnP Template Language (UTL); however, COM object interfaces typically are specified in Interface Definition Language (IDL).</span></span> <span data-ttu-id="97f2a-110">Можно также указать COM-интерфейс в файле библиотеки типов или заголовка.</span><span class="sxs-lookup"><span data-stu-id="97f2a-110">You can also specify the COM interface in a type library or header file.</span></span> <span data-ttu-id="97f2a-111">Пакет средств разработки программного обеспечения платформы (SDK) включает средство Utl2idl, которое преобразует описание службы в УТЛ в COM-интерфейс в IDL.</span><span class="sxs-lookup"><span data-stu-id="97f2a-111">The Platform Software Development Kit (SDK) includes the Utl2idl tool, which translates a service description in UTL to a COM interface in IDL.</span></span>

<span data-ttu-id="97f2a-112">В следующих примерах иллюстрируется процесс преобразования.</span><span class="sxs-lookup"><span data-stu-id="97f2a-112">The following samples illustrate this conversion process.</span></span> <span data-ttu-id="97f2a-113">Описание службы предоставляется разработчиком устройства и написано на УТЛ.</span><span class="sxs-lookup"><span data-stu-id="97f2a-113">The service description is provided by the device developer and is written in UTL.</span></span>

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

<span data-ttu-id="97f2a-114">Следующим шагом является запуск средства Utl2idl.</span><span class="sxs-lookup"><span data-stu-id="97f2a-114">The next step is to run the Utl2idl tool.</span></span> <span data-ttu-id="97f2a-115">Он создает IDL-файл, содержащий интерфейс COM.</span><span class="sxs-lookup"><span data-stu-id="97f2a-115">It produces the IDL file that contains the COM interface.</span></span> <span data-ttu-id="97f2a-116">Дополнительные сведения о IDL-файлах и ключевом слове **Interface** см. в разделе [файл определения интерфейса (IDL)](/windows/desktop/Midl/interface-definition-idl-file) и [**интерфейс**](/windows/desktop/Midl/interface) в справочнике по MIDL.</span><span class="sxs-lookup"><span data-stu-id="97f2a-116">For more information about IDL files and the **interface** keyword, see [Interface Definition (IDL) File](/windows/desktop/Midl/interface-definition-idl-file) and [**interface**](/windows/desktop/Midl/interface) in the MIDL reference.</span></span>

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
> <span data-ttu-id="97f2a-117">Возвращаемое значение является первым \[ выходным \] параметром в списке аргументов в описании службы, однако он указан как последний параметр после перевода.</span><span class="sxs-lookup"><span data-stu-id="97f2a-117">The return value is the first \[out\] parameter in the list of arguments in the service description; however, it is listed as the last parameter after translation.</span></span>
> 
> <span data-ttu-id="97f2a-118">Все остальные параметры остаются в том же порядке.</span><span class="sxs-lookup"><span data-stu-id="97f2a-118">All other parameters remain in the same order.</span></span>

 

<span data-ttu-id="97f2a-119">Чтобы предоставить функциональные возможности службы, реализуйте этот COM-интерфейс.</span><span class="sxs-lookup"><span data-stu-id="97f2a-119">To provide the functionality of the service, implement this COM interface.</span></span>

## <a name="obtaining-information-about-an-endpoint"></a><span data-ttu-id="97f2a-120">Получение сведений о конечной точке</span><span class="sxs-lookup"><span data-stu-id="97f2a-120">Obtaining Information About an Endpoint</span></span>

<span data-ttu-id="97f2a-121">В инфраструктуре UPnP сведения о конечной точке включают сведения о запросе и его источнике.</span><span class="sxs-lookup"><span data-stu-id="97f2a-121">In the UPnP framework, endpoint information includes information about a request and its source.</span></span> <span data-ttu-id="97f2a-122">Устройство может проверить эти сведения, чтобы принять решение о запросе.</span><span class="sxs-lookup"><span data-stu-id="97f2a-122">A device can examine this information in order to make a decision about the request.</span></span>

<span data-ttu-id="97f2a-123">Сведения о конечной точке могут быть доступны для реализованной службы.</span><span class="sxs-lookup"><span data-stu-id="97f2a-123">Endpoint information is optionally available to the implemented service.</span></span> <span data-ttu-id="97f2a-124">Узел устройства имеет доступ к сведениям о конечной точке; Однако по умолчанию узел устройства не передает сведения в реализованную службу.</span><span class="sxs-lookup"><span data-stu-id="97f2a-124">The device host has access to endpoint information; however, the device host does not communicate the information to the implemented service by default.</span></span> <span data-ttu-id="97f2a-125">Вы можете разрешить узлу устройства совместно использовать сведения о конечной точке с реализованной службой, изменив интерфейс COM в IDL-файле (созданном средством Utl2idl).</span><span class="sxs-lookup"><span data-stu-id="97f2a-125">You can enable the device host to share the endpoint information with the implemented service by modifying the COM interface in the IDL file (produced by the Utl2idl tool).</span></span> <span data-ttu-id="97f2a-126">\[В \] каждый метод, для которого требуются сведения о конечной точке, можно добавить параметр in.</span><span class="sxs-lookup"><span data-stu-id="97f2a-126">You can add an \[in\] parameter to each method that requires endpoint information.</span></span> <span data-ttu-id="97f2a-127">Дополнительный \[ параметр in \] должен быть первым в списке аргументов, указателем на интерфейс [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) и явно названным **пункремотиндпоинтинфо**.</span><span class="sxs-lookup"><span data-stu-id="97f2a-127">The additional \[in\] parameter must be the first one in the list of arguments, a pointer to an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface, and explicitly named **punkRemoteEndpointInfo**.</span></span> <span data-ttu-id="97f2a-128">Изменения в XML-коде службы не являются обязательными и не рекомендуются.</span><span class="sxs-lookup"><span data-stu-id="97f2a-128">Modifications to the Service XML are not required, or recommended.</span></span> <span data-ttu-id="97f2a-129">В следующем примере показано новое определение метода **поверон** при его дополнении для получения сведений о конечной точке:</span><span class="sxs-lookup"><span data-stu-id="97f2a-129">The following example shows the new definition of the **PowerOn** method when it is amended so that it receives endpoint information:</span></span>

<span data-ttu-id="97f2a-130">"HRESULT Поверон ( \[ в \] IUnknown \* пункремотиндпоинтинфо);"</span><span class="sxs-lookup"><span data-stu-id="97f2a-130">"HRESULT PowerOn(\[in\] IUnknown \*punkRemoteEndpointInfo);"</span></span>

<span data-ttu-id="97f2a-131">Указатель на объект сведений о конечной точке, интерфейс [**иупнпремотиндпоинтинфо**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) , передается через этот новый параметр узлом устройства.</span><span class="sxs-lookup"><span data-stu-id="97f2a-131">A pointer to an endpoint information object, an [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) interface, is passed through this new parameter by the device host.</span></span> <span data-ttu-id="97f2a-132">Интерфейс **иупнпремотиндпоинтинфо** предоставляет три метода для доступа к сведениям о конечной точке.</span><span class="sxs-lookup"><span data-stu-id="97f2a-132">The **IUPnPRemoteEndpointInfo** interface provides three methods for accessing the endpoint information.</span></span> <span data-ttu-id="97f2a-133">Необходимо вызвать соответствующий метод, чтобы получить сведения о конечной точке, необходимые для реализации службы.</span><span class="sxs-lookup"><span data-stu-id="97f2a-133">You must call the appropriate method to get the endpoint information that is required by the service implementation.</span></span>

<span data-ttu-id="97f2a-134">В качестве альтернативы ручному изменению COM-интерфейса можно использовать средство Utl2idl с параметром **-CI** .</span><span class="sxs-lookup"><span data-stu-id="97f2a-134">As an alternative to manual modification of the COM interface, you can use the Utl2idl tool with the **-ci** switch.</span></span> <span data-ttu-id="97f2a-135">Этот параметр приводит к тому, что средство добавляет параметр сведений о конечной точке в каждый из методов в интерфейсе COM.</span><span class="sxs-lookup"><span data-stu-id="97f2a-135">This switch causes the tool to add the endpoint information parameter to each of the methods in the COM interface.</span></span> <span data-ttu-id="97f2a-136">Использование параметра **-CI** не облегчает изменение отдельных методов.</span><span class="sxs-lookup"><span data-stu-id="97f2a-136">Using the **-ci** switch does not facilitate modification of individual methods.</span></span> <span data-ttu-id="97f2a-137">Если сведения о конечной точке не требуются для всех методов интерфейса, следует добавить параметр вручную, чтобы получить наиболее эффективные реализации.</span><span class="sxs-lookup"><span data-stu-id="97f2a-137">If endpoint information is not needed by all methods of an interface, you should add the parameter manually in order to produce the most efficient implementations.</span></span>

## <a name="implementing-a-service-object"></a><span data-ttu-id="97f2a-138">Реализация объекта службы</span><span class="sxs-lookup"><span data-stu-id="97f2a-138">Implementing a Service Object</span></span>

<span data-ttu-id="97f2a-139">Для преобразования описания каждой службы устройства необходимо использовать средство Utl2idl.</span><span class="sxs-lookup"><span data-stu-id="97f2a-139">You must use the Utl2idl tool to translate each service description of a device.</span></span>

<span data-ttu-id="97f2a-140">Объект, предоставляющий функциональность для службы, называется [*объектом службы*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="97f2a-140">An object that provides the functionality for a service is referred to as a [*service object*](s-gly.md).</span></span> <span data-ttu-id="97f2a-141">Помимо предоставления функциональных возможностей службы, объекты службы обрабатывали ошибки с помощью интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="97f2a-141">In addition to providing service functionality, service objects handle errors by using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="97f2a-142">Дополнительные сведения см. в разделе [Использование API узла устройства с технологией UPnP](using-the-device-host-api-with-upnp-technology.md).</span><span class="sxs-lookup"><span data-stu-id="97f2a-142">For more information, see [Using the Device Host API with UPnP Technology](using-the-device-host-api-with-upnp-technology.md).</span></span>

<span data-ttu-id="97f2a-143">Чтобы обеспечить совместимость с Visual Basic, который не поддерживает \[ параметры out \] , параметры/директион **направления** в описании службы преобразуются в \[ выходные \] Параметры в IDL.</span><span class="sxs-lookup"><span data-stu-id="97f2a-143">To ensure compatibility with Visual Basic, which does not support \[out\] parameters, the **direction** out **/direction** parameters in the service description are converted to \[in, out\] parameters in IDL.</span></span> <span data-ttu-id="97f2a-144">Сервер должен освободить эти \[ выходные \] Параметры.</span><span class="sxs-lookup"><span data-stu-id="97f2a-144">The server must free these \[in, out\] parameters.</span></span>

## <a name="implementing-a-device-control-object"></a><span data-ttu-id="97f2a-145">Реализация объекта управления устройством</span><span class="sxs-lookup"><span data-stu-id="97f2a-145">Implementing a Device Control Object</span></span>

<span data-ttu-id="97f2a-146">Помимо реализации объектов службы, необходимо реализовать [*объект управления устройством*](d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="97f2a-146">In addition to implementing service objects, you must implement a [*device control object*](d-gly.md).</span></span> <span data-ttu-id="97f2a-147">Объект управления устройством является центральной точкой управления и контроля для объектов службы устройства.</span><span class="sxs-lookup"><span data-stu-id="97f2a-147">A device control object is the central point of management and control for the device's service objects.</span></span> <span data-ttu-id="97f2a-148">Во время регистрации объект управления устройством передается на узел устройства.</span><span class="sxs-lookup"><span data-stu-id="97f2a-148">At registration time, the device control object is passed to the device host.</span></span> <span data-ttu-id="97f2a-149">При получении подписки на события или управляющего запроса для одной из служб устройства узел устройства вызывает этот объект управления устройством для получения соответствующего объекта службы.</span><span class="sxs-lookup"><span data-stu-id="97f2a-149">When an event subscription or control request arrives for one of the device's services, the device host calls into this device control object to obtain the relevant service object.</span></span> <span data-ttu-id="97f2a-150">В этот момент объект управления устройством либо создает экземпляр объекта службы, либо возвращает интерфейс существующего экземпляра объекта службы.</span><span class="sxs-lookup"><span data-stu-id="97f2a-150">At that time, the device control object either creates an instance of the service object or returns the interface of an existing instance of the service object.</span></span>

<span data-ttu-id="97f2a-151">Описание устройства можно зарегистрировать на нескольких компьютерах или несколько раз на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="97f2a-151">You can register a device description on multiple computers or multiple times on the same computer.</span></span> <span data-ttu-id="97f2a-152">Так как уникальное имя устройства (УДН) должно отличаться для каждого экземпляра устройства, узел устройства создает уникальный УДН для каждого устройства и встроенного устройства каждый раз при регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="97f2a-152">Because the Unique Device Name (UDN) must be different for each instance of the device, the device host generates a unique UDN for each device and embedded device each time the device is registered.</span></span> <span data-ttu-id="97f2a-153">Используйте УДН, указанный в шаблоне описания устройства, чтобы получить фактические УДН, созданные узлом устройства и связанные с устройством.</span><span class="sxs-lookup"><span data-stu-id="97f2a-153">Use the UDN specified in the device description template to obtain the actual UDN generated by the device host and associated with the device.</span></span> <span data-ttu-id="97f2a-154">Чтобы отменить регистрацию устройства, необходимо использовать идентификатор, предоставленный инфраструктурой UPnP при регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="97f2a-154">To unregister a device, you must use the ID provided by the UPnP framework when the device was registered.</span></span>

<span data-ttu-id="97f2a-155">Объекты управления устройствами должны реализовывать интерфейс [**иупнпдевицеконтрол**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) .</span><span class="sxs-lookup"><span data-stu-id="97f2a-155">Device control objects must implement the [**IUPnPDeviceControl**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) interface.</span></span> <span data-ttu-id="97f2a-156">Узел устройства вызывает метод [**иупнпдевицеконтрол:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) объекта управления устройством, передавая в нем описание устройства на основе UPnP, которое ранее было опубликовано узлом устройства, и строку инициализации, указанную во время регистрации (см. раздел [Регистрация размещенного устройства на узле устройства](registering-a-hosted-device-with-the-device-host.md)).</span><span class="sxs-lookup"><span data-stu-id="97f2a-156">The device host invokes the [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method of the device control object, passing in the UPnP-based device description that the device host previously published for the device and an initialization string that was specified at registration time (see [Registering a Hosted Device with the Device Host](registering-a-hosted-device-with-the-device-host.md)).</span></span> <span data-ttu-id="97f2a-157">В описании этого устройства объект управления устройством считывает Уднс, назначенный каждому устройству в дереве устройств.</span><span class="sxs-lookup"><span data-stu-id="97f2a-157">From this device description, the device control object reads the UDNs assigned to each of the devices in the device tree.</span></span> <span data-ttu-id="97f2a-158">Для получения этих сведений можно также использовать метод [**иупнпрегистрар:: жетуникуедевиценаме**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) .</span><span class="sxs-lookup"><span data-stu-id="97f2a-158">You can also use the [**IUPnPRegistrar::GetUniqueDeviceName**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) method to obtain this information.</span></span>

<span data-ttu-id="97f2a-159">Когда узлу устройства требуется указатель на объект службы, реализующий определенную службу, он вызывает метод [**иупнпдевицеконтрол:: жетсервицеобжект**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) для объекта управления устройством.</span><span class="sxs-lookup"><span data-stu-id="97f2a-159">When the device host requires a pointer to a service object that implements a particular service, it invokes the [**IUPnPDeviceControl::GetServiceObject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) method on the device control object.</span></span> <span data-ttu-id="97f2a-160">Узел устройства передает УДН и идентификатор службы, для которой он запрашивает объект службы, и адрес указателя [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , в котором метод должен вернуть указатель на объект службы.</span><span class="sxs-lookup"><span data-stu-id="97f2a-160">The device host passes the UDN and the service ID of the service for which it is requesting a service object and the address of an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer at which the method is expected to return a pointer to the service object.</span></span> <span data-ttu-id="97f2a-161">Параметр УДН необходим, так как управляющий объект устройства управляет службами для всего дерева устройств, включая вложенные устройства.</span><span class="sxs-lookup"><span data-stu-id="97f2a-161">The UDN parameter is necessary because the device control object manages services for the entire device tree, including nested devices.</span></span> <span data-ttu-id="97f2a-162">Если узел устройства запрашивает вложенное устройство, **жетсервицеобжект** использует УДН для его обнаружения.</span><span class="sxs-lookup"><span data-stu-id="97f2a-162">If the device host requests a nested device, **GetServiceObject** uses the UDN to identify it.</span></span>

 

 