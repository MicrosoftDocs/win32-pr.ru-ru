---
title: Интерфейс Ивмдрмнеттрансмиттер
description: Интерфейс Ивмдрмнеттрансмиттер предоставляет методы, необходимые для использования Windows Media DRM для сетевых устройств в качестве передатчика. Чтобы получить экземпляр этого интерфейса, вызовите Ивмдрмпровидер CreateObject. Передайте IID \_ ивмдрмнеттрансмиттер в качестве параметра riid.
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- Формат Windows Media в интерфейсе Ивмдрмнеттрансмиттер
- Ивмдрмнеттрансмиттер интерфейса Windows Media Format, описание
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a56db31bb7c03aa70aa136dcd07a8f41f1d9b84d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338300"
---
# <a name="iwmdrmnettransmitter-interface"></a><span data-ttu-id="d5c6b-106">Интерфейс Ивмдрмнеттрансмиттер</span><span class="sxs-lookup"><span data-stu-id="d5c6b-106">IWMDRMNetTransmitter interface</span></span>

<span data-ttu-id="d5c6b-107">Интерфейс **ивмдрмнеттрансмиттер** предоставляет методы, необходимые для использования Windows Media DRM для сетевых устройств в качестве передатчика.</span><span class="sxs-lookup"><span data-stu-id="d5c6b-107">The **IWMDRMNetTransmitter** interface provides methods needed to use Windows Media DRM for Network Devices as a transmitter.</span></span>

<span data-ttu-id="d5c6b-108">Чтобы получить экземпляр этого интерфейса, вызовите метод [**ивмдрмпровидер:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="d5c6b-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="d5c6b-109">Передайте **IID \_ ивмдрмнеттрансмиттер** в качестве параметра *riid* .</span><span class="sxs-lookup"><span data-stu-id="d5c6b-109">Pass **IID\_IWMDRMNetTransmitter** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="d5c6b-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="d5c6b-110">Members</span></span>

<span data-ttu-id="d5c6b-111">Интерфейс **ивмдрмнеттрансмиттер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d5c6b-111">The **IWMDRMNetTransmitter** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d5c6b-112">**Ивмдрмнеттрансмиттер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d5c6b-112">**IWMDRMNetTransmitter** also has these types of members:</span></span>

-   [<span data-ttu-id="d5c6b-113">Методы</span><span class="sxs-lookup"><span data-stu-id="d5c6b-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d5c6b-114">Методы</span><span class="sxs-lookup"><span data-stu-id="d5c6b-114">Methods</span></span>

<span data-ttu-id="d5c6b-115">Интерфейс **ивмдрмнеттрансмиттер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d5c6b-115">The **IWMDRMNetTransmitter** interface has these methods.</span></span>



| <span data-ttu-id="d5c6b-116">Метод</span><span class="sxs-lookup"><span data-stu-id="d5c6b-116">Method</span></span>                                                                        | <span data-ttu-id="d5c6b-117">Описание</span><span class="sxs-lookup"><span data-stu-id="d5c6b-117">Description</span></span>                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5c6b-118">**жетлеафлиценсереспонсе**</span><span class="sxs-lookup"><span data-stu-id="d5c6b-118">**GetLeafLicenseResponse**</span></span>](iwmdrmnettransmitter-getleaflicenseresponse.md) | <span data-ttu-id="d5c6b-119">Создает сообщение с ответом на конечную лицензию.</span><span class="sxs-lookup"><span data-stu-id="d5c6b-119">Generates a leaf license response message.</span></span><br/>                                                       |
| [<span data-ttu-id="d5c6b-120">**жетрутлиценсереспонсе**</span><span class="sxs-lookup"><span data-stu-id="d5c6b-120">**GetRootLicenseResponse**</span></span>](iwmdrmnettransmitter-getrootlicenseresponse.md) | <span data-ttu-id="d5c6b-121">Создает сообщение с ответом корневой лицензии</span><span class="sxs-lookup"><span data-stu-id="d5c6b-121">Generates a root license response message</span></span><br/>                                                        |
| [<span data-ttu-id="d5c6b-122">**сетлиценсечалленже**</span><span class="sxs-lookup"><span data-stu-id="d5c6b-122">**SetLicenseChallenge**</span></span>](iwmdrmnettransmitter-setlicensechallenge.md)       | <span data-ttu-id="d5c6b-123">Обрабатывает запрос лицензии, отправленный получателем DRM Microsoft Windows Media для сетевых устройств</span><span class="sxs-lookup"><span data-stu-id="d5c6b-123">Processes a license challenge sent by a Microsoft Windows Media DRM for Network Devices receiver</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d5c6b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5c6b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c6b-125">**Интерфейсы**</span><span class="sxs-lookup"><span data-stu-id="d5c6b-125">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="d5c6b-126">**Интерфейс Ивмдрмнетрецеивер**</span><span class="sxs-lookup"><span data-stu-id="d5c6b-126">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> </dl>

 

