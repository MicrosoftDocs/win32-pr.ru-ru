---
description: В 64-разрядных ОС Windows части записей реестра хранятся отдельно для 32-разрядных приложений и 64-разрядных приложений и сопоставлены с отдельными логическими представлениями реестра с помощью средства перенаправления реестра и отражения реестра, так как в 64-разрядной версии приложения могут использоваться разные ключи и значения реестра, чем в 32-разрядной версии. Также существуют общие разделы реестра, которые не перенаправлены или не отражаются.
ms.assetid: 08dc034c-15ce-41d9-8e74-a49b61ad40a6
title: 32-разрядные и 64-битные данные приложения в реестре
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc82dfbf9b22cf90866e13109aeea2bcdb10e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910015"
---
# <a name="32-bit-and-64-bit-application-data-in-the-registry"></a><span data-ttu-id="f074a-104">32-разрядные и 64-битные данные приложения в реестре</span><span class="sxs-lookup"><span data-stu-id="f074a-104">32-bit and 64-bit Application Data in the Registry</span></span>

<span data-ttu-id="f074a-105">В 64-разрядных ОС Windows части записей реестра хранятся отдельно для 32-разрядных приложений и 64-разрядных приложений и сопоставлены с отдельными логическими представлениями реестра с помощью средства [перенаправления реестра](/windows/desktop/WinProg64/registry-redirector) и [отражения реестра](/windows/desktop/WinProg64/registry-reflection), так как в 64-разрядной версии приложения могут использоваться разные ключи и значения реестра, чем в 32-разрядной версии.</span><span class="sxs-lookup"><span data-stu-id="f074a-105">On 64-bit Windows, portions of the registry entries are stored separately for 32-bit application and 64-bit applications and mapped into separate logical registry views using the [registry redirector](/windows/desktop/WinProg64/registry-redirector) and [registry reflection](/windows/desktop/WinProg64/registry-reflection), because the 64-bit version of an application may use different registry keys and values than the 32-bit version.</span></span> <span data-ttu-id="f074a-106">Также существуют [общие разделы реестра](/windows/desktop/WinProg64/shared-registry-keys) , которые не перенаправлены или не отражаются.</span><span class="sxs-lookup"><span data-stu-id="f074a-106">There are also [shared registry keys](/windows/desktop/WinProg64/shared-registry-keys) that are not redirected or reflected.</span></span>

<span data-ttu-id="f074a-107">Родительским элементом для каждого 64-разрядного узла реестра является Image-Specificный узел или.</span><span class="sxs-lookup"><span data-stu-id="f074a-107">The parent of each 64-bit registry node is the Image-Specific Node or ISN.</span></span> <span data-ttu-id="f074a-108">Перенаправитель реестра прозрачно направляет доступ к реестру приложения соответствующему подузлу.</span><span class="sxs-lookup"><span data-stu-id="f074a-108">The registry redirector transparently directs an application's registry access to the appropriate ISN subnode.</span></span> <span data-ttu-id="f074a-109">Подузлы перенаправления в дереве реестра создаются автоматически компонентом WOW64 с именем **WOW6432Node**.</span><span class="sxs-lookup"><span data-stu-id="f074a-109">Redirection subnodes in the registry tree are created automatically by the WOW64 component using the name **Wow6432Node**.</span></span> <span data-ttu-id="f074a-110">Поэтому важно не присвоить имя ни одному разделу реестра, созданному в **WOW6432Node**.</span><span class="sxs-lookup"><span data-stu-id="f074a-110">As a result, it is essential not to name any registry key you create **Wow6432Node**.</span></span>

<span data-ttu-id="f074a-111">\_ \_ Флаги WOW64 64KEY и key \_ WOW64 \_ 32KEY обеспечивают явный доступ к 64-разрядному представлению реестра и 32-разрядному представлению соответственно.</span><span class="sxs-lookup"><span data-stu-id="f074a-111">The KEY\_WOW64\_64KEY and KEY\_WOW64\_32KEY flags enable explicit access to the 64-bit registry view and the 32-bit view, respectively.</span></span> <span data-ttu-id="f074a-112">Дополнительные сведения см. [в разделе доступ к альтернативному представлению реестра](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).</span><span class="sxs-lookup"><span data-stu-id="f074a-112">For more information, see [Accessing an Alternate Registry View](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).</span></span>

<span data-ttu-id="f074a-113">Чтобы отключить и включить отражение реестра для определенного ключа, используйте функции [**регдисаблерефлектионкэй**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) и [**реженаблерефлектионкэй**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) .</span><span class="sxs-lookup"><span data-stu-id="f074a-113">To disable and enable registry reflection for a particular key, use the [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) and [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) functions.</span></span> <span data-ttu-id="f074a-114">Приложения должны отключать отражение только для разделов реестра, которые они создают, и не пытаться отключить отражение для стандартных ключей, таких как **hKey \_ локальный \_ компьютер** или **hKey \_ текущий \_ пользователь**.</span><span class="sxs-lookup"><span data-stu-id="f074a-114">Applications should disable reflection only for the registry keys that they create and not attempt to disable reflection for the predefined keys such as **HKEY\_LOCAL\_MACHINE** or **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="f074a-115">Чтобы определить, какие ключи находятся в списке отражения, используйте функцию [**регкуерирефлектионкэй**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) .</span><span class="sxs-lookup"><span data-stu-id="f074a-115">To determine which keys are on the reflection list, use the [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f074a-116">См. также</span><span class="sxs-lookup"><span data-stu-id="f074a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f074a-117">Перенаправитель реестра</span><span class="sxs-lookup"><span data-stu-id="f074a-117">registry redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)
</dt> <dt>

[<span data-ttu-id="f074a-118">отражение реестра</span><span class="sxs-lookup"><span data-stu-id="f074a-118">registry reflection</span></span>](/windows/desktop/WinProg64/registry-reflection)
</dt> </dl>

 

 
