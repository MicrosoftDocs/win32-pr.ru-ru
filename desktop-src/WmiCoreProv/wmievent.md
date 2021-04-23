---
description: Класс WMIEvent является базовым классом, из которого производятся все классы событий WMI.
ms.assetid: 0393d3fc-7566-4eda-940e-248d622a903a
title: Класс WMIEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIEvent
- WMIEvent.SECURITY_DESCRIPTOR
- WMIEvent.TIME_CREATED
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 99f6804ef1dad4f37bd2727da2e91e801fb0ece2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081354"
---
# <a name="wmievent-class"></a><span data-ttu-id="f8d97-103">Класс WMIEvent</span><span class="sxs-lookup"><span data-stu-id="f8d97-103">WMIEvent class</span></span>

<span data-ttu-id="f8d97-104">Класс **WMIEvent** является базовым классом, из которого производятся все классы событий WMI.</span><span class="sxs-lookup"><span data-stu-id="f8d97-104">The **WMIEvent** class is a base class from which all WMI event classes are derived.</span></span>

<span data-ttu-id="f8d97-105">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f8d97-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f8d97-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="f8d97-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8d97-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8d97-107">Syntax</span></span>

``` syntax
[]
class WMIEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="f8d97-108">Члены</span><span class="sxs-lookup"><span data-stu-id="f8d97-108">Members</span></span>

<span data-ttu-id="f8d97-109">Класс **WMIEvent** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f8d97-109">The **WMIEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="f8d97-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f8d97-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f8d97-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f8d97-111">Properties</span></span>

<span data-ttu-id="f8d97-112">Класс **WMIEvent** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f8d97-112">The **WMIEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8d97-113">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="f8d97-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8d97-114">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f8d97-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f8d97-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8d97-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8d97-116">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="f8d97-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="f8d97-117">Это свойство наследуется от [**\_ \_ события**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="f8d97-117">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="f8d97-118">Дополнительные сведения о константах, используемых для задания этого дескриптора безопасности, см. в разделе [константы безопасности WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="f8d97-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="f8d97-119">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="f8d97-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8d97-120">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8d97-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8d97-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8d97-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8d97-122">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="f8d97-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="f8d97-123">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="f8d97-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="f8d97-124">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="f8d97-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="f8d97-125">Это свойство наследуется от [**\_ \_ события**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="f8d97-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="f8d97-126">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f8d97-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8d97-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8d97-127">Remarks</span></span>

<span data-ttu-id="f8d97-128">Класс **WMIEvent** является производным от [**\_ \_ екстринсицевент**](/windows/desktop/WmiSdk/--extrinsicevent).</span><span class="sxs-lookup"><span data-stu-id="f8d97-128">The **WMIEvent** class is derived from [**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8d97-129">Требования</span><span class="sxs-lookup"><span data-stu-id="f8d97-129">Requirements</span></span>



| <span data-ttu-id="f8d97-130">Требование</span><span class="sxs-lookup"><span data-stu-id="f8d97-130">Requirement</span></span> | <span data-ttu-id="f8d97-131">Значение</span><span class="sxs-lookup"><span data-stu-id="f8d97-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d97-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8d97-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f8d97-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8d97-133">Windows Vista</span></span><br/>                                                                                                                              |
| <span data-ttu-id="f8d97-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8d97-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f8d97-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f8d97-135">Windows Server 2003</span></span><br/>                                                                                                                        |
| <span data-ttu-id="f8d97-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f8d97-136">Namespace</span></span><br/>                | <span data-ttu-id="f8d97-137">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="f8d97-137">Root\\WMI</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="f8d97-138">MOF</span><span class="sxs-lookup"><span data-stu-id="f8d97-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8d97-139"><dt>WMI. mof; </dt> <dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8d97-139"><dt>Wmi.mof; </dt> <dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8d97-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f8d97-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8d97-141"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8d97-141"><dt>WmiProv.dll</dt></span></span> </dl>                                                                |



## <a name="see-also"></a><span data-ttu-id="f8d97-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8d97-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8d97-143">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="f8d97-143">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="f8d97-144">**\_\_екстринсицевент**</span><span class="sxs-lookup"><span data-stu-id="f8d97-144">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

