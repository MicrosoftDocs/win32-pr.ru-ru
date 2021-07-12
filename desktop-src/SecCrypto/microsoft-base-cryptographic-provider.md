---
description: Базовый поставщик служб шифрования Майкрософт — это поставщик служб шифрования (CSP), распространяемый с CryptoAPI версии 1,0 и 2,0. Это универсальный поставщик, поддерживающий цифровые подписи и шифрование данных.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Базовый поставщик служб шифрования Майкрософт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53bd4b2f7faf140e57d25b54d3161b47dcaf740
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581892"
---
# <a name="microsoft-base-cryptographic-provider"></a><span data-ttu-id="28f4e-104">Базовый поставщик служб шифрования Майкрософт</span><span class="sxs-lookup"><span data-stu-id="28f4e-104">Microsoft Base Cryptographic Provider</span></span>

<span data-ttu-id="28f4e-105">Базовый поставщик служб шифрования Майкрософт — это поставщик служб [*шифрования (CSP*](../secgloss/c-gly.md) ), распространяемый с [*CryptoAPI*](../secgloss/c-gly.md) версии 1,0 и 2,0.</span><span class="sxs-lookup"><span data-stu-id="28f4e-105">The Microsoft Base Cryptographic Provider is the initial [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) provider, and is distributed with [*CryptoAPI*](../secgloss/c-gly.md) versions 1.0 and 2.0.</span></span> <span data-ttu-id="28f4e-106">Это универсальный поставщик, поддерживающий [*цифровые подписи*](../secgloss/d-gly.md) и шифрование данных.</span><span class="sxs-lookup"><span data-stu-id="28f4e-106">It is a general-purpose provider that supports [*digital signatures*](../secgloss/d-gly.md) and data encryption.</span></span>

<span data-ttu-id="28f4e-107">Алгоритм открытого ключа RSA используется для всех операций открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="28f4e-107">The RSA public key algorithm is used for all public key operations.</span></span>

<span data-ttu-id="28f4e-108">Чтобы обеспечить обратную совместимость с более ранними версиями, Новая версия поставщика сохраняет версию 1,0 в Винкрипт. h.</span><span class="sxs-lookup"><span data-stu-id="28f4e-108">To maintain backward compatibility with earlier versions the new version of the provider retains the version 1.0 designation of the name in Wincrypt.h.</span></span> <span data-ttu-id="28f4e-109">Тем не менее версия 2,0 этого поставщика в настоящее время доставляются.</span><span class="sxs-lookup"><span data-stu-id="28f4e-109">However, version 2.0 of this provider is currently shipping.</span></span> <span data-ttu-id="28f4e-110">Чтобы определить фактическую версию используемого поставщика, вызовите [**криптжетпровпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) , указав для аргумента *двпарам* значение **PP \_ Version**.</span><span class="sxs-lookup"><span data-stu-id="28f4e-110">To determine the actual version of the provider in use, call [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with the *dwParam* argument set to **PP\_VERSION**.</span></span> <span data-ttu-id="28f4e-111">Если 0x0200 возвращается в *pbData*, то используется версия 2,0.</span><span class="sxs-lookup"><span data-stu-id="28f4e-111">If 0x0200 is returned in *pbData*, then you have version 2.0.</span></span>

|                   | <span data-ttu-id="28f4e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="28f4e-112">Value</span></span>            |
|-------------------|------------------|
| <span data-ttu-id="28f4e-113">**Тип поставщика**</span><span class="sxs-lookup"><span data-stu-id="28f4e-113">**Provider type**</span></span> | <span data-ttu-id="28f4e-114">PROV \_ RSA \_ Full</span><span class="sxs-lookup"><span data-stu-id="28f4e-114">PROV\_RSA\_FULL</span></span>  |
| <span data-ttu-id="28f4e-115">**Имя поставщика**</span><span class="sxs-lookup"><span data-stu-id="28f4e-115">**Provider name**</span></span> | <span data-ttu-id="28f4e-116">\_Prov MS DEF \_</span><span class="sxs-lookup"><span data-stu-id="28f4e-116">MS\_DEF\_PROV</span></span>    |



 

 

 
