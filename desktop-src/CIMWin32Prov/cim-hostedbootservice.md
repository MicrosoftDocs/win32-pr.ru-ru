---
description: Класс CIM \_ хостедбутсервице связывает систему размещения и службу загрузки. Так как эта связь является подклассом из CIM \_ HostedService, она наследует схему определения области или именования, определенную для службы, когда служба откладывается на ее систему размещения.
ms.assetid: 91621288-a231-4423-94df-7601bdf2ebe1
ms.tgt_platform: multiple
title: Класс CIM_HostedBootService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootService
- CIM_HostedBootService.Antecedent
- CIM_HostedBootService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12baa364653feda1400ad15d658e6739859b2521
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141731"
---
# <a name="cim_hostedbootservice-class"></a><span data-ttu-id="51bd5-104">\_Класс CIM хостедбутсервице</span><span class="sxs-lookup"><span data-stu-id="51bd5-104">CIM\_HostedBootService class</span></span>

<span data-ttu-id="51bd5-105">Класс **CIM \_ хостедбутсервице** связывает систему размещения и службу загрузки.</span><span class="sxs-lookup"><span data-stu-id="51bd5-105">The **CIM\_HostedBootService** class associates a hosting system and a boot service.</span></span> <span data-ttu-id="51bd5-106">Так как эта связь является подклассом из [**CIM \_ HostedService**](cim-hostedservice.md), она наследует схему определения области или именования, определенную для службы, когда служба откладывается на ее систему размещения.</span><span class="sxs-lookup"><span data-stu-id="51bd5-106">Since this relationship is subclassed from [**CIM\_HostedService**](cim-hostedservice.md), it inherits the scoping/naming scheme defined for service, where a service defers to its hosting system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51bd5-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="51bd5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="51bd5-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="51bd5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="51bd5-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="51bd5-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="51bd5-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="51bd5-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="51bd5-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51bd5-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{6DAE7092-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootService : CIM_HostedService
{
  CIM_System      REF Antecedent;
  CIM_BootService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="51bd5-112">Члены</span><span class="sxs-lookup"><span data-stu-id="51bd5-112">Members</span></span>

<span data-ttu-id="51bd5-113">Класс **CIM \_ хостедбутсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="51bd5-113">The **CIM\_HostedBootService** class has these types of members:</span></span>

-   [<span data-ttu-id="51bd5-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="51bd5-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51bd5-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="51bd5-115">Properties</span></span>

<span data-ttu-id="51bd5-116">Класс **CIM \_ хостедбутсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="51bd5-116">The **CIM\_HostedBootService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51bd5-117">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="51bd5-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51bd5-118">Тип данных: **\_ система CIM**</span><span class="sxs-lookup"><span data-stu-id="51bd5-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="51bd5-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="51bd5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51bd5-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent)</span><span class="sxs-lookup"><span data-stu-id="51bd5-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent)</span></span>
</dt> </dl>

<span data-ttu-id="51bd5-121">[**\_ Система CIM**](cim-system.md) , которая описывает систему размещения.</span><span class="sxs-lookup"><span data-stu-id="51bd5-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="51bd5-122">**Него**</span><span class="sxs-lookup"><span data-stu-id="51bd5-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51bd5-123">Тип данных: **CIM \_ бутсервице**</span><span class="sxs-lookup"><span data-stu-id="51bd5-123">Data type: **CIM\_BootService**</span></span>
</dt> <dt>

<span data-ttu-id="51bd5-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="51bd5-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51bd5-125">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="51bd5-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="51bd5-126">[**\_ Бутсервице CIM**](cim-bootservice.md) , описывающий службу загрузки, размещенную в системе.</span><span class="sxs-lookup"><span data-stu-id="51bd5-126">A [**CIM\_BootService**](cim-bootservice.md) that describes the boot service hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51bd5-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51bd5-127">Remarks</span></span>

<span data-ttu-id="51bd5-128">Класс **CIM \_ хостедбутсервице** является производным от [**CIM \_ HostedService**](cim-hostedservice.md).</span><span class="sxs-lookup"><span data-stu-id="51bd5-128">The **CIM\_HostedBootService** class is derived from [**CIM\_HostedService**](cim-hostedservice.md).</span></span>

<span data-ttu-id="51bd5-129">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="51bd5-129">WMI does not implement this class.</span></span>

<span data-ttu-id="51bd5-130">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="51bd5-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="51bd5-131">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="51bd5-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="51bd5-132">Требования</span><span class="sxs-lookup"><span data-stu-id="51bd5-132">Requirements</span></span>



| <span data-ttu-id="51bd5-133">Требование</span><span class="sxs-lookup"><span data-stu-id="51bd5-133">Requirement</span></span> | <span data-ttu-id="51bd5-134">Значение</span><span class="sxs-lookup"><span data-stu-id="51bd5-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51bd5-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51bd5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="51bd5-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51bd5-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="51bd5-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51bd5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="51bd5-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51bd5-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="51bd5-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="51bd5-139">Namespace</span></span><br/>                | <span data-ttu-id="51bd5-140">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="51bd5-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="51bd5-141">MOF</span><span class="sxs-lookup"><span data-stu-id="51bd5-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51bd5-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51bd5-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="51bd5-143">DLL</span><span class="sxs-lookup"><span data-stu-id="51bd5-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51bd5-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51bd5-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51bd5-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51bd5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51bd5-146">**CIM \_ HostedService**</span><span class="sxs-lookup"><span data-stu-id="51bd5-146">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> </dl>

 

