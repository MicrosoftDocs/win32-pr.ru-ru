---
title: Установка прав для конкретных типов объектов
description: В следующей процедуре показано, как задать элемент управления доступом, который может наследоваться только конкретным классом объектов.
ms.assetid: 42712458-69c7-4fe1-bfb3-b3fb28092a56
ms.tgt_platform: multiple
keywords:
- Установка прав для типов объектов Active Directory
- объекты Active Directory, установка прав доступа
- Active Directory, использование, безопасность, установка прав для типов объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f44cfbe753e6f92787f8269eab1f4eab4c2e98
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103987308"
---
# <a name="setting-rights-to-specific-types-of-objects"></a><span data-ttu-id="d9ee0-106">Установка прав для конкретных типов объектов</span><span class="sxs-lookup"><span data-stu-id="d9ee0-106">Setting Rights to Specific Types of Objects</span></span>

<span data-ttu-id="d9ee0-107">В следующей процедуре показано, как задать элемент управления доступом, который может наследоваться только конкретным классом объектов.</span><span class="sxs-lookup"><span data-stu-id="d9ee0-107">The following procedure shows how to set an ACE that can be inherited only by a specific class of objects.</span></span>

 <span data-ttu-id="d9ee0-108">**Задание элемента управления доступом, который может наследоваться только конкретным классом объектов**</span><span class="sxs-lookup"><span data-stu-id="d9ee0-108">**To set an ACE that can be inherited only by a specific class of objects**</span></span>

1.  <span data-ttu-id="d9ee0-109">Задайте для свойства [**иадсакцессконтролентри. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) **ADS \_ AceType \_ доступ к \_ разрешенному \_ объекту** или **ADS \_ AceType \_ доступ к \_ \_ объекту**.</span><span class="sxs-lookup"><span data-stu-id="d9ee0-109">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="d9ee0-110">Задайте свойство [**иадсакцессконтролентри. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) , чтобы включить флаг AD \_ ацефлаг \_ inherit \_ ACE.</span><span class="sxs-lookup"><span data-stu-id="d9ee0-110">Set the [**IADsAccessControlEntry.AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to include the ADS\_ACEFLAG\_INHERIT\_ACE flag.</span></span>
3.  <span data-ttu-id="d9ee0-111">Присвойте свойству [**иадсакцессконтролентри. инхеритедобжекттипе**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) значение **schemaIDGUID** класса Object, который может наследовать ACE.</span><span class="sxs-lookup"><span data-stu-id="d9ee0-111">Set the [**IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the **schemaIDGUID** of the object class that can inherit the ACE.</span></span>
4.  <span data-ttu-id="d9ee0-112">Установите свойство [**иадсакцессконтролентри. flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) в **значение \_ флаг ADS \_ наследуемого \_ типа \_ объекта**.</span><span class="sxs-lookup"><span data-stu-id="d9ee0-112">Set the [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_FLAG\_INHERITED OBJECT\_TYPE\_PRESENT**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9ee0-113">Установка **ADS \_ ацефлаг \_ наследования \_ ACE** для наследуемого элемента управления доступом.</span><span class="sxs-lookup"><span data-stu-id="d9ee0-113">Set **ADS\_ACEFLAG\_INHERIT\_ACE** to cause the ACE to be inherited.</span></span> <span data-ttu-id="d9ee0-114">Кроме того, необходимо указать, что **ADS \_ ацефлаг \_ наследует \_ только \_ ACE** , если тип объекта, к которому применяется этот ACE, не соответствует типу объекта контейнера, в котором указан элемент управления доступом.</span><span class="sxs-lookup"><span data-stu-id="d9ee0-114">In addition, you must set **ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE** if the object type this ACE applies to does not match the object type of the container where the ACE is specified.</span></span> <span data-ttu-id="d9ee0-115">Если это не сделано, запись ACE также вступит в силу в контейнере и может предоставить непреднамеренное право.</span><span class="sxs-lookup"><span data-stu-id="d9ee0-115">If this is not done, the ACE will also become effective on the container and can grant unintended rights.</span></span>

 

<span data-ttu-id="d9ee0-116">Дополнительные сведения и примеры кода, которые можно использовать для задания этого типа ACE, см. в разделе [пример кода для настройки записи ACE в объекте каталога](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="d9ee0-116">For more information and code examples that can be used to set this type of ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 