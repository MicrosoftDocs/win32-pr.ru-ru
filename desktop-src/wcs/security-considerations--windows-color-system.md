---
title: Цветовая система Windows — вопросы безопасности
description: Цветовая система Windows — вопросы безопасности
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
keywords:
- Цветовая система Windows (WCS), безопасность
- WCS (цветовая система Windows), безопасность
- Управление цветом изображений, безопасность
- Управление цветом, безопасность
- безопасность для цветовой системы Windows (WCS)
- Модуль управления цветом (CMM)
- CMM (модуль управления цветом)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef47ada0c233900f6e56a1e438d411a2ae84abd3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105720062"
---
# <a name="security-considerations-windows-color-system"></a><span data-ttu-id="9e50c-110">Вопросы безопасности: цветовая система Windows</span><span class="sxs-lookup"><span data-stu-id="9e50c-110">Security Considerations: Windows Color System</span></span>

<span data-ttu-id="9e50c-111">В этом документе содержатся сведения о вопросах безопасности, связанных с управлением цветом изображений.</span><span class="sxs-lookup"><span data-stu-id="9e50c-111">This document provides information about security considerations related to image color management.</span></span> <span data-ttu-id="9e50c-112">Этот документ не предоставляет все, что нужно знать о проблемах безопасности. вместо этого используйте его в качестве отправной точки и справочной информации для этой области технологий.</span><span class="sxs-lookup"><span data-stu-id="9e50c-112">This document doesn't provide all you need to know about security issues—instead, use it as a starting point and reference for this technology area.</span></span>

## <a name="non-microsoft-cmms-can-run-in-system-context"></a><span data-ttu-id="9e50c-113">Сторонние Кммс могут работать в контексте системы</span><span class="sxs-lookup"><span data-stu-id="9e50c-113">Non-Microsoft CMMs can run in system context</span></span>

<span data-ttu-id="9e50c-114">Модули управления цветом (не Майкрософт) (Кммс) должны рассматриваться как драйверы принтеров сторонних производителей, так как они могут работать в контексте системы для операций печати.</span><span class="sxs-lookup"><span data-stu-id="9e50c-114">Non-Microsoft Color Management Modules (CMMs) should be treated like non-Microsoft printer drivers because they have the potential to run in a system context for printing operations.</span></span>
