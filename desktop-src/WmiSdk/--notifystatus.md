---
description: Выступает в качестве родительского класса для классов ошибок, определяемых поставщиком.
ms.assetid: fc2747f5-cfbc-4d61-894d-4585a03dda3f
ms.tgt_platform: multiple
title: Класс __NotifyStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NotifyStatus
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f19ef1f6088b5a058f4483f197877358177c81f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817609"
---
# <a name="__notifystatus-class"></a><span data-ttu-id="11d20-103">\_\_Класс Нотифистатус</span><span class="sxs-lookup"><span data-stu-id="11d20-103">\_\_NotifyStatus class</span></span>

<span data-ttu-id="11d20-104">Абстрактный системный класс **\_ \_ нотифистатус** выступает в качестве родительского класса для классов ошибок, определяемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="11d20-104">The **\_\_NotifyStatus** abstract system class serves as the parent class for provider-defined error classes.</span></span>

<span data-ttu-id="11d20-105">Следующий синтаксис упрощен из кода MOF-файл (MF) и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="11d20-105">The following syntax is simplified from Managed Object Format (MF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="11d20-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11d20-106">Syntax</span></span>

``` syntax
[abstract]
class __NotifyStatus
{
  uint32 StatusCode;
};
```

## <a name="members"></a><span data-ttu-id="11d20-107">Члены</span><span class="sxs-lookup"><span data-stu-id="11d20-107">Members</span></span>

<span data-ttu-id="11d20-108">Класс **\_ \_ нотифистатус** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="11d20-108">The **\_\_NotifyStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="11d20-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="11d20-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11d20-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="11d20-110">Properties</span></span>

<span data-ttu-id="11d20-111">Класс **\_ \_ нотифистатус** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="11d20-111">The **\_\_NotifyStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11d20-112">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="11d20-112">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d20-113">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11d20-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11d20-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11d20-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11d20-115">Содержит код ошибки или сведения для операции.</span><span class="sxs-lookup"><span data-stu-id="11d20-115">Contains an error or information code for an operation.</span></span> <span data-ttu-id="11d20-116">Это может быть любой определяемый пользователем код, но значение 0 (ноль) обычно зарезервировано для обозначения успеха.</span><span class="sxs-lookup"><span data-stu-id="11d20-116">This can be any user-defined code, but the value 0 (zero) is usually reserved to indicate success.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11d20-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11d20-117">Remarks</span></span>

<span data-ttu-id="11d20-118">Несмотря на то, что класс **\_ \_ нотифистатус** может быть родительским классом для классов ошибок, определяемых поставщиком, рекомендуется, чтобы поставщики производных классов ошибок от [**\_ \_ екстендедстатус**](--extendedstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="11d20-118">Although the **\_\_NotifyStatus** class can be the parent class for provider-defined error classes, it is recommended that providers derive error classes from [**\_\_ExtendedStatus**](--extendedstatus.md) instead.</span></span> <span data-ttu-id="11d20-119">Использование **\_ \_ екстендедстатус** обеспечивает более высокую стандартизацию классов ошибок.</span><span class="sxs-lookup"><span data-stu-id="11d20-119">Using **\_\_ExtendedStatus** allows for greater standardization of error classes.</span></span>

<span data-ttu-id="11d20-120">Поставщики никогда не должны создавать экземпляры **\_ \_ нотифистатус** напрямую, так как эти экземпляры сообщают больше информации, чем простой код возврата.</span><span class="sxs-lookup"><span data-stu-id="11d20-120">Providers should never create instances of **\_\_NotifyStatus** directly, because these instances convey no more information than a simple return code.</span></span>

## <a name="requirements"></a><span data-ttu-id="11d20-121">Требования</span><span class="sxs-lookup"><span data-stu-id="11d20-121">Requirements</span></span>



| <span data-ttu-id="11d20-122">Требование</span><span class="sxs-lookup"><span data-stu-id="11d20-122">Requirement</span></span> | <span data-ttu-id="11d20-123">Значение</span><span class="sxs-lookup"><span data-stu-id="11d20-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="11d20-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11d20-124">Minimum supported client</span></span><br/> | <span data-ttu-id="11d20-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11d20-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="11d20-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11d20-126">Minimum supported server</span></span><br/> | <span data-ttu-id="11d20-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11d20-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="11d20-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="11d20-128">Namespace</span></span><br/>                | <span data-ttu-id="11d20-129">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="11d20-129">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="11d20-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11d20-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11d20-131">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="11d20-131">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




