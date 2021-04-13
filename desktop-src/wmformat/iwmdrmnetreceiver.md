---
title: Интерфейс Ивмдрмнетрецеивер
description: Интерфейс Ивмдрмнетрецеивер предоставляет методы, необходимые для использования Microsoft Windows Media DRM для сетевых устройств в качестве получателя. Чтобы получить экземпляр этого интерфейса, вызовите Ивмдрмпровидер CreateObject. Передайте IID \_ ивмдрмнетрецеивер в качестве параметра riid.
ms.assetid: 29966260-c0aa-4e7e-b827-a872c7429333
keywords:
- Формат Windows Media в интерфейсе Ивмдрмнетрецеивер
- Ивмдрмнетрецеивер интерфейса Windows Media Format, описание
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a85ae1525a81e97984e29a5dd28763d934dba2b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411981"
---
# <a name="iwmdrmnetreceiver-interface"></a><span data-ttu-id="e66c2-106">Интерфейс Ивмдрмнетрецеивер</span><span class="sxs-lookup"><span data-stu-id="e66c2-106">IWMDRMNetReceiver interface</span></span>

<span data-ttu-id="e66c2-107">Интерфейс **ивмдрмнетрецеивер** предоставляет методы, необходимые для использования Microsoft Windows Media DRM для сетевых устройств в качестве получателя.</span><span class="sxs-lookup"><span data-stu-id="e66c2-107">The **IWMDRMNetReceiver** interface provides methods needed to use Microsoft Windows Media DRM for Network Devices as a receiver.</span></span>

<span data-ttu-id="e66c2-108">Чтобы получить экземпляр этого интерфейса, вызовите метод [**ивмдрмпровидер:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="e66c2-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="e66c2-109">Передайте **IID \_ ивмдрмнетрецеивер** в качестве параметра *riid* .</span><span class="sxs-lookup"><span data-stu-id="e66c2-109">Pass **IID\_IWMDRMNetReceiver** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="e66c2-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="e66c2-110">Members</span></span>

<span data-ttu-id="e66c2-111">Интерфейс **ивмдрмнетрецеивер** наследует от [**ивмдрмевентженератор**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="e66c2-111">The **IWMDRMNetReceiver** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="e66c2-112">**Ивмдрмнетрецеивер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e66c2-112">**IWMDRMNetReceiver** also has these types of members:</span></span>

-   [<span data-ttu-id="e66c2-113">Методы</span><span class="sxs-lookup"><span data-stu-id="e66c2-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e66c2-114">Методы</span><span class="sxs-lookup"><span data-stu-id="e66c2-114">Methods</span></span>

<span data-ttu-id="e66c2-115">Интерфейс **ивмдрмнетрецеивер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e66c2-115">The **IWMDRMNetReceiver** interface has these methods.</span></span>



| <span data-ttu-id="e66c2-116">Метод</span><span class="sxs-lookup"><span data-stu-id="e66c2-116">Method</span></span>                                                                               | <span data-ttu-id="e66c2-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e66c2-117">Description</span></span>                                                                                                                     |
|:-------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e66c2-118">**жетлиценсечалленже**</span><span class="sxs-lookup"><span data-stu-id="e66c2-118">**GetLicenseChallenge**</span></span>](iwmdrmnetreceiver-getlicensechallenge.md)                 | <span data-ttu-id="e66c2-119">Создает запрос лицензии, который отправляется передатчику при запросе защищенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="e66c2-119">Generates a license challenge that is sent to the transmitter when requesting protected content.</span></span><br/>                     |
| [<span data-ttu-id="e66c2-120">**жетрегистратиончалленже**</span><span class="sxs-lookup"><span data-stu-id="e66c2-120">**GetRegistrationChallenge**</span></span>](iwmdrmnetreceiver-getregistrationchallenge.md)       | <span data-ttu-id="e66c2-121">Создает запрос регистрации, который отправляется передатчику при регистрации или повторной проверке получателя.</span><span class="sxs-lookup"><span data-stu-id="e66c2-121">Generates a registration challenge that is sent to the transmitter when the receiver is registering or revalidating.</span></span><br/> |
| [<span data-ttu-id="e66c2-122">**процесслиценсереспонсе**</span><span class="sxs-lookup"><span data-stu-id="e66c2-122">**ProcessLicenseResponse**</span></span>](iwmdrmnetreceiver-processlicenseresponse.md)           | <span data-ttu-id="e66c2-123">Обрабатывает ответ лицензии, отправленный передатчиком, в ответ на запрос лицензии.</span><span class="sxs-lookup"><span data-stu-id="e66c2-123">Processes the license response sent by the transmitter in reply to a license challenge.</span></span><br/>                              |
| [<span data-ttu-id="e66c2-124">**процессрегистратионреспонсе**</span><span class="sxs-lookup"><span data-stu-id="e66c2-124">**ProcessRegistrationResponse**</span></span>](iwmdrmnetreceiver-processregistrationresponse.md) | <span data-ttu-id="e66c2-125">Обрабатывает ответ регистрации, отправленный передатчиком, в ответ на запрос регистрации.</span><span class="sxs-lookup"><span data-stu-id="e66c2-125">Processes the registration response sent by the transmitter in reply to a registration challenge.</span></span><br/>                    |



 

## <a name="see-also"></a><span data-ttu-id="e66c2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e66c2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e66c2-127">**Интерфейсы**</span><span class="sxs-lookup"><span data-stu-id="e66c2-127">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e66c2-128">**ивмдрмевентженератор**</span><span class="sxs-lookup"><span data-stu-id="e66c2-128">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> <dt>

[<span data-ttu-id="e66c2-129">**Интерфейс Ивмдрмнеттрансмиттер**</span><span class="sxs-lookup"><span data-stu-id="e66c2-129">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





