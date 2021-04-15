---
description: Эта политика системы на компьютере отключает создание контрольных точек с установщик Windows.
ms.assetid: 706d6c85-3876-4205-b7da-b0fd709e65dd
title: лимитсистемресторечеккпоинтинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7606d266b4e9e42f6287669df9b3ab33a3ad9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682703"
---
# <a name="limitsystemrestorecheckpointing"></a><span data-ttu-id="de91a-103">лимитсистемресторечеккпоинтинг</span><span class="sxs-lookup"><span data-stu-id="de91a-103">LimitSystemRestoreCheckpointing</span></span>

<span data-ttu-id="de91a-104">Эта [Политика системы](system-policy.md) на компьютере отключает создание контрольных точек с установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="de91a-104">This per-machine [system policy](system-policy.md) turns off the creation of checkpoints by Windows Installer.</span></span>

<span data-ttu-id="de91a-105">Если задано значение 0 или отсутствует, установщик выполняет обычную контрольную точку для установки или удаления.</span><span class="sxs-lookup"><span data-stu-id="de91a-105">Set to 0 or absent, the installer does normal checkpointing for install or uninstall.</span></span> <span data-ttu-id="de91a-106">Если задано значение 1, установщик не создает контрольных точек.</span><span class="sxs-lookup"><span data-stu-id="de91a-106">Set to 1, the installer creates no checkpoints.</span></span>

<span data-ttu-id="de91a-107">Эта политика влияет только на контрольные точки, установленные установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="de91a-107">This policy affects only checkpoints set by Windows Installer.</span></span> <span data-ttu-id="de91a-108">На компьютерах под управлением Windows XP администраторам может потребоваться отключить контрольные точки в установщик Windows для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="de91a-108">On Windows XP computers, administrators may decide to disable checkpointing from within Windows Installer to improve performance.</span></span> <span data-ttu-id="de91a-109">[**Восстановление системы**](../sr/system-restore-portal.md) также создает дополнительные контрольные точки.</span><span class="sxs-lookup"><span data-stu-id="de91a-109">[**System Restore**](../sr/system-restore-portal.md) also creates additional checkpoints.</span></span> <span data-ttu-id="de91a-110">Дополнительные сведения см. в статьях [точки восстановления системы и установщик Windows](system-restore-points-and-the-windows-installer.md) и [Настройка точки восстановления из настраиваемого действия](setting-a-restore-point-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="de91a-110">For more information, see [System Restore Points and the Windows Installer](system-restore-points-and-the-windows-installer.md) and [Setting a Restore Point from a Custom Action](setting-a-restore-point-from-a-custom-action.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="de91a-111">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="de91a-111">Registry Key</span></span>

<span data-ttu-id="de91a-112">Задайте значение с именем Лимитсистемресторечеккпоинтинг в следующем разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="de91a-112">Set the value named LimitSystemRestoreCheckpointing under the following registry key.</span></span>

<span data-ttu-id="de91a-113">**\_Проводник hKey \_ \\ политики программного обеспечения на локальном компьютере, \\ \\ \\ установщик Microsoft Windows \\**</span><span class="sxs-lookup"><span data-stu-id="de91a-113">**HKEY\_LOCAL\_MACHINE\\Software\\Policies\\Microsoft\\Windows\\Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="de91a-114">Тип данных</span><span class="sxs-lookup"><span data-stu-id="de91a-114">Data Type</span></span>

<span data-ttu-id="de91a-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="de91a-115">**REG\_DWORD**</span></span>

 

 
