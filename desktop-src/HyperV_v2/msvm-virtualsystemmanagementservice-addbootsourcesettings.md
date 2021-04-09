---
description: Добавляет источники загрузки в конфигурацию виртуальной системы при применении к &\# 0034; state&\# 0034; Конфигурация виртуальной системы.
ms.assetid: 2d091554-73d4-47c6-a0c2-97644fc9abe9
title: Метод Аддбутсаурцесеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e20a1184e11113ba25ac060ec19dab5d2391b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143882"
---
# <a name="addbootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="308cd-103">Метод Аддбутсаурцесеттингс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="308cd-103">AddBootSourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="308cd-104">Добавляет исходные загрузочные источники в конфигурацию виртуальной системы при их применении к конфигурации виртуальной системы "состояние".</span><span class="sxs-lookup"><span data-stu-id="308cd-104">Adds boot sources to a virtual system configuration when applied to a "state" virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="308cd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="308cd-105">Syntax</span></span>


```mof
uint32 AddBootSourceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           BootSourceSettings[],
  [out] CIM_SettingData              REF ResultingBootSourceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="308cd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="308cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="308cd-107">*Аффектедконфигуратион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="308cd-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="308cd-108">[**\_ Виртуалсистемсеттингдата CIM**](cim-virtualsystemsettingdata.md) , содержащий затронутую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="308cd-108">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) containing the affected configuration.</span></span>

</dd> <dt>

<span data-ttu-id="308cd-109">*Бутсаурцесеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="308cd-109">*BootSourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="308cd-110">Массив, содержащий параметры источника загрузки.</span><span class="sxs-lookup"><span data-stu-id="308cd-110">An array containing the boot source settings.</span></span>

</dd> <dt>

<span data-ttu-id="308cd-111">*Ресултингбутсаурцесеттингс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="308cd-111">*ResultingBootSourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="308cd-112">При успешном выполнении возвращает [**значение \_ SettingData CIM**](cim-settingdata.md) с результирующими параметрами источника загрузки.</span><span class="sxs-lookup"><span data-stu-id="308cd-112">On success, returns a [**CIM\_SettingData**](cim-settingdata.md) with the resulting boot source settings.</span></span>

</dd> <dt>

<span data-ttu-id="308cd-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="308cd-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="308cd-114">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="308cd-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="308cd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="308cd-115">Return value</span></span>

<span data-ttu-id="308cd-116">При успешном выполнении возвращает 0 или 4096; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="308cd-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="308cd-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="308cd-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="308cd-118">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="308cd-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="308cd-119">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="308cd-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="308cd-120">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="308cd-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="308cd-121">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="308cd-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="308cd-122">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="308cd-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="308cd-123">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="308cd-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="308cd-124">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="308cd-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="308cd-125">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="308cd-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="308cd-126">Требования</span><span class="sxs-lookup"><span data-stu-id="308cd-126">Requirements</span></span>



| <span data-ttu-id="308cd-127">Требование</span><span class="sxs-lookup"><span data-stu-id="308cd-127">Requirement</span></span> | <span data-ttu-id="308cd-128">Значение</span><span class="sxs-lookup"><span data-stu-id="308cd-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="308cd-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="308cd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="308cd-130">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="308cd-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="308cd-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="308cd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="308cd-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="308cd-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="308cd-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="308cd-133">Namespace</span></span><br/>                | <span data-ttu-id="308cd-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="308cd-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="308cd-135">MOF</span><span class="sxs-lookup"><span data-stu-id="308cd-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="308cd-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="308cd-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="308cd-137">DLL</span><span class="sxs-lookup"><span data-stu-id="308cd-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="308cd-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="308cd-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="308cd-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="308cd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="308cd-140">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="308cd-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

