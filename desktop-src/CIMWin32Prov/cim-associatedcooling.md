---
description: Ассоциация CIM \_ ассоЦиатедкулинг указывает, что вентиляторы или другие устройства охлаждения относятся к устройству (в отличие от блока охлаждения корпуса или шкафа).
ms.assetid: 7b20e429-593c-4365-a340-1aef9b0fadf5
ms.tgt_platform: multiple
title: Класс CIM_AssociatedCooling
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedCooling
- CIM_AssociatedCooling.Dependent
- CIM_AssociatedCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb838129226b225f024917e8f8e77ddc92ddf2ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142097"
---
# <a name="cim_associatedcooling-class"></a><span data-ttu-id="feecf-103">\_Класс CIM ассоЦиатедкулинг</span><span class="sxs-lookup"><span data-stu-id="feecf-103">CIM\_AssociatedCooling class</span></span>

<span data-ttu-id="feecf-104">Ассоциация **CIM \_ ассоЦиатедкулинг** указывает, что вентиляторы или другие устройства охлаждения относятся к устройству (в отличие от блока охлаждения корпуса или шкафа).</span><span class="sxs-lookup"><span data-stu-id="feecf-104">The **CIM\_AssociatedCooling** association indicates when fans or other cooling devices are specific to a device (versus providing enclosure or cabinet cooling).</span></span>

<span data-ttu-id="feecf-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="feecf-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="feecf-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="feecf-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="feecf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="feecf-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{306F88F2-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedCooling : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_CoolingDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="feecf-108">Члены</span><span class="sxs-lookup"><span data-stu-id="feecf-108">Members</span></span>

<span data-ttu-id="feecf-109">Класс **CIM \_ ассоЦиатедкулинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="feecf-109">The **CIM\_AssociatedCooling** class has these types of members:</span></span>

-   [<span data-ttu-id="feecf-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="feecf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="feecf-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="feecf-111">Properties</span></span>

<span data-ttu-id="feecf-112">Класс **CIM \_ ассоЦиатедкулинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="feecf-112">The **CIM\_AssociatedCooling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="feecf-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="feecf-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feecf-114">Тип данных: **CIM \_ кулингдевице**</span><span class="sxs-lookup"><span data-stu-id="feecf-114">Data type: **CIM\_CoolingDevice**</span></span>
</dt> <dt>

<span data-ttu-id="feecf-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="feecf-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feecf-116">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="feecf-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="feecf-117">Логическое значение типа [**CIM \_**](cim-logicaldevice.md) , которое описывает устройство охлаждения.</span><span class="sxs-lookup"><span data-stu-id="feecf-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the cooling device.</span></span>

</dd> <dt>

<span data-ttu-id="feecf-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="feecf-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feecf-119">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="feecf-119">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="feecf-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="feecf-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feecf-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="feecf-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="feecf-122">Логическое значение типа CIM, которое ссылается на устройство, для которого выполняется охлаждение. [**\_**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="feecf-122">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that references the logical device being cooled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="feecf-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="feecf-123">Remarks</span></span>

<span data-ttu-id="feecf-124">Класс **CIM \_ ассоЦиатедкулинг** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="feecf-124">The **CIM\_AssociatedCooling** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="feecf-125">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="feecf-125">WMI does not implement this class.</span></span>

<span data-ttu-id="feecf-126">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="feecf-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="feecf-127">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="feecf-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="feecf-128">Требования</span><span class="sxs-lookup"><span data-stu-id="feecf-128">Requirements</span></span>



| <span data-ttu-id="feecf-129">Требование</span><span class="sxs-lookup"><span data-stu-id="feecf-129">Requirement</span></span> | <span data-ttu-id="feecf-130">Значение</span><span class="sxs-lookup"><span data-stu-id="feecf-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="feecf-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="feecf-131">Minimum supported client</span></span><br/> | <span data-ttu-id="feecf-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feecf-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="feecf-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="feecf-133">Minimum supported server</span></span><br/> | <span data-ttu-id="feecf-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="feecf-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="feecf-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="feecf-135">Namespace</span></span><br/>                | <span data-ttu-id="feecf-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="feecf-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="feecf-137">MOF</span><span class="sxs-lookup"><span data-stu-id="feecf-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="feecf-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="feecf-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="feecf-139">DLL</span><span class="sxs-lookup"><span data-stu-id="feecf-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="feecf-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="feecf-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feecf-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="feecf-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feecf-142">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="feecf-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

