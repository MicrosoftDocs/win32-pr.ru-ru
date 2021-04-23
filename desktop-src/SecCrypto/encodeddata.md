---
description: Представляет блок данных в кодировке ASN. 1.
ms.assetid: af7acc5f-da0a-4235-8496-05db94664ea5
title: Объект Енкодеддата
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d05fce31ad4ef08bf9f573c0158a683bdbeba739
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669383"
---
# <a name="encodeddata-object"></a><span data-ttu-id="5c8a8-103">Объект Енкодеддата</span><span class="sxs-lookup"><span data-stu-id="5c8a8-103">EncodedData object</span></span>

<span data-ttu-id="5c8a8-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5c8a8-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="5c8a8-105">Вместо этого используйте [**класс асненкодеддата**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="5c8a8-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="5c8a8-106">Объект **енкодеддата** представляет блок данных в кодировке ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="5c8a8-106">The **EncodedData** object represents a block of ASN.1 encoded data.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="5c8a8-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="5c8a8-107">When to use</span></span>

<span data-ttu-id="5c8a8-108">Объект **енкодеддата** возвращается несколькими свойствами объекта CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="5c8a8-108">The **EncodedData** object is returned by several CAPICOM object properties.</span></span> <span data-ttu-id="5c8a8-109">При возвращении этот объект используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="5c8a8-109">When returned, this object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="5c8a8-110">Получение строкового представления закодированных данных.</span><span class="sxs-lookup"><span data-stu-id="5c8a8-110">Obtain a string representation of the encoded data.</span></span>
-   <span data-ttu-id="5c8a8-111">Получите объект декодера, если он существует, связанный с закодированными данными.</span><span class="sxs-lookup"><span data-stu-id="5c8a8-111">Obtain the decoder object, if it exists, that is associated with the encoded data.</span></span>
-   <span data-ttu-id="5c8a8-112">Определите тип закодированных данных.</span><span class="sxs-lookup"><span data-stu-id="5c8a8-112">Determine the type of encoded data.</span></span>

## <a name="members"></a><span data-ttu-id="5c8a8-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="5c8a8-113">Members</span></span>

<span data-ttu-id="5c8a8-114">Объект **енкодеддата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5c8a8-114">The **EncodedData** object has these types of members:</span></span>

-   [<span data-ttu-id="5c8a8-115">Методы</span><span class="sxs-lookup"><span data-stu-id="5c8a8-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="5c8a8-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="5c8a8-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5c8a8-117">Методы</span><span class="sxs-lookup"><span data-stu-id="5c8a8-117">Methods</span></span>

<span data-ttu-id="5c8a8-118">Объект **енкодеддата** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="5c8a8-118">The **EncodedData** object has these methods.</span></span>



| <span data-ttu-id="5c8a8-119">Метод</span><span class="sxs-lookup"><span data-stu-id="5c8a8-119">Method</span></span>                                 | <span data-ttu-id="5c8a8-120">Описание</span><span class="sxs-lookup"><span data-stu-id="5c8a8-120">Description</span></span>                                                     |
|:---------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="5c8a8-121">**Показан**</span><span class="sxs-lookup"><span data-stu-id="5c8a8-121">**Decoder**</span></span>](encodeddata-decoder.md) | <span data-ttu-id="5c8a8-122">Получает объект декодера, если он существует.</span><span class="sxs-lookup"><span data-stu-id="5c8a8-122">Obtains a decoder object, if one exists.</span></span><br/>             |
| [<span data-ttu-id="5c8a8-123">**Формат**</span><span class="sxs-lookup"><span data-stu-id="5c8a8-123">**Format**</span></span>](encodeddata-format.md)   | <span data-ttu-id="5c8a8-124">Возвращает строковое представление закодированных данных.</span><span class="sxs-lookup"><span data-stu-id="5c8a8-124">Returns a string representation of the encoded data.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5c8a8-125">Свойства</span><span class="sxs-lookup"><span data-stu-id="5c8a8-125">Properties</span></span>

