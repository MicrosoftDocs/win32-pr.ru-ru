---
description: Обновляет родительский объект для указанных конечных и дочерних файлов виртуального жесткого диска.
ms.assetid: 5ad41218-bcfd-449a-a66e-2096a1d96bf5
title: Метод Сетпарентвиртуалхарддиск класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetParentVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f1d14d3b2ee19a9768e1ee9ed9333a452153cc9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683368"
---
# <a name="setparentvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="5e4ca-103">Метод Сетпарентвиртуалхарддиск \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="5e4ca-103">SetParentVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="5e4ca-104">Обновляет родительский объект для указанных конечных и дочерних файлов виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="5e4ca-104">Updates the parent for the specified leaf and child virtual hard disk files.</span></span> <span data-ttu-id="5e4ca-105">Ограничения на использование для этого метода см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="5e4ca-105">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e4ca-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e4ca-106">Syntax</span></span>


```mof
uint32 SetParentVirtualHardDisk(
  [in]  string              ChildPath,
  [in]  string              ParentPath,
  [in]  string              LeafPath,
  [in]  boolean             IgnoreIDMismatch,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5e4ca-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e4ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e4ca-108">*ChildPath* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e4ca-108">*ChildPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e4ca-109">Полный путь, указывающий расположение файла дочернего виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="5e4ca-109">A fully qualified path that specifies the location of the child virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="5e4ca-110">*Парентпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e4ca-110">*ParentPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e4ca-111">Полный путь, указывающий расположение файла родительского виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="5e4ca-111">A fully qualified path that specifies the location of the parent virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="5e4ca-112">*Леафпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e4ca-112">*LeafPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e4ca-113">Полный путь, указывающий расположение конечного файла виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="5e4ca-113">A fully qualified path that specifies the location of the leaf virtual hard disk file.</span></span> <span data-ttu-id="5e4ca-114">Параметр может иметь **значение NULL** , если виртуальный жесткий диск находится в автономном режиме, но должен быть указан, если используется виртуальный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="5e4ca-114">The parameter can be **Null** if the virtual hard disk is offline, but must be specified if the virtual hard disk is in use.</span></span>

</dd> <dt>

<span data-ttu-id="5e4ca-115">*Игнореидмисматч* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e4ca-115">*IgnoreIDMismatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e4ca-116">Указывает, следует ли принудительно задавать родительский диск, если идентификаторы виртуальных дисков не совпадают.</span><span class="sxs-lookup"><span data-stu-id="5e4ca-116">Indicates if the parent should be forcibly set when the virtual disk identifiers do not match.</span></span> <span data-ttu-id="5e4ca-117">Этот параметр следует использовать с осторожностью, так как если новый родительский виртуальный жесткий диск не идентичен исходному родителю, может произойти повреждение данных.</span><span class="sxs-lookup"><span data-stu-id="5e4ca-117">This parameter must be used with caution because if the new parent virtual hard disk is not identical to the original parent, data corruption can occur.</span></span>

</dd> <dt>

<span data-ttu-id="5e4ca-118">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5e4ca-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e4ca-119">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5e4ca-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e4ca-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e4ca-120">Return value</span></span>

<span data-ttu-id="5e4ca-121">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5e4ca-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="5e4ca-122">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="5e4ca-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5e4ca-123">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="5e4ca-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5e4ca-124">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="5e4ca-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5e4ca-125">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="5e4ca-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5e4ca-126">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="5e4ca-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5e4ca-127">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="5e4ca-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5e4ca-128">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="5e4ca-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5e4ca-129">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="5e4ca-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5e4ca-130">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="5e4ca-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5e4ca-131">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="5e4ca-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5e4ca-132">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="5e4ca-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5e4ca-133">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="5e4ca-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5e4ca-134">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="5e4ca-134">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="5e4ca-135">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="5e4ca-135">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="5e4ca-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e4ca-136">Remarks</span></span>

<span data-ttu-id="5e4ca-137">С этим методом можно использовать только следующие типы виртуальных жестких дисков:</span><span class="sxs-lookup"><span data-stu-id="5e4ca-137">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="5e4ca-138">Разностный виртуальный жесткий диск</span><span class="sxs-lookup"><span data-stu-id="5e4ca-138">Differencing VHD</span></span>
-   <span data-ttu-id="5e4ca-139">Разностные VHDX</span><span class="sxs-lookup"><span data-stu-id="5e4ca-139">Differencing VHDX</span></span>

<span data-ttu-id="5e4ca-140">Доступ к классу [**\_ ) мсвм**](msvm-imagemanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="5e4ca-140">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5e4ca-141">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5e4ca-141">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e4ca-142">Требования</span><span class="sxs-lookup"><span data-stu-id="5e4ca-142">Requirements</span></span>



| <span data-ttu-id="5e4ca-143">Требование</span><span class="sxs-lookup"><span data-stu-id="5e4ca-143">Requirement</span></span> | <span data-ttu-id="5e4ca-144">Значение</span><span class="sxs-lookup"><span data-stu-id="5e4ca-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e4ca-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e4ca-145">Minimum supported client</span></span><br/> | <span data-ttu-id="5e4ca-146">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5e4ca-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5e4ca-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e4ca-147">Minimum supported server</span></span><br/> | <span data-ttu-id="5e4ca-148">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5e4ca-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5e4ca-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5e4ca-149">Namespace</span></span><br/>                | <span data-ttu-id="5e4ca-150">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="5e4ca-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5e4ca-151">MOF</span><span class="sxs-lookup"><span data-stu-id="5e4ca-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e4ca-152"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e4ca-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e4ca-153">DLL</span><span class="sxs-lookup"><span data-stu-id="5e4ca-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e4ca-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5e4ca-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5e4ca-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e4ca-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e4ca-156">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="5e4ca-156">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

