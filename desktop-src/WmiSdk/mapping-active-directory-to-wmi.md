---
description: Поставщик служб каталогов дублирует классы и экземпляры из Active Directory в пространство имен протокола LDAP облегченного доступа к каталогу.
ms.assetid: 0215b614-cb10-4195-837d-bf81d523c560
ms.tgt_platform: multiple
title: Сопоставление Active Directory WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0162f722eb8a053270ac2a8e75eaed4f1cd405
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663775"
---
# <a name="mapping-active-directory-to-wmi"></a><span data-ttu-id="694ee-103">Сопоставление Active Directory WMI</span><span class="sxs-lookup"><span data-stu-id="694ee-103">Mapping Active Directory to WMI</span></span>

<span data-ttu-id="694ee-104">Поставщик служб каталогов дублирует классы и экземпляры из Active Directory в пространство имен протокола LDAP облегченного доступа к каталогу.</span><span class="sxs-lookup"><span data-stu-id="694ee-104">The Directory Services Provider mirrors classes and instances from Active Directory into the WMI Lightweight Directory Access Protocol (LDAP) namespace.</span></span> <span data-ttu-id="694ee-105">Из-за фундаментальных различий в двух средах нельзя просто переименовать Active Directory классы и экземпляры и, надеюсь, получить правильный доступ к этим классам и экземплярам в WMI.</span><span class="sxs-lookup"><span data-stu-id="694ee-105">Because of fundamental differences in the two environments, you cannot simply rename the Active Directory classes and instances and hope to properly access those classes and instances in WMI.</span></span> <span data-ttu-id="694ee-106">Вместо этого поставщик служб каталогов следует правилам именования, чтобы сохранить связи между классами Active Directory и экземплярами.</span><span class="sxs-lookup"><span data-stu-id="694ee-106">Instead, the Directory Services provider follows naming rules to preserve the relationships that exist between the Active Directory classes and instances.</span></span>

<span data-ttu-id="694ee-107">Следующие разделы содержат сведения о сопоставлении Active Directory классах и экземплярах:</span><span class="sxs-lookup"><span data-stu-id="694ee-107">The following topics provide information about mapping Active Directory classes and instances:</span></span>

-   [<span data-ttu-id="694ee-108">Сопоставление классов Active Directory</span><span class="sxs-lookup"><span data-stu-id="694ee-108">Mapping Active Directory Classes</span></span>](mapping-active-directory-classes.md)
-   [<span data-ttu-id="694ee-109">Сопоставление экземпляров Active Directory</span><span class="sxs-lookup"><span data-stu-id="694ee-109">Mapping Active Directory Instances</span></span>](mapping-active-directory-instances.md)

> [!Note]  
> <span data-ttu-id="694ee-110">Дополнительные сведения о поддержке и установке этого компонента в определенной операционной системе см. в статье [доступность компонентов WMI в операционной системе](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="694ee-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



