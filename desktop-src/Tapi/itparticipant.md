---
description: Интерфейс ИтпартиЦипант реализуется с помощью MSP-Ипконф. Он позволяет приложению получать сведения о участниках Конференции и получать указатели на потоки, связанные с этими участниками.
ms.assetid: 8c3edfc1-3165-48b7-9d83-8892c192498b
title: Интерфейс ИтпартиЦипант (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8b7aa9d845d8d2489be0850bcc3fcf3f93ccdac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679599"
---
# <a name="itparticipant-interface"></a><span data-ttu-id="0cbb0-104">Интерфейс ИтпартиЦипант</span><span class="sxs-lookup"><span data-stu-id="0cbb0-104">ITParticipant interface</span></span>

<span data-ttu-id="0cbb0-105">\[**ИтпартиЦипант** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0cbb0-105">\[**ITParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0cbb0-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="0cbb0-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0cbb0-107">Интерфейс **итпартиЦипант** реализуется с помощью [MSP-ипконф](ipconf-msp.md).</span><span class="sxs-lookup"><span data-stu-id="0cbb0-107">The **ITParticipant** interface is implemented by the [IPConf MSP](ipconf-msp.md).</span></span> <span data-ttu-id="0cbb0-108">Он позволяет приложению получать сведения о участниках Конференции и получать указатели на потоки, связанные с этими участниками.</span><span class="sxs-lookup"><span data-stu-id="0cbb0-108">It allows an application to retrieve information on conference participants, and get pointers to the streams associated with those participants.</span></span>

<span data-ttu-id="0cbb0-109">Этот интерфейс предоставляется на объекте Call, когда вызов использует конференции IP.</span><span class="sxs-lookup"><span data-stu-id="0cbb0-109">This interface is exposed on the call object when a call uses the IP Conferencing.</span></span> <span data-ttu-id="0cbb0-110">Указатель может быть получен путем вызова **QueryInterface** с помощью указателя [**иткаллинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="0cbb0-110">A pointer can be obtained by calling **QueryInterface** using an [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) pointer.</span></span>

## <a name="members"></a><span data-ttu-id="0cbb0-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="0cbb0-111">Members</span></span>

<span data-ttu-id="0cbb0-112">Интерфейс **итпартиЦипант** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0cbb0-112">The **ITParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0cbb0-113">**ИтпартиЦипант** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0cbb0-113">**ITParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="0cbb0-114">Методы</span><span class="sxs-lookup"><span data-stu-id="0cbb0-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0cbb0-115">Методы</span><span class="sxs-lookup"><span data-stu-id="0cbb0-115">Methods</span></span>

<span data-ttu-id="0cbb0-116">Интерфейс **итпартиЦипант** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="0cbb0-116">The **ITParticipant** interface has these methods.</span></span>



| <span data-ttu-id="0cbb0-117">Метод</span><span class="sxs-lookup"><span data-stu-id="0cbb0-117">Method</span></span>                                                                      | <span data-ttu-id="0cbb0-118">Описание</span><span class="sxs-lookup"><span data-stu-id="0cbb0-118">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0cbb0-119">**енумератестреамс**</span><span class="sxs-lookup"><span data-stu-id="0cbb0-119">**EnumerateStreams**</span></span>](itparticipant-enumeratestreams.md)                  | <span data-ttu-id="0cbb0-120">Перечисляет потоки, связанные с текущим участником.</span><span class="sxs-lookup"><span data-stu-id="0cbb0-120">Enumerates streams associated with the current participant.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="0cbb0-121">**получить \_ медиатипес**</span><span class="sxs-lookup"><span data-stu-id="0cbb0-121">**get\_MediaTypes**</span></span>](itparticipant-get-mediatypes.md)                     | <span data-ttu-id="0cbb0-122">Возвращает [**типы носителей**](tapimediatype--constants.md) , связанные с участником.</span><span class="sxs-lookup"><span data-stu-id="0cbb0-122">Gets the [**media types**](tapimediatype--constants.md) associated with a participant.</span></span><br/>                                                                      |
| [<span data-ttu-id="0cbb0-123">**получить \_ партиЦипанттипединфо**</span><span class="sxs-lookup"><span data-stu-id="0cbb0-123">**get\_ParticipantTypedInfo**</span></span>](itparticipant-get-participanttypedinfo.md) | <span data-ttu-id="0cbb0-124">Возвращает представление BSTR требуемого типа информации, например Пти \_ EMAILADDRESS.</span><span class="sxs-lookup"><span data-stu-id="0cbb0-124">Gets a BSTR representation of the needed type of information, such as PTI\_EMAILADDRESS.</span></span><br/>                                                                     |
| [<span data-ttu-id="0cbb0-125">**получение \_ состояния**</span><span class="sxs-lookup"><span data-stu-id="0cbb0-125">**get\_Status**</span></span>](itparticipant-get-status.md)                             | <span data-ttu-id="0cbb0-126">Возвращает состояние участника.</span><span class="sxs-lookup"><span data-stu-id="0cbb0-126">Gets the status of the participant.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="0cbb0-127">**получение \_ потоков**</span><span class="sxs-lookup"><span data-stu-id="0cbb0-127">**get\_Streams**</span></span>](itparticipant-get-streams.md)                           | <span data-ttu-id="0cbb0-128">Создает коллекцию потоков, связанных с текущим участником.</span><span class="sxs-lookup"><span data-stu-id="0cbb0-128">Creates a collection of streams associated with the current participant.</span></span> <span data-ttu-id="0cbb0-129">Предоставляется для клиентских приложений автоматизации, например, написанных на Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0cbb0-129">Provided for Automation client applications, such as those written in Visual Basic.</span></span><br/> |
| [<span data-ttu-id="0cbb0-130">**\_состояние размещения**</span><span class="sxs-lookup"><span data-stu-id="0cbb0-130">**put\_Status**</span></span>](itparticipant-put-status.md)                             | <span data-ttu-id="0cbb0-131">Указывает, включен ли поток, связанный с участником.</span><span class="sxs-lookup"><span data-stu-id="0cbb0-131">Sets whether a stream associated with the participant is enabled.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="0cbb0-132">Требования</span><span class="sxs-lookup"><span data-stu-id="0cbb0-132">Requirements</span></span>



| <span data-ttu-id="0cbb0-133">Требование</span><span class="sxs-lookup"><span data-stu-id="0cbb0-133">Requirement</span></span> | <span data-ttu-id="0cbb0-134">Значение</span><span class="sxs-lookup"><span data-stu-id="0cbb0-134">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0cbb0-135">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="0cbb0-135">TAPI version</span></span><br/> | <span data-ttu-id="0cbb0-136">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="0cbb0-136">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="0cbb0-137">Header</span><span class="sxs-lookup"><span data-stu-id="0cbb0-137">Header</span></span><br/>       | <dl> <span data-ttu-id="0cbb0-138"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cbb0-138"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0cbb0-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0cbb0-139">Library</span></span><br/>      | <dl> <span data-ttu-id="0cbb0-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cbb0-140"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="0cbb0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0cbb0-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="0cbb0-142"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cbb0-142"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cbb0-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0cbb0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cbb0-144">Ипконф MSP</span><span class="sxs-lookup"><span data-stu-id="0cbb0-144">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="0cbb0-145">Интерфейсы MSP Ипконф</span><span class="sxs-lookup"><span data-stu-id="0cbb0-145">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> <dt>

[<span data-ttu-id="0cbb0-146">**иткаллинфо**</span><span class="sxs-lookup"><span data-stu-id="0cbb0-146">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> </dl>

 

