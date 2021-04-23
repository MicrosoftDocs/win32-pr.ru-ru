---
title: Установка разрешений для определенного свойства
description: Разрешения можно задать для применения к определенному свойству объекта.
ms.assetid: 7bafba5a-a437-4777-98a0-f478b738a8ca
ms.tgt_platform: multiple
keywords:
- Установка разрешений для конкретного свойства Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99dbfc3dc682103166b41957a3f52206d84fe671
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069743"
---
# <a name="setting-permissions-to-a-specific-property"></a><span data-ttu-id="7cd84-104">Установка разрешений для определенного свойства</span><span class="sxs-lookup"><span data-stu-id="7cd84-104">Setting Permissions to a Specific Property</span></span>

<span data-ttu-id="7cd84-105">Разрешения можно задать для применения к определенному свойству объекта.</span><span class="sxs-lookup"><span data-stu-id="7cd84-105">Permissions can be set to apply to a specific property of an object.</span></span>

<span data-ttu-id="7cd84-106">**Установка разрешений, относящихся к определенному свойству объекта**</span><span class="sxs-lookup"><span data-stu-id="7cd84-106">**To set permissions that apply to a specific property of an object**</span></span>

1.  <span data-ttu-id="7cd84-107">Задайте для свойства [**иадсакцессконтролентри. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) значение **ADS \_ справа \_ DS \_ Read \_ prop** и/или **ADSS \_ right \_ DS- \_ \_ prop**.</span><span class="sxs-lookup"><span data-stu-id="7cd84-107">Set the [**IADsAccessControlEntry.AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_RIGHT\_DS\_READ\_PROP** and/or **ADS\_RIGHT\_DS\_WRITE\_PROP**.</span></span>
2.  <span data-ttu-id="7cd84-108">Задайте для свойства [**иадсакцессконтролентри. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) **ADS \_ AceType \_ доступ к \_ разрешенному \_ объекту** или **ADS \_ AceType \_ доступ к \_ \_ объекту**.</span><span class="sxs-lookup"><span data-stu-id="7cd84-108">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
3.  <span data-ttu-id="7cd84-109">Присвойте свойству [**иадсакцессконтролентри. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) значение **schemaIDGUID** свойства.</span><span class="sxs-lookup"><span data-stu-id="7cd84-109">Set the [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the **schemaIDGUID** of the property.</span></span> <span data-ttu-id="7cd84-110">Это **schemaIDGUID** объекта **attributeSchema** , определяющего свойство в схеме.</span><span class="sxs-lookup"><span data-stu-id="7cd84-110">This is the **schemaIDGUID** of the **attributeSchema** object that defines the property in the schema.</span></span> <span data-ttu-id="7cd84-111">Идентификатор GUID должен быть указан в виде строки формы, созданной функцией [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) в библиотеке COM.</span><span class="sxs-lookup"><span data-stu-id="7cd84-111">The GUID must be specified as a string of the form produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function in the COM library.</span></span>
4.  <span data-ttu-id="7cd84-112">Присвойте параметру [**иадсакцессконтролентри. flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) значение **\_ \_ \_ тип \_ объекта флага ADS**.</span><span class="sxs-lookup"><span data-stu-id="7cd84-112">Set [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**.</span></span>

<span data-ttu-id="7cd84-113">Дополнительные сведения о **schemaIDGUID** предопределенного атрибута см. в разделе [Справочник по службам домен Active Directory](active-directory-domain-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="7cd84-113">For more information about the **schemaIDGUID** of a predefined attribute, see [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

<span data-ttu-id="7cd84-114">Дополнительные сведения и пример кода, который можно использовать для получения schemaIDGUID, см. в разделе [чтение объектов attributeSchema и classSchema](reading-attributeschema-and-classschema-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7cd84-114">For more information and a code example that can be used to retrieve a schemaIDGUID, see [Reading attributeSchema and classSchema Objects](reading-attributeschema-and-classschema-objects.md).</span></span>

<span data-ttu-id="7cd84-115">Дополнительные сведения о создании элемента управления доступом см. в разделе [Установка прав доступа для объекта](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="7cd84-115">For more information about how to create an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="7cd84-116">Дополнительные сведения и пример кода, который можно использовать для задания ACE, относящегося к конкретному свойству, см. в разделе [пример кода для настройки записи ACE в объекте каталога](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="7cd84-116">For more information and a code example that can be used to set a property-specific ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 