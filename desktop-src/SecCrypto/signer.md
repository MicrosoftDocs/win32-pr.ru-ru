---
description: Устанавливает подписывающий объекта Сигнеддата или Сигнедкоде.
ms.assetid: fca6489c-56cf-472f-ac0f-73ba531fa212
title: Объект SignIn
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 974341eb996f2b5d3701757a5352ef56e2837390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669165"
---
# <a name="signer-object"></a><span data-ttu-id="0faf4-103">Объект SignIn</span><span class="sxs-lookup"><span data-stu-id="0faf4-103">Signer object</span></span>

<span data-ttu-id="0faf4-104">\[Объект- **подписавший** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="0faf4-104">\[The **Signer** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0faf4-105">Вместо этого используйте [**класс кмссигнер**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="0faf4-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="0faf4-106">Объект- **подписывающий** устанавливает подписывающий объекта [**сигнеддата**](signeddata.md) или [**сигнедкоде**](signedcode.md) .</span><span class="sxs-lookup"><span data-stu-id="0faf4-106">The **Signer** object establishes the signer of a [**SignedData**](signeddata.md) or [**SignedCode**](signedcode.md) object.</span></span> <span data-ttu-id="0faf4-107">[**Сертификат**](certificate.md) объекта " **подписавший** " должен иметь доступный закрытый ключ, который можно использовать для подписывания данных.</span><span class="sxs-lookup"><span data-stu-id="0faf4-107">The [**Certificate**](certificate.md) of the **Signer** object must have an available private key that can be used to sign data.</span></span>

## <a name="members"></a><span data-ttu-id="0faf4-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="0faf4-108">Members</span></span>

<span data-ttu-id="0faf4-109">Объект **SignIn** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0faf4-109">The **Signer** object has these types of members:</span></span>

-   [<span data-ttu-id="0faf4-110">Методы</span><span class="sxs-lookup"><span data-stu-id="0faf4-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0faf4-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="0faf4-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0faf4-112">Методы</span><span class="sxs-lookup"><span data-stu-id="0faf4-112">Methods</span></span>

<span data-ttu-id="0faf4-113">У объекта **подписавши** есть эти методы.</span><span class="sxs-lookup"><span data-stu-id="0faf4-113">The **Signer** object has these methods.</span></span>



| <span data-ttu-id="0faf4-114">Метод</span><span class="sxs-lookup"><span data-stu-id="0faf4-114">Method</span></span>                      | <span data-ttu-id="0faf4-115">Описание</span><span class="sxs-lookup"><span data-stu-id="0faf4-115">Description</span></span>                                                       |
|:----------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="0faf4-116">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="0faf4-116">**Load**</span></span>](signer-load.md) | <span data-ttu-id="0faf4-117">Загружает сертификат подписи из указанного PFX-файла.</span><span class="sxs-lookup"><span data-stu-id="0faf4-117">Loads a signing certificate from a specified PFX file.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0faf4-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="0faf4-118">Properties</span></span>

<span data-ttu-id="0faf4-119">У объекта **подписавши** есть эти свойства.</span><span class="sxs-lookup"><span data-stu-id="0faf4-119">The **Signer** object has these properties.</span></span>



| <span data-ttu-id="0faf4-120">Свойство</span><span class="sxs-lookup"><span data-stu-id="0faf4-120">Property</span></span>                                                                     | <span data-ttu-id="0faf4-121">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="0faf4-121">Access type</span></span>           | <span data-ttu-id="0faf4-122">Описание</span><span class="sxs-lookup"><span data-stu-id="0faf4-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0faf4-123">**аусентикатедаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="0faf4-123">**AuthenticatedAttributes**</span></span>](signer-authenticatedattributes.md)<br/> | <span data-ttu-id="0faf4-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0faf4-124">Read-only</span></span><br/>  | <span data-ttu-id="0faf4-125">Коллекция атрибутов, прошедших проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="0faf4-125">The collection of authenticated attributes.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="0faf4-126">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="0faf4-126">**Certificate**</span></span>](signer-certificate.md)<br/>                         | <span data-ttu-id="0faf4-127">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0faf4-127">Read/write</span></span><br/> | <span data-ttu-id="0faf4-128">Объект [**сертификата**](certificate.md) , представляющий сертификат подписи данных.</span><span class="sxs-lookup"><span data-stu-id="0faf4-128">The [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span><br/> <span data-ttu-id="0faf4-129">Когда значение этого свойства сбрасывается прямо или косвенно, полное [*состояние*](../secgloss/s-gly.md) объекта сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="0faf4-129">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span><br/> <span data-ttu-id="0faf4-130">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0faf4-130">This is the default property.</span></span><br/> |
| [<span data-ttu-id="0faf4-131">**Цепочк**</span><span class="sxs-lookup"><span data-stu-id="0faf4-131">**Chain**</span></span>](signer-chain.md)<br/>                                     | <span data-ttu-id="0faf4-132">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0faf4-132">Read-only</span></span><br/>  | <span data-ttu-id="0faf4-133">Цепочка подписи.</span><span class="sxs-lookup"><span data-stu-id="0faf4-133">The chain of the signer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="0faf4-134">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="0faf4-134">**Options**</span></span>](signer-options.md)<br/>                                 | <span data-ttu-id="0faf4-135">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0faf4-135">Read/write</span></span><br/> | <span data-ttu-id="0faf4-136">Задает или получает параметр сертификата подписывания.</span><span class="sxs-lookup"><span data-stu-id="0faf4-136">Sets or retrieves the signer's certificate option.</span></span><br/>                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="0faf4-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0faf4-137">Remarks</span></span>

<span data-ttu-id="0faf4-138">Объект- **подписавший** может быть создан и защищен для создания скриптов.</span><span class="sxs-lookup"><span data-stu-id="0faf4-138">The **Signer** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="0faf4-139">ProgID для объекта- **подписавший** — CAPICOM. Подписавший. 2.</span><span class="sxs-lookup"><span data-stu-id="0faf4-139">The ProgID for the **Signer** object is CAPICOM.Signer.2.</span></span>

<span data-ttu-id="0faf4-140">**CAPICOM 1. *x*:** идентификатор ProgID для объекта- **подписавший** — CAPICOM. Подписавший. 1.</span><span class="sxs-lookup"><span data-stu-id="0faf4-140">**CAPICOM 1.*x*:** The ProgID for the **Signer** object is CAPICOM.Signer.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="0faf4-141">Требования</span><span class="sxs-lookup"><span data-stu-id="0faf4-141">Requirements</span></span>



| <span data-ttu-id="0faf4-142">Требование</span><span class="sxs-lookup"><span data-stu-id="0faf4-142">Requirement</span></span> | <span data-ttu-id="0faf4-143">Значение</span><span class="sxs-lookup"><span data-stu-id="0faf4-143">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0faf4-144">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0faf4-144">Redistributable</span></span><br/> | <span data-ttu-id="0faf4-145">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="0faf4-145">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0faf4-146">DLL</span><span class="sxs-lookup"><span data-stu-id="0faf4-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="0faf4-147"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0faf4-147"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0faf4-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0faf4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0faf4-149">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="0faf4-149">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
