---
description: Выступает в качестве родительского класса для \_ \_ системного класса Win32Provider.
ms.assetid: e4cad7c6-4650-4334-b8c4-ac65381bced7
ms.tgt_platform: multiple
title: Класс __Provider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Provider
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 733323c106a5d682e7eddbe3a41bf9c156520c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712123"
---
# <a name="__provider-class"></a><span data-ttu-id="d251f-103">\_\_Класс поставщика</span><span class="sxs-lookup"><span data-stu-id="d251f-103">\_\_Provider class</span></span>

<span data-ttu-id="d251f-104">Класс системы **\_ \_ поставщика** является абстрактным базовым классом, который служит родительским классом для системного класса [**\_ \_ Win32Provider**](--win32provider.md) .</span><span class="sxs-lookup"><span data-stu-id="d251f-104">The **\_\_Provider** system class is an abstract base class that serves as the parent class for the [**\_\_Win32Provider**](--win32provider.md) system class.</span></span>

<span data-ttu-id="d251f-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="d251f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d251f-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="d251f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d251f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d251f-107">Syntax</span></span>

``` syntax
[abstract]
class __Provider : __SystemClass
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="d251f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d251f-108">Members</span></span>

<span data-ttu-id="d251f-109">Класс **\_ \_ поставщика** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d251f-109">The **\_\_Provider** class has these types of members:</span></span>

-   [<span data-ttu-id="d251f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d251f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d251f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="d251f-111">Properties</span></span>

<span data-ttu-id="d251f-112">Класс **\_ \_ поставщика** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d251f-112">The **\_\_Provider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d251f-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="d251f-113">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d251f-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d251f-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d251f-115">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d251f-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d251f-116">Квалификаторы: [ **ключ**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d251f-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d251f-117">Строка, не зависящая от языка, которая уникально идентифицирует поставщик.</span><span class="sxs-lookup"><span data-stu-id="d251f-117">Language-neutral string that uniquely identifies the provider.</span></span> <span data-ttu-id="d251f-118">Для предотвращения конфликтов имен рекомендуется следующий формат:</span><span class="sxs-lookup"><span data-stu-id="d251f-118">The following format is suggested to prevent naming conflicts:</span></span>

<span data-ttu-id="d251f-119">\|версия поставщика \| поставщика</span><span class="sxs-lookup"><span data-stu-id="d251f-119">vendor\|provider\|version</span></span>

<span data-ttu-id="d251f-120">Например, это имя поставщика представляет версию 1,0 Microsoft Тестпровидер:</span><span class="sxs-lookup"><span data-stu-id="d251f-120">For example, this provider name represents version 1.0 of the Microsoft TestProvider:</span></span>

<span data-ttu-id="d251f-121">«Microsoft \| тестпровидер \| v 1.0»</span><span class="sxs-lookup"><span data-stu-id="d251f-121">"Microsoft\|TestProvider\|V1.0"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d251f-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d251f-122">Remarks</span></span>

<span data-ttu-id="d251f-123">Класс **\_ \_ поставщика** является производным от [**\_ \_ системкласс**](--systemclass.md), у которого нет свойств.</span><span class="sxs-lookup"><span data-stu-id="d251f-123">The **\_\_Provider** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="d251f-124">Поставщики создают экземпляры [**\_ \_ Win32Provider**](--win32provider.md) , чтобы указать сведения о своей физической реализации.</span><span class="sxs-lookup"><span data-stu-id="d251f-124">Providers create [**\_\_Win32Provider**](--win32provider.md) instances to specify information about their physical implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="d251f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d251f-125">Requirements</span></span>



| <span data-ttu-id="d251f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d251f-126">Requirement</span></span> | <span data-ttu-id="d251f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d251f-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d251f-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d251f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d251f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d251f-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d251f-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d251f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d251f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d251f-131">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d251f-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d251f-132">Namespace</span></span><br/>                | <span data-ttu-id="d251f-133">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="d251f-133">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d251f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d251f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d251f-135">**\_\_системкласс**</span><span class="sxs-lookup"><span data-stu-id="d251f-135">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="d251f-136">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="d251f-136">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="d251f-137">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="d251f-137">**\_\_Win32Provider**</span></span>](--win32provider.md)
</dt> </dl>

 

