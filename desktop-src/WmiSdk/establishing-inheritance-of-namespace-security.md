---
description: Можно контролировать, наследует ли Дочернее пространство имен дескриптор безопасности родительского пространства имен.
ms.assetid: d4fbd5af-69e2-4c60-907a-cb2a1506b7c9
ms.tgt_platform: multiple
title: Установка наследования безопасности пространства имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e242299b78ede3ff49679305a97823bc022358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702999"
---
# <a name="establishing-inheritance-of-namespace-security"></a><span data-ttu-id="003df-103">Установка наследования безопасности пространства имен</span><span class="sxs-lookup"><span data-stu-id="003df-103">Establishing Inheritance of Namespace Security</span></span>

<span data-ttu-id="003df-104">Можно контролировать, наследует ли Дочернее пространство имен дескриптор безопасности родительского пространства имен.</span><span class="sxs-lookup"><span data-stu-id="003df-104">You can control whether a child namespace inherits the security descriptor of the parent namespace.</span></span>

<span data-ttu-id="003df-105">Пространства имен WMI имеют дескрипторы безопасности, которые управляют доступом к пространству имен и данным пространства имен.</span><span class="sxs-lookup"><span data-stu-id="003df-105">WMI namespaces have security descriptors that control who can access the namespace and the data of the namespace.</span></span> <span data-ttu-id="003df-106">Каждый дескриптор безопасности имеет избирательный список управления доступом (DACL) и список управления доступом (SACL) безопасности.</span><span class="sxs-lookup"><span data-stu-id="003df-106">Each security descriptor has a discretionary access control list (DACL) and a security access control list (SACL).</span></span> <span data-ttu-id="003df-107">Эти списки содержат записи контроля доступа (ACE).</span><span class="sxs-lookup"><span data-stu-id="003df-107">These lists contain access control entries (ACE).</span></span>

<span data-ttu-id="003df-108">В зависимости от установленных [**констант флага Ace пространства имен**](namespace-ace-flag-constants.md) разрешения, применяемые к пространству имен, могут наследоваться всеми дочерними пространствами этого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="003df-108">Depending on the [**Namespace ACE Flag Constants**](namespace-ace-flag-constants.md) that are set, permissions that are applied to a namespace may be inherited by all the child namespaces of that namespace.</span></span> <span data-ttu-id="003df-109">Дочернее пространство имен наследует дескриптор безопасности своего родительского пространства имен при создании дочернего пространства имен, если флаг **\_ наследования \_ ACE** находится в дескрипторе безопасности родительского пространства имен.</span><span class="sxs-lookup"><span data-stu-id="003df-109">A child namespace inherits the security descriptor of its parent namespace when the child namespace is created if the **CONTAINER\_INHERIT\_ACE** flag is in the parent namespace security descriptor.</span></span> <span data-ttu-id="003df-110">Если **контейнер \_ наследует \_ ACE \| не \_ пропогате \_ inherit \_ ACE** , то только Дочернее пространство имен наследует дескриптор безопасности, а не внучатый пространства имен.</span><span class="sxs-lookup"><span data-stu-id="003df-110">If **CONTAINER\_INHERIT\_ACE\|NO\_PROPOGATE\_INHERIT\_ACE** is set, then only the child namespace inherits the security descriptor, not grandchild namespaces.</span></span> <span data-ttu-id="003df-111">Дочерние пространства имен могут переопределять разрешения безопасности своего родителя, вызывая методы класса [**\_ \_ системсекурити**](--systemsecurity.md) для записи нового дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="003df-111">Child namespaces can override the security permissions of their parent by calling methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class to write a new security descriptor.</span></span> <span data-ttu-id="003df-112">Невозможно изменить параметры безопасности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="003df-112">The default security settings cannot be changed.</span></span> <span data-ttu-id="003df-113">Дополнительные сведения см. в разделе [Настройка дескрипторов безопасности намепаце](setting-namespace-security-descriptors.md). Дополнительные сведения об DACL см. в разделе [списки управления доступом (ACL)](/windows/desktop/SecAuthZ/access-control-lists) и [**константы типа Ace пространства имен**](namespace-ace-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="003df-113">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).For more information about DACLs, see [Access Control Lists (ACL)](/windows/desktop/SecAuthZ/access-control-lists) and [**Namespace ACE Type Constants**](namespace-ace-type-constants.md).</span></span>

<span data-ttu-id="003df-114">Обратите внимание, что разрешения по умолчанию нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="003df-114">Note that the default permissions cannot be changed.</span></span> <span data-ttu-id="003df-115">Кроме того, установка флага **\_ \_ защищенного списка DACL SE** при настройке дескриптора безопасности (SD) не используется для добавления специализированного SD в Дочернее пространство имен.</span><span class="sxs-lookup"><span data-stu-id="003df-115">Furthermore, setting the **SE\_DACL\_PROTECTED** flag while setting the security descriptor (SD) is not used to add a specialized SD to a child namespace.</span></span> <span data-ttu-id="003df-116">Чтобы переопределить унаследованный SD, просто задайте новый.</span><span class="sxs-lookup"><span data-stu-id="003df-116">To override an inherited SD, simply set a new one.</span></span> <span data-ttu-id="003df-117">Чтобы унаследовать этот SD к дочернему пространству имен, передайте контейнеру значение флага **\_ \_ ACE** в дескрипторе безопасности пространства имен.</span><span class="sxs-lookup"><span data-stu-id="003df-117">To inherit that SD to a child namespace, pass the **CONTAINER\_INHERIT\_ACE** flag in the namespace security descriptor.</span></span> <span data-ttu-id="003df-118">Чтобы унаследовать только дочерний элемент, а не потомков, передайте `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`</span><span class="sxs-lookup"><span data-stu-id="003df-118">To inherit to just the child, and not the descendants, pass `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`</span></span>

<span data-ttu-id="003df-119">.</span><span class="sxs-lookup"><span data-stu-id="003df-119">.</span></span>

## <a name="related-topics"></a><span data-ttu-id="003df-120">См. также</span><span class="sxs-lookup"><span data-stu-id="003df-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="003df-121">Настройка дескрипторов безопасности Намепаце</span><span class="sxs-lookup"><span data-stu-id="003df-121">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="003df-122">**\_\_системсекурити**</span><span class="sxs-lookup"><span data-stu-id="003df-122">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 
