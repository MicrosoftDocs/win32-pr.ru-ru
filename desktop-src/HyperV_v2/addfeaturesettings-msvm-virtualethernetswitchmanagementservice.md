---
description: Добавляет параметры компонентов в конфигурацию порта коммутатора Ethernet.
ms.assetid: 628a6546-cc78-4fde-be0c-533a2c3f9483
title: Метод Аддфеатуресеттингс класса Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e3b46a26d3c67f5efce4944c8b2e874febced32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998567"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="5b9c0-103">Метод Аддфеатуресеттингс \_ класса Виртуалесернетсвитчманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="5b9c0-103">AddFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="5b9c0-104">Добавляет параметры компонентов в конфигурацию порта коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="5b9c0-104">Adds feature settings to the configuration of an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b9c0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b9c0-105">Syntax</span></span>


```mof
uint32 AddFeatureSettings(
  [in]  CIM_SettingData         REF AffectedConfiguration,
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5b9c0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b9c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b9c0-107">*Аффектедконфигуратион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5b9c0-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b9c0-108">Ссылка на производный класс " [**\_ SettingData" CIM**](/previous-versions//cc136911(v=vs.85)) , представляющий затронутый порт коммутатора Ethernet или конфигурацию коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="5b9c0-108">A reference to a [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) derived class that represents the affected Ethernet switch port or Ethernet switch configuration.</span></span>

</dd> <dt>

<span data-ttu-id="5b9c0-109">*Феатуресеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5b9c0-109">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b9c0-110">Массив строк, содержащий внедренный экземпляр класса, производного от класса [**мсвм \_ феатуресеттингдата**](msvm-featuresettingdata.md) , который описывает параметры компонентов, добавляемых в конфигурацию порта коммутатора.</span><span class="sxs-lookup"><span data-stu-id="5b9c0-110">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class, that describes the feature settings to be added to the switch port configuration.</span></span>

</dd> <dt>

<span data-ttu-id="5b9c0-111">*Ресултингфеатуресеттингс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5b9c0-111">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b9c0-112">Массив ссылок на экземпляры класса [**мсвм \_ феатуресеттингдата**](msvm-featuresettingdata.md) , представляющие добавленные параметры функции.</span><span class="sxs-lookup"><span data-stu-id="5b9c0-112">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the added feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="5b9c0-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5b9c0-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b9c0-114">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5b9c0-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b9c0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b9c0-115">Return value</span></span>

<span data-ttu-id="5b9c0-116">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5b9c0-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="5b9c0-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="5b9c0-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5b9c0-118">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="5b9c0-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5b9c0-119">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="5b9c0-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5b9c0-120">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="5b9c0-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5b9c0-121">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="5b9c0-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5b9c0-122">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="5b9c0-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5b9c0-123">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="5b9c0-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5b9c0-124">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="5b9c0-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="5b9c0-125">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="5b9c0-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5b9c0-126">Требования</span><span class="sxs-lookup"><span data-stu-id="5b9c0-126">Requirements</span></span>



| <span data-ttu-id="5b9c0-127">Требование</span><span class="sxs-lookup"><span data-stu-id="5b9c0-127">Requirement</span></span> | <span data-ttu-id="5b9c0-128">Значение</span><span class="sxs-lookup"><span data-stu-id="5b9c0-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b9c0-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b9c0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5b9c0-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5b9c0-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5b9c0-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b9c0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5b9c0-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5b9c0-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5b9c0-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5b9c0-133">Namespace</span></span><br/>                | <span data-ttu-id="5b9c0-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="5b9c0-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5b9c0-135">MOF</span><span class="sxs-lookup"><span data-stu-id="5b9c0-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b9c0-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b9c0-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b9c0-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5b9c0-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b9c0-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5b9c0-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5b9c0-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b9c0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b9c0-140">**модифифеатуресеттингс**</span><span class="sxs-lookup"><span data-stu-id="5b9c0-140">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="5b9c0-141">**ремовефеатуресеттингс**</span><span class="sxs-lookup"><span data-stu-id="5b9c0-141">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="5b9c0-142">**Мсвм \_ виртуалесернетсвитчманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="5b9c0-142">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

