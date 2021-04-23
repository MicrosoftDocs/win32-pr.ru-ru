---
title: Установка разрешений для группы свойств
description: Разрешения могут быть применены к группе свойств.
ms.assetid: cb9f6c04-be94-45b4-ba84-2a79b7625fdd
ms.tgt_platform: multiple
keywords:
- Установка разрешений для группы свойств Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f2993a537b76b64c7e8e6323c850494b3ce306
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789457"
---
# <a name="setting-permissions-on-a-group-of-properties"></a><span data-ttu-id="9c275-104">Установка разрешений для группы свойств</span><span class="sxs-lookup"><span data-stu-id="9c275-104">Setting Permissions on a Group of Properties</span></span>

<span data-ttu-id="9c275-105">Разрешения могут быть применены к группе свойств.</span><span class="sxs-lookup"><span data-stu-id="9c275-105">Permissions can be applied to a group of properties.</span></span> <span data-ttu-id="9c275-106">Набор свойств определяется идентификатором GUID в атрибуте [**ригхтсгуид**](/windows/desktop/ADSchema/a-rightsguid) объекта [**контролакцессригхт**](/windows/desktop/ADSchema/c-controlaccessright) .</span><span class="sxs-lookup"><span data-stu-id="9c275-106">A property set is identified by the GUID in the [**rightsGUID**](/windows/desktop/ADSchema/a-rightsguid) attribute of a [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright) object.</span></span> <span data-ttu-id="9c275-107">Этот идентификатор GUID задается в атрибуте [**аттрибутесекуритигуид**](/windows/desktop/ADSchema/a-attributesecurityguid) объекта [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) каждого атрибута в группе.</span><span class="sxs-lookup"><span data-stu-id="9c275-107">This GUID is set in the [**attributeSecurityGUID**](/windows/desktop/ADSchema/a-attributesecurityguid) attribute of the [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object of each attribute in the group.</span></span>

<span data-ttu-id="9c275-108">В следующей процедуре показано, как задать разрешения, которые применяются к группе свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="9c275-108">The following procedure shows how to set permissions that apply to a group of object properties.</span></span>

<span data-ttu-id="9c275-109">**Установка разрешений, относящихся к группе свойств объекта**</span><span class="sxs-lookup"><span data-stu-id="9c275-109">**To set permissions that apply to a group of object properties**</span></span>

1.  <span data-ttu-id="9c275-110">Задайте для свойства [**иадсакцессконтролентри. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) значение **ADS \_ справа \_ DS redirectory \_ Read \_ prop**, **AD \_ right \_ DS \_ запись \_ prop** или оба значения вместе.</span><span class="sxs-lookup"><span data-stu-id="9c275-110">Set the [**IADsAccessControlEntry.AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_RIGHT\_DS\_READ\_PROP**, **ADS\_RIGHT\_DS\_WRITE\_PROP** or both values combined.</span></span>
2.  <span data-ttu-id="9c275-111">Задайте для свойства [**иадсакцессконтролентри. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) значение **ADS \_ AceType \_ доступ к \_ разрешенному \_ объекту** или **ADS \_ AceType \_ доступ к \_ \_ объекту**.</span><span class="sxs-lookup"><span data-stu-id="9c275-111">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to either **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
3.  <span data-ttu-id="9c275-112">Задайте для свойства [**иадсакцессконтролентри. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) идентификатор GUID набора свойств.</span><span class="sxs-lookup"><span data-stu-id="9c275-112">Set the [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the GUID of the property set.</span></span> <span data-ttu-id="9c275-113">Это свойство [**ригхтсгуид**](/windows/desktop/ADSchema/a-rightsguid) объекта [**контролакцессригхт**](/windows/desktop/ADSchema/c-controlaccessright) , идентифицирующее набор свойств.</span><span class="sxs-lookup"><span data-stu-id="9c275-113">This is the [**rightsGUID**](/windows/desktop/ADSchema/a-rightsguid) property of the [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright) object that identifies the property set.</span></span> <span data-ttu-id="9c275-114">Этот GUID также задается как [**аттрибутесекуритигуид**](/windows/desktop/ADSchema/a-attributesecurityguid) в объекте attributeSchema каждого свойства в группе.</span><span class="sxs-lookup"><span data-stu-id="9c275-114">This GUID is also set as the [**attributeSecurityGUID**](/windows/desktop/ADSchema/a-attributesecurityguid) in the attributeSchema object of each property in the group.</span></span>
4.  <span data-ttu-id="9c275-115">Установите для свойства [**иадсакцессконтролентри. flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) значение **\_ \_ тип объекта \_ \_ флага ADS**.</span><span class="sxs-lookup"><span data-stu-id="9c275-115">Set the [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**.</span></span>

<span data-ttu-id="9c275-116">Имейте в виду, что не следует задавать **флаг \_ \_ \_ \_ доступа к AD right DS Control** в свойстве [**иадсакцессконтролентри. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) .</span><span class="sxs-lookup"><span data-stu-id="9c275-116">Be aware that you should not set the **ADS\_RIGHT\_DS\_CONTROL\_ACCESS** flag in the [**IADsAccessControlEntry.AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property.</span></span> <span data-ttu-id="9c275-117">Этот флаг используется только для указания права доступа к элементу управления.</span><span class="sxs-lookup"><span data-stu-id="9c275-117">This flag is only used to specify a control access right.</span></span>

<span data-ttu-id="9c275-118">Дополнительные сведения и пример кода, который можно использовать для установки прав доступа для набора свойств, см. в разделе [пример кода для настройки разрешений для группы свойств](example-code-for-setting-permissions-on-a-group-of-properties.md).</span><span class="sxs-lookup"><span data-stu-id="9c275-118">For more information and a code example that can be used to set access rights for a property set, see [Example Code for Setting Permissions on a Group of Properties](example-code-for-setting-permissions-on-a-group-of-properties.md).</span></span>

<span data-ttu-id="9c275-119">Дополнительные сведения о создании записи ACE см. [в разделе Установка прав доступа для объекта](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="9c275-119">For more information about creating an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="9c275-120">Дополнительные сведения и пример кода, который можно использовать для установки ACE для набора свойств, см. в разделе [пример кода для настройки записи ACE в объекте каталога](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="9c275-120">For more information and a code example that can be used to set an ACE for a property set, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 