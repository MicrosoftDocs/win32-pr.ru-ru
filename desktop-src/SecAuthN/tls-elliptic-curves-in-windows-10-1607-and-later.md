---
description: Эллиптические кривые включены в Windows 10 версии 1607 и более поздних.
title: Эллиптические кривые TLS в Windows 10 версии 1607 и более поздних
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 813a7c117f5f1e3fc1c6484fc57d1c9f14cf9567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265928"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1607-and-later"></a><span data-ttu-id="f4974-103">Эллиптические кривые TLS в Windows 10 версии 1607 и более поздних</span><span class="sxs-lookup"><span data-stu-id="f4974-103">TLS Elliptic Curves in Windows 10 version 1607 and later</span></span>

<span data-ttu-id="f4974-104">Для Windows 10, 1607 и более поздних версий, следующие эллиптические кривые включены и по умолчанию используют поставщик Schannel (Майкрософт) в этом порядке приоритета:</span><span class="sxs-lookup"><span data-stu-id="f4974-104">For Windows 10, versions 1607 and later, the following elliptic curves are enabled and in this priority order by default using the Microsoft Schannel Provider:</span></span>

| <span data-ttu-id="f4974-105">Строка эллиптической кривой</span><span class="sxs-lookup"><span data-stu-id="f4974-105">Elliptic curve string</span></span> | <span data-ttu-id="f4974-106">Доступно в режиме FIPS</span><span class="sxs-lookup"><span data-stu-id="f4974-106">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="f4974-107">curve25519</span><span class="sxs-lookup"><span data-stu-id="f4974-107">curve25519</span></span> | <span data-ttu-id="f4974-108">Нет</span><span class="sxs-lookup"><span data-stu-id="f4974-108">No</span></span> |
| <span data-ttu-id="f4974-109">NistP256</span><span class="sxs-lookup"><span data-stu-id="f4974-109">NistP256</span></span> | <span data-ttu-id="f4974-110">Да</span><span class="sxs-lookup"><span data-stu-id="f4974-110">Yes</span></span> |
| <span data-ttu-id="f4974-111">NistP384</span><span class="sxs-lookup"><span data-stu-id="f4974-111">NistP384</span></span> | <span data-ttu-id="f4974-112">Да</span><span class="sxs-lookup"><span data-stu-id="f4974-112">Yes</span></span> |


<span data-ttu-id="f4974-113">Следующие эллиптические кривые поддерживаются поставщиком Schannel (Майкрософт), но не включены по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4974-113">The following elliptic curves are supported by the Microsoft Schannel Provider, but not enabled by default:</span></span>

| <span data-ttu-id="f4974-114">Строка эллиптической кривой</span><span class="sxs-lookup"><span data-stu-id="f4974-114">Elliptic curve string</span></span> | <span data-ttu-id="f4974-115">Доступно в режиме FIPS</span><span class="sxs-lookup"><span data-stu-id="f4974-115">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="f4974-116">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="f4974-116">brainpoolP256r1</span></span> | <span data-ttu-id="f4974-117">Нет</span><span class="sxs-lookup"><span data-stu-id="f4974-117">No</span></span> |
| <span data-ttu-id="f4974-118">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="f4974-118">brainpoolP384r1</span></span> | <span data-ttu-id="f4974-119">Нет</span><span class="sxs-lookup"><span data-stu-id="f4974-119">No</span></span> |
| <span data-ttu-id="f4974-120">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="f4974-120">brainpoolP512r1</span></span> | <span data-ttu-id="f4974-121">Нет</span><span class="sxs-lookup"><span data-stu-id="f4974-121">No</span></span> |
| <span data-ttu-id="f4974-122">nistP192</span><span class="sxs-lookup"><span data-stu-id="f4974-122">nistP192</span></span> | <span data-ttu-id="f4974-123">Нет</span><span class="sxs-lookup"><span data-stu-id="f4974-123">No</span></span> |
| <span data-ttu-id="f4974-124">nistP224</span><span class="sxs-lookup"><span data-stu-id="f4974-124">nistP224</span></span> | <span data-ttu-id="f4974-125">Нет</span><span class="sxs-lookup"><span data-stu-id="f4974-125">No</span></span> |
| <span data-ttu-id="f4974-126">nistP521</span><span class="sxs-lookup"><span data-stu-id="f4974-126">nistP521</span></span> | <span data-ttu-id="f4974-127">Да</span><span class="sxs-lookup"><span data-stu-id="f4974-127">Yes</span></span> |
| <span data-ttu-id="f4974-128">secP160k1</span><span class="sxs-lookup"><span data-stu-id="f4974-128">secP160k1</span></span> | <span data-ttu-id="f4974-129">Нет</span><span class="sxs-lookup"><span data-stu-id="f4974-129">No</span></span> |
| <span data-ttu-id="f4974-130">secP160r1</span><span class="sxs-lookup"><span data-stu-id="f4974-130">secP160r1</span></span> | <span data-ttu-id="f4974-131">Нет</span><span class="sxs-lookup"><span data-stu-id="f4974-131">No</span></span> |
| <span data-ttu-id="f4974-132">secP160r2</span><span class="sxs-lookup"><span data-stu-id="f4974-132">secP160r2</span></span> | <span data-ttu-id="f4974-133">Нет</span><span class="sxs-lookup"><span data-stu-id="f4974-133">No</span></span> |
| <span data-ttu-id="f4974-134">secP192k1</span><span class="sxs-lookup"><span data-stu-id="f4974-134">secP192k1</span></span> | <span data-ttu-id="f4974-135">Нет</span><span class="sxs-lookup"><span data-stu-id="f4974-135">No</span></span> |
| <span data-ttu-id="f4974-136">secP192r1</span><span class="sxs-lookup"><span data-stu-id="f4974-136">secP192r1</span></span> | <span data-ttu-id="f4974-137">Нет</span><span class="sxs-lookup"><span data-stu-id="f4974-137">No</span></span> |
| <span data-ttu-id="f4974-138">secP224k1</span><span class="sxs-lookup"><span data-stu-id="f4974-138">secP224k1</span></span> | <span data-ttu-id="f4974-139">Нет</span><span class="sxs-lookup"><span data-stu-id="f4974-139">No</span></span> |
| <span data-ttu-id="f4974-140">secP224r1</span><span class="sxs-lookup"><span data-stu-id="f4974-140">secP224r1</span></span> | <span data-ttu-id="f4974-141">Нет</span><span class="sxs-lookup"><span data-stu-id="f4974-141">No</span></span> |
| <span data-ttu-id="f4974-142">secP256k1</span><span class="sxs-lookup"><span data-stu-id="f4974-142">secP256k1</span></span> | <span data-ttu-id="f4974-143">Нет</span><span class="sxs-lookup"><span data-stu-id="f4974-143">No</span></span> |
| <span data-ttu-id="f4974-144">secP256r1</span><span class="sxs-lookup"><span data-stu-id="f4974-144">secP256r1</span></span> | <span data-ttu-id="f4974-145">Нет</span><span class="sxs-lookup"><span data-stu-id="f4974-145">No</span></span> |
| <span data-ttu-id="f4974-146">secP384r1</span><span class="sxs-lookup"><span data-stu-id="f4974-146">secP384r1</span></span> | <span data-ttu-id="f4974-147">Нет</span><span class="sxs-lookup"><span data-stu-id="f4974-147">No</span></span> |
| <span data-ttu-id="f4974-148">secP521r1</span><span class="sxs-lookup"><span data-stu-id="f4974-148">secP521r1</span></span> | <span data-ttu-id="f4974-149">Нет</span><span class="sxs-lookup"><span data-stu-id="f4974-149">No</span></span> |



