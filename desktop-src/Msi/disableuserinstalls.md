---
description: Это системная политика для каждого компьютера, которую можно использовать, когда администратор хочет установить только приложения для каждого компьютера.
ms.assetid: 3afa1d89-b76b-4184-b0d7-25cbf6749c7f
title: дисаблеусеринсталлс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ee8275567c62fc383c0488d6ad3ef8dfc928f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143864"
---
# <a name="disableuserinstalls"></a><span data-ttu-id="720f0-103">дисаблеусеринсталлс</span><span class="sxs-lookup"><span data-stu-id="720f0-103">DisableUserInstalls</span></span>

<span data-ttu-id="720f0-104">Это [Системная политика](system-policy.md) для каждого компьютера, которую можно использовать, когда администратор хочет установить только приложения для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="720f0-104">This is a per-machine [system policy](system-policy.md) that can be used when the administrator only wants per-machine applications installed.</span></span>

<span data-ttu-id="720f0-105">Если эта политика не задана, установщик выполняет поиск приложений в реестре в следующем порядке: управляемые приложения, зарегистрированные как пользовательские, неуправляемые приложения, зарегистрированные на уровне пользователя, и приложения, зарегистрированные как для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="720f0-105">If this policy is not set, the installer searches the registry for applications in the following order: managed applications registered as per-user, unmanaged applications registered as per-user, and finally applications registered as per-machine.</span></span>

<span data-ttu-id="720f0-106">Если для этой политики задано значение 1, установщик пропускает все приложения, зарегистрированные на уровне пользователя, и выполняет поиск только тех приложений, которые зарегистрированы для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="720f0-106">If this policy is set to 1, the installer ignores all applications registered as per-user and only searches for applications registered as per-machine.</span></span> <span data-ttu-id="720f0-107">Вызовы установщик Windows программного интерфейса приложения или системы игнорируют приложения для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="720f0-107">Calls to the Windows Installer application programming interface or system ignore per-user applications.</span></span> <span data-ttu-id="720f0-108">Попытка выполнить установку в [контексте установки](installation-context.md) на уровне пользователя приводит к тому, что установщик выводит сообщение об ошибке и останавливает установку.</span><span class="sxs-lookup"><span data-stu-id="720f0-108">An attempt to perform an installation in the per-user [installation context](installation-context.md) causes the installer to display an error message and stops the installation.</span></span> <span data-ttu-id="720f0-109">В этом случае установщик Windows также предотвращает установку отдельных пользователей с сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="720f0-109">In this case, the Windows Installer also prevents per-user installations from a terminal server.</span></span>

## <a name="registry-key"></a><span data-ttu-id="720f0-110">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="720f0-110">Registry Key</span></span>

<span data-ttu-id="720f0-111">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="720f0-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="720f0-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="720f0-112">Data Type</span></span>

<span data-ttu-id="720f0-113">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="720f0-113">**REG\_DWORD**</span></span>

 

 



