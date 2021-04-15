---
description: Интерфейс ИтпартиЦипантконтрол реализуется с помощью MSP-Ипконф.
ms.assetid: e617f2a4-6be8-4cb1-9f03-470c5100b834
title: Интерфейс ИтпартиЦипантконтрол (Конфприв. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96075748f0c35cbc5af3c6cd07277d15222e0658
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688913"
---
# <a name="itparticipantcontrol-interface"></a><span data-ttu-id="064c1-103">Интерфейс ИтпартиЦипантконтрол</span><span class="sxs-lookup"><span data-stu-id="064c1-103">ITParticipantControl interface</span></span>

<span data-ttu-id="064c1-104">\[**ИтпартиЦипантконтрол** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="064c1-104">\[**ITParticipantControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="064c1-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="064c1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="064c1-106">Интерфейс **итпартиЦипантконтрол** реализуется с помощью MSP-ипконф.</span><span class="sxs-lookup"><span data-stu-id="064c1-106">The **ITParticipantControl** interface is implemented by the IPConf MSP.</span></span> <span data-ttu-id="064c1-107">Этот интерфейс предоставляется для объекта вызова.</span><span class="sxs-lookup"><span data-stu-id="064c1-107">This interface is exposed on the call object.</span></span> <span data-ttu-id="064c1-108">Этот интерфейс позволяет приложению извлекать указатели на участников Конференции.</span><span class="sxs-lookup"><span data-stu-id="064c1-108">This interface allows an application to retrieve pointers to the participants in a conference.</span></span> <span data-ttu-id="064c1-109">Интерфейс **итпартиЦипантконтрол** создается путем вызова **QueryInterface** в [**иткаллинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span><span class="sxs-lookup"><span data-stu-id="064c1-109">The **ITParticipantControl** interface is created by calling **QueryInterface** on [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span></span>

## <a name="members"></a><span data-ttu-id="064c1-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="064c1-110">Members</span></span>

<span data-ttu-id="064c1-111">Интерфейс **итпартиЦипантконтрол** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="064c1-111">The **ITParticipantControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="064c1-112">**ИтпартиЦипантконтрол** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="064c1-112">**ITParticipantControl** also has these types of members:</span></span>

-   [<span data-ttu-id="064c1-113">Методы</span><span class="sxs-lookup"><span data-stu-id="064c1-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="064c1-114">Методы</span><span class="sxs-lookup"><span data-stu-id="064c1-114">Methods</span></span>

<span data-ttu-id="064c1-115">Интерфейс **итпартиЦипантконтрол** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="064c1-115">The **ITParticipantControl** interface has these methods.</span></span>



| <span data-ttu-id="064c1-116">Метод</span><span class="sxs-lookup"><span data-stu-id="064c1-116">Method</span></span>                                                                      | <span data-ttu-id="064c1-117">Описание</span><span class="sxs-lookup"><span data-stu-id="064c1-117">Description</span></span>                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="064c1-118">**енумератепартиЦипантс**</span><span class="sxs-lookup"><span data-stu-id="064c1-118">**EnumerateParticipants**</span></span>](itparticipantcontrol-enumerateparticipants.md) | <span data-ttu-id="064c1-119">Перечисляет участников, которые в настоящее время участвуют в Конференции.</span><span class="sxs-lookup"><span data-stu-id="064c1-119">Enumerates participants currently involved in the conference.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="064c1-120">**получение \_ участников**</span><span class="sxs-lookup"><span data-stu-id="064c1-120">**get\_Participants**</span></span>](itparticipantcontrol-get-participants.md)          | <span data-ttu-id="064c1-121">Создает коллекцию участников, связанных с текущей Конференцией.</span><span class="sxs-lookup"><span data-stu-id="064c1-121">Creates a collection of participants associated with the current conference.</span></span> <span data-ttu-id="064c1-122">Предоставляется для клиентских приложений автоматизации, например, написанных на Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="064c1-122">Provided for Automation client applications, such as those written in Visual Basic.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="064c1-123">Требования</span><span class="sxs-lookup"><span data-stu-id="064c1-123">Requirements</span></span>



| <span data-ttu-id="064c1-124">Требование</span><span class="sxs-lookup"><span data-stu-id="064c1-124">Requirement</span></span> | <span data-ttu-id="064c1-125">Значение</span><span class="sxs-lookup"><span data-stu-id="064c1-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="064c1-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="064c1-126">TAPI version</span></span><br/> | <span data-ttu-id="064c1-127">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="064c1-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="064c1-128">Header</span><span class="sxs-lookup"><span data-stu-id="064c1-128">Header</span></span><br/>       | <dl> <span data-ttu-id="064c1-129"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="064c1-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="064c1-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="064c1-130">Library</span></span><br/>      | <dl> <span data-ttu-id="064c1-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="064c1-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="064c1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="064c1-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="064c1-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="064c1-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

