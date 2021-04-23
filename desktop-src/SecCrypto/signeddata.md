---
description: Предоставляет свойства и методы для установки содержимого, подписанного цифровой подписью, для цифрового подписывания или для цифровой подписи, а также для проверки цифровых подписей подписанных данных. Подписанное сообщение находится в \# формате PKCS 7.
ms.assetid: 500437e8-a637-4e89-9ac9-aa3ea20d437f
title: Объект Сигнеддата
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d0424826f7dc5d041b877ced1cd7f50490d7801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685173"
---
# <a name="signeddata-object"></a><span data-ttu-id="9bec2-104">Объект Сигнеддата</span><span class="sxs-lookup"><span data-stu-id="9bec2-104">SignedData object</span></span>

<span data-ttu-id="9bec2-105">\[Объект **сигнеддата** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="9bec2-105">\[The **SignedData** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9bec2-106">Вместо этого используйте [**класс SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="9bec2-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="9bec2-107">Объект **сигнеддата** предоставляет свойства и методы для установки содержимого, подписанного [*цифровой подписью*](../secgloss/d-gly.md), для цифрового подписывания и цифровой подписи данных, а также для проверки цифровой сигнатуры подписанных данных.</span><span class="sxs-lookup"><span data-stu-id="9bec2-107">The **SignedData** object provides properties and methods to establish the content to be signed with a [*digital signature*](../secgloss/d-gly.md), to sign or cosign data digitally, and to verify the digital signature of signed data.</span></span> <span data-ttu-id="9bec2-108">Подписанное сообщение находится в \# формате PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="9bec2-108">The signed message is in PKCS \#7 format.</span></span>

<span data-ttu-id="9bec2-109">Подпись данных, если она проверена, подтверждает связь между подписавшим и данными и показывает, что данные не изменялись каким-либо образом после создания подписи.</span><span class="sxs-lookup"><span data-stu-id="9bec2-109">A data signature, if verified, proves the association between a signer and data and shows that the data was not changed in any way after the signature was created.</span></span>

## <a name="members"></a><span data-ttu-id="9bec2-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="9bec2-110">Members</span></span>

<span data-ttu-id="9bec2-111">Объект **сигнеддата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9bec2-111">The **SignedData** object has these types of members:</span></span>

-   [<span data-ttu-id="9bec2-112">Методы</span><span class="sxs-lookup"><span data-stu-id="9bec2-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="9bec2-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="9bec2-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9bec2-114">Методы</span><span class="sxs-lookup"><span data-stu-id="9bec2-114">Methods</span></span>

<span data-ttu-id="9bec2-115">Объект **сигнеддата** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="9bec2-115">The **SignedData** object has these methods.</span></span>



| <span data-ttu-id="9bec2-116">Метод</span><span class="sxs-lookup"><span data-stu-id="9bec2-116">Method</span></span>                              | <span data-ttu-id="9bec2-117">Описание</span><span class="sxs-lookup"><span data-stu-id="9bec2-117">Description</span></span>                                                         |
|:------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="9bec2-118">**Знак подписывания**</span><span class="sxs-lookup"><span data-stu-id="9bec2-118">**CoSign**</span></span>](signeddata-cosign.md) | <span data-ttu-id="9bec2-119">Сописывает уже подписанное сообщение.</span><span class="sxs-lookup"><span data-stu-id="9bec2-119">Cosigns an already signed message.</span></span><br/>                       |
| [<span data-ttu-id="9bec2-120">**Писать**</span><span class="sxs-lookup"><span data-stu-id="9bec2-120">**Sign**</span></span>](signeddata-sign.md)     | <span data-ttu-id="9bec2-121">Создает цифровую подпись для подписанного содержимого.</span><span class="sxs-lookup"><span data-stu-id="9bec2-121">Creates a digital signature on the content to be signed.</span></span><br/> |
| [<span data-ttu-id="9bec2-122">**Проверка**</span><span class="sxs-lookup"><span data-stu-id="9bec2-122">**Verify**</span></span>](signeddata-verify.md) | <span data-ttu-id="9bec2-123">Определяет допустимость подписи или сигнатур.</span><span class="sxs-lookup"><span data-stu-id="9bec2-123">Determines the validity of a signature or signatures.</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="9bec2-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="9bec2-124">Properties</span></span>

<span data-ttu-id="9bec2-125">Объект **сигнеддата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9bec2-125">The **SignedData** object has these properties.</span></span>



| <span data-ttu-id="9bec2-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="9bec2-126">Property</span></span>                                                   | <span data-ttu-id="9bec2-127">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="9bec2-127">Access type</span></span>           | <span data-ttu-id="9bec2-128">Описание</span><span class="sxs-lookup"><span data-stu-id="9bec2-128">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9bec2-129">**Сертификаты**</span><span class="sxs-lookup"><span data-stu-id="9bec2-129">**Certificates**</span></span>](signeddata-certificates.md)<br/> | <span data-ttu-id="9bec2-130">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bec2-130">Read-only</span></span><br/>  | <span data-ttu-id="9bec2-131">Извлекает коллекцию [**сертификатов**](certificates.md) подписанных данных.</span><span class="sxs-lookup"><span data-stu-id="9bec2-131">Retrieves the [**Certificates**](certificates.md) collection of the signed data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="9bec2-132">**Содержани**</span><span class="sxs-lookup"><span data-stu-id="9bec2-132">**Content**</span></span>](signeddata-content.md)<br/>           | <span data-ttu-id="9bec2-133">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9bec2-133">Read/write</span></span><br/> | <span data-ttu-id="9bec2-134">Данные для подписи.</span><span class="sxs-lookup"><span data-stu-id="9bec2-134">Data to be signed.</span></span> <span data-ttu-id="9bec2-135">Это свойство должно быть инициализировано до вызова метода [**Sign**](signeddata-sign.md) .</span><span class="sxs-lookup"><span data-stu-id="9bec2-135">This property must be initialized before the [**Sign**](signeddata-sign.md) method is called.</span></span><br/> <span data-ttu-id="9bec2-136">Когда значение этого свойства сбрасывается прямо или косвенно, все [*состояние*](../secgloss/s-gly.md) объекта сбрасывается, и все сигнатуры, связанные с объектом до изменения свойства, теряются.</span><span class="sxs-lookup"><span data-stu-id="9bec2-136">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any signature that was associated with the object before the property was changed is lost.</span></span><br/> <span data-ttu-id="9bec2-137">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9bec2-137">This is the default property.</span></span><br/> |
| [<span data-ttu-id="9bec2-138">**Подписавшими**</span><span class="sxs-lookup"><span data-stu-id="9bec2-138">**Signers**</span></span>](signeddata-signers.md)<br/>           | <span data-ttu-id="9bec2-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bec2-139">Read-only</span></span><br/>  | <span data-ttu-id="9bec2-140">Извлекает коллекцию [**подписывающих**](signers.md) , представляющую создатели подписей данных.</span><span class="sxs-lookup"><span data-stu-id="9bec2-140">Retrieves the [**Signers**](signers.md) collection that represents the signature creators of the data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="9bec2-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9bec2-141">Remarks</span></span>

<span data-ttu-id="9bec2-142">Объект **сигнеддата** может быть создан и защищен для создания скриптов.</span><span class="sxs-lookup"><span data-stu-id="9bec2-142">The **SignedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="9bec2-143">ProgID для объекта **сигнеддата** — CAPICOM. Сигнеддата. 1.</span><span class="sxs-lookup"><span data-stu-id="9bec2-143">The ProgID for the **SignedData** object is CAPICOM.SignedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bec2-144">Требования</span><span class="sxs-lookup"><span data-stu-id="9bec2-144">Requirements</span></span>



| <span data-ttu-id="9bec2-145">Требование</span><span class="sxs-lookup"><span data-stu-id="9bec2-145">Requirement</span></span> | <span data-ttu-id="9bec2-146">Значение</span><span class="sxs-lookup"><span data-stu-id="9bec2-146">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bec2-147">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="9bec2-147">Redistributable</span></span><br/> | <span data-ttu-id="9bec2-148">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="9bec2-148">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9bec2-149">DLL</span><span class="sxs-lookup"><span data-stu-id="9bec2-149">DLL</span></span><br/>             | <dl> <span data-ttu-id="9bec2-150"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bec2-150"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bec2-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9bec2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bec2-152">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="9bec2-152">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
