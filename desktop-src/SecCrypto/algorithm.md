---
description: Указывает алгоритм, используемый для подписывания, запечатывание и шифрования операций.
ms.assetid: 9a3071a3-e62d-43d3-acd7-0685592c78b4
title: Объект Algorithm (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f564efe9df3122951969a45443d58ace60e9db30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665133"
---
# <a name="algorithm-object"></a><span data-ttu-id="7b1ee-103">Объект Algorithm</span><span class="sxs-lookup"><span data-stu-id="7b1ee-103">Algorithm object</span></span>

<span data-ttu-id="7b1ee-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7b1ee-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="7b1ee-105">Вместо этого используйте [**класс алгорисмидентифиер**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="7b1ee-105">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="7b1ee-106">Объект **Algorithm** задает алгоритм, используемый для подписывания, запечатывание и шифрования операций.</span><span class="sxs-lookup"><span data-stu-id="7b1ee-106">The **Algorithm** object specifies the algorithm used for signing, enveloping, and encrypting operations.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="7b1ee-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="7b1ee-107">When to use</span></span>

<span data-ttu-id="7b1ee-108">Объект **Algorithm** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="7b1ee-108">The **Algorithm** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="7b1ee-109">Задайте или получите используемый алгоритм.</span><span class="sxs-lookup"><span data-stu-id="7b1ee-109">Set or retrieve the algorithm to be used.</span></span>
-   <span data-ttu-id="7b1ee-110">Задайте или получите длину ключа.</span><span class="sxs-lookup"><span data-stu-id="7b1ee-110">Set or retrieve the key length.</span></span>

> [!Note]  
> <span data-ttu-id="7b1ee-111">CAPICOM пытается использовать стандартный поставщик служб шифрования (CSP) системы.</span><span class="sxs-lookup"><span data-stu-id="7b1ee-111">CAPICOM attempts to use the system default cryptographic service provider (CSP).</span></span> <span data-ttu-id="7b1ee-112">Если этот поставщик CSP не может предоставить запрошенный алгоритм или длину ключа, то CAPICOM ищет доступный поставщику CSP, который может управлять запрошенным алгоритмом и длиной ключа, в следующем порядке доступности: корпорацией Майкрософт расширенный поставщик служб шифрования, поставщик строгой криптографии Майкрософт, базовый поставщик служб шифрования.</span><span class="sxs-lookup"><span data-stu-id="7b1ee-112">If that CSP cannot provide the requested algorithm or key length, CAPICOM searches for an available Microsoft-provided CSP that can handle the requested algorithm and key length, in this order of availability: Microsoft Enhanced Cryptographic Provider, Microsoft Strong Cryptographic Provider, Microsoft Base Cryptographic Provider.</span></span>

 

## <a name="members"></a><span data-ttu-id="7b1ee-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="7b1ee-113">Members</span></span>

<span data-ttu-id="7b1ee-114">Объект **алгоритма** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7b1ee-114">The **Algorithm** object has these types of members:</span></span>

-   [<span data-ttu-id="7b1ee-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="7b1ee-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b1ee-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="7b1ee-116">Properties</span></span>

<span data-ttu-id="7b1ee-117">Объект **алгоритма** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7b1ee-117">The **Algorithm** object has these properties.</span></span>



| <span data-ttu-id="7b1ee-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="7b1ee-118">Property</span></span>                                            | <span data-ttu-id="7b1ee-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="7b1ee-119">Access type</span></span>           | <span data-ttu-id="7b1ee-120">Описание</span><span class="sxs-lookup"><span data-stu-id="7b1ee-120">Description</span></span>                                                                                                                       |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b1ee-121">**KeyLength**</span><span class="sxs-lookup"><span data-stu-id="7b1ee-121">**KeyLength**</span></span>](algorithm-keylength.md)<br/> | <span data-ttu-id="7b1ee-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="7b1ee-122">Read/write</span></span><br/> | <span data-ttu-id="7b1ee-123">Задает или получает длину ключа.</span><span class="sxs-lookup"><span data-stu-id="7b1ee-123">Sets or retrieves the length of the key.</span></span><br/>                                                                               |
| [<span data-ttu-id="7b1ee-124">**Имя**</span><span class="sxs-lookup"><span data-stu-id="7b1ee-124">**Name**</span></span>](algorithm-name.md)<br/>           | <span data-ttu-id="7b1ee-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="7b1ee-125">Read/write</span></span><br/> | <span data-ttu-id="7b1ee-126">Задает или получает алгоритм, используемый для подписывания, запечатывание и шифрования операций.</span><span class="sxs-lookup"><span data-stu-id="7b1ee-126">Sets or retrieves the algorithm used for signing, enveloping, and encrypting operations.</span></span> <span data-ttu-id="7b1ee-127">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7b1ee-127">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7b1ee-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b1ee-128">Remarks</span></span>

<span data-ttu-id="7b1ee-129">Не удается создать объект **алгоритма** .</span><span class="sxs-lookup"><span data-stu-id="7b1ee-129">The **Algorithm** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b1ee-130">Требования</span><span class="sxs-lookup"><span data-stu-id="7b1ee-130">Requirements</span></span>



| <span data-ttu-id="7b1ee-131">Требование</span><span class="sxs-lookup"><span data-stu-id="7b1ee-131">Requirement</span></span> | <span data-ttu-id="7b1ee-132">Значение</span><span class="sxs-lookup"><span data-stu-id="7b1ee-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b1ee-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7b1ee-133">End of client support</span></span><br/> | <span data-ttu-id="7b1ee-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b1ee-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7b1ee-135">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7b1ee-135">End of server support</span></span><br/> | <span data-ttu-id="7b1ee-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b1ee-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7b1ee-137">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="7b1ee-137">Redistributable</span></span><br/>       | <span data-ttu-id="7b1ee-138">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="7b1ee-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7b1ee-139">Header</span><span class="sxs-lookup"><span data-stu-id="7b1ee-139">Header</span></span><br/>                | <dl> <span data-ttu-id="7b1ee-140"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b1ee-140"><dt>Capicom.h</dt></span></span> </dl>   |
| <span data-ttu-id="7b1ee-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7b1ee-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7b1ee-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b1ee-142"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b1ee-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b1ee-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b1ee-144">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="7b1ee-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
