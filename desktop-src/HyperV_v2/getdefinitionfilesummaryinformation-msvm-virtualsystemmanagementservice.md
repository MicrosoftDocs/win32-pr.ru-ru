---
description: Возвращает сводные данные о виртуальной машине для указанных файлов определения виртуальной машины.
ms.assetid: 5a3d7f2c-3b89-4dd6-909d-4452afc3705f
title: Метод Жетдефинитионфилесуммаринформатион класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetDefinitionFileSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a46daedd282d07c2367931a9f20a7fbfa1849f9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682798"
---
# <a name="getdefinitionfilesummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a4a3e-103">Метод Жетдефинитионфилесуммаринформатион \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="a4a3e-103">GetDefinitionFileSummaryInformation method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a4a3e-104">Возвращает сводные данные о виртуальной машине для указанных файлов определения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a4a3e-104">Returns virtual machine summary information for the specified virtual machine definition files.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4a3e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4a3e-105">Syntax</span></span>


```mof
uint32 GetDefinitionFileSummaryInformation(
  [in]  string                      DefinitionFiles[],
  [out] Msvm_SummaryInformationBase SummaryInformation[]
);
```



## <a name="parameters"></a><span data-ttu-id="a4a3e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4a3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4a3e-107">*Дефинитионфилес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4a3e-107">*DefinitionFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4a3e-108">Массив путей к XML-файлам конфигурации, для которых возвращаются сводные данные.</span><span class="sxs-lookup"><span data-stu-id="a4a3e-108">An array of paths to XML configuration files for which to return summary information.</span></span>

</dd> <dt>

<span data-ttu-id="a4a3e-109">*SummaryInformation* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a4a3e-109">*SummaryInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4a3e-110">Массив экземпляров [**мсвм \_ суммаринформатионбасе**](msvm-summaryinformation.md) , содержащих запрашиваемые сведения для виртуальных машин и (или) моментальных снимков, указанных в массиве *дефинитионфилес* .</span><span class="sxs-lookup"><span data-stu-id="a4a3e-110">An array of [**Msvm\_SummaryInformationBase**](msvm-summaryinformation.md) instances containing the requested information for the virtual machines and/or snapshots specified in the *DefinitionFiles* array.</span></span> <span data-ttu-id="a4a3e-111">Возвращаются только свойства **Name**, **ElementName**, **CreationTime** и **Notes** , все остальные свойства будут иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a4a3e-111">Only the **Name**, **ElementName**, **CreationTime**, and **Notes** properties are returned, all other properties will be **Null**.</span></span>

> [!Note]  

 

<span data-ttu-id="a4a3e-112">До Windows 10 версии 1703 тип данных был [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md).</span><span class="sxs-lookup"><span data-stu-id="a4a3e-112">Prior to Windows 10, version 1703, datatype was [**Msvm\_SummaryInformation**](msvm-summaryinformation.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4a3e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4a3e-113">Return value</span></span>

<span data-ttu-id="a4a3e-114">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a4a3e-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a4a3e-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="a4a3e-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a4a3e-116">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="a4a3e-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a4a3e-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="a4a3e-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a4a3e-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="a4a3e-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a4a3e-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="a4a3e-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a4a3e-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="a4a3e-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a4a3e-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="a4a3e-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a4a3e-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="a4a3e-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a4a3e-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="a4a3e-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a4a3e-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="a4a3e-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a4a3e-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="a4a3e-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a4a3e-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="a4a3e-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a4a3e-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="a4a3e-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a4a3e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="a4a3e-128">Requirements</span></span>



| <span data-ttu-id="a4a3e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="a4a3e-129">Requirement</span></span> | <span data-ttu-id="a4a3e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="a4a3e-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a3e-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4a3e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a4a3e-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a4a3e-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a4a3e-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4a3e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a4a3e-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a4a3e-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a4a3e-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a4a3e-135">Namespace</span></span><br/>                | <span data-ttu-id="a4a3e-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="a4a3e-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a4a3e-137">MOF</span><span class="sxs-lookup"><span data-stu-id="a4a3e-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4a3e-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4a3e-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4a3e-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a4a3e-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4a3e-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a4a3e-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a4a3e-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4a3e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4a3e-142">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="a4a3e-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




