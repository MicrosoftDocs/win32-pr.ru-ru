---
title: Настройка пользовательского интерфейса метода EAP
description: Описание настройки запрашивающей стороны путем предоставления конфигурации метода EAP для EAPHost.
ms.assetid: f6a23201-e221-4098-863f-71a81735d927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9b82debadc075b1fcc12dad06484c0fd3617874
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "105710223"
---
# <a name="configuring-the-eap-method-user-interface"></a><span data-ttu-id="6dd76-103">Настройка пользовательского интерфейса метода EAP</span><span class="sxs-lookup"><span data-stu-id="6dd76-103">Configuring the EAP Method User Interface</span></span>

<span data-ttu-id="6dd76-104">В этом разделе описывается настройка запрашивающей стороны путем предоставления конфигурации метода EAP для EAPHost.</span><span class="sxs-lookup"><span data-stu-id="6dd76-104">This topic explains how to configure the supplicant by supplying an EAP method configuration to EAPHost.</span></span>

<span data-ttu-id="6dd76-105">Для создания запрашивающей стороне проверки подлинности на основе EAP с помощью EAPHost необходимо предоставить для EAPHost конфигурацию метода EAP с помощью функции [**еафостпирбегинсессион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) .</span><span class="sxs-lookup"><span data-stu-id="6dd76-105">For a supplicant to perform an EAP-based authentication using EAPHost, a supplicant must supply an EAP method configuration to EAPHost through the [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) function.</span></span>

1.  <span data-ttu-id="6dd76-106">Чтобы получить конфигурацию метода EAP, запрашивающий объект обычно запрашивает EAPHost с помощью [**еафостпиржетмесодс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) , чтобы получить полный набор методов EAP, доступных и установленных на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="6dd76-106">To obtain the EAP method configuration, a supplicant typically queries EAPHost using [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) to learn the complete set of EAP methods that are available and installed on the local machine.</span></span> <span data-ttu-id="6dd76-107">Список методов обычно предоставляется пользователю в виде сочетания окна или другого элемента управления пользовательского интерфейса, который позволяет пользователю выбрать нужный метод.</span><span class="sxs-lookup"><span data-stu-id="6dd76-107">The list of methods is typically presented to the user in a combination box or other UI control that allows the user to select the method they want.</span></span>
    > [!Note]  
    > <span data-ttu-id="6dd76-108">С помощью этого параметра можно отфильтровать отображаемый список методов на основе бит свойств метода, указанных **в \_ методе EAP \_ info. еаппропертиес**.</span><span class="sxs-lookup"><span data-stu-id="6dd76-108">The supplicant may choose to filter the displayed list of methods based on the method property bits indicated in **EAP\_METHOD\_INFO.eapProperties**.</span></span> <span data-ttu-id="6dd76-109">Некоторые методы могут быть не подходящими для характеристик безопасности транспорта, предоставляемого вызывающим объектом, например.</span><span class="sxs-lookup"><span data-stu-id="6dd76-109">Some methods may not be appropriate for the security characteristics of the transport provided by the supplicant, for example.</span></span>

     

2.  <span data-ttu-id="6dd76-110">После заполнения элементом управления пользовательского интерфейса набора возможных методов EAP пользователь выбирает метод, который требуется настроить.</span><span class="sxs-lookup"><span data-stu-id="6dd76-110">Once the UI control is populated with the set of possible EAP methods, the user selects the method they want to configure.</span></span> <span data-ttu-id="6dd76-111">Как правило, запрашивающая сторона предоставляет пользователю кнопку **конфигурации** или **свойств** , чтобы получить доступ к свойствам конфигурации выбранного метода EAP.</span><span class="sxs-lookup"><span data-stu-id="6dd76-111">Typically, the supplicant provides a **Configuration** or **Properties** button for the user to access configuration properties of the selected EAP method.</span></span>
    > [!Note]
    > <span data-ttu-id="6dd76-112">В основе этого запрашивающего устройства учитывается, что существуют настраиваемые пользователем свойства, основанные на **еаппропсуппортсконфиг** бит, который включается в **\_ методе EAP ( \_ info. еаппропертиес**).</span><span class="sxs-lookup"><span data-stu-id="6dd76-112">The supplicant is aware that there are user-configurable properties based on the **eapPropSupportsConfig** bit being enabled in **EAP\_METHOD\_INFO.eapProperties**.</span></span>
    >
    > <span data-ttu-id="6dd76-113">Дополнительные сведения см. в разделе [**Свойства метода EAP**](eap-method-properties.md).</span><span class="sxs-lookup"><span data-stu-id="6dd76-113">For more information, see [**EAP Method Properties**](eap-method-properties.md).</span></span>

     

