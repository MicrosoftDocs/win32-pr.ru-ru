---
description: Экспортирует виртуальную машину или моментальный снимок виртуальной машины в файл.
ms.assetid: b88712e4-a1a6-4188-8082-f4973f89018d
title: Метод Експортсистемдефинитион класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ExportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9f6b6dc5728a4275965ccd482d851601ecd1c6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808380"
---
# <a name="exportsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="b3450-103">Метод Експортсистемдефинитион \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="b3450-103">ExportSystemDefinition method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="b3450-104">Экспортирует виртуальную машину или моментальный снимок виртуальной машины в файл.</span><span class="sxs-lookup"><span data-stu-id="b3450-104">Exports a virtual machine, or a snapshot of a virtual machine, to a file.</span></span> <span data-ttu-id="b3450-105">Виртуальная машина должна находиться в состоянии "отключено" или "сохранено" для экспорта.</span><span class="sxs-lookup"><span data-stu-id="b3450-105">The virtual machine must be in the "powered off" or "saved" state to be exported.</span></span> <span data-ttu-id="b3450-106">Виртуальная машина, связанные с ней параметры конфигурации и связанные с ней параметры ресурсов будут сохранены в результирующем файле.</span><span class="sxs-lookup"><span data-stu-id="b3450-106">The virtual machine, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3450-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3450-107">Syntax</span></span>


```mof
uint32 ExportSystemDefinition(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ExportDirectory,
  [in]  string                 ExportSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b3450-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3450-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3450-109">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3450-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3450-110">Ссылка на систему [**CIM, \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) представляющая экспортируемую виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="b3450-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) that represents the virtual machine to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="b3450-111">*Експортдиректори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3450-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3450-112">Полный путь к каталогу, в который должна быть экспортирована виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="b3450-112">The fully qualified path of the directory to which the virtual machine is to be exported.</span></span> <span data-ttu-id="b3450-113">Если свойство **креатевмекспортсубдиректори** класса [**мсвм \_ Виртуалсистемекспортсеттингдата**](msvm-virtualsystemexportsettingdata.md) в параметре *експортсеттингдата* имеет значение **true**, то этот каталог можно повторно использовать для экспорта нескольких виртуальных машин, и этот метод помещает каждое определение виртуальной машины в отдельный подкаталог под этим путем.</span><span class="sxs-lookup"><span data-stu-id="b3450-113">If the **CreateVmExportSubdirectory** property of the [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) class in the *ExportSettingData* parameter is set to **True**, then this directory can be reused for exporting multiple virtual machines and this method places each virtual machine definition in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="b3450-114">*Експортсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3450-114">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3450-115">Встроенный экземпляр класса [**мсвм \_ виртуалсистемекспортсеттингдата**](msvm-virtualsystemexportsettingdata.md) , представляющий параметры для операции экспорта.</span><span class="sxs-lookup"><span data-stu-id="b3450-115">An embedded instance of the [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) class that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="b3450-116">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b3450-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3450-117">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b3450-117">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3450-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3450-118">Return value</span></span>

<span data-ttu-id="b3450-119">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b3450-119">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b3450-120">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="b3450-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b3450-121">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="b3450-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b3450-122">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="b3450-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b3450-123">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="b3450-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b3450-124">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="b3450-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b3450-125">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="b3450-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b3450-126">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="b3450-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b3450-127">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="b3450-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b3450-128">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="b3450-128">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b3450-129">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="b3450-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b3450-130">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="b3450-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b3450-131">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="b3450-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b3450-132">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="b3450-132">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b3450-133">Требования</span><span class="sxs-lookup"><span data-stu-id="b3450-133">Requirements</span></span>



| <span data-ttu-id="b3450-134">Требование</span><span class="sxs-lookup"><span data-stu-id="b3450-134">Requirement</span></span> | <span data-ttu-id="b3450-135">Значение</span><span class="sxs-lookup"><span data-stu-id="b3450-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3450-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b3450-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b3450-137">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b3450-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b3450-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b3450-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b3450-139">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b3450-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b3450-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b3450-140">Namespace</span></span><br/>                | <span data-ttu-id="b3450-141">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="b3450-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b3450-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b3450-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3450-143"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3450-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3450-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b3450-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3450-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b3450-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b3450-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3450-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3450-147">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="b3450-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

