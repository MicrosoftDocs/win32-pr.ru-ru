---
description: Интерфейс IH323LineEx реализуется с помощью интерфейса H323 MSP и доступен только для объектов Address в H. 323. Этот интерфейс предоставляет методы, обеспечивающие создание и обработку терминалов, которые могут взаимодействовать между клиентами H323 и SDP.
ms.assetid: 2ab57343-8cf5-4af2-91f7-46926cfce6dd
title: Интерфейс IH323LineEx (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41888b16f645a3af1eefd9df61623cb28684bfdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675839"
---
# <a name="ih323lineex-interface"></a><span data-ttu-id="30f0b-104">Интерфейс IH323LineEx</span><span class="sxs-lookup"><span data-stu-id="30f0b-104">IH323LineEx interface</span></span>

<span data-ttu-id="30f0b-105">\[**IH323LineEx** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="30f0b-105">\[**IH323LineEx** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="30f0b-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="30f0b-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="30f0b-107">Интерфейс **IH323LineEx** реализуется с помощью интерфейса [H323 MSP](h323-msp.md) и доступен только для объектов Address в H. 323.</span><span class="sxs-lookup"><span data-stu-id="30f0b-107">The **IH323LineEx** interface is implemented by the [H323 MSP](h323-msp.md) and is available only on H.323 address objects.</span></span> <span data-ttu-id="30f0b-108">Этот интерфейс предоставляет методы, обеспечивающие создание и обработку терминалов, которые могут взаимодействовать между клиентами H323 и SDP.</span><span class="sxs-lookup"><span data-stu-id="30f0b-108">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span>

> [!Note]  
> <span data-ttu-id="30f0b-109">Все методы в этом интерфейсе должны вызываться только после регистрации для входящих вызовов по этому адресу.</span><span class="sxs-lookup"><span data-stu-id="30f0b-109">All methods in this interface should be called only after registering for incoming calls on this address.</span></span>

 

## <a name="members"></a><span data-ttu-id="30f0b-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="30f0b-110">Members</span></span>

<span data-ttu-id="30f0b-111">Интерфейс **IH323LineEx** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="30f0b-111">The **IH323LineEx** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="30f0b-112">**IH323LineEx** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="30f0b-112">**IH323LineEx** also has these types of members:</span></span>

-   [<span data-ttu-id="30f0b-113">Методы</span><span class="sxs-lookup"><span data-stu-id="30f0b-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="30f0b-114">Методы</span><span class="sxs-lookup"><span data-stu-id="30f0b-114">Methods</span></span>

<span data-ttu-id="30f0b-115">Интерфейс **IH323LineEx** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="30f0b-115">The **IH323LineEx** interface has these methods.</span></span>



| <span data-ttu-id="30f0b-116">Метод</span><span class="sxs-lookup"><span data-stu-id="30f0b-116">Method</span></span>                                                                                 | <span data-ttu-id="30f0b-117">Описание</span><span class="sxs-lookup"><span data-stu-id="30f0b-117">Description</span></span>                                                              |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="30f0b-118">**сеталиас**</span><span class="sxs-lookup"><span data-stu-id="30f0b-118">**SetAlias**</span></span>](ih323lineex-setalias.md)                                               | <span data-ttu-id="30f0b-119">Настраивает псевдоним H. 323 по умолчанию для адреса.</span><span class="sxs-lookup"><span data-stu-id="30f0b-119">Configures a default H.323 alias for the address.</span></span><br/>             |
| [<span data-ttu-id="30f0b-120">**сетдефаулткапабилитипреферренце**</span><span class="sxs-lookup"><span data-stu-id="30f0b-120">**SetDefaultCapabilityPreferrence**</span></span>](ih323lineex-setdefaultcapabilitypreferrence.md) | <span data-ttu-id="30f0b-121">Настройка веса предпочтений для возможностей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="30f0b-121">Configures the preference weighting for default capabilities.</span></span><br/> |
| [<span data-ttu-id="30f0b-122">**SetExternalT120Address**</span><span class="sxs-lookup"><span data-stu-id="30f0b-122">**SetExternalT120Address**</span></span>](ih323lineex-setexternalt120address.md)                   | <span data-ttu-id="30f0b-123">Настраивает внешний адрес T. 120 для обмена данными.</span><span class="sxs-lookup"><span data-stu-id="30f0b-123">Configures an external T.120 address for data exchange.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="30f0b-124">Требования</span><span class="sxs-lookup"><span data-stu-id="30f0b-124">Requirements</span></span>



| <span data-ttu-id="30f0b-125">Требование</span><span class="sxs-lookup"><span data-stu-id="30f0b-125">Requirement</span></span> | <span data-ttu-id="30f0b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="30f0b-126">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30f0b-127">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="30f0b-127">TAPI version</span></span><br/> | <span data-ttu-id="30f0b-128">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="30f0b-128">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="30f0b-129">Header</span><span class="sxs-lookup"><span data-stu-id="30f0b-129">Header</span></span><br/>       | <dl> <span data-ttu-id="30f0b-130"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="30f0b-130"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="30f0b-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="30f0b-131">Library</span></span><br/>      | <dl> <span data-ttu-id="30f0b-132"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30f0b-132"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="30f0b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="30f0b-133">DLL</span></span><br/>          | <dl> <span data-ttu-id="30f0b-134"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30f0b-134"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="30f0b-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30f0b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f0b-136">H323 MSP</span><span class="sxs-lookup"><span data-stu-id="30f0b-136">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

