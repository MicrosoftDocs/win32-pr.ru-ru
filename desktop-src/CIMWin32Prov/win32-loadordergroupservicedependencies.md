---
description: '\_Класс WMI взаимосвязей Win32 лоадордерграупсервицедепенденЦиес связывает базовую службу и группу порядка загрузки, от которой зависит служба, чтобы начать выполнение.'
ms.assetid: 56739b80-9028-4a2e-85ed-973a078860c1
ms.tgt_platform: multiple
title: Класс Win32_LoadOrderGroupServiceDependencies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceDependencies
- Win32_LoadOrderGroupServiceDependencies.Antecedent
- Win32_LoadOrderGroupServiceDependencies.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b95d1aa01def951802434e787931ce348d04ccb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142499"
---
# <a name="win32_loadordergroupservicedependencies-class"></a><span data-ttu-id="62a3c-103">\_Класс Win32 лоадордерграупсервицедепенденЦиес</span><span class="sxs-lookup"><span data-stu-id="62a3c-103">Win32\_LoadOrderGroupServiceDependencies class</span></span>

<span data-ttu-id="62a3c-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ лоадордерграупсервицедепенденЦиес** связывает базовую службу и группу порядка загрузки, от которой зависит служба, чтобы начать выполнение.</span><span class="sxs-lookup"><span data-stu-id="62a3c-104">The **Win32\_LoadOrderGroupServiceDependencies** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a base service and a load order group that the service depends on to start running.</span></span>

<span data-ttu-id="62a3c-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="62a3c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="62a3c-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="62a3c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a3c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62a3c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceDependencies : CIM_Dependency
{
  Win32_LoadOrderGroup REF Antecedent;
  Win32_BaseService    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="62a3c-108">Члены</span><span class="sxs-lookup"><span data-stu-id="62a3c-108">Members</span></span>

<span data-ttu-id="62a3c-109">Класс **Win32 \_ лоадордерграупсервицедепенденЦиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="62a3c-109">The **Win32\_LoadOrderGroupServiceDependencies** class has these types of members:</span></span>

-   [<span data-ttu-id="62a3c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="62a3c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62a3c-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="62a3c-111">Properties</span></span>

<span data-ttu-id="62a3c-112">Класс **Win32 \_ лоадордерграупсервицедепенденЦиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="62a3c-112">The **Win32\_LoadOrderGroupServiceDependencies** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62a3c-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="62a3c-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a3c-114">Тип данных: **Win32 \_ лоадордерграуп**</span><span class="sxs-lookup"><span data-stu-id="62a3c-114">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="62a3c-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62a3c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62a3c-116">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ лоадордерграуп")</span><span class="sxs-lookup"><span data-stu-id="62a3c-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="62a3c-117">Ссылка на экземпляр, представляющий свойства группы порядка загрузки, которые должны быть запущены до запуска зависимой базовой службы этого класса.</span><span class="sxs-lookup"><span data-stu-id="62a3c-117">Reference to the instance representing the properties of the load order group that must start before the dependent base service of this class can start.</span></span>

</dd> <dt>

<span data-ttu-id="62a3c-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="62a3c-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a3c-119">Тип данных: **Win32 \_ басесервице**</span><span class="sxs-lookup"><span data-stu-id="62a3c-119">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="62a3c-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62a3c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62a3c-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ басесервице")</span><span class="sxs-lookup"><span data-stu-id="62a3c-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="62a3c-122">Ссылка на экземпляр, представляющий свойства базовой службы, зависящие от группы порядка загрузки, с которой начинается выполнение.</span><span class="sxs-lookup"><span data-stu-id="62a3c-122">Reference to the instance representing the properties of the base service that is dependent upon the load order group to start running.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62a3c-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62a3c-123">Remarks</span></span>

<span data-ttu-id="62a3c-124">Класс **Win32 \_ лоадордерграупсервицедепенденЦиес** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="62a3c-124">The **Win32\_LoadOrderGroupServiceDependencies** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="62a3c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="62a3c-125">Requirements</span></span>



| <span data-ttu-id="62a3c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="62a3c-126">Requirement</span></span> | <span data-ttu-id="62a3c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="62a3c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62a3c-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62a3c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="62a3c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62a3c-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62a3c-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62a3c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="62a3c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62a3c-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62a3c-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="62a3c-132">Namespace</span></span><br/>                | <span data-ttu-id="62a3c-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="62a3c-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="62a3c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="62a3c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62a3c-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62a3c-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="62a3c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="62a3c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62a3c-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62a3c-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62a3c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62a3c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a3c-139">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="62a3c-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="62a3c-140">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="62a3c-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

