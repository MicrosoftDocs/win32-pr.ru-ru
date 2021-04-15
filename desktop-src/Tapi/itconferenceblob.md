---
description: Управляет текстовым описанием Конференции.
ms.assetid: b9ce61d1-3fc5-4963-8d2f-586a4b6a159d
title: Интерфейс Итконференцеблоб (Сдпблб. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c961b8fb006f1e172f82827216292cb9d12a158f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688858"
---
# <a name="itconferenceblob-interface"></a><span data-ttu-id="49a9f-103">Интерфейс Итконференцеблоб</span><span class="sxs-lookup"><span data-stu-id="49a9f-103">ITConferenceBlob interface</span></span>

<span data-ttu-id="49a9f-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="49a9f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="49a9f-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="49a9f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="49a9f-106">Интерфейс **итконференцеблоб** управляет текстовым описанием Конференции.</span><span class="sxs-lookup"><span data-stu-id="49a9f-106">The **ITConferenceBlob** interface manipulates a textual conference description.</span></span> <span data-ttu-id="49a9f-107">Интерфейс должен быть независимым от формата и синтаксиса описания Конференции.</span><span class="sxs-lookup"><span data-stu-id="49a9f-107">The interface is intended to be independent of the format and syntax of the conference description.</span></span> <span data-ttu-id="49a9f-108">Чтобы управлять конкретными аспектами описания конференции, приложение должно запросить другой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="49a9f-108">To manipulate specific aspects of the conference description, the application must query for another interface.</span></span> <span data-ttu-id="49a9f-109">В настоящее время поддерживаются только описания конференций SDP. приложение должно использовать **QueryInterface** для [**итсдп**](itsdp.md) для доступа к различным полям описания конференции SDP.</span><span class="sxs-lookup"><span data-stu-id="49a9f-109">Currently, only SDP conference descriptions are supported; the application must use **QueryInterface** for [**ITSdp**](itsdp.md) to access the various fields of the SDP conference description.</span></span> <span data-ttu-id="49a9f-110">Интерфейс **итконференцеблоб** создается путем вызова **QueryInterface** в [**итдиректорйобжект**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span><span class="sxs-lookup"><span data-stu-id="49a9f-110">The **ITConferenceBlob** interface is created by calling **QueryInterface** on [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span></span>

## <a name="members"></a><span data-ttu-id="49a9f-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="49a9f-111">Members</span></span>

<span data-ttu-id="49a9f-112">Интерфейс **итконференцеблоб** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="49a9f-112">The **ITConferenceBlob** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="49a9f-113">**Итконференцеблоб** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="49a9f-113">**ITConferenceBlob** also has these types of members:</span></span>

-   [<span data-ttu-id="49a9f-114">Методы</span><span class="sxs-lookup"><span data-stu-id="49a9f-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="49a9f-115">Методы</span><span class="sxs-lookup"><span data-stu-id="49a9f-115">Methods</span></span>

<span data-ttu-id="49a9f-116">Интерфейс **итконференцеблоб** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="49a9f-116">The **ITConferenceBlob** interface has these methods.</span></span>



| <span data-ttu-id="49a9f-117">Метод</span><span class="sxs-lookup"><span data-stu-id="49a9f-117">Method</span></span>                                                             | <span data-ttu-id="49a9f-118">Описание</span><span class="sxs-lookup"><span data-stu-id="49a9f-118">Description</span></span>                                                                                                                                   |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49a9f-119">**получить \_ кодировку**</span><span class="sxs-lookup"><span data-stu-id="49a9f-119">**get\_CharacterSet**</span></span>](itconferenceblob-get-characterset.md)     | <span data-ttu-id="49a9f-120">Возвращает признак [**\_ \_ набора символов большого двоичного**](blob-character-set.md) объекта в кодировке ASCII, Unicode и т. д.</span><span class="sxs-lookup"><span data-stu-id="49a9f-120">Gets the [**BLOB\_CHARACTER\_SET**](blob-character-set.md) indicator of whether blob characters are in ASCII, Unicode, and so on.</span></span><br/> |
| [<span data-ttu-id="49a9f-121">**получить \_ конференцеблоб**</span><span class="sxs-lookup"><span data-stu-id="49a9f-121">**get\_ConferenceBlob**</span></span>](itconferenceblob-get-conferenceblob.md) | <span data-ttu-id="49a9f-122">Получает указатель на большой двоичный объект конференции.</span><span class="sxs-lookup"><span data-stu-id="49a9f-122">Gets a pointer to the conference blob.</span></span><br/>                                                                                             |
| [<span data-ttu-id="49a9f-123">**Ini**</span><span class="sxs-lookup"><span data-stu-id="49a9f-123">**Init**</span></span>](itconferenceblob-init.md)                              | <span data-ttu-id="49a9f-124">Инициализирует Конференц-большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="49a9f-124">Initializes the conference blob.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="49a9f-125">**сетконференцеблоб**</span><span class="sxs-lookup"><span data-stu-id="49a9f-125">**SetConferenceBlob**</span></span>](itconferenceblob-setconferenceblob.md)    | <span data-ttu-id="49a9f-126">Фиксирует изменения в большом двоичном объекте Конференции.</span><span class="sxs-lookup"><span data-stu-id="49a9f-126">Commits changes to the conference blob.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="49a9f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="49a9f-127">Requirements</span></span>



| <span data-ttu-id="49a9f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="49a9f-128">Requirement</span></span> | <span data-ttu-id="49a9f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="49a9f-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49a9f-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="49a9f-130">TAPI version</span></span><br/> | <span data-ttu-id="49a9f-131">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="49a9f-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="49a9f-132">Header</span><span class="sxs-lookup"><span data-stu-id="49a9f-132">Header</span></span><br/>       | <dl> <span data-ttu-id="49a9f-133"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="49a9f-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="49a9f-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="49a9f-134">Library</span></span><br/>      | <dl> <span data-ttu-id="49a9f-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49a9f-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="49a9f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="49a9f-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="49a9f-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49a9f-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

