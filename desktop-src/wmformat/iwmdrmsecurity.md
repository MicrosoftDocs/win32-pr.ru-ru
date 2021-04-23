---
title: Интерфейс Ивмдрмсекурити
description: Интерфейс Ивмдрмсекурити управляет различными сведениями, относящимися к безопасности, для клиентских компьютеров и подсистемы управления цифровыми правами (DRM). Чтобы получить экземпляр этого интерфейса, вызовите Ивмдрмпровидер CreateObject.
ms.assetid: 9439aedc-359d-4b2c-a88c-7b0e8eacb5a0
keywords:
- Формат Windows Media в интерфейсе Ивмдрмсекурити
- Ивмдрмсекурити интерфейса Windows Media Format, описание
topic_type:
- apiref
api_name:
- IWMDRMSecurity
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8b18e56c24fd0f3d3f86f217f547d626b74ded0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334299"
---
# <a name="iwmdrmsecurity-interface"></a><span data-ttu-id="44ace-105">Интерфейс Ивмдрмсекурити</span><span class="sxs-lookup"><span data-stu-id="44ace-105">IWMDRMSecurity interface</span></span>

<span data-ttu-id="44ace-106">Интерфейс **ивмдрмсекурити** управляет различными сведениями, относящимися к безопасности, для клиентских компьютеров и подсистемы управления цифровыми правами (DRM).</span><span class="sxs-lookup"><span data-stu-id="44ace-106">The **IWMDRMSecurity** interface manages a variety of security-related information for the client computer and digital rights management (DRM) subsystem.</span></span>

<span data-ttu-id="44ace-107">Чтобы получить экземпляр этого интерфейса, вызовите метод [**ивмдрмпровидер:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="44ace-107">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="44ace-108">Передайте **IID \_ ивмдрмсекурити** в качестве параметра *riid* .</span><span class="sxs-lookup"><span data-stu-id="44ace-108">Pass **IID\_IWMDRMSecurity** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="44ace-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="44ace-109">Members</span></span>

<span data-ttu-id="44ace-110">Интерфейс **ивмдрмсекурити** наследует от [**ивмдрмевентженератор**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="44ace-110">The **IWMDRMSecurity** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="44ace-111">**Ивмдрмсекурити** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="44ace-111">**IWMDRMSecurity** also has these types of members:</span></span>

-   [<span data-ttu-id="44ace-112">Методы</span><span class="sxs-lookup"><span data-stu-id="44ace-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="44ace-113">Методы</span><span class="sxs-lookup"><span data-stu-id="44ace-113">Methods</span></span>

<span data-ttu-id="44ace-114">Интерфейс **ивмдрмсекурити** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="44ace-114">The **IWMDRMSecurity** interface has these methods.</span></span>



| <span data-ttu-id="44ace-115">Метод</span><span class="sxs-lookup"><span data-stu-id="44ace-115">Method</span></span>                                                                                      | <span data-ttu-id="44ace-116">Описание</span><span class="sxs-lookup"><span data-stu-id="44ace-116">Description</span></span>                                                                                                      |
|:--------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44ace-117">**чеккцертфорревокатион**</span><span class="sxs-lookup"><span data-stu-id="44ace-117">**CheckCertForRevocation**</span></span>](iwmdrmsecurity-checkcertforrevocation.md)                     | <span data-ttu-id="44ace-118">Определяет, был ли отозван сертификат.</span><span class="sxs-lookup"><span data-stu-id="44ace-118">Determines whether a certificate has been revoked.</span></span><br/>                                                    |
| [<span data-ttu-id="44ace-119">**жетконтентенаблерсфорревокатионс**</span><span class="sxs-lookup"><span data-stu-id="44ace-119">**GetContentEnablersForRevocations**</span></span>](iwmdrmsecurity-getcontentenablersforrevocations.md) | <span data-ttu-id="44ace-120">Получает интерфейсы включения содержимого, которые обеспечивают возобновление компонентов на основе отозванных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="44ace-120">Retrieves content enabler interfaces that enable renewal of components based on revoked certificates.</span></span><br/> |
| [<span data-ttu-id="44ace-121">**жетконтентенаблерсфромхашес**</span><span class="sxs-lookup"><span data-stu-id="44ace-121">**GetContentEnablersFromHashes**</span></span>](iwmdrmsecurity-getcontentenablersfromhashes.md)         | <span data-ttu-id="44ace-122">Получает интерфейсы включения содержимого, которые обеспечивают возобновление компонентов на основе хэшированных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="44ace-122">Retrieves content enabler interfaces that enable renewal of components based on hashed certificates.</span></span><br/>  |
| [<span data-ttu-id="44ace-123">**жетмачинецертификате**</span><span class="sxs-lookup"><span data-stu-id="44ace-123">**GetMachineCertificate**</span></span>](iwmdrmsecurity-getmachinecertificate.md)                       | <span data-ttu-id="44ace-124">Получает сертификат компьютера подсистемы DRM на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="44ace-124">Retrieves the machine certificate of the DRM subsystem on the client computer.</span></span><br/>                        |
| [<span data-ttu-id="44ace-125">**жетревокатиондата**</span><span class="sxs-lookup"><span data-stu-id="44ace-125">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)                               | <span data-ttu-id="44ace-126">Извлекает список отзыва сертификатов из локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="44ace-126">Retrieves a certificate revocation list from the local store.</span></span><br/>                                         |
| [<span data-ttu-id="44ace-127">**жетревокатиондатаверсион**</span><span class="sxs-lookup"><span data-stu-id="44ace-127">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)                 | <span data-ttu-id="44ace-128">Возвращает номер версии списка отзыва сертификатов в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="44ace-128">Retrieves the version number of a certificate revocation list in the local store.</span></span><br/>                     |
| [<span data-ttu-id="44ace-129">**жетсекуритиверсион**</span><span class="sxs-lookup"><span data-stu-id="44ace-129">**GetSecurityVersion**</span></span>](iwmdrmsecurity-getsecurityversion.md)                             | <span data-ttu-id="44ace-130">Извлекает версию подсистемы DRM на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="44ace-130">Retrieves the version of the DRM subsystem on the client computer.</span></span><br/>                                    |
| [<span data-ttu-id="44ace-131">**перформсекуритюпдате**</span><span class="sxs-lookup"><span data-stu-id="44ace-131">**PerformSecurityUpdate**</span></span>](iwmdrmsecurity-performsecurityupdate.md)                       | <span data-ttu-id="44ace-132">Инициирует обновление безопасности для подсистемы DRM на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="44ace-132">Initiates a security update to the DRM subsystem on the client computer.</span></span><br/>                              |
| [<span data-ttu-id="44ace-133">**сетревокатиондата**</span><span class="sxs-lookup"><span data-stu-id="44ace-133">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)                               | <span data-ttu-id="44ace-134">Задает список отзыва сертификатов в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="44ace-134">Sets a certificate revocation list in the local store.</span></span><br/>                                                |



 

## <a name="see-also"></a><span data-ttu-id="44ace-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44ace-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44ace-136">**Пример индивидуализации DRM**</span><span class="sxs-lookup"><span data-stu-id="44ace-136">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="44ace-137">**Интерфейсы**</span><span class="sxs-lookup"><span data-stu-id="44ace-137">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="44ace-138">**ивмдрмевентженератор**</span><span class="sxs-lookup"><span data-stu-id="44ace-138">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





