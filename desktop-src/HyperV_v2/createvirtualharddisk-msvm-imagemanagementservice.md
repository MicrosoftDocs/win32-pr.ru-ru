---
description: Создает файл виртуального жесткого диска.
ms.assetid: 6c136000-1df2-4456-833c-094671408338
title: Метод Креатевиртуалхарддиск класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CreateVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b80a309274eb51ad7aff768898a9c3bd211f37cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683981"
---
# <a name="createvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="2525d-103">Метод Креатевиртуалхарддиск \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="2525d-103">CreateVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="2525d-104">Создает файл виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="2525d-104">Creates a virtual hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2525d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2525d-105">Syntax</span></span>


```mof
uint32 CreateVirtualHardDisk(
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2525d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2525d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2525d-107">*Виртуалдисксеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2525d-107">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2525d-108">Строка, содержащая встроенный экземпляр класса [**мсвм \_ виртуалхарддисксеттингдата**](msvm-virtualharddisksettingdata.md) , который используется для определения атрибутов создаваемого виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="2525d-108">String that contains an embedded instance of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that is used to define attributes of the virtual hard disk to be created.</span></span>

</dd> <dt>

<span data-ttu-id="2525d-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2525d-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2525d-110">Ссылка на задание (может иметь **значение NULL** , если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="2525d-110">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2525d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2525d-111">Return value</span></span>

<span data-ttu-id="2525d-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="2525d-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2525d-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="2525d-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2525d-114">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="2525d-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2525d-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="2525d-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2525d-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="2525d-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2525d-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="2525d-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2525d-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="2525d-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2525d-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="2525d-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2525d-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="2525d-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2525d-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="2525d-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2525d-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="2525d-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2525d-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="2525d-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2525d-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="2525d-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2525d-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="2525d-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="2525d-126">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="2525d-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="2525d-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2525d-127">Remarks</span></span>

<span data-ttu-id="2525d-128">Доступ к классу [**\_ ) мсвм**](msvm-imagemanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="2525d-128">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2525d-129">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2525d-129">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2525d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="2525d-130">Requirements</span></span>



| <span data-ttu-id="2525d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="2525d-131">Requirement</span></span> | <span data-ttu-id="2525d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2525d-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2525d-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2525d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2525d-134">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2525d-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2525d-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2525d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2525d-136">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2525d-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2525d-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2525d-137">Namespace</span></span><br/>                | <span data-ttu-id="2525d-138">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="2525d-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2525d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2525d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2525d-140"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2525d-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2525d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2525d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2525d-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2525d-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2525d-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2525d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2525d-144">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="2525d-144">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

