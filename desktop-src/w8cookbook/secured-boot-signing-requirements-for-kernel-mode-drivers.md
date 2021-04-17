---
title: Требования к подписывания функций безопасной загрузки для драйверов режима ядра
description: Требования к подписывания функций безопасной загрузки для драйверов режима ядра
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a63a8b1fca1677aa125bac96dfec290dcd736b5
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "105700958"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a><span data-ttu-id="22e1d-103">Требования к подписывания функций безопасной загрузки для драйверов режима ядра</span><span class="sxs-lookup"><span data-stu-id="22e1d-103">Secure boot feature signing requirements for kernel-mode drivers</span></span>

## <a name="platforms"></a><span data-ttu-id="22e1d-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="22e1d-104">Platforms</span></span>

<span data-ttu-id="22e1d-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="22e1d-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="22e1d-106">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="22e1d-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="22e1d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="22e1d-107">Description</span></span>

<span data-ttu-id="22e1d-108">В Windows 8 и Windows Server 2012, включая WinPE, ядро заблокировано для предотвращения вредоносных программ, появившихся с помощью загрузки или корневых наборов, от обхода требований безопасности операционной системы Windows для подписанных драйверов.</span><span class="sxs-lookup"><span data-stu-id="22e1d-108">In Windows 8 and Windows Server 2012, including WinPE, the kernel has been locked down to prevent malware introduced by boot or root kits from circumventing Windows operating system security requirements for signed drivers.</span></span>

<span data-ttu-id="22e1d-109">Это изменение влияет на все драйверы режима ядра для устройств, поддерживающих безопасную загрузку по интерфейсу UEFI. Для сертификации Windows 8 для клиентских компьютеров требуется безопасная Загрузка UEFI, а для серверов — необязательно.</span><span class="sxs-lookup"><span data-stu-id="22e1d-109">This change affects all kernel-mode drivers for devices that support unified extensible firmware interface (UEFI) Secure Boot; UEFI Secure Boot is required for Windows 8 certification for client machines, and optional for servers.</span></span> <span data-ttu-id="22e1d-110">Он не влияет на драйверы пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="22e1d-110">It does not affect user-mode drivers.</span></span>

<span data-ttu-id="22e1d-111">Стандартная разработка для драйверов в режиме ядра включает в себя использование отладки в режиме ядра или параметра данных конфигурации загрузки (BCD) <testsigning> .</span><span class="sxs-lookup"><span data-stu-id="22e1d-111">Standard development for kernel-mode drivers involves either the use of kernel mode debugging or the boot configuration data (BCD) <testsigning> setting.</span></span> <span data-ttu-id="22e1d-112">Оба эти параметра отключены, если включена безопасная загрузка.</span><span class="sxs-lookup"><span data-stu-id="22e1d-112">Both of these are disabled when Secured Boot is on.</span></span>

## <a name="manifestation"></a><span data-ttu-id="22e1d-113">Проявление</span><span class="sxs-lookup"><span data-stu-id="22e1d-113">Manifestation</span></span>

<span data-ttu-id="22e1d-114">Драйверы режима ядра не будут выполняться, если они не подписаны должным образом доверенным центром сертификации (ЦС).</span><span class="sxs-lookup"><span data-stu-id="22e1d-114">Kernel-mode drivers will not run if they are not properly signed by a trusted certification authority (CA).</span></span> <span data-ttu-id="22e1d-115">Операционная система не позволит запускать недоверенные драйверы и стандартные механизмы, такие как отладка ядра и тестсигнинг, не будут разрешены.</span><span class="sxs-lookup"><span data-stu-id="22e1d-115">The operating system will not allow untrusted drivers to run and standard mechanisms like kernel debugging and testsigning will not be permitted.</span></span>

## <a name="mitigation"></a><span data-ttu-id="22e1d-116">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="22e1d-116">Mitigation</span></span>

<span data-ttu-id="22e1d-117">Для тестирования драйверов необходимо отключить безопасную загрузку в BIOS, а также удовлетворить другие требования к подписи тестирования (см. ниже).</span><span class="sxs-lookup"><span data-stu-id="22e1d-117">To test drivers, you must disable Secure Boot in BIOS as well as meet the other test-signing requirements (see below).</span></span>

<span data-ttu-id="22e1d-118">При более широком распространении драйверов они должны быть правильно подписаны доверенным центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="22e1d-118">When distributing drivers more widely they must be properly signed by a trusted CA.</span></span>

## <a name="resources"></a><span data-ttu-id="22e1d-119">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="22e1d-119">Resources</span></span>

-   <span data-ttu-id="22e1d-120">[Подписание драйверов](/previous-versions/windows/hardware/design/dn653563(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="22e1d-120">[Signing Drivers](/previous-versions/windows/hardware/design/dn653563(v=vs.85))</span></span>

 

 