---
description: Указывает на запись, исправленную проверку компьютера MCA (CMC) или исправленную ошибку платформы (CPE). Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: 4edbca20-2525-4e35-ab79-8cf421343144
title: Класс MSMCAInfo_Entry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_Entry
- MSMCAInfo_Entry.Data
- MSMCAInfo_Entry.Length
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cda6abba06dc4d4f3fec3a4763391eee1fa81274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712613"
---
# <a name="msmcainfo_entry-class"></a><span data-ttu-id="63e3b-104">\_Класс записи мсмкаинфо</span><span class="sxs-lookup"><span data-stu-id="63e3b-104">MSMCAInfo\_Entry class</span></span>

<span data-ttu-id="63e3b-105">Класс **\_ записи мсмкаинфо** указывает на запись, исправленную проверку компьютера (CMC) или исправленную ошибку платформы (CPE).</span><span class="sxs-lookup"><span data-stu-id="63e3b-105">The **MSMCAInfo\_Entry** class indicates an MCA, corrected machine check (CMC), or corrected platform error (CPE) information entry.</span></span> <span data-ttu-id="63e3b-106">Этот класс доступен только в 64-разрядных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="63e3b-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="63e3b-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="63e3b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="63e3b-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="63e3b-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e3b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63e3b-109">Syntax</span></span>

``` syntax
class MSMCAInfo_Entry : MSMCAInfo
{
  uint8  Data[];
  uint32 Length;
};
```

## <a name="members"></a><span data-ttu-id="63e3b-110">Члены</span><span class="sxs-lookup"><span data-stu-id="63e3b-110">Members</span></span>

<span data-ttu-id="63e3b-111">Класс **\_ записи мсмкаинфо** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="63e3b-111">The **MSMCAInfo\_Entry** class has these types of members:</span></span>

-   [<span data-ttu-id="63e3b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="63e3b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63e3b-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="63e3b-113">Properties</span></span>

<span data-ttu-id="63e3b-114">Класс **\_ записи мсмкаинфо** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="63e3b-114">The **MSMCAInfo\_Entry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63e3b-115">**Data**</span><span class="sxs-lookup"><span data-stu-id="63e3b-115">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e3b-116">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="63e3b-116">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="63e3b-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e3b-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e3b-118">Массив целых чисел, содержащий полную запись об ошибке MCA, сообщаемую уровнем абстрагирования системы (SAL).</span><span class="sxs-lookup"><span data-stu-id="63e3b-118">Integer array that contains a complete MCA error record as reported by the system abstraction layer (SAL).</span></span> <span data-ttu-id="63e3b-119">SAL — это код, записываемый в ПЗУ, который вызывается операционной системой для выполнения операций, зависящих от платформы.</span><span class="sxs-lookup"><span data-stu-id="63e3b-119">The SAL is code burned into ROM that the operating system calls to perform platform-dependent operations.</span></span> <span data-ttu-id="63e3b-120">Он аналогичен BIOS на платформе x86.</span><span class="sxs-lookup"><span data-stu-id="63e3b-120">It is similar to the BIOS on an x86 platform.</span></span>

</dd> <dt>

<span data-ttu-id="63e3b-121">**Длина**</span><span class="sxs-lookup"><span data-stu-id="63e3b-121">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e3b-122">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63e3b-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63e3b-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e3b-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e3b-124">Число байтов в записи об ошибке.</span><span class="sxs-lookup"><span data-stu-id="63e3b-124">Number of bytes in the error record.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63e3b-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63e3b-125">Remarks</span></span>

<span data-ttu-id="63e3b-126">Класс **\_ записи мсмкаинфо** является производным от [**мсмкаинфо**](msmcainfo.md).</span><span class="sxs-lookup"><span data-stu-id="63e3b-126">The **MSMCAInfo\_Entry** class is derived from [**MSMCAInfo**](msmcainfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="63e3b-127">Требования</span><span class="sxs-lookup"><span data-stu-id="63e3b-127">Requirements</span></span>



| <span data-ttu-id="63e3b-128">Требование</span><span class="sxs-lookup"><span data-stu-id="63e3b-128">Requirement</span></span> | <span data-ttu-id="63e3b-129">Значение</span><span class="sxs-lookup"><span data-stu-id="63e3b-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63e3b-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63e3b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="63e3b-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="63e3b-131">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="63e3b-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63e3b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="63e3b-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="63e3b-133">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="63e3b-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="63e3b-134">Namespace</span></span><br/>                | <span data-ttu-id="63e3b-135">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="63e3b-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="63e3b-136">MOF</span><span class="sxs-lookup"><span data-stu-id="63e3b-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63e3b-137"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63e3b-137"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="63e3b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="63e3b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63e3b-139"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63e3b-139"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63e3b-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63e3b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e3b-141">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="63e3b-141">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="63e3b-142">**мсмкаинфо**</span><span class="sxs-lookup"><span data-stu-id="63e3b-142">**MSMCAInfo**</span></span>](msmcainfo.md)
</dt> </dl>

 

 




