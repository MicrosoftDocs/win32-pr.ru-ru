---
description: Ниже показана функциональность интерфейса Итконнектион.
ms.assetid: 44dc39cf-3222-41ed-b29c-df2d32615500
title: Интерфейс Итконнектион (Сдпблб. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00da80631c0ef4e8186aa36425f18e4d2a62bfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679956"
---
# <a name="itconnection-interface"></a><span data-ttu-id="ef815-103">Интерфейс Итконнектион</span><span class="sxs-lookup"><span data-stu-id="ef815-103">ITConnection interface</span></span>

<span data-ttu-id="ef815-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="ef815-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ef815-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="ef815-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ef815-106">Интерфейс **итконнектион** предоставляет следующие функциональные возможности:</span><span class="sxs-lookup"><span data-stu-id="ef815-106">The **ITConnection** interface provides the following functionality:</span></span>

-   <span data-ttu-id="ef815-107">Предоставляет доступ к сведениям об адресе и сроку жизни (TTL) для сеанса.</span><span class="sxs-lookup"><span data-stu-id="ef815-107">Provides access to the address and time to live (TTL) information for the session.</span></span>
-   <span data-ttu-id="ef815-108">Предоставляет доступ к сведениям о пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="ef815-108">Provides access to the bandwidth information.</span></span>
-   <span data-ttu-id="ef815-109">Позволяет управлять ключом шифрования.</span><span class="sxs-lookup"><span data-stu-id="ef815-109">Enables manipulation of the encryption key.</span></span>

<span data-ttu-id="ef815-110">Интерфейс **итконнектион** создается путем вызова **QueryInterface** в [**итконференцеблоб**](itconferenceblob.md).</span><span class="sxs-lookup"><span data-stu-id="ef815-110">The **ITConnection** interface is created by calling **QueryInterface** on [**ITConferenceBlob**](itconferenceblob.md).</span></span>

## <a name="members"></a><span data-ttu-id="ef815-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="ef815-111">Members</span></span>

<span data-ttu-id="ef815-112">Интерфейс **итконнектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="ef815-112">The **ITConnection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="ef815-113">**Итконнектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ef815-113">**ITConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="ef815-114">Методы</span><span class="sxs-lookup"><span data-stu-id="ef815-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ef815-115">Методы</span><span class="sxs-lookup"><span data-stu-id="ef815-115">Methods</span></span>

<span data-ttu-id="ef815-116">Интерфейс **итконнектион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ef815-116">The **ITConnection** interface has these methods.</span></span>



| <span data-ttu-id="ef815-117">Метод</span><span class="sxs-lookup"><span data-stu-id="ef815-117">Method</span></span>                                                               | <span data-ttu-id="ef815-118">Описание</span><span class="sxs-lookup"><span data-stu-id="ef815-118">Description</span></span>                                                                                                                                    |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef815-119">**получить \_ addressType**</span><span class="sxs-lookup"><span data-stu-id="ef815-119">**get\_AddressType**</span></span>](itconnection-get-addresstype.md)             | <span data-ttu-id="ef815-120">Возвращает тип адреса.</span><span class="sxs-lookup"><span data-stu-id="ef815-120">Gets the address type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="ef815-121">**получить \_ пропускную способность**</span><span class="sxs-lookup"><span data-stu-id="ef815-121">**get\_Bandwidth**</span></span>](itconnection-get-bandwidth.md)                 | <span data-ttu-id="ef815-122">Возвращает значение пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="ef815-122">Gets bandwidth value.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="ef815-123">**получить \_ бандвидсмодифиер**</span><span class="sxs-lookup"><span data-stu-id="ef815-123">**get\_BandwidthModifier**</span></span>](itconnection-get-bandwidthmodifier.md) | <span data-ttu-id="ef815-124">Возвращает модификатор пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="ef815-124">Gets the bandwidth modifier.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="ef815-125">**получить \_ нетворктипе**</span><span class="sxs-lookup"><span data-stu-id="ef815-125">**get\_NetworkType**</span></span>](itconnection-get-networktype.md)             | <span data-ttu-id="ef815-126">Возвращает тип сети.</span><span class="sxs-lookup"><span data-stu-id="ef815-126">Gets the network type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="ef815-127">**получить \_ нумаддрессес**</span><span class="sxs-lookup"><span data-stu-id="ef815-127">**get\_NumAddresses**</span></span>](itconnection-get-numaddresses.md)           | <span data-ttu-id="ef815-128">Возвращает число адресов, используемых для сеанса.</span><span class="sxs-lookup"><span data-stu-id="ef815-128">Gets the number of addresses to be used for the session.</span></span><br/>                                                                            |
| [<span data-ttu-id="ef815-129">**получить \_ стартаддресс**</span><span class="sxs-lookup"><span data-stu-id="ef815-129">**get\_StartAddress**</span></span>](itconnection-get-startaddress.md)           | <span data-ttu-id="ef815-130">Возвращает первый адрес, используемый для сеанса.</span><span class="sxs-lookup"><span data-stu-id="ef815-130">Gets the first address to be used for the session.</span></span><br/>                                                                                  |
| [<span data-ttu-id="ef815-131">**получение \_ TTL**</span><span class="sxs-lookup"><span data-stu-id="ef815-131">**get\_Ttl**</span></span>](itconnection-get-ttl.md)                             | <span data-ttu-id="ef815-132">Возвращает область срока [*жизни*](t-tapgloss.md) (TTL) для передач адресов.</span><span class="sxs-lookup"><span data-stu-id="ef815-132">Gets the [*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span><br/> |
| [<span data-ttu-id="ef815-133">**GetEncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="ef815-133">**GetEncryptionKey**</span></span>](itconnection-getencryptionkey.md)            | <span data-ttu-id="ef815-134">Возвращает ключ шифрования.</span><span class="sxs-lookup"><span data-stu-id="ef815-134">Gets the encryption key.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="ef815-135">**разместить \_ addressType**</span><span class="sxs-lookup"><span data-stu-id="ef815-135">**put\_AddressType**</span></span>](itconnection-put-addresstype.md)             | <span data-ttu-id="ef815-136">Задает тип адреса.</span><span class="sxs-lookup"><span data-stu-id="ef815-136">Sets the address type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="ef815-137">**разместить \_ нетворктипе**</span><span class="sxs-lookup"><span data-stu-id="ef815-137">**put\_NetworkType**</span></span>](itconnection-put-networktype.md)             | <span data-ttu-id="ef815-138">Задает тип сети.</span><span class="sxs-lookup"><span data-stu-id="ef815-138">Sets the network type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="ef815-139">**сетаддрессинфо**</span><span class="sxs-lookup"><span data-stu-id="ef815-139">**SetAddressInfo**</span></span>](itconnection-setaddressinfo.md)                | <span data-ttu-id="ef815-140">Задает сведения об адресе.</span><span class="sxs-lookup"><span data-stu-id="ef815-140">Sets address information.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="ef815-141">**сетбандвидсинфо**</span><span class="sxs-lookup"><span data-stu-id="ef815-141">**SetBandwidthInfo**</span></span>](itconnection-setbandwidthinfo.md)            | <span data-ttu-id="ef815-142">Задает значение пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="ef815-142">Sets the bandwidth value.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="ef815-143">**SetEncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="ef815-143">**SetEncryptionKey**</span></span>](itconnection-setencryptionkey.md)            | <span data-ttu-id="ef815-144">Задает ключ шифрования, необходимый для расшифровки сеанса, или указывает механизм для получения используемого ключа внешними средствами.</span><span class="sxs-lookup"><span data-stu-id="ef815-144">Sets the encryption key needed to decrypt the session or an indication to a mechanism to obtain a usable key by external means.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="ef815-145">Требования</span><span class="sxs-lookup"><span data-stu-id="ef815-145">Requirements</span></span>



| <span data-ttu-id="ef815-146">Требование</span><span class="sxs-lookup"><span data-stu-id="ef815-146">Requirement</span></span> | <span data-ttu-id="ef815-147">Значение</span><span class="sxs-lookup"><span data-stu-id="ef815-147">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef815-148">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="ef815-148">TAPI version</span></span><br/> | <span data-ttu-id="ef815-149">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ef815-149">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ef815-150">Header</span><span class="sxs-lookup"><span data-stu-id="ef815-150">Header</span></span><br/>       | <dl> <span data-ttu-id="ef815-151"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef815-151"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef815-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ef815-152">Library</span></span><br/>      | <dl> <span data-ttu-id="ef815-153"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef815-153"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ef815-154">DLL</span><span class="sxs-lookup"><span data-stu-id="ef815-154">DLL</span></span><br/>          | <dl> <span data-ttu-id="ef815-155"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef815-155"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

