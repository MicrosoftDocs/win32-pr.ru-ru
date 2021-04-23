---
description: Если для этой системной политики на уровне компьютера задано значение &\# 0034; 2&\# 0034; установщик всегда отключен для всех приложений. Если для этого параметра политики задано значение &\# 0034; 1&\# 0034;, установщик отключен для неуправляемых приложений, но по-прежнему включен для управляемых приложений.
ms.assetid: 7f941559-54c3-4802-b827-5954bd4669f8
title: дисаблемси
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf8a784f5e8090bf6ba2007091c22cf4bc070c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080923"
---
# <a name="disablemsi"></a><span data-ttu-id="1e54e-104">дисаблемси</span><span class="sxs-lookup"><span data-stu-id="1e54e-104">DisableMSI</span></span>

<span data-ttu-id="1e54e-105">Если для этой [системной политики](system-policy.md) на уровне компьютера задано значение "2", установщик всегда отключается для всех приложений.</span><span class="sxs-lookup"><span data-stu-id="1e54e-105">If the value of this per-machine [system policy](system-policy.md) is set to "2" the installer is always disabled for all applications.</span></span> <span data-ttu-id="1e54e-106">Если для этого параметра политики задано значение "1", установщик отключен для неуправляемых приложений, но по-прежнему включен для управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="1e54e-106">If this policy value is set to "1", the installer is disabled for unmanaged applications but is still enabled for managed applications.</span></span>

<span data-ttu-id="1e54e-107">В следующей таблице перечислены возможные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1e54e-107">The following table lists the possible configurations.</span></span>



| <span data-ttu-id="1e54e-108">дисаблемси</span><span class="sxs-lookup"><span data-stu-id="1e54e-108">DisableMSI</span></span> | <span data-ttu-id="1e54e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1e54e-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e54e-110">*Default*</span><span class="sxs-lookup"><span data-stu-id="1e54e-110">*Default*</span></span>  | <span data-ttu-id="1e54e-111">В Windows Server 2003, Windows Server 2003 R2, Windows Server 2008 и Windows Server 2008 R2, если значение политики равно null, отсутствует или имеет любое значение, отличное от 1 или 2, установщик Windows включена для управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="1e54e-111">On Windows Server 2003, Windows Server 2003 R2, Windows Server 2008, and Windows Server 2008 R2, if the policy value is Null, absent, or any number other than 1 or 2, the Windows Installer is enabled for managed applications.</span></span> <span data-ttu-id="1e54e-112">Установка неуправляемого приложения заблокирована.</span><span class="sxs-lookup"><span data-stu-id="1e54e-112">Unmanaged application installs are blocked.</span></span><br/> <span data-ttu-id="1e54e-113">В Windows XP, Windows Vista и Windows 7 установщик Windows включены для всех приложений.</span><span class="sxs-lookup"><span data-stu-id="1e54e-113">On Windows XP, Windows Vista, and Windows 7, the Windows Installer is enabled for all applications.</span></span> <span data-ttu-id="1e54e-114">Все операции установки разрешены.</span><span class="sxs-lookup"><span data-stu-id="1e54e-114">All install operations are allowed.</span></span><br/> |
| <span data-ttu-id="1e54e-115">0</span><span class="sxs-lookup"><span data-stu-id="1e54e-115">0</span></span>          | <span data-ttu-id="1e54e-116">Установщик Windows включена для всех приложений.</span><span class="sxs-lookup"><span data-stu-id="1e54e-116">Windows Installer is enabled for all applications.</span></span> <span data-ttu-id="1e54e-117">Все операции установки разрешены.</span><span class="sxs-lookup"><span data-stu-id="1e54e-117">All install operations are allowed.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="1e54e-118">1</span><span class="sxs-lookup"><span data-stu-id="1e54e-118">1</span></span>          | <span data-ttu-id="1e54e-119">Установщик Windows отключен для неуправляемых приложений, но по-прежнему включен для управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="1e54e-119">The Windows Installer is disabled for unmanaged applications but is still enabled for managed applications.</span></span> <span data-ttu-id="1e54e-120">Пользовательские установки без повышенных привилегий блокируются.</span><span class="sxs-lookup"><span data-stu-id="1e54e-120">Non-elevated per-user installations are blocked.</span></span> <span data-ttu-id="1e54e-121">Установки с повышенными правами на пользователя и на компьютер разрешены.</span><span class="sxs-lookup"><span data-stu-id="1e54e-121">Per-user elevated and per-machine installs are allowed.</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="1e54e-122">2</span><span class="sxs-lookup"><span data-stu-id="1e54e-122">2</span></span>          | <span data-ttu-id="1e54e-123">Установщик Windows всегда отключается для всех приложений.</span><span class="sxs-lookup"><span data-stu-id="1e54e-123">Windows Installer is always disabled for all applications.</span></span> <span data-ttu-id="1e54e-124">Установка не разрешена, включая восстановление, повторную установку или установку по требованию.</span><span class="sxs-lookup"><span data-stu-id="1e54e-124">No installs are allowed including repairs, reinstalls, or on-demand installations.</span></span>                                                                                                                                                                                                                                                                                               |



 

## <a name="registry-key"></a><span data-ttu-id="1e54e-125">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="1e54e-125">Registry Key</span></span>

<span data-ttu-id="1e54e-126">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="1e54e-126">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="1e54e-127">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1e54e-127">Data Type</span></span>

<span data-ttu-id="1e54e-128">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="1e54e-128">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e54e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="1e54e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e54e-130">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="1e54e-130">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




