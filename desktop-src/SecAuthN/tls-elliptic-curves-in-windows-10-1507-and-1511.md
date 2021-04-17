---
description: Эллиптические кривые включены в Windows 10 версий 1507 и 1511.
title: Эллиптические кривые TLS в Windows 10 версии 1507 и 1511
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: c38d1014433e1274d8dff52be09d59761d3b1761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719634"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1507-and-1511"></a><span data-ttu-id="db93a-103">Эллиптические кривые TLS в Windows 10 версии 1507 и 1511</span><span class="sxs-lookup"><span data-stu-id="db93a-103">TLS Elliptic Curves in Windows 10 version 1507 and 1511</span></span>

<span data-ttu-id="db93a-104">Для Windows 10, 1507 и 1511, следующие эллиптические кривые включены и по умолчанию используют поставщик Microsoft Schannel в этом порядке по приоритету.</span><span class="sxs-lookup"><span data-stu-id="db93a-104">For Windows 10, versions 1507 and 1511, the following elliptic curves are enabled and in this priority order by default using the Microsoft Schannel Provider:</span></span>

| <span data-ttu-id="db93a-105">Строка эллиптической кривой</span><span class="sxs-lookup"><span data-stu-id="db93a-105">Elliptic curve string</span></span> | <span data-ttu-id="db93a-106">Доступно в режиме FIPS</span><span class="sxs-lookup"><span data-stu-id="db93a-106">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="db93a-107">NistP256</span><span class="sxs-lookup"><span data-stu-id="db93a-107">NistP256</span></span> | <span data-ttu-id="db93a-108">Да</span><span class="sxs-lookup"><span data-stu-id="db93a-108">Yes</span></span> |
| <span data-ttu-id="db93a-109">NistP384</span><span class="sxs-lookup"><span data-stu-id="db93a-109">NistP384</span></span> | <span data-ttu-id="db93a-110">Да</span><span class="sxs-lookup"><span data-stu-id="db93a-110">Yes</span></span> |


<span data-ttu-id="db93a-111">Следующие эллиптические кривые поддерживаются поставщиком Schannel (Майкрософт), но не включены по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="db93a-111">The following elliptic curves are supported by the Microsoft Schannel Provider, but not enabled by default:</span></span>

| <span data-ttu-id="db93a-112">Строка эллиптической кривой</span><span class="sxs-lookup"><span data-stu-id="db93a-112">Elliptic curve string</span></span> | <span data-ttu-id="db93a-113">Доступно в режиме FIPS</span><span class="sxs-lookup"><span data-stu-id="db93a-113">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="db93a-114">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="db93a-114">brainpoolP256r1</span></span> | <span data-ttu-id="db93a-115">Нет</span><span class="sxs-lookup"><span data-stu-id="db93a-115">No</span></span> |
| <span data-ttu-id="db93a-116">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="db93a-116">brainpoolP384r1</span></span> | <span data-ttu-id="db93a-117">Нет</span><span class="sxs-lookup"><span data-stu-id="db93a-117">No</span></span> |
| <span data-ttu-id="db93a-118">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="db93a-118">brainpoolP512r1</span></span> | <span data-ttu-id="db93a-119">Нет</span><span class="sxs-lookup"><span data-stu-id="db93a-119">No</span></span> |
| <span data-ttu-id="db93a-120">nistP192</span><span class="sxs-lookup"><span data-stu-id="db93a-120">nistP192</span></span> | <span data-ttu-id="db93a-121">Нет</span><span class="sxs-lookup"><span data-stu-id="db93a-121">No</span></span> |
| <span data-ttu-id="db93a-122">nistP224</span><span class="sxs-lookup"><span data-stu-id="db93a-122">nistP224</span></span> | <span data-ttu-id="db93a-123">Нет</span><span class="sxs-lookup"><span data-stu-id="db93a-123">No</span></span> |
| <span data-ttu-id="db93a-124">nistP521</span><span class="sxs-lookup"><span data-stu-id="db93a-124">nistP521</span></span> | <span data-ttu-id="db93a-125">Да</span><span class="sxs-lookup"><span data-stu-id="db93a-125">Yes</span></span> |
| <span data-ttu-id="db93a-126">secP160k1</span><span class="sxs-lookup"><span data-stu-id="db93a-126">secP160k1</span></span> | <span data-ttu-id="db93a-127">Нет</span><span class="sxs-lookup"><span data-stu-id="db93a-127">No</span></span> |
| <span data-ttu-id="db93a-128">secP160r1</span><span class="sxs-lookup"><span data-stu-id="db93a-128">secP160r1</span></span> | <span data-ttu-id="db93a-129">Нет</span><span class="sxs-lookup"><span data-stu-id="db93a-129">No</span></span> |
| <span data-ttu-id="db93a-130">secP160r2</span><span class="sxs-lookup"><span data-stu-id="db93a-130">secP160r2</span></span> | <span data-ttu-id="db93a-131">Нет</span><span class="sxs-lookup"><span data-stu-id="db93a-131">No</span></span> |
| <span data-ttu-id="db93a-132">secP192k1</span><span class="sxs-lookup"><span data-stu-id="db93a-132">secP192k1</span></span> | <span data-ttu-id="db93a-133">Нет</span><span class="sxs-lookup"><span data-stu-id="db93a-133">No</span></span> |
| <span data-ttu-id="db93a-134">secP192r1</span><span class="sxs-lookup"><span data-stu-id="db93a-134">secP192r1</span></span> | <span data-ttu-id="db93a-135">Нет</span><span class="sxs-lookup"><span data-stu-id="db93a-135">No</span></span> |
| <span data-ttu-id="db93a-136">secP224k1</span><span class="sxs-lookup"><span data-stu-id="db93a-136">secP224k1</span></span> | <span data-ttu-id="db93a-137">Нет</span><span class="sxs-lookup"><span data-stu-id="db93a-137">No</span></span> |
| <span data-ttu-id="db93a-138">secP224r1</span><span class="sxs-lookup"><span data-stu-id="db93a-138">secP224r1</span></span> | <span data-ttu-id="db93a-139">Нет</span><span class="sxs-lookup"><span data-stu-id="db93a-139">No</span></span> |
| <span data-ttu-id="db93a-140">secP256k1</span><span class="sxs-lookup"><span data-stu-id="db93a-140">secP256k1</span></span> | <span data-ttu-id="db93a-141">Нет</span><span class="sxs-lookup"><span data-stu-id="db93a-141">No</span></span> |
| <span data-ttu-id="db93a-142">secP256r1</span><span class="sxs-lookup"><span data-stu-id="db93a-142">secP256r1</span></span> | <span data-ttu-id="db93a-143">Нет</span><span class="sxs-lookup"><span data-stu-id="db93a-143">No</span></span> |
| <span data-ttu-id="db93a-144">secP384r1</span><span class="sxs-lookup"><span data-stu-id="db93a-144">secP384r1</span></span> | <span data-ttu-id="db93a-145">Нет</span><span class="sxs-lookup"><span data-stu-id="db93a-145">No</span></span> |
| <span data-ttu-id="db93a-146">secP521r1</span><span class="sxs-lookup"><span data-stu-id="db93a-146">secP521r1</span></span> | <span data-ttu-id="db93a-147">Нет</span><span class="sxs-lookup"><span data-stu-id="db93a-147">No</span></span> |