<span data-ttu-id="5c8a8-126">Объект **енкодеддата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5c8a8-126">The **EncodedData** object has these properties.</span></span>



| <span data-ttu-id="5c8a8-127">Свойство</span><span class="sxs-lookup"><span data-stu-id="5c8a8-127">Property</span></span>                                      | <span data-ttu-id="5c8a8-128">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="5c8a8-128">Access type</span></span>          | <span data-ttu-id="5c8a8-129">Описание</span><span class="sxs-lookup"><span data-stu-id="5c8a8-129">Description</span></span>                                                          |
|:----------------------------------------------|:---------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="5c8a8-130">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5c8a8-130">**Value**</span></span>](encodeddata-value.md)<br/> | <span data-ttu-id="5c8a8-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c8a8-131">Read-only</span></span><br/> | <span data-ttu-id="5c8a8-132">Извлекает закодированные данные.</span><span class="sxs-lookup"><span data-stu-id="5c8a8-132">Retrieves the encoded data.</span></span> <span data-ttu-id="5c8a8-133">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5c8a8-133">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c8a8-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c8a8-134">Remarks</span></span>

<span data-ttu-id="5c8a8-135">Единственным поддерживаемым типом закодированных данных является [**цертификатеполиЦиес**](certificatepolicies.md).</span><span class="sxs-lookup"><span data-stu-id="5c8a8-135">The only supported type of encoded data is [**CertificatePolicies**](certificatepolicies.md).</span></span>

<span data-ttu-id="5c8a8-136">Не удается создать объект **енкодеддата** .</span><span class="sxs-lookup"><span data-stu-id="5c8a8-136">The **EncodedData** object cannot be created.</span></span>

<span data-ttu-id="5c8a8-137">Следующие свойства элемента CAPICOM возвращают объект **енкодеддата** :</span><span class="sxs-lookup"><span data-stu-id="5c8a8-137">The following CAPICOM object properties return an **EncodedData** object:</span></span>

-   <span data-ttu-id="5c8a8-138">**PublicKey. Енкодедкэй**</span><span class="sxs-lookup"><span data-stu-id="5c8a8-138">**PublicKey.EncodedKey**</span></span>
-   <span data-ttu-id="5c8a8-139">**PublicKey. Енкодедпараметерс**</span><span class="sxs-lookup"><span data-stu-id="5c8a8-139">**PublicKey.EncodedParameters**</span></span>
-   <span data-ttu-id="5c8a8-140">**Расширение. Енкодеддата**</span><span class="sxs-lookup"><span data-stu-id="5c8a8-140">**Extension.EncodedData**</span></span>
-   <span data-ttu-id="5c8a8-141">**Policy. Енкодеддата**</span><span class="sxs-lookup"><span data-stu-id="5c8a8-141">**Policy.EncodedData**</span></span>

## <a name="requirements"></a><span data-ttu-id="5c8a8-142">Требования</span><span class="sxs-lookup"><span data-stu-id="5c8a8-142">Requirements</span></span>



| <span data-ttu-id="5c8a8-143">Требование</span><span class="sxs-lookup"><span data-stu-id="5c8a8-143">Requirement</span></span> | <span data-ttu-id="5c8a8-144">Значение</span><span class="sxs-lookup"><span data-stu-id="5c8a8-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c8a8-145">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="5c8a8-145">End of client support</span></span><br/> | <span data-ttu-id="5c8a8-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c8a8-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5c8a8-147">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="5c8a8-147">End of server support</span></span><br/> | <span data-ttu-id="5c8a8-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c8a8-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5c8a8-149">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="5c8a8-149">Redistributable</span></span><br/>       | <span data-ttu-id="5c8a8-150">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="5c8a8-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5c8a8-151">DLL</span><span class="sxs-lookup"><span data-stu-id="5c8a8-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="5c8a8-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c8a8-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
