---
title: Дескриптор безопасности по умолчанию
description: С помощью домен Active Directory Services можно также указать безопасность по умолчанию для каждого типа объектов.
ms.assetid: 6642c966-c163-4d63-8707-62a545d15094
ms.tgt_platform: multiple
keywords:
- Дескриптор безопасности по умолчанию AD
- AD дескрипторов безопасности, по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372f285c3e8c17b481811d7356c40ae07316801d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069789"
---
# <a name="default-security-descriptor"></a><span data-ttu-id="28f06-105">Дескриптор безопасности по умолчанию</span><span class="sxs-lookup"><span data-stu-id="28f06-105">Default Security Descriptor</span></span>

<span data-ttu-id="28f06-106">С помощью домен Active Directory Services можно также указать безопасность по умолчанию для каждого типа объектов.</span><span class="sxs-lookup"><span data-stu-id="28f06-106">With Active Directory Domain Services, you can also specify default security for each type of object.</span></span> <span data-ttu-id="28f06-107">Это указывается в атрибуте [**дефаултсекуритидескриптор**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) в определении объекта [**classSchema**](/windows/desktop/ADSchema/c-classschema) в [схеме Active Directory](active-directory-schema.md).</span><span class="sxs-lookup"><span data-stu-id="28f06-107">This is specified in the [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) attribute in the [**classSchema**](/windows/desktop/ADSchema/c-classschema) object definition in the [Active Directory schema](active-directory-schema.md).</span></span> <span data-ttu-id="28f06-108">Этот дескриптор безопасности используется для обеспечения защиты объекта по умолчанию, если во время создания объекта не указан дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="28f06-108">This security descriptor is used to provide default protection on the object if there is no security descriptor specified during the creation of the object.</span></span>

> [!Note]  
> <span data-ttu-id="28f06-109">Записи ACE из дескриптора безопасности по умолчанию обрабатываются так, как если бы они были указаны как часть создания объекта.</span><span class="sxs-lookup"><span data-stu-id="28f06-109">ACEs from a default security descriptor are handled as if they were specified as part of object creation.</span></span> <span data-ttu-id="28f06-110">Таким образом, записи ACE по умолчанию помещаются перед унаследованными Aceми и переопределяют их соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="28f06-110">Therefore, the default ACEs are placed preceding inherited ACEs and override them as appropriate.</span></span> <span data-ttu-id="28f06-111">Дополнительные сведения см. [в разделе порядок элементов ACE в списке DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="28f06-111">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

<span data-ttu-id="28f06-112">[**Дефаултсекуритидескриптор**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) задается в специальном строковом формате с использованием [языка определения дескрипторов безопасности](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL).</span><span class="sxs-lookup"><span data-stu-id="28f06-112">The [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) is specified in a special string format using the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL).</span></span> <span data-ttu-id="28f06-113">Для преобразования двоичной формы дескриптора безопасности в формат строки и наоборот можно использовать две функции.</span><span class="sxs-lookup"><span data-stu-id="28f06-113">Two functions can be used to convert binary form of the security descriptor to string format and vice versa.</span></span> <span data-ttu-id="28f06-114">Это следующие функции:</span><span class="sxs-lookup"><span data-stu-id="28f06-114">These functions are:</span></span>

-   [<span data-ttu-id="28f06-115">конвертсекуритидескриптортострингсекуритидескриптор</span><span class="sxs-lookup"><span data-stu-id="28f06-115">ConvertSecurityDescriptorToStringSecurityDescriptor</span></span>](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
-   [<span data-ttu-id="28f06-116">конвертстрингсекуритидескриптортосекуритидескриптор</span><span class="sxs-lookup"><span data-stu-id="28f06-116">ConvertStringSecurityDescriptorToSecurityDescriptor</span></span>](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

<span data-ttu-id="28f06-117">Дополнительные сведения и дескрипторы безопасности по умолчанию предопределенных классов объектов см. на страницах справочника по классам в справочнике по схеме Active Directory справочника по [службам домен Active Directory](active-directory-domain-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="28f06-117">For more information and the default security descriptors of the predefined object classes, see the class reference pages in the Active Directory Schema Reference of the [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

<span data-ttu-id="28f06-118">Дополнительные сведения и пример кода, который считывает или изменяет свойство [**дефаултсекуритидескриптор**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) класса Object, см. в разделе [Чтение Дефаултсекуритидескриптор для класса Object](reading-the-defaultsecuritydescriptor-for-an-object-class.md) и [изменение дефаултсекуритидескриптор для класса Object](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).</span><span class="sxs-lookup"><span data-stu-id="28f06-118">For more information and a code example that reads or modifies the [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) property of an object class, see [Reading the defaultSecurityDescriptor for an Object Class](reading-the-defaultsecuritydescriptor-for-an-object-class.md) and [Modifying the defaultSecurityDescriptor for an Object Class](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).</span></span>

 

 