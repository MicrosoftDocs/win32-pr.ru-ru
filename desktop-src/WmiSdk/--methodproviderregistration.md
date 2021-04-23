---
description: Регистрирует поставщики методов с помощью инструментария WMI.
ms.assetid: c5a8ccd3-487e-42a3-bb31-d27da9a711c4
ms.tgt_platform: multiple
title: Класс __MethodProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: dd59a88c9c0ff7b4b6726b58ce69f879eb3893ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703015"
---
# <a name="__methodproviderregistration-class"></a><span data-ttu-id="7548d-103">\_\_Класс Месодпровидеррегистратион</span><span class="sxs-lookup"><span data-stu-id="7548d-103">\_\_MethodProviderRegistration class</span></span>

<span data-ttu-id="7548d-104">Системный класс **\_ \_ месодпровидеррегистратион** регистрирует поставщиков методов с помощью инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="7548d-104">The **\_\_MethodProviderRegistration** system class registers method providers with WMI.</span></span>

<span data-ttu-id="7548d-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="7548d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7548d-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="7548d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7548d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7548d-107">Syntax</span></span>

``` syntax
class __MethodProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="7548d-108">Члены</span><span class="sxs-lookup"><span data-stu-id="7548d-108">Members</span></span>

<span data-ttu-id="7548d-109">Класс **\_ \_ месодпровидеррегистратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7548d-109">The **\_\_MethodProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="7548d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7548d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7548d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="7548d-111">Properties</span></span>

<span data-ttu-id="7548d-112">Класс **\_ \_ месодпровидеррегистратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7548d-112">The **\_\_MethodProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7548d-113">**поставщики**</span><span class="sxs-lookup"><span data-stu-id="7548d-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7548d-114">Тип данных: **\_ \_ поставщик**</span><span class="sxs-lookup"><span data-stu-id="7548d-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="7548d-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7548d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7548d-116">Ссылка на экземпляр [**\_ \_ поставщика**](--provider.md) , представляющий путь к объекту поставщика метода.</span><span class="sxs-lookup"><span data-stu-id="7548d-116">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path of the method provider.</span></span> <span data-ttu-id="7548d-117">Это свойство наследуется от [**\_ \_ провидеррегистратион**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="7548d-117">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7548d-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7548d-118">Remarks</span></span>

<span data-ttu-id="7548d-119">Класс **\_ \_ месодпровидеррегистратион** является производным от [**\_ \_ провидеррегистратион**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="7548d-119">The **\_\_MethodProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="7548d-120">Только администраторы могут зарегистрировать или удалить поставщик метода, создав экземпляр [**\_ \_ Win32Provider**](--win32provider.md) и **\_ \_ месодпровидеррегистратион**.</span><span class="sxs-lookup"><span data-stu-id="7548d-120">Only administrators can register or delete a method provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_MethodProviderRegistration**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7548d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="7548d-121">Requirements</span></span>



| <span data-ttu-id="7548d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="7548d-122">Requirement</span></span> | <span data-ttu-id="7548d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7548d-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7548d-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7548d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7548d-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7548d-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7548d-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7548d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7548d-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7548d-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="7548d-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7548d-128">Namespace</span></span><br/>                | <span data-ttu-id="7548d-129">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="7548d-129">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="7548d-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7548d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7548d-131">**\_\_провидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="7548d-131">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="7548d-132">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="7548d-132">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="7548d-133">Регистрация поставщика методов</span><span class="sxs-lookup"><span data-stu-id="7548d-133">Registering a Method Provider</span></span>](registering-a-method-provider.md)
</dt> </dl>

 

