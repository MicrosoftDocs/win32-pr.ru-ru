---
description: Удаляет параметры виртуального ресурса из конфигурации виртуальной системы.
ms.assetid: 0deb7719-e605-4ba5-9bb2-037d0cafee24
title: Метод Ремовебутсаурцесеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2693be33d291ea5a975119a5478af580ef2bb3f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682495"
---
# <a name="removebootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="2bc9d-103">Метод Ремовебутсаурцесеттингс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="2bc9d-103">RemoveBootSourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="2bc9d-104">Удаляет параметры виртуального ресурса из конфигурации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="2bc9d-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="2bc9d-105">При применении к частям "текущей" конфигурации виртуальной системы, так как ресурсы активной виртуальной системы могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="2bc9d-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bc9d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2bc9d-106">Syntax</span></span>


```mof
uint32 RemoveBootSourceSettings(
  [in]  CIM_SettingData REF BootSourceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2bc9d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2bc9d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bc9d-108">*Бутсаурцесеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2bc9d-108">*BootSourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bc9d-109">Ссылка на массив SettingData объекта [**CIM \_**](cim-settingdata.md) , описывающий удаляемые параметры источника загрузки.</span><span class="sxs-lookup"><span data-stu-id="2bc9d-109">Reference to an array of [**CIM\_SettingData**](cim-settingdata.md) that describe the boot source settings to remove.</span></span>

</dd> <dt>

<span data-ttu-id="2bc9d-110">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2bc9d-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2bc9d-111">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2bc9d-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bc9d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2bc9d-112">Return value</span></span>

<span data-ttu-id="2bc9d-113">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="2bc9d-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="2bc9d-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="2bc9d-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2bc9d-115">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="2bc9d-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2bc9d-116">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="2bc9d-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2bc9d-117">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="2bc9d-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2bc9d-118">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="2bc9d-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2bc9d-119">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="2bc9d-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2bc9d-120">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="2bc9d-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2bc9d-121">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="2bc9d-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2bc9d-122">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="2bc9d-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2bc9d-123">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="2bc9d-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2bc9d-124">Требования</span><span class="sxs-lookup"><span data-stu-id="2bc9d-124">Requirements</span></span>



| <span data-ttu-id="2bc9d-125">Требование</span><span class="sxs-lookup"><span data-stu-id="2bc9d-125">Requirement</span></span> | <span data-ttu-id="2bc9d-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2bc9d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc9d-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2bc9d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2bc9d-128">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2bc9d-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2bc9d-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2bc9d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2bc9d-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2bc9d-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2bc9d-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2bc9d-131">Namespace</span></span><br/>                | <span data-ttu-id="2bc9d-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="2bc9d-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2bc9d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="2bc9d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bc9d-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2bc9d-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2bc9d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2bc9d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bc9d-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2bc9d-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2bc9d-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2bc9d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bc9d-138">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="2bc9d-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

