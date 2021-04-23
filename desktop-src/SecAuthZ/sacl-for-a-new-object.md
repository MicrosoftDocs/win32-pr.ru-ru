---
description: Список SACL для нового объекта
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: Список SACL для нового объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb5bb5f276a869da3f48776bf96379edbd4af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650564"
---
# <a name="sacl-for-a-new-object"></a><span data-ttu-id="318be-103">Список SACL для нового объекта</span><span class="sxs-lookup"><span data-stu-id="318be-103">SACL for a New Object</span></span>

<span data-ttu-id="318be-104">Для создания списка SACL для большинства типов новых защищаемых объектов система использует следующий алгоритм:</span><span class="sxs-lookup"><span data-stu-id="318be-104">The system uses the following algorithm to build a SACL for most types of new securable objects:</span></span>

1.  <span data-ttu-id="318be-105">Список SACL объекта является списком SACL из [*дескриптора безопасности*](/windows/desktop/SecGloss/s-gly) , указанного создателем объекта.</span><span class="sxs-lookup"><span data-stu-id="318be-105">The object's SACL is the SACL from the [*security descriptor*](/windows/desktop/SecGloss/s-gly) specified by the object's creator.</span></span> <span data-ttu-id="318be-106">Система объединяет все наследуемые ACE в указанный список SACL, если только \_ \_ бит защищенного списка SACL не установлен в контрольных битах дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="318be-106">The system merges any inheritable ACEs into the specified SACL unless the SE\_SACL\_PROTECTED bit is set in the security descriptor's control bits.</span></span> <span data-ttu-id="318be-107">Атрибуты доступа к СИСТЕМным \_ ресурсам \_ \_ ACE и \_ \_ идентификатор политики системы \_ в пределах \_ родительского объекта будут объединены в новый объект, даже если \_ \_ установлен бит защищенного списка SACL.</span><span class="sxs-lookup"><span data-stu-id="318be-107">SYSTEM\_RESOURCE\_ATTRIBUTE\_ACEs and SYSTEM\_SCOPED\_POLICY\_ID\_ACEs from a parent object will be merged to a new object even if the SE\_SACL\_PROTECTED bit is set.</span></span>
2.  <span data-ttu-id="318be-108">Если создатель не указал дескриптор безопасности, система создает список SACL объекта из наследуемых ACE.</span><span class="sxs-lookup"><span data-stu-id="318be-108">If the creator does not specify a security descriptor, the system builds the object's SACL from inheritable ACEs.</span></span>
3.  <span data-ttu-id="318be-109">Если указанный или унаследованный список SACL отсутствует, объект не имеет списка SACL.</span><span class="sxs-lookup"><span data-stu-id="318be-109">If there is no specified or inherited SACL, the object has no SACL.</span></span>

<span data-ttu-id="318be-110">Чтобы указать список SACL для нового объекта, автор объекта должен \_ \_ включить [привилегию](privileges.md) имени безопасности SE.</span><span class="sxs-lookup"><span data-stu-id="318be-110">To specify a SACL for a new object, the object's creator must have the SE\_SECURITY\_NAME [privilege](privileges.md) enabled.</span></span> <span data-ttu-id="318be-111">Если указанный список SACL для нового объекта содержит только \_ \_ ACE атрибута системных ресурсов \_ , то \_ привилегия предоставления имени безопасности SE \_ не требуется.</span><span class="sxs-lookup"><span data-stu-id="318be-111">If the specified SACL for a new object contain only SYSTEM\_RESOURCE\_ATTRIBUTE\_ACEs, then the SE\_SECURITY\_NAME privilege is not required.</span></span> <span data-ttu-id="318be-112">Автор не нуждается в этой привилегии, если SACL объекта построен из унаследованных ACE.</span><span class="sxs-lookup"><span data-stu-id="318be-112">The creator does not need this privilege if the object's SACL is built from inherited ACEs.</span></span>

<span data-ttu-id="318be-113">Система использует другой алгоритм для создания списка SACL для нового объекта Active Directory.</span><span class="sxs-lookup"><span data-stu-id="318be-113">The system uses a different algorithm to build a SACL for a new Active Directory object.</span></span> <span data-ttu-id="318be-114">Дополнительные сведения см. [в разделе как устанавливаются дескрипторы безопасности для новых объектов каталога](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span><span class="sxs-lookup"><span data-stu-id="318be-114">For more information, see [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span></span>

 

 
