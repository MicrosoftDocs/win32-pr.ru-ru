---
description: Интерфейс Икэйфрамеконтрол реализуется с помощью MSP-интерфейса H. 323 и доступен только для объектов потока H. 323.
ms.assetid: 68cb1df1-f7fa-447a-8ea5-80dc1e802760
title: Интерфейс Икэйфрамеконтрол (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c326c6a492777d7c41ae450a1c502c343aeb8cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688949"
---
# <a name="ikeyframecontrol-interface"></a><span data-ttu-id="0694c-103">Интерфейс Икэйфрамеконтрол</span><span class="sxs-lookup"><span data-stu-id="0694c-103">IKeyFrameControl interface</span></span>

<span data-ttu-id="0694c-104">\[**Икэйфрамеконтрол** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0694c-104">\[**IKeyFrameControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0694c-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="0694c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0694c-106">Интерфейс **икэйфрамеконтрол** реализуется с помощью MSP-интерфейса [h. 323](h323-msp.md) и доступен только для объектов потока h. 323.</span><span class="sxs-lookup"><span data-stu-id="0694c-106">The **IKeyFrameControl** interface is implemented by the [H.323 MSP](h323-msp.md) and is available only on H.323 stream objects.</span></span> <span data-ttu-id="0694c-107">Этот интерфейс предоставляет методы, обеспечивающие создание и обработку терминалов, которые могут взаимодействовать между клиентами H323 и SDP.</span><span class="sxs-lookup"><span data-stu-id="0694c-107">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span> <span data-ttu-id="0694c-108">В нем есть два метода, которые позволяют приложению запрашивать удаленную конечную точку для обновления видеоизображения с помощью опорного кадра.</span><span class="sxs-lookup"><span data-stu-id="0694c-108">It has two methods that allow the application to ask the remote endpoint to update the video image with a keyframe.</span></span>

## <a name="members"></a><span data-ttu-id="0694c-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="0694c-109">Members</span></span>

<span data-ttu-id="0694c-110">Интерфейс **икэйфрамеконтрол** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0694c-110">The **IKeyFrameControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0694c-111">**Икэйфрамеконтрол** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0694c-111">**IKeyFrameControl** also has these types of members:</span></span>

-   [<span data-ttu-id="0694c-112">Методы</span><span class="sxs-lookup"><span data-stu-id="0694c-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0694c-113">Методы</span><span class="sxs-lookup"><span data-stu-id="0694c-113">Methods</span></span>

<span data-ttu-id="0694c-114">Интерфейс **икэйфрамеконтрол** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="0694c-114">The **IKeyFrameControl** interface has these methods.</span></span>



| <span data-ttu-id="0694c-115">Метод</span><span class="sxs-lookup"><span data-stu-id="0694c-115">Method</span></span>                                                                  | <span data-ttu-id="0694c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="0694c-116">Description</span></span>                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0694c-117">**периодикупдатепиктуре**</span><span class="sxs-lookup"><span data-stu-id="0694c-117">**PeriodicUpdatePicture**</span></span>](ikeyframecontrol-periodicupdatepicture.md) | <span data-ttu-id="0694c-118">Настраивает таймер в потоке, который периодически запрашивает обновления изображений.</span><span class="sxs-lookup"><span data-stu-id="0694c-118">Configures a timer in the stream that will ask for picture updates periodically.</span></span><br/> |
| [<span data-ttu-id="0694c-119">**упдатепиктуре**</span><span class="sxs-lookup"><span data-stu-id="0694c-119">**UpdatePicture**</span></span>](ikeyframecontrol-updatepicture.md)                 | <span data-ttu-id="0694c-120">Запрашивает у отправителя видео обновление изображения.</span><span class="sxs-lookup"><span data-stu-id="0694c-120">Asks the video sender to update the picture.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="0694c-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0694c-121">Requirements</span></span>



| <span data-ttu-id="0694c-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0694c-122">Requirement</span></span> | <span data-ttu-id="0694c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0694c-123">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0694c-124">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="0694c-124">TAPI version</span></span><br/> | <span data-ttu-id="0694c-125">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="0694c-125">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0694c-126">Header</span><span class="sxs-lookup"><span data-stu-id="0694c-126">Header</span></span><br/>       | <dl> <span data-ttu-id="0694c-127"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="0694c-127"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="0694c-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0694c-128">Library</span></span><br/>      | <dl> <span data-ttu-id="0694c-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0694c-129"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0694c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0694c-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="0694c-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0694c-131"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0694c-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0694c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0694c-133">H323 MSP</span><span class="sxs-lookup"><span data-stu-id="0694c-133">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

