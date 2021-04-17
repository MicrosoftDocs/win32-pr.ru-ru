---
description: Если для этой системной политики на уровне компьютера задано значение &\# 0034; 1&\# 0034;, установщик не запрашивает пользователей, когда скрипты на веб-странице используют интерфейс автоматизации установщика.
ms.assetid: 1365996d-30a2-43f9-8e1b-7704d46a11c9
title: сафефорскриптинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2907c4b021101ff936bdddf98a5cc1e32a01b991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662700"
---
# <a name="safeforscripting"></a><span data-ttu-id="f5312-103">сафефорскриптинг</span><span class="sxs-lookup"><span data-stu-id="f5312-103">SafeForScripting</span></span>

<span data-ttu-id="f5312-104">Если для этой [системной политики](system-policy.md) на уровне компьютера задано значение "1", установщик не запрашивает у пользователей, когда скрипты на веб-странице используют [интерфейс автоматизации](automation-interface.md)установщика.</span><span class="sxs-lookup"><span data-stu-id="f5312-104">If this per-machine [system policy](system-policy.md) is set to "1", the installer does not prompt users when scripts within a Web page use the installer's [automation interface](automation-interface.md).</span></span>

<span data-ttu-id="f5312-105">Перед настройкой этой политики следует принять во внимание, соответствует ли вышеуказанная строка пользователя подходящему уровню безопасности для пользователей.</span><span class="sxs-lookup"><span data-stu-id="f5312-105">Before setting this policy, you should consider whether foregoing the user prompt provides an appropriate level of security for your users.</span></span> <span data-ttu-id="f5312-106">Если эта политика не задана, то когда сценарий, размещенный в браузере, пытается установить приложение, система предупреждает пользователя и попросит его принять или отказать в установке.</span><span class="sxs-lookup"><span data-stu-id="f5312-106">If this policy is not set, when a script hosted by an Internet browser tries to install an application, the system warns the user and asks them to accept or refuse the installation.</span></span> <span data-ttu-id="f5312-107">Параметр Сафефорскриптинг подавляет это предупреждение и может разрешить установку приложений в системе без ведома пользователя.</span><span class="sxs-lookup"><span data-stu-id="f5312-107">Setting SafeForScripting suppresses this warning and may allow the installation of applications on the system without the user's knowledge.</span></span> <span data-ttu-id="f5312-108">Эта политика может быть полезна для предприятия, использующего веб-средства для распространения программ.</span><span class="sxs-lookup"><span data-stu-id="f5312-108">This policy may be useful for an enterprise that uses web-based tools to distribute programs.</span></span>

<span data-ttu-id="f5312-109">Дополнительные сведения см. в разделе [рекомендации по созданию безопасных установок](guidelines-for-authoring-secure-installations.md) и [цифровых подписей, установщик Windows](digital-signatures-and-windows-installer.md) и [скачивании установки из Интернета](downloading-an-installation-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="f5312-109">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md) and [Downloading an Installation from the Internet](downloading-an-installation-from-the-internet.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="f5312-110">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="f5312-110">Registry Key</span></span>

<span data-ttu-id="f5312-111">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="f5312-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="f5312-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f5312-112">Data Type</span></span>

<span data-ttu-id="f5312-113">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f5312-113">**REG\_DWORD**</span></span>

 

 



