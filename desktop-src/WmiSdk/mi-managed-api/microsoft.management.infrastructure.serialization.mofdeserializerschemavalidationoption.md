---
description: Дополнительные сведения о перечислении Мофдесериализерсчемавалидатионоптион
title: Перечисление MofDeserializerSchemaValidationOption (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: MofDeserializerSchemaValidationOption enumeration (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: T:Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption
ms.date: 11/14/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Default
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Strict
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Loose
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.IgnorePropertyType
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Ignore
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption::Default
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption::Strict
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption::Loose
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption::IgnorePropertyType
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption::Ignore
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Default
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Strict
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Loose
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.IgnorePropertyType
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Ignore
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: efb6c5a694d09bcb59fedf3f186498c940a95c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155242"
---
# <a name="mofdeserializerschemavalidationoption-enumeration"></a><span data-ttu-id="4ef3c-103">Перечисление Мофдесериализерсчемавалидатионоптион</span><span class="sxs-lookup"><span data-stu-id="4ef3c-103">MofDeserializerSchemaValidationOption enumeration</span></span>

<span data-ttu-id="4ef3c-104">Определяет константы, указывающие параметры проверки схемы для десериализации.</span><span class="sxs-lookup"><span data-stu-id="4ef3c-104">Defines constants that specify schema validation options for deserialization.</span></span>

<span data-ttu-id="4ef3c-105">**Пространство имен:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4ef3c-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="4ef3c-106">**Сборка:**  Microsoft. Management. Infrastructure (в Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="4ef3c-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="4ef3c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ef3c-107">Syntax</span></span>

``` csharp
internal enum MofDeserializerSchemaValidationOption
```

``` c++
private enum class MofDeserializerSchemaValidationOption
```

``` fsharp
type internal MofDeserializerSchemaValidationOption
```

``` vb
Friend Enumeration MofDeserializerSchemaValidationOption
```

## <a name="members"></a><span data-ttu-id="4ef3c-108">Члены</span><span class="sxs-lookup"><span data-stu-id="4ef3c-108">Members</span></span>

||<span data-ttu-id="4ef3c-109">Имя участника</span><span class="sxs-lookup"><span data-stu-id="4ef3c-109">Member name</span></span>|<span data-ttu-id="4ef3c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4ef3c-110">Description</span></span>|
|-|-|-|
||<span data-ttu-id="4ef3c-111">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4ef3c-111">Default</span></span>|<span data-ttu-id="4ef3c-112">Указывает проверку схемы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4ef3c-112">Specifies default schema validation.</span></span>|
||<span data-ttu-id="4ef3c-113">Strict</span><span class="sxs-lookup"><span data-stu-id="4ef3c-113">Strict</span></span>|<span data-ttu-id="4ef3c-114">Указывает на точность проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="4ef3c-114">Specifies strict schema validation.</span></span>|
||<span data-ttu-id="4ef3c-115">Закреплен</span><span class="sxs-lookup"><span data-stu-id="4ef3c-115">Loose</span></span>|<span data-ttu-id="4ef3c-116">Указывает свободную проверку схемы.</span><span class="sxs-lookup"><span data-stu-id="4ef3c-116">Specifies loose schema validation.</span></span>|
||<span data-ttu-id="4ef3c-117">игнорепропертитипе</span><span class="sxs-lookup"><span data-stu-id="4ef3c-117">IgnorePropertyType</span></span>|<span data-ttu-id="4ef3c-118">Указывает, что проверка схемы должна пропускать типы свойств.</span><span class="sxs-lookup"><span data-stu-id="4ef3c-118">Specifies that schema validation should ignore property types.</span></span>|
||<span data-ttu-id="4ef3c-119">Игнорировать</span><span class="sxs-lookup"><span data-stu-id="4ef3c-119">Ignore</span></span>|<span data-ttu-id="4ef3c-120">Указывает, что проверка схемы должна игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="4ef3c-120">Specifies that schema validation should be ignored.</span></span>|

## <a name="see-also"></a><span data-ttu-id="4ef3c-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="4ef3c-121">See Also</span></span>

<span data-ttu-id="4ef3c-122">[Пространство имен Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4ef3c-122">[Microsoft.Management.Infrastructure.Serialization Namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
