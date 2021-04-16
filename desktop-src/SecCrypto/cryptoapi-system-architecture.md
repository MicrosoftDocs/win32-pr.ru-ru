---
description: Описывает архитектуру системы CryptoAPI.
ms.assetid: 244329bb-fc71-4ab9-8831-a9478108ffa3
title: Архитектура системы CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d5dcf1756c9b581d75d4e52d57fbce089976a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343142"
---
# <a name="cryptoapi-system-architecture"></a><span data-ttu-id="de85a-103">Архитектура системы CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="de85a-103">CryptoAPI System Architecture</span></span>

<span data-ttu-id="de85a-104">Архитектура системы CryptoAPI состоит из пяти основных функциональных областей:</span><span class="sxs-lookup"><span data-stu-id="de85a-104">The CryptoAPI system architecture is composed of five major functional areas:</span></span>

-   [<span data-ttu-id="de85a-105">Базовые криптографические функции</span><span class="sxs-lookup"><span data-stu-id="de85a-105">Base Cryptographic Functions</span></span>](#base-cryptographic-functions)
-   [<span data-ttu-id="de85a-106">Функции шифрования и расшифровки сертификатов</span><span class="sxs-lookup"><span data-stu-id="de85a-106">Certificate Encode/Decode Functions</span></span>](#certificate-encodedecode-functions)
-   [<span data-ttu-id="de85a-107">Функции хранилища сертификатов</span><span class="sxs-lookup"><span data-stu-id="de85a-107">Certificate Store Functions</span></span>](#certificate-store-functions)
-   [<span data-ttu-id="de85a-108">Упрощенные функции сообщений</span><span class="sxs-lookup"><span data-stu-id="de85a-108">Simplified Message Functions</span></span>](#simplified-message-functions)
-   [<span data-ttu-id="de85a-109">Низкоуровневые функции сообщений</span><span class="sxs-lookup"><span data-stu-id="de85a-109">Low-level Message Functions</span></span>](#low-level-message-functions)

## <a name="base-cryptographic-functions"></a><span data-ttu-id="de85a-110">Базовые криптографические функции</span><span class="sxs-lookup"><span data-stu-id="de85a-110">Base Cryptographic Functions</span></span>

-   <span data-ttu-id="de85a-111">*Функции контекста* , используемые для подключения к CSP.</span><span class="sxs-lookup"><span data-stu-id="de85a-111">*Context functions* used to connect to a CSP.</span></span> <span data-ttu-id="de85a-112">Эти функции позволяют приложениям выбрать конкретного CSP по имени или выбрать конкретного CSP, который может предоставить необходимый класс функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="de85a-112">These functions enable applications to choose a specific CSP by name or to choose a specific CSP that can provide a needed class of functionality.</span></span>
-   <span data-ttu-id="de85a-113">[*Функции создания ключей*](../secgloss/k-gly.md) , используемые для создания и хранения [*криптографических ключей*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="de85a-113">[*Key generation functions*](../secgloss/k-gly.md) used to generate and store [*cryptographic keys*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="de85a-114">Полная поддержка включает в себя изменение [*режимов цепочки*](../secgloss/c-gly.md), [*векторов инициализации*](../secgloss/i-gly.md)и других функций шифрования.</span><span class="sxs-lookup"><span data-stu-id="de85a-114">Full support is included for changing [*chaining modes*](../secgloss/c-gly.md), [*initialization vectors*](../secgloss/i-gly.md), and other encryption features.</span></span> <span data-ttu-id="de85a-115">Дополнительные сведения см. в разделе [Создание ключей и функции Exchange](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="de85a-115">For more information, see [Key Generation and Exchange Functions](cryptography-functions.md).</span></span>
-   <span data-ttu-id="de85a-116">*Функции обмена ключами* , используемые для обмена или передачи ключей.</span><span class="sxs-lookup"><span data-stu-id="de85a-116">*Key exchange functions* used to exchange or transmit keys.</span></span> <span data-ttu-id="de85a-117">Дополнительные сведения см. в статьях [Хранение криптографических ключей и Exchange](cryptographic-key-storage-and-exchange.md) , [Создание ключей и функции Exchange](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="de85a-117">For more information, see [Cryptographic Key Storage and Exchange](cryptographic-key-storage-and-exchange.md) and [Key Generation and Exchange Functions](cryptography-functions.md).</span></span>

## <a name="certificate-encodedecode-functions"></a><span data-ttu-id="de85a-118">Функции шифрования и расшифровки сертификатов</span><span class="sxs-lookup"><span data-stu-id="de85a-118">Certificate Encode/Decode Functions</span></span>

-   <span data-ttu-id="de85a-119">Функции, используемые для шифрования или расшифровки данных.</span><span class="sxs-lookup"><span data-stu-id="de85a-119">Functions used to encrypt or decrypt data.</span></span> <span data-ttu-id="de85a-120">Также включена поддержка [*хэширования*](../secgloss/h-gly.md) данных.</span><span class="sxs-lookup"><span data-stu-id="de85a-120">Support is also included for [*hashing*](../secgloss/h-gly.md) data.</span></span> <span data-ttu-id="de85a-121">Дополнительные сведения см. в разделе [функции шифрования и расшифровки данных](cryptography-functions.md) , а затем — [Шифрование и расшифровка данных](data-encryption-and-decryption.md).</span><span class="sxs-lookup"><span data-stu-id="de85a-121">For more information, see [Data Encryption and Decryption Functions](cryptography-functions.md) and [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>

## <a name="certificate-store-functions"></a><span data-ttu-id="de85a-122">Функции хранилища сертификатов</span><span class="sxs-lookup"><span data-stu-id="de85a-122">Certificate Store Functions</span></span>

-   <span data-ttu-id="de85a-123">Функции, используемые для управления коллекциями цифровых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="de85a-123">Functions used to manage collections of digital certificates.</span></span> <span data-ttu-id="de85a-124">Дополнительные сведения см. в статье [цифровые сертификаты](digital-certificates.md) и [функции хранилища сертификатов](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="de85a-124">For more information, see [Digital Certificates](digital-certificates.md) and [Certificate Store Functions](cryptography-functions.md).</span></span>

## <a name="simplified-message-functions"></a><span data-ttu-id="de85a-125">Упрощенные функции сообщений</span><span class="sxs-lookup"><span data-stu-id="de85a-125">Simplified Message Functions</span></span>

-   <span data-ttu-id="de85a-126">Функции, используемые для шифрования и расшифровки сообщений и данных.</span><span class="sxs-lookup"><span data-stu-id="de85a-126">Functions used to encrypt and decrypt messages and data.</span></span>
-   <span data-ttu-id="de85a-127">Функции, используемые для подписи сообщений и данных.</span><span class="sxs-lookup"><span data-stu-id="de85a-127">Functions used to sign messages and data.</span></span>
-   <span data-ttu-id="de85a-128">Функции, используемые для проверки подлинности подписей в полученных сообщениях и связанных данных.</span><span class="sxs-lookup"><span data-stu-id="de85a-128">Functions used to verify the authenticity of signatures on received messages and related data.</span></span>

<span data-ttu-id="de85a-129">Дополнительные сведения см. в разделе [упрощенные сообщения](simplified-messages.md) и [упрощенные функции сообщений](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="de85a-129">For more information, see [Simplified Messages](simplified-messages.md) and [Simplified Message Functions](cryptography-functions.md).</span></span>

## <a name="low-level-message-functions"></a><span data-ttu-id="de85a-130">Низкоуровневые функции сообщений</span><span class="sxs-lookup"><span data-stu-id="de85a-130">Low-level Message Functions</span></span>

-   <span data-ttu-id="de85a-131">Функции, используемые для выполнения всех задач, выполняемых упрощенными функциями сообщений.</span><span class="sxs-lookup"><span data-stu-id="de85a-131">Functions used to perform all of the tasks performed by the simplified message functions.</span></span> <span data-ttu-id="de85a-132">Низкоуровневые функции сообщений обеспечивают большую гибкость, чем упрощенные функции сообщений, но требует больше вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="de85a-132">The low-level message functions provide more flexibility than the simplified message functions but require more function calls.</span></span> <span data-ttu-id="de85a-133">Дополнительные сведения см. в разделе [сообщения низкого уровня](low-level-messages.md) и [низкоуровневые функции сообщений](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="de85a-133">For more information, see [Low-level Messages](low-level-messages.md) and [Low-level Message Functions](cryptography-functions.md).</span></span>

![Архитектура CryptoAPI](images/cryparch.png)

<span data-ttu-id="de85a-135">Каждая из функциональных областей содержит ключевое слово в имени функции, которое указывает на свою функциональную область.</span><span class="sxs-lookup"><span data-stu-id="de85a-135">Each of the functional areas has a key word in its function name that indicates its functional area.</span></span>



| <span data-ttu-id="de85a-136">Функциональная область</span><span class="sxs-lookup"><span data-stu-id="de85a-136">Functional area</span></span>              | <span data-ttu-id="de85a-137">Соглашение об именах функций</span><span class="sxs-lookup"><span data-stu-id="de85a-137">Function name convention</span></span> |
|------------------------------|--------------------------|
| <span data-ttu-id="de85a-138">Базовые криптографические функции</span><span class="sxs-lookup"><span data-stu-id="de85a-138">Base cryptographic functions</span></span> | <span data-ttu-id="de85a-139">Загадоч</span><span class="sxs-lookup"><span data-stu-id="de85a-139">Crypt</span></span>                    |
| <span data-ttu-id="de85a-140">Функции кодирования и декодирования</span><span class="sxs-lookup"><span data-stu-id="de85a-140">Encoding/decoding functions</span></span>  | <span data-ttu-id="de85a-141">Загадоч</span><span class="sxs-lookup"><span data-stu-id="de85a-141">Crypt</span></span>                    |
| <span data-ttu-id="de85a-142">Функции хранилища сертификатов</span><span class="sxs-lookup"><span data-stu-id="de85a-142">Certificate store functions</span></span>  | <span data-ttu-id="de85a-143">Магазин</span><span class="sxs-lookup"><span data-stu-id="de85a-143">Store</span></span>                    |
| <span data-ttu-id="de85a-144">Упрощенные функции сообщений</span><span class="sxs-lookup"><span data-stu-id="de85a-144">Simplified message functions</span></span> | <span data-ttu-id="de85a-145">Сообщение</span><span class="sxs-lookup"><span data-stu-id="de85a-145">Message</span></span>                  |
| <span data-ttu-id="de85a-146">Низкоуровневые функции сообщений</span><span class="sxs-lookup"><span data-stu-id="de85a-146">Low-level message functions</span></span>  | <span data-ttu-id="de85a-147">Об</span><span class="sxs-lookup"><span data-stu-id="de85a-147">Msg</span></span>                      |



 

<span data-ttu-id="de85a-148">Приложения используют функции во всех этих областях.</span><span class="sxs-lookup"><span data-stu-id="de85a-148">Applications use functions in all of these areas.</span></span> <span data-ttu-id="de85a-149">Эти функции вместе составляют интерфейс CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="de85a-149">These functions, taken together, make up CryptoAPI.</span></span> <span data-ttu-id="de85a-150">[*Базовые криптографические функции*](../secgloss/b-gly.md) используют CSP для необходимых криптографических алгоритмов, а также для создания и безопасного хранения [криптографических ключей](cryptographic-keys.md).</span><span class="sxs-lookup"><span data-stu-id="de85a-150">The [*base cryptographic functions*](../secgloss/b-gly.md) use the CSPs for the necessary cryptographic algorithms and for the generation and secure storage of [cryptographic keys](cryptographic-keys.md).</span></span>

<span data-ttu-id="de85a-151">Используются два различных типа криптографических ключей: [*ключи сеанса*](../secgloss/s-gly.md), которые используются для одной пары шифрования и расшифровки, а [*открытые и закрытые*](../secgloss/p-gly.md)ключи, которые используются на более постоянной основе.</span><span class="sxs-lookup"><span data-stu-id="de85a-151">Two different kinds of cryptographic keys are used: [*session keys*](../secgloss/s-gly.md), which are used for a single encryption/decryption, and [*public/private key pairs*](../secgloss/p-gly.md), which are used on a more permanent basis.</span></span>

> [!Note]  
> <span data-ttu-id="de85a-152">Хотя приложение может напрямую взаимодействовать с любой из пяти функциональных областей, оно не может напрямую взаимодействовать с CSP.</span><span class="sxs-lookup"><span data-stu-id="de85a-152">Although an application can communicate directly with any of the five functional areas, it cannot communicate directly with a CSP.</span></span> <span data-ttu-id="de85a-153">Обмен данными между приложениями и CSP осуществляется через [*базовые криптографические функции*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="de85a-153">All application-to-CSP communications occur through the [*base cryptographic functions*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="de85a-154">Базовые криптографические функции имеют параметр, указывающий используемый CSP.</span><span class="sxs-lookup"><span data-stu-id="de85a-154">Base cryptographic functions have a parameter that specifies which CSP to use.</span></span> <span data-ttu-id="de85a-155">Этому параметру можно присвоить **значение NULL** , чтобы выбрать CSP по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="de85a-155">This parameter can be set to **NULL** to select a default CSP.</span></span>

 

 

 
