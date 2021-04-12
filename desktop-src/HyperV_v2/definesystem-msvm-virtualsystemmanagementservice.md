---
description: Создает новый экземпляр виртуальной машины.
ms.assetid: 15BC967D-F392-45A6-ACF6-5C2F2334AAE6
title: Метод Дефинесистем класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 965d24313607a767d546503d005a6493234b2f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265666"
---
# <a name="definesystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="97a85-103">Метод Дефинесистем \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="97a85-103">DefineSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="97a85-104">Создает новый экземпляр виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="97a85-104">Creates a new virtual machine instance.</span></span> <span data-ttu-id="97a85-105">Свойства, которые не указаны, будут заполнены значениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="97a85-105">Properties that are not specified will be populated with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="97a85-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97a85-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="97a85-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="97a85-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97a85-108">*SystemSettings* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="97a85-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97a85-109">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="97a85-109">Type: **string**</span></span>

<span data-ttu-id="97a85-110">Встроенный экземпляр класса [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , который используется для определения атрибутов создаваемой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="97a85-110">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that is used to define the attributes of the virtual machine to be created.</span></span> <span data-ttu-id="97a85-111">Этот параметр обязателен.</span><span class="sxs-lookup"><span data-stu-id="97a85-111">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="97a85-112">*Ресаурцесеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="97a85-112">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97a85-113">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="97a85-113">Type: **string\[\]**</span></span>

<span data-ttu-id="97a85-114">Ряд внедренных экземпляров класса [**мсвм \_ ресаурцеаллокатионсеттингдата**](msvm-resourceallocationsettingdata.md) (или производных классов).</span><span class="sxs-lookup"><span data-stu-id="97a85-114">A number of embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class (or derived classes thereof).</span></span> <span data-ttu-id="97a85-115">Вместе эти экземпляры описывают виртуальные ресурсы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="97a85-115">Together these instances describe the virtual resources of the virtual machine.</span></span> <span data-ttu-id="97a85-116">Для виртуальной машины будет создан набор устройств по умолчанию независимо от того, задан ли этот параметр.</span><span class="sxs-lookup"><span data-stu-id="97a85-116">A default set of devices will be created for the virtual machine regardless of whether this parameter is set.</span></span> <span data-ttu-id="97a85-117">Например, процессор и память автоматически создаются и настраиваются со значениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="97a85-117">For example, processor and memory are automatically created and configured with default values.</span></span>

</dd> <dt>

<span data-ttu-id="97a85-118">*Референцеконфигуратион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="97a85-118">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97a85-119">Тип: **CIM \_ виртуалсистемсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="97a85-119">Type: **CIM\_VirtualSystemSettingData**</span></span>

<span data-ttu-id="97a85-120">Ссылка на экземпляр класса [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , который является объектом верхнего уровня эталонной конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="97a85-120">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that is the top level object of a reference virtual machine configuration.</span></span> <span data-ttu-id="97a85-121">Конфигурация ссылки используется для дополнения конфигурации новой виртуальной машины, если параметры *SystemSettings* и *ресаурцесеттингс* не предпредоставил соответствующие сведения.</span><span class="sxs-lookup"><span data-stu-id="97a85-121">The reference configuration is used to complement the configuration of the new virtual machine if the *SystemSettings* and *ResourceSettings* parameters did not provide respective information.</span></span>

</dd> <dt>

<span data-ttu-id="97a85-122">*Ресултингсистем* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="97a85-122">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97a85-123">Тип: **CIM \_ ComputerSystem** .</span><span class="sxs-lookup"><span data-stu-id="97a85-123">Type: **CIM\_ComputerSystem**</span></span>

<span data-ttu-id="97a85-124">Ссылка на экземпляр класса платформы [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий только что созданную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="97a85-124">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the newly created virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="97a85-125">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="97a85-125">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97a85-126">Тип: **CIM \_ конкретежоб**</span><span class="sxs-lookup"><span data-stu-id="97a85-126">Type: **CIM\_ConcreteJob**</span></span>

<span data-ttu-id="97a85-127">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="97a85-127">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97a85-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97a85-128">Return value</span></span>

<span data-ttu-id="97a85-129">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97a85-129">Type: **uint32**</span></span>

<span data-ttu-id="97a85-130">Если этот метод выполняется синхронно, он возвращает 0, если он выполняется.</span><span class="sxs-lookup"><span data-stu-id="97a85-130">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="97a85-131">Если этот метод выполняется асинхронно, возвращается 4096, а для отслеживания хода выполнения асинхронной операции можно использовать выходной параметр *задания* .</span><span class="sxs-lookup"><span data-stu-id="97a85-131">If this method is executed asynchronously, it returns 4096 and the *Job* output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="97a85-132">Любое другое возвращаемое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="97a85-132">Any other return value indicates an error.</span></span>

<dl> <dt>

<span data-ttu-id="97a85-133">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="97a85-133">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="97a85-134">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="97a85-134">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="97a85-135">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="97a85-135">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="97a85-136">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="97a85-136">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="97a85-137">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="97a85-137">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="97a85-138">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="97a85-138">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="97a85-139">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="97a85-139">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="97a85-140">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="97a85-140">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="97a85-141">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="97a85-141">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="97a85-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97a85-142">Remarks</span></span>

<span data-ttu-id="97a85-143">Доступ к классу [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="97a85-143">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="97a85-144">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="97a85-144">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="97a85-145">Требования</span><span class="sxs-lookup"><span data-stu-id="97a85-145">Requirements</span></span>



| <span data-ttu-id="97a85-146">Требование</span><span class="sxs-lookup"><span data-stu-id="97a85-146">Requirement</span></span> | <span data-ttu-id="97a85-147">Значение</span><span class="sxs-lookup"><span data-stu-id="97a85-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97a85-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97a85-148">Minimum supported client</span></span><br/> | <span data-ttu-id="97a85-149">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="97a85-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="97a85-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97a85-150">Minimum supported server</span></span><br/> | <span data-ttu-id="97a85-151">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="97a85-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="97a85-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="97a85-152">Namespace</span></span><br/>                | <span data-ttu-id="97a85-153">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="97a85-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="97a85-154">MOF</span><span class="sxs-lookup"><span data-stu-id="97a85-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97a85-155"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97a85-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="97a85-156">DLL</span><span class="sxs-lookup"><span data-stu-id="97a85-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97a85-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="97a85-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="97a85-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97a85-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97a85-159">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="97a85-159">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

