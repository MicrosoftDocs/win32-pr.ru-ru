---
description: Удаляет параметры компонента с порта коммутатора Ethernet.
ms.assetid: 3d45259e-34e4-417b-a895-4926b0eaaf59
title: Метод Ремовефеатуресеттингс класса Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.RemoveFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 919e2b69e2a0ef215a522c601088cb7aa2976a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683849"
---
# <a name="removefeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="ef466-103">Метод Ремовефеатуресеттингс \_ класса Виртуалесернетсвитчманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="ef466-103">RemoveFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="ef466-104">Удаляет параметры компонента с порта коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="ef466-104">Removes feature settings from an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef466-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef466-105">Syntax</span></span>


```mof
uint32 RemoveFeatureSettings(
  [in]  Msvm_FeatureSettingData REF FeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ef466-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef466-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef466-107">*Феатуресеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef466-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef466-108">Массив ссылок на экземпляры класса [**мсвм \_ феатуресеттингдата**](msvm-featuresettingdata.md) , представляющие удаляемые параметры компонентов.</span><span class="sxs-lookup"><span data-stu-id="ef466-108">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the feature settings to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="ef466-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ef466-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef466-110">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ef466-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef466-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef466-111">Return value</span></span>

<span data-ttu-id="ef466-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ef466-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ef466-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="ef466-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ef466-114">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="ef466-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ef466-115">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="ef466-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ef466-116">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="ef466-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ef466-117">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="ef466-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ef466-118">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="ef466-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ef466-119">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ef466-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ef466-120">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="ef466-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ef466-121">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="ef466-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="ef466-122">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="ef466-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ef466-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ef466-123">Requirements</span></span>



| <span data-ttu-id="ef466-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ef466-124">Requirement</span></span> | <span data-ttu-id="ef466-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ef466-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef466-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef466-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ef466-127">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ef466-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ef466-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef466-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ef466-129">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ef466-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ef466-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ef466-130">Namespace</span></span><br/>                | <span data-ttu-id="ef466-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ef466-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ef466-132">MOF</span><span class="sxs-lookup"><span data-stu-id="ef466-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef466-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef466-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef466-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ef466-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef466-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef466-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ef466-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef466-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef466-137">**аддфеатуресеттингс**</span><span class="sxs-lookup"><span data-stu-id="ef466-137">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="ef466-138">**модифифеатуресеттингс**</span><span class="sxs-lookup"><span data-stu-id="ef466-138">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="ef466-139">**Мсвм \_ виртуалесернетсвитчманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="ef466-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

