---
description: '\_Класс WMI взаимосвязей Win32 принтершаре связывает локальный принтер и общую папку, которая представляет его по мере просмотра по сети.'
ms.assetid: 9ac99e52-5e8f-4329-960f-7bd1fd229e37
ms.tgt_platform: multiple
title: Класс Win32_PrinterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterShare
- Win32_PrinterShare.Antecedent
- Win32_PrinterShare.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57bc15fc5d3db78179335b039851d7d3b7cbf8a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896265"
---
# <a name="win32_printershare-class"></a><span data-ttu-id="5668a-103">\_Класс Win32 принтершаре</span><span class="sxs-lookup"><span data-stu-id="5668a-103">Win32\_PrinterShare class</span></span>

<span data-ttu-id="5668a-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ принтершаре** связывает локальный принтер и общую папку, которая представляет его по мере просмотра по сети.</span><span class="sxs-lookup"><span data-stu-id="5668a-104">The **Win32\_PrinterShare** association [WMI class](../wmisdk/retrieving-a-class.md) relates a local printer and the share that represents it as it is viewed over a network.</span></span>

<span data-ttu-id="5668a-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="5668a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5668a-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="5668a-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5668a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5668a-107">Syntax</span></span>

``` syntax
class Win32_PrinterShare : CIM_Dependency
{
  Win32_Printer REF Antecedent;
  Win32_Share   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5668a-108">Члены</span><span class="sxs-lookup"><span data-stu-id="5668a-108">Members</span></span>

<span data-ttu-id="5668a-109">Класс **Win32 \_ принтершаре** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5668a-109">The **Win32\_PrinterShare** class has these types of members:</span></span>

-   [<span data-ttu-id="5668a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="5668a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5668a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="5668a-111">Properties</span></span>

<span data-ttu-id="5668a-112">Класс **Win32 \_ принтершаре** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5668a-112">The **Win32\_PrinterShare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5668a-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="5668a-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5668a-114">Тип данных: **\_ принтер Win32**</span><span class="sxs-lookup"><span data-stu-id="5668a-114">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="5668a-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5668a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5668a-116">Квалификаторы: [ **ключ**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5668a-116">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5668a-117">Ссылка на экземпляр, представляющий локальный принтер, совместно используемый в этой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="5668a-117">Reference to the instance representing the local printer shared in this association.</span></span>

</dd> <dt>

<span data-ttu-id="5668a-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="5668a-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5668a-119">Тип данных: **\_ общий ресурс Win32**</span><span class="sxs-lookup"><span data-stu-id="5668a-119">Data type: **Win32\_Share**</span></span>
</dt> <dt>

<span data-ttu-id="5668a-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5668a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5668a-121">Квалификаторы: [ **ключ**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5668a-121">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5668a-122">Ссылка на экземпляр, представляющий общую папку принтера в этой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="5668a-122">Reference to the instance representing the share of the printer in this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5668a-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5668a-123">Remarks</span></span>

<span data-ttu-id="5668a-124">Класс **Win32 \_ принтершаре** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5668a-124">The **Win32\_PrinterShare** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5668a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="5668a-125">Requirements</span></span>



| <span data-ttu-id="5668a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="5668a-126">Requirement</span></span> | <span data-ttu-id="5668a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="5668a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5668a-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5668a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5668a-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5668a-129">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="5668a-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5668a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5668a-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5668a-131">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="5668a-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5668a-132">Namespace</span></span><br/>                | <span data-ttu-id="5668a-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5668a-133">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="5668a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5668a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5668a-135"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5668a-135"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="5668a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5668a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5668a-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5668a-137"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="5668a-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5668a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5668a-139">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="5668a-139">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
