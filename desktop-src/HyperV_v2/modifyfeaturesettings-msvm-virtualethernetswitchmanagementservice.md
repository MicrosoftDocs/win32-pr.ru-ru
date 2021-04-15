---
description: Изменяет настройки компонентов порта коммутатора Ethernet.
ms.assetid: 8c21a932-fffb-40fd-9166-d7e351329217
title: Метод Модифифеатуресеттингс класса Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0bee92019f9457a42a0c87ab619f7de1f7d203ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683690"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="f32cf-103">Метод Модифифеатуресеттингс \_ класса Виртуалесернетсвитчманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="f32cf-103">ModifyFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="f32cf-104">Изменяет настройки компонентов порта коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="f32cf-104">Modifies the feature settings of an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="f32cf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f32cf-105">Syntax</span></span>


```mof
uint32 ModifyFeatureSettings(
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f32cf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f32cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f32cf-107">*Феатуресеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f32cf-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f32cf-108">Массив строк, содержащий встроенный экземпляр класса, производного от класса [**мсвм \_ феатуресеттингдата**](msvm-featuresettingdata.md) , который описывает изменяемые параметры функции порта коммутатора.</span><span class="sxs-lookup"><span data-stu-id="f32cf-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class, that describes the switch port feature settings to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="f32cf-109">*Ресултингфеатуресеттингс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f32cf-109">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f32cf-110">Массив ссылок на экземпляры класса [**мсвм \_ феатуресеттингдата**](msvm-featuresettingdata.md) , представляющие измененные параметры функции.</span><span class="sxs-lookup"><span data-stu-id="f32cf-110">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the modified feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="f32cf-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f32cf-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f32cf-112">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f32cf-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f32cf-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f32cf-113">Return value</span></span>

<span data-ttu-id="f32cf-114">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f32cf-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f32cf-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="f32cf-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f32cf-116">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="f32cf-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f32cf-117">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="f32cf-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f32cf-118">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="f32cf-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f32cf-119">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="f32cf-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f32cf-120">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="f32cf-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f32cf-121">**Несовместимые параметры** (6)</span><span class="sxs-lookup"><span data-stu-id="f32cf-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f32cf-122">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="f32cf-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f32cf-123">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="f32cf-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f32cf-124">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f32cf-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f32cf-125">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="f32cf-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f32cf-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f32cf-126">Requirements</span></span>



| <span data-ttu-id="f32cf-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f32cf-127">Requirement</span></span> | <span data-ttu-id="f32cf-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f32cf-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f32cf-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f32cf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f32cf-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f32cf-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f32cf-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f32cf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f32cf-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f32cf-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f32cf-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f32cf-133">Namespace</span></span><br/>                | <span data-ttu-id="f32cf-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f32cf-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f32cf-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f32cf-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f32cf-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f32cf-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f32cf-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f32cf-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f32cf-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f32cf-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f32cf-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f32cf-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f32cf-140">**аддфеатуресеттингс**</span><span class="sxs-lookup"><span data-stu-id="f32cf-140">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="f32cf-141">**ремовефеатуресеттингс**</span><span class="sxs-lookup"><span data-stu-id="f32cf-141">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="f32cf-142">**Мсвм \_ виртуалесернетсвитчманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="f32cf-142">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

