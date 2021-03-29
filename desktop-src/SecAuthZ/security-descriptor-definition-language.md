---
description: Описание языка определения дескрипторов безопасности (SDDL).
ms.assetid: 2b15325e-34ed-497b-ae6d-3ec3ac168232
title: Язык определения дескрипторов безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9de9d3535efe5c33ac633a9dbd295405d74b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897781"
---
# <a name="security-descriptor-definition-language"></a><span data-ttu-id="9e0a7-103">Язык определения дескрипторов безопасности</span><span class="sxs-lookup"><span data-stu-id="9e0a7-103">Security Descriptor Definition Language</span></span>

<span data-ttu-id="9e0a7-104">Язык определения дескрипторов безопасности (SDDL) определяет строковый формат, используемый функциями [**конвертсекуритидескриптортострингсекуритидескриптор**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) и [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) для описания [*дескриптора безопасности*](/windows/desktop/SecGloss/s-gly) в виде текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-104">The security descriptor definition language (SDDL) defines the string format that the [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use to describe a [*security descriptor*](/windows/desktop/SecGloss/s-gly) as a text string.</span></span> <span data-ttu-id="9e0a7-105">Язык также определяет строковые элементы для описания сведений в компонентах дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-105">The language also defines string elements for describing information in the components of a security descriptor.</span></span>

> [!Note]  
> <span data-ttu-id="9e0a7-106">[*Записи управления*](/windows/desktop/SecGloss/a-gly) условным доступом (ACE) имеют разный формат SDDL, чем другие типы ACE.</span><span class="sxs-lookup"><span data-stu-id="9e0a7-106">Conditional [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) have a different SDDL format than other ACE types.</span></span> <span data-ttu-id="9e0a7-107">Сведения об элементах ACE см. в разделе [строки ACE](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="9e0a7-107">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="9e0a7-108">Сведения об условных ACE см. в разделе [язык определения дескрипторов безопасности для условных элементов ACE](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="9e0a7-108">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9e0a7-109">См. также</span><span class="sxs-lookup"><span data-stu-id="9e0a7-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e0a7-110">Формат строки дескриптора безопасности</span><span class="sxs-lookup"><span data-stu-id="9e0a7-110">Security Descriptor String Format</span></span>](security-descriptor-string-format.md)
</dt> <dt>

[<span data-ttu-id="9e0a7-111">Язык определения дескрипторов безопасности для условных элементов ACE</span><span class="sxs-lookup"><span data-stu-id="9e0a7-111">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[<span data-ttu-id="9e0a7-112">Строки ACE</span><span class="sxs-lookup"><span data-stu-id="9e0a7-112">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="9e0a7-113">Строки идентификатора безопасности</span><span class="sxs-lookup"><span data-stu-id="9e0a7-113">SID Strings</span></span>](sid-strings.md)
</dt> <dt>

<span data-ttu-id="9e0a7-114">[\[MS-ДТИП \] : язык описания дескрипторов безопасности](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="9e0a7-114">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

 

 
