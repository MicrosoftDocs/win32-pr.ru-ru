---
description: DACL для нового объекта
ms.assetid: ff1146d7-5229-4c75-9768-28c3fab5fcea
title: DACL для нового объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01d1ec8e92d4d56f977d4454b9a67df0a9bd489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155095"
---
# <a name="dacl-for-a-new-object"></a><span data-ttu-id="dce06-103">DACL для нового объекта</span><span class="sxs-lookup"><span data-stu-id="dce06-103">DACL for a New Object</span></span>

<span data-ttu-id="dce06-104">Система использует следующий алгоритм для создания списка DACL для большинства типов новых защищаемых объектов:</span><span class="sxs-lookup"><span data-stu-id="dce06-104">The system uses the following algorithm to build a DACL for most types of new securable objects:</span></span>

1.  <span data-ttu-id="dce06-105">DACL объекта — это список DACL из [*дескриптора безопасности*](/windows/desktop/SecGloss/s-gly) , указанного создателем объекта.</span><span class="sxs-lookup"><span data-stu-id="dce06-105">The object's DACL is the DACL from the [*security descriptor*](/windows/desktop/SecGloss/s-gly) specified by the object's creator.</span></span> <span data-ttu-id="dce06-106">Система объединяет все наследуемые ACE в указанный список DACL, если в \_ \_ контрольных битах дескриптора безопасности не установлен бит защищенного списка DACL SE.</span><span class="sxs-lookup"><span data-stu-id="dce06-106">The system merges any inheritable ACEs into the specified DACL unless the SE\_DACL\_PROTECTED bit is set in the security descriptor's control bits.</span></span>
2.  <span data-ttu-id="dce06-107">Если создатель не указал дескриптор безопасности, система создает DACL объекта из наследуемых ACE.</span><span class="sxs-lookup"><span data-stu-id="dce06-107">If the creator does not specify a security descriptor, the system builds the object's DACL from inheritable ACEs.</span></span>
3.  <span data-ttu-id="dce06-108">Если дескриптор безопасности не указан и не существует наследуемых ACE, DACL объекта является DACL по умолчанию от [*основного*](/windows/desktop/SecGloss/p-gly) [*маркера или токена олицетворения*](/windows/desktop/SecGloss/i-gly) создателя.</span><span class="sxs-lookup"><span data-stu-id="dce06-108">If no security descriptor is specified and there are no inheritable ACEs, the object's DACL is the default DACL from the [*primary*](/windows/desktop/SecGloss/p-gly) or [*impersonation token*](/windows/desktop/SecGloss/i-gly) of the creator.</span></span>
4.  <span data-ttu-id="dce06-109">Если указанный, унаследованный или DACL по умолчанию нет, система создает объект без DACL, что позволяет всем пользователям иметь полный доступ к объекту.</span><span class="sxs-lookup"><span data-stu-id="dce06-109">If there is no specified, inherited, or default DACL, the system creates the object with no DACL, which allows everyone full access to the object.</span></span>

<span data-ttu-id="dce06-110">Система использует другой алгоритм для создания списка DACL для нового объекта Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dce06-110">The system uses a different algorithm to build a DACL for a new Active Directory object.</span></span> <span data-ttu-id="dce06-111">Дополнительные сведения см. [в разделе как устанавливаются дескрипторы безопасности для новых объектов каталога](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span><span class="sxs-lookup"><span data-stu-id="dce06-111">For more information, see [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span></span>

 

 
