---
description: '\_Ассоциация СОФТВАРЕФЕАТУРЕСОФТВАРИЛЕМЕНТС CIM определяет программные элементы, составляющие определенную функцию программного обеспечения.'
ms.assetid: 933586c5-b85e-4136-b557-5151a48abc32
ms.tgt_platform: multiple
title: Класс CIM_SoftwareFeatureSoftwareElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSoftwareElements
- CIM_SoftwareFeatureSoftwareElements.PartComponent
- CIM_SoftwareFeatureSoftwareElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71712ebb3f8bf2ab2067325f16cf31af7fb1dc38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655682"
---
# <a name="cim_softwarefeaturesoftwareelements-class"></a><span data-ttu-id="020cb-103">\_Класс CIM софтварефеатуресофтварилементс</span><span class="sxs-lookup"><span data-stu-id="020cb-103">CIM\_SoftwareFeatureSoftwareElements class</span></span>

<span data-ttu-id="020cb-104">Ассоциация **\_ софтварефеатуресофтварилементс CIM** определяет программные элементы, составляющие определенную функцию программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="020cb-104">The **CIM\_SoftwareFeatureSoftwareElements** association identifies the software elements that make up a specific software feature.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="020cb-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="020cb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="020cb-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="020cb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="020cb-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="020cb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="020cb-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="020cb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="020cb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="020cb-109">Syntax</span></span>

``` syntax
[UUID("{A91081E2-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSoftwareElements : CIM_Component
{
  CIM_SoftwareElement REF PartComponent;
  CIM_SoftwareFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="020cb-110">Члены</span><span class="sxs-lookup"><span data-stu-id="020cb-110">Members</span></span>

<span data-ttu-id="020cb-111">Класс **CIM \_ софтварефеатуресофтварилементс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="020cb-111">The **CIM\_SoftwareFeatureSoftwareElements** class has these types of members:</span></span>

-   [<span data-ttu-id="020cb-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="020cb-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="020cb-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="020cb-113">Properties</span></span>

<span data-ttu-id="020cb-114">Класс **CIM \_ софтварефеатуресофтварилементс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="020cb-114">The **CIM\_SoftwareFeatureSoftwareElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="020cb-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="020cb-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="020cb-116">Тип данных: **CIM \_ софтварефеатуре**</span><span class="sxs-lookup"><span data-stu-id="020cb-116">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="020cb-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="020cb-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="020cb-118">Квалификаторы: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="020cb-118">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="020cb-119">Компонент группы.</span><span class="sxs-lookup"><span data-stu-id="020cb-119">The group component.</span></span>

<span data-ttu-id="020cb-120">Это свойство наследуется [**от \_ компонента CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="020cb-120">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> <dt>

<span data-ttu-id="020cb-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="020cb-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="020cb-122">Тип данных: **CIM \_ софтварилемент**</span><span class="sxs-lookup"><span data-stu-id="020cb-122">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="020cb-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="020cb-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="020cb-124">Компонент части.</span><span class="sxs-lookup"><span data-stu-id="020cb-124">The part component.</span></span>

<span data-ttu-id="020cb-125">Это свойство наследуется [**от \_ компонента CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="020cb-125">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="020cb-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="020cb-126">Remarks</span></span>

<span data-ttu-id="020cb-127">Ассоциация **CIM \_ софтварефеатуресофтварилементс** является производной от [**\_ компонента CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="020cb-127">The **CIM\_SoftwareFeatureSoftwareElements** association is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="020cb-128">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="020cb-128">WMI does not implement this class.</span></span> <span data-ttu-id="020cb-129">Классы WMI, производные от **CIM \_ софтварефеатуресофтварилементс**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="020cb-129">For WMI classes derived from **CIM\_SoftwareFeatureSoftwareElements**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="020cb-130">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="020cb-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="020cb-131">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="020cb-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="020cb-132">Требования</span><span class="sxs-lookup"><span data-stu-id="020cb-132">Requirements</span></span>



| <span data-ttu-id="020cb-133">Требование</span><span class="sxs-lookup"><span data-stu-id="020cb-133">Requirement</span></span> | <span data-ttu-id="020cb-134">Значение</span><span class="sxs-lookup"><span data-stu-id="020cb-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="020cb-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="020cb-135">Minimum supported client</span></span><br/> | <span data-ttu-id="020cb-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="020cb-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="020cb-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="020cb-137">Minimum supported server</span></span><br/> | <span data-ttu-id="020cb-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="020cb-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="020cb-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="020cb-139">Namespace</span></span><br/>                | <span data-ttu-id="020cb-140">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="020cb-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="020cb-141">MOF</span><span class="sxs-lookup"><span data-stu-id="020cb-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="020cb-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="020cb-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="020cb-143">DLL</span><span class="sxs-lookup"><span data-stu-id="020cb-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="020cb-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="020cb-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="020cb-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="020cb-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="020cb-146">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="020cb-146">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

