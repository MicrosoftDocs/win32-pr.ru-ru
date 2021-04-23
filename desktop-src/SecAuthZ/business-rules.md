---
description: Бизнес-правило позволяет приложению использовать логику во время выполнения для определения разрешений, предоставленных клиенту.
ms.assetid: 2220d533-87f5-41a6-a688-a3307f0853fa
title: Бизнес-правила
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f77d94ce623086b8850406f9bae4f412d3bbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273094"
---
# <a name="business-rules"></a><span data-ttu-id="6e528-103">Бизнес-правила</span><span class="sxs-lookup"><span data-stu-id="6e528-103">Business Rules</span></span>

<span data-ttu-id="6e528-104">Бизнес-правило позволяет приложению использовать логику во время выполнения для определения разрешений, предоставленных клиенту.</span><span class="sxs-lookup"><span data-stu-id="6e528-104">A business rule allows an application to use logic at run time to qualify permissions granted to the client.</span></span>

<span data-ttu-id="6e528-105">Бизнес-правило — это сценарий, написанный на языке программирования Visual Basic Scripting Edition (VBScript) или написанный с помощью программного обеспечения разработки Microsoft JScript, связанного с объектом [**иазтаск**](/windows/desktop/api/Azroles/nn-azroles-iaztask) .</span><span class="sxs-lookup"><span data-stu-id="6e528-105">A business rule is a script written in the Visual Basic Scripting Edition (VBScript) programming language or written using the Microsoft JScript development software that is associated with an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object.</span></span> <span data-ttu-id="6e528-106">Когда приложение проверяет доступ для операции, диспетчер авторизации сначала проверяет, имеет ли текущий клиент доступ к любым задачам, содержащим эту операцию, но не связанным с бизнес-правилами.</span><span class="sxs-lookup"><span data-stu-id="6e528-106">When an application checks access for an operation, Authorization Manager first checks if the current client has access to any tasks that contain that operation but that are not associated with business rules.</span></span> <span data-ttu-id="6e528-107">Если такой способ доступа не предоставлен, диспетчер авторизации выполняет сценарии бизнес-правил, связанные с любой задачей, содержащей эту операцию.</span><span class="sxs-lookup"><span data-stu-id="6e528-107">If access is not granted this way, Authorization Manager runs business-rule scripts associated with any task that contains the operation.</span></span>

<span data-ttu-id="6e528-108">Приложение передает сведения в сценарий бизнес-правила в виде пары массивов, представляющих имена и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="6e528-108">An application passes information to a business-rule script as a pair of arrays that represent the names and values of parameters.</span></span> <span data-ttu-id="6e528-109">Скрипт имеет доступ к этим параметрам через объект [**азбизрулеконтекст**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) , который создается при выполнении скрипта.</span><span class="sxs-lookup"><span data-stu-id="6e528-109">The script has access to these parameters through an [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) object that is created when the script runs.</span></span>

<span data-ttu-id="6e528-110">Сценарий бизнес-правила не может быть назначен задаче, содержащейся в делегированной области.</span><span class="sxs-lookup"><span data-stu-id="6e528-110">A business-rule script cannot be assigned to a task contained by a delegated scope.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e528-111">См. также</span><span class="sxs-lookup"><span data-stu-id="6e528-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e528-112">Квалификация доступа с помощью бизнес-логики в C++</span><span class="sxs-lookup"><span data-stu-id="6e528-112">Qualifying Access with Business Logic in C++</span></span>](qualifying-access-with-business-logic-in-c--.md)
</dt> </dl>

 

 



