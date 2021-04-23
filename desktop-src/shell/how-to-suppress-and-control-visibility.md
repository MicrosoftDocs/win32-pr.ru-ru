---
description: В этом разделе рассказывается, как управлять видимостью команд.
title: Как подавлять и контролировать видимость команд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f689d8b93ce9facb62b654f3f8be62f665e001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264417"
---
# <a name="how-to-suppress-and-control-verb-visibility"></a><span data-ttu-id="a0b0b-103">Как подавлять и контролировать видимость команд</span><span class="sxs-lookup"><span data-stu-id="a0b0b-103">How to Suppress and Control Verb Visibility</span></span>

<span data-ttu-id="a0b0b-104">В этом разделе рассказывается, как управлять видимостью команд.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-104">This topic tells you how to control verb visibility.</span></span>

## <a name="instructions"></a><span data-ttu-id="a0b0b-105">Инструкции</span><span class="sxs-lookup"><span data-stu-id="a0b0b-105">Instructions</span></span>


<span data-ttu-id="a0b0b-106">Для управления видимостью команды можно использовать параметры политики Windows.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-106">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="a0b0b-107">Команды можно подавлять с помощью параметров политики, добавив подраздел **суппрессионполици** или значение **суппрессионполициекс** GUID в подраздел реестра команды.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-107">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** subkey or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="a0b0b-108">Присвойте параметру подраздела **СУППРЕССИОНПОЛИЦИ** идентификатор политики.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-108">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="a0b0b-109">Если политика включена, команда и связанная с ней запись контекстного меню подавляются.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-109">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="a0b0b-110">Возможные значения идентификатора политики см. в описании перечисления [**ограничений**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .</span><span class="sxs-lookup"><span data-stu-id="a0b0b-110">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

 

 



