---
title: Установка прав на определенные свойства объектов конкретных типов
description: Разрешения, относящиеся к свойствам, можно использовать совместно с наследованием объектов, чтобы обеспечить эффективное и подробное делегирование администрирования.
ms.assetid: d2ebbe3a-78f7-4bb5-bac0-13236031b7b1
ms.tgt_platform: multiple
keywords:
- Установка прав для конкретных свойств объектов конкретных типов Active Directory
- Active Directory, использование, безопасность и установка прав доступа к конкретным свойствам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79bfa24b574639e64fbb17c33fabee1185cc014c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487392"
---
# <a name="setting-rights-to-specific-properties-of-specific-types-of-objects"></a><span data-ttu-id="c748a-105">Установка прав на определенные свойства объектов конкретных типов</span><span class="sxs-lookup"><span data-stu-id="c748a-105">Setting Rights to Specific Properties of Specific Types of Objects</span></span>

<span data-ttu-id="c748a-106">Разрешения, относящиеся к свойствам, можно использовать совместно с наследованием объектов, чтобы обеспечить эффективное и подробное делегирование администрирования.</span><span class="sxs-lookup"><span data-stu-id="c748a-106">Property-specific permissions can be used in combination with object specific inheritance to provide the powerful and detailed delegation of administration.</span></span> <span data-ttu-id="c748a-107">Можно задать объект ACE, наследуемый от конкретного свойства, чтобы разрешить указанному пользователю или группе чтение или запись определенного атрибута в указанном классе дочерних объектов в контейнере.</span><span class="sxs-lookup"><span data-stu-id="c748a-107">You can set a property-specific object-inheritable ACE to allow a specified user or group to read and/or write a specific attribute on a specified class of child objects in a container.</span></span> <span data-ttu-id="c748a-108">Например, можно задать элемент управления доступом в подразделении (OU), чтобы группа могла считывать и записывать атрибут телефонных номеров всех объектов-пользователей в подразделении.</span><span class="sxs-lookup"><span data-stu-id="c748a-108">For example, you can set an ACE on an organizational unit (OU) to enable a group to read and write the telephone number attribute of all user objects in the OU.</span></span>

<span data-ttu-id="c748a-109">**Задание объектов ACE, наследуемых для конкретного свойства**</span><span class="sxs-lookup"><span data-stu-id="c748a-109">**To set property-specific object-inheritable ACEs**</span></span>

1.  <span data-ttu-id="c748a-110">Задайте [**иадсакцессконтролентри. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) для **ADS \_ AceType \_ доступ к \_ разрешенному \_ объекту** или **ADS \_ AceType \_ доступ к \_ \_ объекту**.</span><span class="sxs-lookup"><span data-stu-id="c748a-110">Set [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="c748a-111">Задайте для [**иадсакцессконтролентри. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) значение **schemaIDGUID** атрибута.</span><span class="sxs-lookup"><span data-stu-id="c748a-111">Set [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to the **schemaIDGUID** of the attribute.</span></span> <span data-ttu-id="c748a-112">Например, **schemaIDGUID** атрибута **telephoneNumber** имеет значение {bf967a49-0de6-11D0-a285-00aa003049e2}.</span><span class="sxs-lookup"><span data-stu-id="c748a-112">For example, the **schemaIDGUID** of the **telephoneNumber** attribute is {bf967a49-0de6-11d0-a285-00aa003049e2}.</span></span>
3.  <span data-ttu-id="c748a-113">Установите [**иадсакцессконтролентри. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) в **ADS \_ ацефлаг \_ наследовать \_ ACE**.</span><span class="sxs-lookup"><span data-stu-id="c748a-113">Set [**IADsAccessControlEntry.AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACEFLAG\_INHERIT\_ACE**.</span></span>
4.  <span data-ttu-id="c748a-114">Задайте [**иадсакцессконтролентри. инхеритедобжекттипе**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) в **schemaIDGUID** класса Object, который может наследовать ACE.</span><span class="sxs-lookup"><span data-stu-id="c748a-114">Set [**IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to the **schemaIDGUID** of the object class that can inherit the ACE.</span></span> <span data-ttu-id="c748a-115">Например, **schemaIDGUID** класса **пользователя** — {bf967aba-0de6-11D0-a285-00aa003049e2}.</span><span class="sxs-lookup"><span data-stu-id="c748a-115">For example, the **schemaIDGUID** of the **user** class is {bf967aba-0de6-11d0-a285-00aa003049e2}.</span></span>
5.  <span data-ttu-id="c748a-116">Установите параметр [**иадсакцессконтролентри. flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS \_ \_ тип объекта флаг \_ \_ Present** и **\_ \_ \_ \_ \_ имеется тип наследуемого объекта флага ADS**.</span><span class="sxs-lookup"><span data-stu-id="c748a-116">Set [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT** and **ADS\_FLAG\_INHERITED\_OBJECT\_TYPE\_PRESENT**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c748a-117">Установка ADS \_ ацефлаг \_ наследования \_ ACE для НАСЛЕДУЕМОГО элемента управления доступом.</span><span class="sxs-lookup"><span data-stu-id="c748a-117">Set ADS\_ACEFLAG\_INHERIT\_ACE to cause the ACE to be inherited.</span></span> <span data-ttu-id="c748a-118">Кроме того, Set ADS \_ ацефлаг \_ наследует \_ только \_ ACE, если тип объекта, к которому применяется этот ACE, не соответствует типу объекта контейнера, в котором указан элемент управления доступом.</span><span class="sxs-lookup"><span data-stu-id="c748a-118">In addition, set ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE if the object type this ACE applies to does not match the object type of the container where the ACE is specified.</span></span> <span data-ttu-id="c748a-119">Если это не сделано, запись ACE также вступит в силу в контейнере и может предоставить непредвиденные права.</span><span class="sxs-lookup"><span data-stu-id="c748a-119">If this is not done, the ACE will also become effective on the container and can grant unexpected rights.</span></span>

 

<span data-ttu-id="c748a-120">Дополнительные сведения и примеры кода, которые можно использовать для задания этого типа ACE, см. в разделе [пример кода для настройки записи ACE в объекте каталога](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="c748a-120">For more information and code examples that can be used to set this kind of ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 