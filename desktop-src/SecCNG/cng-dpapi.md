---
description: Корпорация Майкрософт представила в Windows 2000 интерфейс прикладного программирования защиты данных (DPAPI).
ms.assetid: 048DEA72-39E1-4129-A554-F7D08442C2D9
title: CNG DPAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd0771b9838b2dbcfbedb3d025a7f650429bba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662166"
---
# <a name="cng-dpapi"></a><span data-ttu-id="2f066-103">CNG DPAPI</span><span class="sxs-lookup"><span data-stu-id="2f066-103">CNG DPAPI</span></span>

<span data-ttu-id="2f066-104">Корпорация Майкрософт представила в Windows 2000 интерфейс прикладного программирования защиты данных (DPAPI).</span><span class="sxs-lookup"><span data-stu-id="2f066-104">Microsoft introduced the data protection application programming interface (DPAPI) in Windows 2000.</span></span> <span data-ttu-id="2f066-105">API состоит из двух функций: [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata).</span><span class="sxs-lookup"><span data-stu-id="2f066-105">The API consists of two functions, [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata).</span></span> <span data-ttu-id="2f066-106">DPAPI является частью CryptoAPI и предназначен для разработчиков, которым очень мало известно об использовании криптографии.</span><span class="sxs-lookup"><span data-stu-id="2f066-106">DPAPI is part of CryptoAPI and was intended for developers who knew very little about using cryptography.</span></span> <span data-ttu-id="2f066-107">Эти две функции можно использовать для шифрования и расшифровки статических данных на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="2f066-107">The two functions could be used to encrypt and decrypt static data on a single computer.</span></span>

<span data-ttu-id="2f066-108">Однако для облачных вычислений часто требуется, чтобы содержимое, зашифрованное на одном компьютере, было расшифровано на другом.</span><span class="sxs-lookup"><span data-stu-id="2f066-108">Cloud computing, however, often requires that content encrypted on one computer be decrypted on another.</span></span> <span data-ttu-id="2f066-109">Таким образом, начиная с Windows 8, корпорация Майкрософт расширила концепцию использования относительно удобного API для работы с облачными сценариями.</span><span class="sxs-lookup"><span data-stu-id="2f066-109">Therefore, beginning with Windows 8, Microsoft extended the idea of using a relatively straightforward API to encompass cloud scenarios.</span></span> <span data-ttu-id="2f066-110">Этот новый API, именуемый DPAPI-NG, позволяет безопасно обмениваться секретами (ключами, паролями, материалами ключа) и сообщениями, защищая их с набором участников, которые можно использовать для снятия защиты с них на разных компьютерах после надлежащей проверки подлинности и авторизации.</span><span class="sxs-lookup"><span data-stu-id="2f066-110">This new API, called DPAPI-NG, enables you to securely share secrets (keys, passwords, key material) and messages by protecting them to a set of principals that can be used to unprotect them on different computers after proper authentication and authorization.</span></span> <span data-ttu-id="2f066-111">В настоящее время поддерживаются следующие участники:</span><span class="sxs-lookup"><span data-stu-id="2f066-111">The following principals are currently supported:</span></span>

-   <span data-ttu-id="2f066-112">Группа в лесу Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2f066-112">A group in an Active Directory forest.</span></span>
-   <span data-ttu-id="2f066-113">Учетные данные веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="2f066-113">Web credentials.</span></span>

<span data-ttu-id="2f066-114">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="2f066-114">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="2f066-115">Поставщики защиты</span><span class="sxs-lookup"><span data-stu-id="2f066-115">Protection Providers</span></span>](protection-providers.md)
-   [<span data-ttu-id="2f066-116">Дескрипторы защиты</span><span class="sxs-lookup"><span data-stu-id="2f066-116">Protection Descriptors</span></span>](protection-descriptors.md)
-   [<span data-ttu-id="2f066-117">Формат защищенных данных</span><span class="sxs-lookup"><span data-stu-id="2f066-117">Protected Data Format</span></span>](protected-data-format.md)

<span data-ttu-id="2f066-118">DPAPI-NG построен на основе криптографии следующего поколения (CNG) и включает следующие функции:</span><span class="sxs-lookup"><span data-stu-id="2f066-118">DPAPI-NG is built on top of Cryptography Next Generation (CNG) and includes the following functions:</span></span>

-   [<span data-ttu-id="2f066-119">**нкрипткреатепротектиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="2f066-119">**NCryptCreateProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
-   [<span data-ttu-id="2f066-120">**нкриптклосепротектиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="2f066-120">**NCryptCloseProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcloseprotectiondescriptor)
-   [<span data-ttu-id="2f066-121">**нкриптпротектсекрет**</span><span class="sxs-lookup"><span data-stu-id="2f066-121">**NCryptProtectSecret**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptprotectsecret)
-   [<span data-ttu-id="2f066-122">**нкрипткуерипротектиондескрипторнаме**</span><span class="sxs-lookup"><span data-stu-id="2f066-122">**NCryptQueryProtectionDescriptorName**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptqueryprotectiondescriptorname)
-   [<span data-ttu-id="2f066-123">**нкриптрегистерпротектиондескрипторнаме**</span><span class="sxs-lookup"><span data-stu-id="2f066-123">**NCryptRegisterProtectionDescriptorName**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname)
-   [<span data-ttu-id="2f066-124">**нкриптстреамклосе**</span><span class="sxs-lookup"><span data-stu-id="2f066-124">**NCryptStreamClose**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamclose)
-   [<span data-ttu-id="2f066-125">**нкриптстреамопентопротект**</span><span class="sxs-lookup"><span data-stu-id="2f066-125">**NCryptStreamOpenToProtect**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect)
-   [<span data-ttu-id="2f066-126">**нкриптстреамопентаунпротект**</span><span class="sxs-lookup"><span data-stu-id="2f066-126">**NCryptStreamOpenToUnprotect**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect)
-   [<span data-ttu-id="2f066-127">**нкриптстреамупдате**</span><span class="sxs-lookup"><span data-stu-id="2f066-127">**NCryptStreamUpdate**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamupdate)
-   [<span data-ttu-id="2f066-128">**нкриптунпротектсекрет**</span><span class="sxs-lookup"><span data-stu-id="2f066-128">**NCryptUnprotectSecret**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptunprotectsecret)

 

 