## <a name="enabling-elliptic-curves"></a><span data-ttu-id="f4974-150">Включение эллиптических кривых</span><span class="sxs-lookup"><span data-stu-id="f4974-150">Enabling Elliptic Curves</span></span>

<span data-ttu-id="f4974-151">Чтобы добавить эллиптические кривые, разверните групповую политику или используйте командлеты TLS.</span><span class="sxs-lookup"><span data-stu-id="f4974-151">To add elliptic curves, either deploy a group policy or use the TLS cmdlets:</span></span>
- <span data-ttu-id="f4974-152">Чтобы использовать групповую политику, [Настройте порядок КРИВЫХ ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) в разделе конфигурация компьютера > административные шаблоны > параметры конфигурации сети > SSL с списком приоритет для всех включенных эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="f4974-152">To use group policy, [configure ECC Curve Order](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) under Computer Configuration > Administrative Templates > Network > SSL Configuration Settings with the priority list for all elliptic curves you want enabled.</span></span>

- <span data-ttu-id="f4974-153">Чтобы использовать PowerShell, ознакомьтесь с [командлетами TLS](/powershell/module/tls) , чтобы получить полный список синтаксиса и описаний командлетов TLS.</span><span class="sxs-lookup"><span data-stu-id="f4974-153">To use PowerShell, see [TLS cmdlets](/powershell/module/tls) for a complete list of TLS cmdlet syntax and descriptions.</span></span>


> [!NOTE]
> <span data-ttu-id="f4974-154">До Windows 10 строки комплекта шифров были добавлены с эллиптической кривой для определения приоритета кривой.</span><span class="sxs-lookup"><span data-stu-id="f4974-154">Prior to Windows 10, cipher suite strings were appended with the elliptic curve to determine the curve priority.</span></span> <span data-ttu-id="f4974-155">Windows 10 поддерживает настройку порядка приоритетов на основе эллиптических кривых, поэтому суффикс эллиптической кривой не является обязательным и переопределяется новым порядковым приоритетом эллиптической кривой, когда он предоставляется, чтобы разрешить организациям использовать групповую политику для настройки различных версий Windows с одинаковыми комплектами шифров.</span><span class="sxs-lookup"><span data-stu-id="f4974-155">Windows 10 supports an elliptic curve priority order setting so the elliptic curve suffix is not required and is overridden by the new elliptic curve priority order, when provided, to allow organizations to use group policy to configure different versions of Windows with the same cipher suites.</span></span>


## <a name="see-also"></a><span data-ttu-id="f4974-156">См. также:</span><span class="sxs-lookup"><span data-stu-id="f4974-156">See Also</span></span>

[<span data-ttu-id="f4974-157">Настройка порядка кривых ECC TLS</span><span class="sxs-lookup"><span data-stu-id="f4974-157">Configuring TLS ECC Curve Order</span></span>](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[<span data-ttu-id="f4974-158">Управление порядком TLS ECC</span><span class="sxs-lookup"><span data-stu-id="f4974-158">Managing TLS ECC order</span></span>](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[<span data-ttu-id="f4974-159">Управление кривыми ECC Windows с помощью групповая политика</span><span class="sxs-lookup"><span data-stu-id="f4974-159">Managing Windows ECC curves using Group Policy</span></span>](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[<span data-ttu-id="f4974-160">Командлеты TLS</span><span class="sxs-lookup"><span data-stu-id="f4974-160">TLS cmdlets</span></span>](/powershell/module/tls)
