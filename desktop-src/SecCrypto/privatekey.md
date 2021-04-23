---
description: Представляет закрытый ключ, связанный с сертификатом.
ms.assetid: 26ad1d1c-17c5-4191-ac97-b911e62b4119
title: Объект PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e87ca7a5bf12bbaf943bccacaa075a51ae75ed37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665177"
---
# <a name="privatekey-object"></a><span data-ttu-id="b4078-103">Объект PrivateKey</span><span class="sxs-lookup"><span data-stu-id="b4078-103">PrivateKey object</span></span>

<span data-ttu-id="b4078-104">\[Объект **PrivateKey** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="b4078-104">\[The **PrivateKey** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b4078-105">Вместо этого используйте [**свойство X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="b4078-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b4078-106">Объект **PrivateKey** представляет [*закрытый ключ*](../secgloss/p-gly.md) , связанный с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="b4078-106">The **PrivateKey** object represents the [*private key*](../secgloss/p-gly.md) associated with a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b4078-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="b4078-107">When to use</span></span>

<span data-ttu-id="b4078-108">Объект **PrivateKey** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="b4078-108">The **PrivateKey** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="b4078-109">Получение сведений о закрытом ключе.</span><span class="sxs-lookup"><span data-stu-id="b4078-109">Retrieve information about the private key.</span></span>
-   <span data-ttu-id="b4078-110">Откройте контейнер закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="b4078-110">Open the private key container.</span></span>
-   <span data-ttu-id="b4078-111">Удалите закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="b4078-111">Delete the private key.</span></span>

## <a name="members"></a><span data-ttu-id="b4078-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="b4078-112">Members</span></span>

<span data-ttu-id="b4078-113">Объект **PrivateKey** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b4078-113">The **PrivateKey** object has these types of members:</span></span>

-   [<span data-ttu-id="b4078-114">Методы</span><span class="sxs-lookup"><span data-stu-id="b4078-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="b4078-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="b4078-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b4078-116">Методы</span><span class="sxs-lookup"><span data-stu-id="b4078-116">Methods</span></span>

<span data-ttu-id="b4078-117">Объект **PrivateKey** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="b4078-117">The **PrivateKey** object has these methods.</span></span>



| <span data-ttu-id="b4078-118">Метод</span><span class="sxs-lookup"><span data-stu-id="b4078-118">Method</span></span>                                                  | <span data-ttu-id="b4078-119">Описание</span><span class="sxs-lookup"><span data-stu-id="b4078-119">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4078-120">**Удален**</span><span class="sxs-lookup"><span data-stu-id="b4078-120">**Delete**</span></span>](privatekey-delete.md)                     | <span data-ttu-id="b4078-121">Удаляет контейнер закрытого ключа, на который ссылается объект **PrivateKey** .</span><span class="sxs-lookup"><span data-stu-id="b4078-121">Deletes the private key container referenced by the **PrivateKey** object.</span></span><br/>                                                                                |
| [<span data-ttu-id="b4078-122">**Доступно**</span><span class="sxs-lookup"><span data-stu-id="b4078-122">**IsAccessible**</span></span>](privatekey-isaccessible.md)         | <span data-ttu-id="b4078-123">Получает логическое значение, указывающее, доступен ли закрытый ключ пользователю.</span><span class="sxs-lookup"><span data-stu-id="b4078-123">Retrieves a Boolean value that indicates whether the private key is accessible by the user.</span></span> <span data-ttu-id="b4078-124">Если значение — true, пользователь может получить доступ к закрытому ключу.</span><span class="sxs-lookup"><span data-stu-id="b4078-124">If true, the user can access the private key.</span></span><br/>                 |
| [<span data-ttu-id="b4078-125">**IsExportable**</span><span class="sxs-lookup"><span data-stu-id="b4078-125">**IsExportable**</span></span>](privatekey-isexportable.md)         | <span data-ttu-id="b4078-126">Возвращает логическое значение, указывающее, можно ли экспортировать закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="b4078-126">Retrieves a Boolean value that indicates whether the private key can be exported.</span></span> <span data-ttu-id="b4078-127">Если значение — true, закрытый ключ можно экспортировать.</span><span class="sxs-lookup"><span data-stu-id="b4078-127">If true, the private key can be exported.</span></span><br/>                               |
| [<span data-ttu-id="b4078-128">**ишардваредевице**</span><span class="sxs-lookup"><span data-stu-id="b4078-128">**IsHardwareDevice**</span></span>](privatekey-ishardwaredevice.md) | <span data-ttu-id="b4078-129">Получает логическое значение, указывающее, хранится ли закрытый ключ на аппаратном устройстве.</span><span class="sxs-lookup"><span data-stu-id="b4078-129">Retrieves a Boolean value that indicates whether the private key is stored on a hardware device.</span></span> <span data-ttu-id="b4078-130">Если значение — true, закрытый ключ хранится на аппаратном устройстве.</span><span class="sxs-lookup"><span data-stu-id="b4078-130">If true, the private key is stored on a hardware device.</span></span><br/> |
| [<span data-ttu-id="b4078-131">**исмачинекэйсет**</span><span class="sxs-lookup"><span data-stu-id="b4078-131">**IsMachineKeyset**</span></span>](privatekey-ismachinekeyset.md)   | <span data-ttu-id="b4078-132">Возвращает логическое значение, указывающее, является ли закрытый ключ ключом компьютера.</span><span class="sxs-lookup"><span data-stu-id="b4078-132">Retrieves a Boolean value that indicates whether the private key is a machine key.</span></span> <span data-ttu-id="b4078-133">Если значение — true, закрытый ключ является ключом компьютера.</span><span class="sxs-lookup"><span data-stu-id="b4078-133">If true, the private key is a machine key.</span></span><br/>                             |
| [<span data-ttu-id="b4078-134">**Защита**</span><span class="sxs-lookup"><span data-stu-id="b4078-134">**IsProtected**</span></span>](privatekey-isprotected.md)           | <span data-ttu-id="b4078-135">Получает логическое значение, указывающее, защищен ли закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="b4078-135">Retrieves a Boolean value that indicates whether the private key is protected.</span></span> <span data-ttu-id="b4078-136">Если значение — true, закрытый ключ защищен.</span><span class="sxs-lookup"><span data-stu-id="b4078-136">If true, the private key is protected.</span></span><br/>                                     |
| [<span data-ttu-id="b4078-137">**Съемная**</span><span class="sxs-lookup"><span data-stu-id="b4078-137">**IsRemovable**</span></span>](privatekey-isremovable.md)           | <span data-ttu-id="b4078-138">Получает логическое значение, указывающее, находится ли закрытый ключ на съемном устройстве.</span><span class="sxs-lookup"><span data-stu-id="b4078-138">Retrieves a Boolean value that indicates whether the private key is on a removable device.</span></span> <span data-ttu-id="b4078-139">Если значение — true, закрытый ключ находится на съемном устройстве.</span><span class="sxs-lookup"><span data-stu-id="b4078-139">If true, the private key is on a removable device.</span></span><br/>             |
| [<span data-ttu-id="b4078-140">**Открыт**</span><span class="sxs-lookup"><span data-stu-id="b4078-140">**Open**</span></span>](privatekey-open.md)                         | <span data-ttu-id="b4078-141">Обращается к существующему контейнеру ключей.</span><span class="sxs-lookup"><span data-stu-id="b4078-141">Accesses an existing key container.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="b4078-142">Свойства</span><span class="sxs-lookup"><span data-stu-id="b4078-142">Properties</span></span>

<span data-ttu-id="b4078-143">Объект **PrivateKey** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b4078-143">The **PrivateKey** object has these properties.</span></span>



| <span data-ttu-id="b4078-144">Свойство</span><span class="sxs-lookup"><span data-stu-id="b4078-144">Property</span></span>                                                                 | <span data-ttu-id="b4078-145">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="b4078-145">Access type</span></span>          | <span data-ttu-id="b4078-146">Описание</span><span class="sxs-lookup"><span data-stu-id="b4078-146">Description</span></span>                                                                                               |
|:-------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4078-147">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="b4078-147">**ContainerName**</span></span>](privatekey-containername.md)<br/>             | <span data-ttu-id="b4078-148">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b4078-148">Read-only</span></span><br/> | <span data-ttu-id="b4078-149">Извлекает строку, содержащую имя контейнера закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="b4078-149">Retrieves a string that contains the private key container name.</span></span> <span data-ttu-id="b4078-150">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b4078-150">This is the default property.</span></span><br/> |
| [<span data-ttu-id="b4078-151">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="b4078-151">**KeySpec**</span></span>](privatekey-keyspec.md)<br/>                         | <span data-ttu-id="b4078-152">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b4078-152">Read-only</span></span><br/> | <span data-ttu-id="b4078-153">Извлекает спецификацию ключа.</span><span class="sxs-lookup"><span data-stu-id="b4078-153">Retrieves the key specification.</span></span><br/>                                                               |
| [<span data-ttu-id="b4078-154">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="b4078-154">**ProviderName**</span></span>](privatekey-providername.md)<br/>               | <span data-ttu-id="b4078-155">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b4078-155">Read-only</span></span><br/> | <span data-ttu-id="b4078-156">Извлекает строку, содержащую имя CSP.</span><span class="sxs-lookup"><span data-stu-id="b4078-156">Retrieves a string that contains the name of the CSP.</span></span><br/>                                          |
| [<span data-ttu-id="b4078-157">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="b4078-157">**ProviderType**</span></span>](privatekey-providertype.md)<br/>               | <span data-ttu-id="b4078-158">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b4078-158">Read-only</span></span><br/> | <span data-ttu-id="b4078-159">Возвращает значение перечисления, указывающее тип поставщика.</span><span class="sxs-lookup"><span data-stu-id="b4078-159">Retrieves an enumeration value that specifies the type of provider.</span></span><br/>                            |
| [<span data-ttu-id="b4078-160">**уникуеконтаинернаме**</span><span class="sxs-lookup"><span data-stu-id="b4078-160">**UniqueContainerName**</span></span>](privatekey-uniquecontainername.md)<br/> | <span data-ttu-id="b4078-161">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b4078-161">Read-only</span></span><br/> | <span data-ttu-id="b4078-162">Извлекает строку, содержащую уникальное имя контейнера закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="b4078-162">Retrieves a string that contains the unique private key container name.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="b4078-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4078-163">Remarks</span></span>

<span data-ttu-id="b4078-164">Объект **PrivateKey** может быть создан и защищен для создания скриптов.</span><span class="sxs-lookup"><span data-stu-id="b4078-164">The **PrivateKey** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="b4078-165">ProgID для объекта **PrivateKey** — CAPICOM. PrivateKey. 1.</span><span class="sxs-lookup"><span data-stu-id="b4078-165">The ProgID for the **PrivateKey** object is CAPICOM.PrivateKey.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4078-166">Требования</span><span class="sxs-lookup"><span data-stu-id="b4078-166">Requirements</span></span>



| <span data-ttu-id="b4078-167">Требование</span><span class="sxs-lookup"><span data-stu-id="b4078-167">Requirement</span></span> | <span data-ttu-id="b4078-168">Значение</span><span class="sxs-lookup"><span data-stu-id="b4078-168">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4078-169">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="b4078-169">Redistributable</span></span><br/> | <span data-ttu-id="b4078-170">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="b4078-170">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b4078-171">DLL</span><span class="sxs-lookup"><span data-stu-id="b4078-171">DLL</span></span><br/>             | <dl> <span data-ttu-id="b4078-172"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4078-172"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
