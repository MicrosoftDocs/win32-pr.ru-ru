---
description: Важно! Этот API не рекомендуется к использованию.
ms.assetid: 4e6eb2df-a917-4533-b9f1-8da39598d0b8
title: Поставщики служб шифрования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5431d8ddda1be977e2a33297613633343fc2f9c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423777"
---
# <a name="cryptographic-service-providers"></a><span data-ttu-id="3b151-103">Поставщики служб шифрования</span><span class="sxs-lookup"><span data-stu-id="3b151-103">Cryptographic Service Providers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b151-104">Это нерекомендуемый API.</span><span class="sxs-lookup"><span data-stu-id="3b151-104">This API is deprecated.</span></span> <span data-ttu-id="3b151-105">Новое и существующее программное обеспечение должно начинаться с использования [API-интерфейсов следующего поколения шифрования.](/windows/desktop/SecCNG/cng-portal)</span><span class="sxs-lookup"><span data-stu-id="3b151-105">New and existing software should start using [Cryptography Next Generation APIs.](/windows/desktop/SecCNG/cng-portal)</span></span> <span data-ttu-id="3b151-106">Корпорация Майкрософт может удалить этот API в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="3b151-106">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="3b151-107">[*Поставщик служб шифрования*](../secgloss/c-gly.md) (CSP) содержит реализации криптографических стандартов и алгоритмов.</span><span class="sxs-lookup"><span data-stu-id="3b151-107">A [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) contains implementations of cryptographic standards and algorithms.</span></span> <span data-ttu-id="3b151-108">Как минимум CSP состоит из [*библиотеки динамической компоновки*](../secgloss/d-gly.md) (DLL), которая реализует функции в [*криптоспи*](../secgloss/c-gly.md) ( [*интерфейс системных программ*](../secgloss/s-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="3b151-108">At a minimum, a CSP consists of a [*dynamic-link library*](../secgloss/d-gly.md) (DLL) that implements the functions in [*CryptoSPI*](../secgloss/c-gly.md) (a [*system program interface*](../secgloss/s-gly.md)).</span></span> <span data-ttu-id="3b151-109">Большинство CSP содержат реализацию всех собственных функций.</span><span class="sxs-lookup"><span data-stu-id="3b151-109">Most CSPs contain the implementation of all of their own functions.</span></span> <span data-ttu-id="3b151-110">Однако некоторые CSP реализуют свои функции в основном в программе Windows-служб, управляемой диспетчером управления службами Windows.</span><span class="sxs-lookup"><span data-stu-id="3b151-110">Some CSPs, however, implement their functions mainly in a Windows-based service program managed by the Windows service control manager.</span></span> <span data-ttu-id="3b151-111">Другие реализуют функции в оборудовании, такие как [*смарт-карта*](../secgloss/s-gly.md) или безопасный сопроцессор.</span><span class="sxs-lookup"><span data-stu-id="3b151-111">Others implement functions in hardware, such as a [*smart card*](../secgloss/s-gly.md) or secure coprocessor.</span></span> <span data-ttu-id="3b151-112">Если CSP не реализует собственные функции, Библиотека DLL выступает в качестве сквозного слоя, что упрощает взаимодействие между операционной системой и фактической реализацией CSP.</span><span class="sxs-lookup"><span data-stu-id="3b151-112">If a CSP does not implement its own functions, the DLL acts as a pass-through layer, facilitating the communication between the operating system and the actual CSP implementation.</span></span>

<span data-ttu-id="3b151-113">Этот раздел содержит следующие темы.</span><span class="sxs-lookup"><span data-stu-id="3b151-113">This section includes the following topics.</span></span>



| <span data-ttu-id="3b151-114">Раздел</span><span class="sxs-lookup"><span data-stu-id="3b151-114">Topic</span></span>                                                                                      | <span data-ttu-id="3b151-115">Содержимое</span><span class="sxs-lookup"><span data-stu-id="3b151-115">Contents</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b151-116">Типы поставщиков служб шифрования</span><span class="sxs-lookup"><span data-stu-id="3b151-116">Cryptographic Provider Types</span></span>](cryptographic-provider-types.md)                           | <span data-ttu-id="3b151-117">Типы поставщиков служб шифрования — это семейства поставщиков службы шифрования, которые совместно используют форматы данных и криптографические протоколы.</span><span class="sxs-lookup"><span data-stu-id="3b151-117">Cryptographic provider types are families of cryptographic services providers that share data formats and cryptographic protocols.</span></span> <span data-ttu-id="3b151-118">Форматы данных включают в себя алгоритмы [*заполнения*](../secgloss/p-gly.md) , [*длины ключей*](../secgloss/k-gly.md)и режимы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3b151-118">Data formats include algorithms [*padding*](../secgloss/p-gly.md) schemes, [*key lengths*](../secgloss/k-gly.md), and default modes.</span></span> |
| [<span data-ttu-id="3b151-119">Поставщики служб шифрования Майкрософт</span><span class="sxs-lookup"><span data-stu-id="3b151-119">Microsoft Cryptographic Service Providers</span></span>](microsoft-cryptographic-service-providers.md) | <span data-ttu-id="3b151-120">Подробные сведения о CSP, доступных в настоящее время в корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3b151-120">Detailed information about CSPs currently available from Microsoft.</span></span>                                                                                                                                                                                                                                                                                       |



 

 

 
