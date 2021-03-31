---
description: Предоставляет дополнительные сведения для использования с методом Креатереференцепоинт \_ класса Коллектионреференцепоинтсервице мсвм.
ms.assetid: abf7953a-e10e-4dab-962f-a7dde5126fbe
title: Класс Msvm_CollectionReferencePointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointSettingData
- Msvm_CollectionReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ac05518a3ea9512745e9d2391c2d8cf1d387c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155543"
---
# <a name="msvm_collectionreferencepointsettingdata-class"></a><span data-ttu-id="946ae-103">\_Класс мсвм коллектионреференцепоинтсеттингдата</span><span class="sxs-lookup"><span data-stu-id="946ae-103">Msvm\_CollectionReferencePointSettingData class</span></span>

<span data-ttu-id="946ae-104">Предоставляет дополнительные сведения для использования с методом [**креатереференцепоинт**](msvm-collectionreferencepointservice-createreferencepoint.md) класса [**\_ коллектионреференцепоинтсервице мсвм**](msvm-collectionreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="946ae-104">Provides additional information to be used with the [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md) method of the [**Msvm\_CollectionReferencePointService**](msvm-collectionreferencepointservice.md) class.</span></span>

<span data-ttu-id="946ae-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="946ae-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="946ae-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="946ae-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a><span data-ttu-id="946ae-107">Члены</span><span class="sxs-lookup"><span data-stu-id="946ae-107">Members</span></span>

<span data-ttu-id="946ae-108">Класс **мсвм \_ коллектионреференцепоинтсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="946ae-108">The **Msvm\_CollectionReferencePointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="946ae-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="946ae-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="946ae-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="946ae-110">Properties</span></span>

<span data-ttu-id="946ae-111">Класс **мсвм \_ коллектионреференцепоинтсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="946ae-111">The **Msvm\_CollectionReferencePointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="946ae-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="946ae-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946ae-113">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="946ae-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="946ae-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="946ae-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="946ae-115">Уровень согласованности контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="946ae-115">Consistency level of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="946ae-116"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="946ae-116"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="946ae-117"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>С **совместимостью приложений** (1)</span><span class="sxs-lookup"><span data-stu-id="946ae-117"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="946ae-118">Эталонная точка указывает на момент времени, когда виртуальная система находилась в состоянии сбоя.</span><span class="sxs-lookup"><span data-stu-id="946ae-118">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="946ae-119"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Отказоустойчивость (2** )</span><span class="sxs-lookup"><span data-stu-id="946ae-119"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="946ae-120">Эталонная точка указывает на момент времени, когда виртуальная система находилась в состоянии совместимости с приложениями.</span><span class="sxs-lookup"><span data-stu-id="946ae-120">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="946ae-121">Требования</span><span class="sxs-lookup"><span data-stu-id="946ae-121">Requirements</span></span>



| <span data-ttu-id="946ae-122">Требование</span><span class="sxs-lookup"><span data-stu-id="946ae-122">Requirement</span></span> | <span data-ttu-id="946ae-123">Значение</span><span class="sxs-lookup"><span data-stu-id="946ae-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="946ae-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="946ae-124">Minimum supported client</span></span><br/> | <span data-ttu-id="946ae-125">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="946ae-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="946ae-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="946ae-126">Minimum supported server</span></span><br/> | <span data-ttu-id="946ae-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="946ae-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="946ae-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="946ae-128">Namespace</span></span><br/>                | <span data-ttu-id="946ae-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="946ae-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="946ae-130">MOF</span><span class="sxs-lookup"><span data-stu-id="946ae-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="946ae-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="946ae-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="946ae-132">DLL</span><span class="sxs-lookup"><span data-stu-id="946ae-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="946ae-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="946ae-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="946ae-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="946ae-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="946ae-135">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="946ae-135">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




