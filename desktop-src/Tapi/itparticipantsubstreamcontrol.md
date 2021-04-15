---
description: Интерфейс ИтпартиЦипантсубстреамконтрол реализуется с помощью MSP-Ипконф.
ms.assetid: d5af0fb1-af18-4efb-9b68-1fa60c1272f6
title: Интерфейс ИтпартиЦипантсубстреамконтрол (Конфприв. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 799b1a85c6619e1175e620f2c5c5ef851005ba50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689494"
---
# <a name="itparticipantsubstreamcontrol-interface"></a><span data-ttu-id="337aa-103">Интерфейс ИтпартиЦипантсубстреамконтрол</span><span class="sxs-lookup"><span data-stu-id="337aa-103">ITParticipantSubStreamControl interface</span></span>

<span data-ttu-id="337aa-104">\[**ИтпартиЦипантсубстреамконтрол** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="337aa-104">\[**ITParticipantSubStreamControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="337aa-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="337aa-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="337aa-106">Интерфейс **итпартиЦипантсубстреамконтрол** реализуется с помощью MSP-ипконф.</span><span class="sxs-lookup"><span data-stu-id="337aa-106">The **ITParticipantSubStreamControl** interface is implemented by the IPConf MSP.</span></span> <span data-ttu-id="337aa-107">Этот интерфейс предоставляется для объекта вызова.</span><span class="sxs-lookup"><span data-stu-id="337aa-107">This interface is exposed on the call object.</span></span> <span data-ttu-id="337aa-108">Этот интерфейс предоставляет методы, позволяющие приложению обнаруживать или контролировать сопоставление подпотока с участником.</span><span class="sxs-lookup"><span data-stu-id="337aa-108">This interface provides methods that allow an application to either discover or control the matching of substream to participant.</span></span> <span data-ttu-id="337aa-109">Интерфейс **итпартиЦипантсубстреамконтрол** создается путем вызова **QueryInterface** в [**иткаллинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span><span class="sxs-lookup"><span data-stu-id="337aa-109">The **ITParticipantSubStreamControl** interface is created by calling **QueryInterface** on [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span></span>

## <a name="members"></a><span data-ttu-id="337aa-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="337aa-110">Members</span></span>

<span data-ttu-id="337aa-111">Интерфейс **итпартиЦипантсубстреамконтрол** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="337aa-111">The **ITParticipantSubStreamControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="337aa-112">**ИтпартиЦипантсубстреамконтрол** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="337aa-112">**ITParticipantSubStreamControl** also has these types of members:</span></span>

-   [<span data-ttu-id="337aa-113">Методы</span><span class="sxs-lookup"><span data-stu-id="337aa-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="337aa-114">Методы</span><span class="sxs-lookup"><span data-stu-id="337aa-114">Methods</span></span>

<span data-ttu-id="337aa-115">Интерфейс **итпартиЦипантсубстреамконтрол** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="337aa-115">The **ITParticipantSubStreamControl** interface has these methods.</span></span>



| <span data-ttu-id="337aa-116">Метод</span><span class="sxs-lookup"><span data-stu-id="337aa-116">Method</span></span>                                                                                              | <span data-ttu-id="337aa-117">Описание</span><span class="sxs-lookup"><span data-stu-id="337aa-117">Description</span></span>                                                     |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="337aa-118">**получить \_ партиЦипантфромсубстреам**</span><span class="sxs-lookup"><span data-stu-id="337aa-118">**get\_ParticipantFromSubStream**</span></span>](itparticipantsubstreamcontrol-get-participantfromsubstream.md) | <span data-ttu-id="337aa-119">Возвращает участников, связанных с данным подпотоком.</span><span class="sxs-lookup"><span data-stu-id="337aa-119">Gets participants associated with a given substream.</span></span><br/> |
| [<span data-ttu-id="337aa-120">**получить \_ субстреамфромпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="337aa-120">**get\_SubStreamFromParticipant**</span></span>](itparticipantsubstreamcontrol-get-substreamfromparticipant.md) | <span data-ttu-id="337aa-121">Возвращает подпотоки, связанные с данным участником.</span><span class="sxs-lookup"><span data-stu-id="337aa-121">Gets substreams associated with a given participant.</span></span><br/> |
| [<span data-ttu-id="337aa-122">**свитчтерминалтосубстреам**</span><span class="sxs-lookup"><span data-stu-id="337aa-122">**SwitchTerminalToSubStream**</span></span>](itparticipantsubstreamcontrol-switchterminaltosubstream.md)        | <span data-ttu-id="337aa-123">Задает участника в подпотоке.</span><span class="sxs-lookup"><span data-stu-id="337aa-123">Sets a participant on a substream.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="337aa-124">Требования</span><span class="sxs-lookup"><span data-stu-id="337aa-124">Requirements</span></span>



| <span data-ttu-id="337aa-125">Требование</span><span class="sxs-lookup"><span data-stu-id="337aa-125">Requirement</span></span> | <span data-ttu-id="337aa-126">Значение</span><span class="sxs-lookup"><span data-stu-id="337aa-126">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="337aa-127">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="337aa-127">TAPI version</span></span><br/> | <span data-ttu-id="337aa-128">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="337aa-128">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="337aa-129">Header</span><span class="sxs-lookup"><span data-stu-id="337aa-129">Header</span></span><br/>       | <dl> <span data-ttu-id="337aa-130"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="337aa-130"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="337aa-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="337aa-131">Library</span></span><br/>      | <dl> <span data-ttu-id="337aa-132"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="337aa-132"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="337aa-133">DLL</span><span class="sxs-lookup"><span data-stu-id="337aa-133">DLL</span></span><br/>          | <dl> <span data-ttu-id="337aa-134"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="337aa-134"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="337aa-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="337aa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="337aa-136">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="337aa-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="337aa-137">**итсубстреам**</span><span class="sxs-lookup"><span data-stu-id="337aa-137">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

