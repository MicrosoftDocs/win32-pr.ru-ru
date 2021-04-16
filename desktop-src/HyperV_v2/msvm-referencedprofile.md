---
description: Описывает профиль, на который ссылается другой зарегистрированный профиль.
ms.assetid: 36FC0161-C57F-488A-9B4A-C86C6EB481D7
title: Класс Msvm_ReferencedProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencedProfile
- Msvm_ReferencedProfile.Antecedent
- Msvm_ReferencedProfile.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbe95658556be8a15bed0e7e5b5b32dda23ff21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683544"
---
# <a name="msvm_referencedprofile-class"></a><span data-ttu-id="034fb-103">\_Класс мсвм референцедпрофиле</span><span class="sxs-lookup"><span data-stu-id="034fb-103">Msvm\_ReferencedProfile class</span></span>

<span data-ttu-id="034fb-104">Описывает профиль, на который ссылается другой зарегистрированный профиль.</span><span class="sxs-lookup"><span data-stu-id="034fb-104">Describes a profile that is referenced by another registered profile.</span></span>

<span data-ttu-id="034fb-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="034fb-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="034fb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="034fb-106">Syntax</span></span>

``` syntax
class Msvm_ReferencedProfile : CIM_ReferencedProfile
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="034fb-107">Члены</span><span class="sxs-lookup"><span data-stu-id="034fb-107">Members</span></span>

<span data-ttu-id="034fb-108">Класс **мсвм \_ референцедпрофиле** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="034fb-108">The **Msvm\_ReferencedProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="034fb-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="034fb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="034fb-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="034fb-110">Properties</span></span>

<span data-ttu-id="034fb-111">Класс **мсвм \_ референцедпрофиле** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="034fb-111">The **Msvm\_ReferencedProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="034fb-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="034fb-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="034fb-113">Тип данных: **[ **CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="034fb-113">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="034fb-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="034fb-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="034fb-115">Зарегистрированный профиль, на который ссылается **зависимый** профиль.</span><span class="sxs-lookup"><span data-stu-id="034fb-115">The registered profile that is referenced by the **Dependent** profile.</span></span>

</dd> <dt>

<span data-ttu-id="034fb-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="034fb-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="034fb-117">Тип данных: **[ **CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="034fb-117">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="034fb-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="034fb-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="034fb-119">Зарегистрированный профиль, который ссылается на другие профили.</span><span class="sxs-lookup"><span data-stu-id="034fb-119">A registered profile that references other profiles.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="034fb-120">Требования</span><span class="sxs-lookup"><span data-stu-id="034fb-120">Requirements</span></span>



| <span data-ttu-id="034fb-121">Требование</span><span class="sxs-lookup"><span data-stu-id="034fb-121">Requirement</span></span> | <span data-ttu-id="034fb-122">Значение</span><span class="sxs-lookup"><span data-stu-id="034fb-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="034fb-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="034fb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="034fb-124">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="034fb-124">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="034fb-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="034fb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="034fb-126">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="034fb-126">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="034fb-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="034fb-127">Namespace</span></span><br/>                | <span data-ttu-id="034fb-128">Корневое \\ взаимодействие</span><span class="sxs-lookup"><span data-stu-id="034fb-128">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="034fb-129">MOF</span><span class="sxs-lookup"><span data-stu-id="034fb-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="034fb-130"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="034fb-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="034fb-131">DLL</span><span class="sxs-lookup"><span data-stu-id="034fb-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="034fb-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="034fb-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