3.  <span data-ttu-id="6dd76-114">Когда пользователь щелкает соответствующий элемент управления пользовательского интерфейса, он вызывает [**еафостпиринвокеконфигуи**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), передавая в функцию значение **HWND** для собственного пользовательского интерфейса вызывающего объекта, структуру [**\_ \_ типа метода EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) , полученную из запроса, в [**структуру \_ \_ сведений о методе EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) и другие необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="6dd76-114">When the user clicks the appropriate UI control, the supplicant calls [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), passing into the function the **HWND** value for the supplicant's own UI, the [**EAP\_METHOD\_TYPE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) structure obtained from the query to [**EAP\_METHOD\_INFO**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) structure and other required parameters.</span></span>
4.  <span data-ttu-id="6dd76-115">Вызов [**еафостпиринвокеконфигуи**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) вызывает собственный пользовательский интерфейс конфигурации метода EAP.</span><span class="sxs-lookup"><span data-stu-id="6dd76-115">Calling [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) invokes an EAP method's own configuration UI.</span></span> <span data-ttu-id="6dd76-116">При возврате из **еафостпиринвокеконфигуи** функция возвращает BLOB-объект конфигурации метода EAP в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="6dd76-116">On return from **EapHostPeerInvokeConfigUI**, the function will return an EAP method configuration BLOB as an out-parameter.</span></span>
5.  <span data-ttu-id="6dd76-117">В качестве объекта-отправительа хранится большой двоичный объект конфигурации, а также структура [**\_ \_ типа метода EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) для использования с [**еафостпирбегинсессион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span><span class="sxs-lookup"><span data-stu-id="6dd76-117">The supplicant stores the configuration BLOB, along with the [**EAP\_METHOD\_TYPE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) structure for use with [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span></span>
6.  <span data-ttu-id="6dd76-118">Точный метод хранения большого двоичного объекта конфигурацию полностью зависит от него.</span><span class="sxs-lookup"><span data-stu-id="6dd76-118">The precise method for storing the configuraiton BLOB is entirely up to the supplicant.</span></span> <span data-ttu-id="6dd76-119">Однако этот объект всегда должен хранить конфигурацию в подходящем и безопасном способе, подходящем для данных конфигурации проверки подлинности системы и пользователя.</span><span class="sxs-lookup"><span data-stu-id="6dd76-119">However, the supplicant should always store the configuration in a suitable, secure manner appropriate for system and user authentication configuration data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6dd76-120">См. также</span><span class="sxs-lookup"><span data-stu-id="6dd76-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dd76-121">Включение групповая политика</span><span class="sxs-lookup"><span data-stu-id="6dd76-121">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="6dd76-122">Реализация поддержки NAP In-Band для методов EAP</span><span class="sxs-lookup"><span data-stu-id="6dd76-122">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="6dd76-123">Реализация поддержки NAP для методов EAP</span><span class="sxs-lookup"><span data-stu-id="6dd76-123">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="6dd76-124">Передача данных между запрашивающим и методами EAP</span><span class="sxs-lookup"><span data-stu-id="6dd76-124">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="6dd76-125">EAPHost отправителей запросов</span><span class="sxs-lookup"><span data-stu-id="6dd76-125">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