## <a name="enabling-elliptic-curves"></a><span data-ttu-id="db93a-148">Включение эллиптических кривых</span><span class="sxs-lookup"><span data-stu-id="db93a-148">Enabling Elliptic Curves</span></span>

<span data-ttu-id="db93a-149">Чтобы добавить эллиптические кривые, разверните групповую политику или используйте командлеты TLS.</span><span class="sxs-lookup"><span data-stu-id="db93a-149">To add elliptic curves, either deploy a group policy or use the TLS cmdlets:</span></span>
- <span data-ttu-id="db93a-150">Чтобы использовать групповую политику, [Настройте порядок КРИВЫХ ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) в разделе конфигурация компьютера > административные шаблоны > параметры конфигурации сети > SSL с списком приоритет для всех включенных эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="db93a-150">To use group policy, [configure ECC Curve Order](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) under Computer Configuration > Administrative Templates > Network > SSL Configuration Settings with the priority list for all elliptic curves you want enabled.</span></span>

- <span data-ttu-id="db93a-151">Чтобы использовать PowerShell, ознакомьтесь с [командлетами TLS](/powershell/module/tls) , чтобы получить полный список синтаксиса и описаний командлетов TLS.</span><span class="sxs-lookup"><span data-stu-id="db93a-151">To use PowerShell, see [TLS cmdlets](/powershell/module/tls) for a complete list of TLS cmdlet syntax and descriptions.</span></span>


> [!NOTE]
> <span data-ttu-id="db93a-152">До Windows 10 строки комплекта шифров были добавлены с эллиптической кривой для определения приоритета кривой.</span><span class="sxs-lookup"><span data-stu-id="db93a-152">Prior to Windows 10, cipher suite strings were appended with the elliptic curve to determine the curve priority.</span></span> <span data-ttu-id="db93a-153">Windows 10 поддерживает настройку порядка приоритетов на основе эллиптических кривых, поэтому суффикс эллиптической кривой не является обязательным и переопределяется новым порядковым приоритетом эллиптической кривой, когда он предоставляется, чтобы разрешить организациям использовать групповую политику для настройки различных версий Windows с одинаковыми комплектами шифров.</span><span class="sxs-lookup"><span data-stu-id="db93a-153">Windows 10 supports an elliptic curve priority order setting so the elliptic curve suffix is not required and is overridden by the new elliptic curve priority order, when provided, to allow organizations to use group policy to configure different versions of Windows with the same cipher suites.</span></span>


## <a name="see-also"></a><span data-ttu-id="db93a-154">См. также:</span><span class="sxs-lookup"><span data-stu-id="db93a-154">See Also</span></span>

[<span data-ttu-id="db93a-155">Настройка порядка кривых ECC TLS</span><span class="sxs-lookup"><span data-stu-id="db93a-155">Configuring TLS ECC Curve Order</span></span>](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[<span data-ttu-id="db93a-156">Управление порядком TLS ECC</span><span class="sxs-lookup"><span data-stu-id="db93a-156">Managing TLS ECC order</span></span>](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[<span data-ttu-id="db93a-157">Управление кривыми ECC Windows с помощью групповая политика</span><span class="sxs-lookup"><span data-stu-id="db93a-157">Managing Windows ECC curves using Group Policy</span></span>](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[<span data-ttu-id="db93a-158">Командлеты TLS</span><span class="sxs-lookup"><span data-stu-id="db93a-158">TLS cmdlets</span></span>](/powershell/module/tls)
