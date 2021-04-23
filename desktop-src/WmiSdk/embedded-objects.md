---
description: Внедренный объект — это объект класса, который существует в объявлении класса или экземпляра другого класса.
ms.assetid: 11a4556b-f682-4850-aedc-793602c5745b
ms.tgt_platform: multiple
title: Внедрение объектов в класс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b94296a6869dddca7fd3df08739615a4a0c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712547"
---
# <a name="embedding-objects-in-a-class"></a><span data-ttu-id="5571a-103">Внедрение объектов в класс</span><span class="sxs-lookup"><span data-stu-id="5571a-103">Embedding Objects in a Class</span></span>

<span data-ttu-id="5571a-104">Внедренный объект — это объект класса, который существует в объявлении класса или экземпляра другого класса.</span><span class="sxs-lookup"><span data-stu-id="5571a-104">An embedded object is an object of a class that exists within a class or instance declaration of another class.</span></span> <span data-ttu-id="5571a-105">Например, класс [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) содержит внедренные [**объекты \_ доверенного лица Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) .</span><span class="sxs-lookup"><span data-stu-id="5571a-105">For example, the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class contains [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) embedded objects.</span></span> <span data-ttu-id="5571a-106">Каждый из объектов **\_ доверенного лица Win32** содержит [**объект \_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="5571a-106">Each of the **Win32\_Trustee** objects contains a [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) object.</span></span> <span data-ttu-id="5571a-107">Инструментарий WMI не ограничивает глубину, до которой класс может иметь внедренные объекты.</span><span class="sxs-lookup"><span data-stu-id="5571a-107">WMI does not limit the depth to which a class can have embedded objects.</span></span> <span data-ttu-id="5571a-108">Однако использование другой структуры, например создание класса взаимосвязей, может сделать более управляемой схему.</span><span class="sxs-lookup"><span data-stu-id="5571a-108">However, using another design, such as creating an association class, may make a more manageable schema.</span></span>

<span data-ttu-id="5571a-109">Дополнительные сведения о внедренных объектах см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="5571a-109">For more information about embedded objects, see the following topics:</span></span>

-   [<span data-ttu-id="5571a-110">Создание внедренных объектов</span><span class="sxs-lookup"><span data-stu-id="5571a-110">Creating Embedded Objects</span></span>](creating-embedded-objects.md)
-   [<span data-ttu-id="5571a-111">Запрос внедренных объектов</span><span class="sxs-lookup"><span data-stu-id="5571a-111">Querying Embedded Objects</span></span>](querying-embedded-objects.md)

## <a name="related-topics"></a><span data-ttu-id="5571a-112">См. также</span><span class="sxs-lookup"><span data-stu-id="5571a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5571a-113">Разработка классов MOF-файл (MOF)</span><span class="sxs-lookup"><span data-stu-id="5571a-113">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
