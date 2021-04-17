---
description: Содержит права доступа для пространства имен в виде дескриптора безопасности.
ms.assetid: 84e514f5-b114-4bfc-ab0b-9745f249168b
ms.tgt_platform: multiple
title: класс __thisNAMESPACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __thisNAMESPACE
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 440ccdf0eda794b5d648cae756f9a9c808eb2db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684152"
---
# <a name="__thisnamespace-class"></a><span data-ttu-id="b4930-103">\_\_класс Сиснамеспаце</span><span class="sxs-lookup"><span data-stu-id="b4930-103">\_\_thisNAMESPACE class</span></span>

<span data-ttu-id="b4930-104">Класс System **\_ \_ сиснамеспаце** содержит права доступа для пространства имен в форме дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="b4930-104">The **\_\_thisNAMESPACE** system class holds the security rights for the namespace in the form of a security descriptor.</span></span> <span data-ttu-id="b4930-105">Этот класс и один экземпляр находятся во всех пространствах имен.</span><span class="sxs-lookup"><span data-stu-id="b4930-105">This class and a single instance is found in all namespaces.</span></span>

<span data-ttu-id="b4930-106">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b4930-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b4930-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="b4930-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4930-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4930-108">Syntax</span></span>

``` syntax
[singleton]
class __thisNAMESPACE : __SystemClass
{
  uint8 SECURITY_DESCRIPTOR[];
};
```

## <a name="members"></a><span data-ttu-id="b4930-109">Члены</span><span class="sxs-lookup"><span data-stu-id="b4930-109">Members</span></span>

<span data-ttu-id="b4930-110">Класс **\_ \_ сиснамеспаце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b4930-110">The **\_\_thisNAMESPACE** class has these types of members:</span></span>

-   [<span data-ttu-id="b4930-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b4930-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4930-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="b4930-112">Properties</span></span>

<span data-ttu-id="b4930-113">Класс **\_ \_ сиснамеспаце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b4930-113">The **\_\_thisNAMESPACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4930-114">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="b4930-114">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4930-115">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b4930-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b4930-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b4930-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4930-117">Дескриптор безопасности, описывающий, кто имеет доступ к пространству имен и кто может выполнять чтение из пространства имен или запись в него.</span><span class="sxs-lookup"><span data-stu-id="b4930-117">Security descriptor describing who can access the namespace and who can read from or write to the namespace.</span></span> <span data-ttu-id="b4930-118">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="b4930-118">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="b4930-119">Дополнительные сведения о формате дескрипторов безопасности см. в разделе [дескрипторы безопасности](/windows/desktop/SecAuthZ/security-descriptors) раздела Безопасность Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b4930-119">For more information about the format of security descriptors, see [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors) in the Security section of the Windows SDK.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4930-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4930-120">Remarks</span></span>

<span data-ttu-id="b4930-121">Одноэлементный экземпляр **\_ \_ сиснамеспаце** доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b4930-121">The singleton instance of **\_\_thisNAMESPACE** is read-only.</span></span> <span data-ttu-id="b4930-122">Чтобы изменить параметры свойства дескриптора безопасности, используйте методы класса [**\_ \_ системсекурити**](--systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="b4930-122">To change the settings of the security descriptor property, use the methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class.</span></span> <span data-ttu-id="b4930-123">Класс **\_ \_ сиснамеспаце** является производным от [**\_ \_ системкласс**](--systemclass.md).</span><span class="sxs-lookup"><span data-stu-id="b4930-123">The **\_\_thisNAMESPACE** class derives from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4930-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b4930-124">Requirements</span></span>



| <span data-ttu-id="b4930-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b4930-125">Requirement</span></span> | <span data-ttu-id="b4930-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b4930-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b4930-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4930-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b4930-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4930-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b4930-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4930-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b4930-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4930-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b4930-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b4930-131">Namespace</span></span><br/>                | <span data-ttu-id="b4930-132">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="b4930-132">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b4930-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4930-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4930-134">**\_\_системкласс**</span><span class="sxs-lookup"><span data-stu-id="b4930-134">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="b4930-135">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="b4930-135">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

