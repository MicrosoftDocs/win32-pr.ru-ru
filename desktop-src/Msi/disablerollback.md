---
description: Если для этой системной политики задано значение 1, установщик не сохраняет файлы отката во время установки и отключает откат установки.
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: дисаблероллбакк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f0ce15e618880f021e04adf7d2146a97f6ed65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991268"
---
# <a name="disablerollback"></a><span data-ttu-id="450a5-103">дисаблероллбакк</span><span class="sxs-lookup"><span data-stu-id="450a5-103">DisableRollback</span></span>

<span data-ttu-id="450a5-104">Если для этой [системной политики](system-policy.md) задано значение 1, установщик не сохраняет файлы отката во время установки и отключает откат установки.</span><span class="sxs-lookup"><span data-stu-id="450a5-104">If this [system policy](system-policy.md) is set to 1, the installer does not store rollback files during installation and disables installation rollback.</span></span> <span data-ttu-id="450a5-105">По умолчанию откат включен.</span><span class="sxs-lookup"><span data-stu-id="450a5-105">By default, rollback is enabled.</span></span> <span data-ttu-id="450a5-106">Администраторам рекомендуется не использовать эту политику, если она совершенно необязательна.</span><span class="sxs-lookup"><span data-stu-id="450a5-106">Administrators are advised to not use this policy unless it is absolutely essential.</span></span> <span data-ttu-id="450a5-107">Дополнительные сведения см. в разделе [ROLLBACK Installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="450a5-107">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="450a5-108">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="450a5-108">Registry Key</span></span>

<span data-ttu-id="450a5-109">Чтобы отключить откат для установки на уровне пользователя, задайте для **дисаблероллбакк** значение 1 в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="450a5-109">To disable rollback for per-user installations, set **DisableRollback** to 1 under the following registry key:</span></span>

<span data-ttu-id="450a5-110">**HKey \_ Текущие \_ политики пользовательского** \\ **программного обеспечения** \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="450a5-110">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="450a5-111">Чтобы отключить откат для установки на компьютере, установите **дисаблероллбакк** в значение 1 в следующем разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="450a5-111">To disable rollback for per-computer installations, set **DisableRollback** to 1 under the following registry key.</span></span>

<span data-ttu-id="450a5-112">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="450a5-112">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="450a5-113">Тип данных</span><span class="sxs-lookup"><span data-stu-id="450a5-113">Data Type</span></span>

<span data-ttu-id="450a5-114">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="450a5-114">**REG\_DWORD**</span></span>

 

 



