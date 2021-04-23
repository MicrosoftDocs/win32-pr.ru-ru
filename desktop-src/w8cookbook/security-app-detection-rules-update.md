---
title: Обновление правил обнаружения приложений безопасности
description: Обновление правил обнаружения приложений безопасности
ms.assetid: A272C09B-A777-4119-BAB9-F91ABC03717A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242c6f9da8d474c16fab7573e216d3157f93b014
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "104070753"
---
# <a name="security-app-detection-rules-update"></a><span data-ttu-id="88d74-103">Обновление правил обнаружения приложений безопасности</span><span class="sxs-lookup"><span data-stu-id="88d74-103">Security app detection rules update</span></span>

## <a name="platforms"></a><span data-ttu-id="88d74-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="88d74-104">Platforms</span></span>

<span data-ttu-id="88d74-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="88d74-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="88d74-106">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88d74-106">**Servers** – Windows Server 2012</span></span>  


### <a name="description"></a><span data-ttu-id="88d74-107">Описание</span><span class="sxs-lookup"><span data-stu-id="88d74-107">Description</span></span>

<span data-ttu-id="88d74-108">Приложения Магазина Windows, добавляемые в Windows 8, устанавливаются в общее расположение в разделе "Program Files" (% ProgramFiles%) называется \\ Program Files \\ виндовсаппс.</span><span class="sxs-lookup"><span data-stu-id="88d74-108">The Windows Store apps being added in Windows 8 are all being installed to a common location under “Program Files” (%programfiles%) called \\program files\\WindowsApps.</span></span>

### <a name="manifestation"></a><span data-ttu-id="88d74-109">Проявление</span><span class="sxs-lookup"><span data-stu-id="88d74-109">Manifestation</span></span>

<span data-ttu-id="88d74-110">Это может привести к конфликтам с существующими конфигурациями, а некоторые средства обнаружения вирусов и противодействия вредоносным программам видят это расположение как потенциальное расположение, которое является причиной проблемы.</span><span class="sxs-lookup"><span data-stu-id="88d74-110">This can cause collisions with existing configurations, and some antivirus/anti-malware detectors see this location as a potential location that is a cause for concern.</span></span>

### <a name="mitigation"></a><span data-ttu-id="88d74-111">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="88d74-111">Mitigation</span></span>

<span data-ttu-id="88d74-112">Текущие рекомендации:</span><span class="sxs-lookup"><span data-stu-id="88d74-112">The current recommendations are:</span></span>

-   <span data-ttu-id="88d74-113">Отказаться от \\ программных файлов \\ виндовсаппс для хранения пользовательских приложений</span><span class="sxs-lookup"><span data-stu-id="88d74-113">Move away from \\program files\\WindowsApps for storing any custom apps</span></span>
-   <span data-ttu-id="88d74-114">Антивирусные и Антивредоносные производители должны обновить свои эвристики, чтобы они не определяли это расположение как расположение вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="88d74-114">Antivirus/antimalware vendors should update their heuristics so they do not identify that location as a malware location</span></span>

 

 




