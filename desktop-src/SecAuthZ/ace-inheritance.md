---
description: Список ACL объектов может содержать элементы ACE, унаследованные от родительского контейнера.
ms.assetid: a9e5ad4d-61c6-43ed-a162-460683bcdb16
title: Наследование ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6462ed9523c94090924981db252b938f2056cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991671"
---
# <a name="ace-inheritance"></a><span data-ttu-id="06ca3-103">Наследование ACE</span><span class="sxs-lookup"><span data-stu-id="06ca3-103">ACE Inheritance</span></span>

<span data-ttu-id="06ca3-104">Список ACL объекта может содержать элементы ACE, унаследованные от родительского контейнера.</span><span class="sxs-lookup"><span data-stu-id="06ca3-104">An object's ACL can contain ACEs that it inherited from its parent container.</span></span> <span data-ttu-id="06ca3-105">Например, подраздел реестра может наследовать ACE от ключа, расположенного выше в иерархии реестра.</span><span class="sxs-lookup"><span data-stu-id="06ca3-105">For example, a registry subkey can inherit ACEs from the key above it in the registry hierarchy.</span></span> <span data-ttu-id="06ca3-106">Аналогичным образом файл в файловой системе NTFS может наследовать ACE от каталога, содержащего его.</span><span class="sxs-lookup"><span data-stu-id="06ca3-106">Likewise, a file in an NTFS file system can inherit ACEs from the directory that contains it.</span></span>

<span data-ttu-id="06ca3-107">Структура [**\_ заголовка ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) элемента ACE содержит набор флагов наследования, которые УПРАВЛЯЮТ наследованием ACE и действием ACE для объекта, к которому он присоединен.</span><span class="sxs-lookup"><span data-stu-id="06ca3-107">The [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure of an ACE contains a set of inheritance flags that control ACE inheritance and the effect of an ACE on the object to which it is attached.</span></span> <span data-ttu-id="06ca3-108">Система интерпретирует флаги наследования и другие сведения о наследовании в соответствии с [правилами наследования ACE](ace-inheritance-rules.md).</span><span class="sxs-lookup"><span data-stu-id="06ca3-108">The system interprets the inheritance flags and other inheritance information according to the [rules of ACE inheritance](ace-inheritance-rules.md).</span></span>

<span data-ttu-id="06ca3-109">Эти правила были дополнены следующими функциями.</span><span class="sxs-lookup"><span data-stu-id="06ca3-109">These rules have been enhanced with the following features:</span></span>

-   <span data-ttu-id="06ca3-110">Поддержка [автоматического распространения наследуемых ACE](automatic-propagation-of-inheritable-aces.md).</span><span class="sxs-lookup"><span data-stu-id="06ca3-110">Support for [automatic propagation of inheritable ACEs](automatic-propagation-of-inheritable-aces.md).</span></span>
-   <span data-ttu-id="06ca3-111">Флаг, который различает унаследованные ACE и ACE, которые были непосредственно применены к объекту.</span><span class="sxs-lookup"><span data-stu-id="06ca3-111">A flag that differentiates between inherited ACEs and ACEs that were directly applied to an object.</span></span>
-   <span data-ttu-id="06ca3-112">Записи ACE для конкретного объекта, которые позволяют указать тип дочернего объекта, который может наследовать ACE.</span><span class="sxs-lookup"><span data-stu-id="06ca3-112">Object-specific ACEs that allow you to specify the type of child object that can inherit the ACE.</span></span>
-   <span data-ttu-id="06ca3-113">Возможность предотвратить наследование ACE или SACL из списка управления доступом с помощью установки защищенных \_ битов ACE SE \_ или SE \_ SACL \_ в контрольных битах [*дескриптора безопасности*](/windows/desktop/SecGloss/s-gly) , за исключением \_ атрибутов системных ресурсов \_ \_ и ACE с \_ \_ \_ идентификатором политики \_ системной области.</span><span class="sxs-lookup"><span data-stu-id="06ca3-113">The ability to prevent a DACL or SACL from inheriting ACEs by setting the SE\_DACL\_PROTECTED or SE\_SACL\_PROTECTED bits in the [*security descriptor's*](/windows/desktop/SecGloss/s-gly) control bits except for SYSTEM\_RESOURCE\_ATTRIBUTE\_ACE and SYSTEM\_SCOPED\_POLICY\_ID\_ACE.</span></span>

 

 
