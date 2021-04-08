---
title: Поиск групп по области или типу в домене
description: В доменах Windows 2000 существует один класс под названием Group для всех областей группы (локальный домен, глобальный, универсальный) и типы (безопасность, распространение).
ms.assetid: e32629d9-aa62-4953-aa49-43af726b7deb
ms.tgt_platform: multiple
keywords:
- Поиск групп по области или типу в доменных службах Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9aae5e2c7be7b9cba590f9bc80f0517bca918
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789469"
---
# <a name="searching-for-groups-by-scope-or-type-in-a-domain"></a><span data-ttu-id="95e3b-104">Поиск групп по области или типу в домене</span><span class="sxs-lookup"><span data-stu-id="95e3b-104">Searching for Groups by Scope or Type in a Domain</span></span>

<span data-ttu-id="95e3b-105">В доменах Windows 2000 существует один класс под названием [**Group**](/windows/desktop/ADSchema/c-group) для всех областей группы (локальный домен, глобальный, универсальный) и типы (безопасность, распространение).</span><span class="sxs-lookup"><span data-stu-id="95e3b-105">In Windows 2000 domains, there is single class called [**group**](/windows/desktop/ADSchema/c-group) for all group scopes (Domain Local, Global, Universal) and types (security, distribution).</span></span> <span data-ttu-id="95e3b-106">Атрибут [**groupType**](/windows/desktop/ADSchema/a-grouptype) объекта Group задает тип и область действия группы.</span><span class="sxs-lookup"><span data-stu-id="95e3b-106">The [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute of the group object specifies the group type and scope.</span></span>

<span data-ttu-id="95e3b-107">Чтобы использовать тип или область для поиска групп в доменах Windows 2000, используйте фильтр, содержащий правило сопоставления для атрибута [**groupType**](/windows/desktop/ADSchema/a-grouptype) .</span><span class="sxs-lookup"><span data-stu-id="95e3b-107">To use type or scope to search for groups on Windows 2000 domains, use a filter that contains a matching rule for the [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute.</span></span> <span data-ttu-id="95e3b-108">Дополнительные сведения о правилах сопоставления см. в разделе [синтаксис фильтра поиска](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="95e3b-108">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="95e3b-109">Дополнительные сведения и пример кода, демонстрирующий Поиск групп в домене, см. в разделе [пример кода для поиска групп в домене](example-code-for-performing-a-query-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="95e3b-109">For more information and a code example that shows how to search for groups in a domain, see [Example Code for Searching for Groups in a Domain](example-code-for-performing-a-query-in-a-domain.md).</span></span>

## <a name="example-ldap-query-strings"></a><span data-ttu-id="95e3b-110">Примеры строк запросов LDAP</span><span class="sxs-lookup"><span data-stu-id="95e3b-110">Example LDAP Query Strings</span></span>

<span data-ttu-id="95e3b-111">В следующих примерах строки запроса показано, как создать строку запроса LDAP, используемую для поиска или фильтрации конкретных типов групп.</span><span class="sxs-lookup"><span data-stu-id="95e3b-111">The following query string examples show how to construct an LDAP query string used to search for or filter specific group types.</span></span>

<span data-ttu-id="95e3b-112">Следующая строка запроса будет искать группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="95e3b-112">The following query string will search for security groups.</span></span> <span data-ttu-id="95e3b-113">В этом примере используется символ "-2147483648" в качестве десятичного эквивалента флага **\_ \_ \_ \_ включения безопасности типа группы ADS** .</span><span class="sxs-lookup"><span data-stu-id="95e3b-113">This example uses "-2147483648" as the decimal equivalent of the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span>


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=-2147483648))
```



<span data-ttu-id="95e3b-114">Следующая строка запроса будет искать универсальные группы рассылки. Это значит, что группы, содержащие **флаг \_ \_ \_ универсальной \_ группы ADS** , не содержат флаг **\_ \_ \_ \_ включения безопасности типа группы баннеров** .</span><span class="sxs-lookup"><span data-stu-id="95e3b-114">The following query string will search for universal distribution groups; that is, groups that contain the **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** flag and do not contain the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span> <span data-ttu-id="95e3b-115">В этом примере используется символ "8" в качестве десятичного эквивалента **\_ \_ \_ универсальной \_ группы ADS типа группы баннеров** и "-2147483648" в качестве десятичного эквивалента флага " **\_ \_ \_ \_ Включение безопасности типа группы баннеров** ".</span><span class="sxs-lookup"><span data-stu-id="95e3b-115">This example uses "8" as the decimal equivalent of **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** and "-2147483648" as the decimal equivalent of the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span>


```C++
(&(objectCategory=group)((&(groupType:1.2.840.113556.1.4.803:=8)(!(groupType:1.2.840.113556.1.4.803:=-2147483648)))))
```



 

 