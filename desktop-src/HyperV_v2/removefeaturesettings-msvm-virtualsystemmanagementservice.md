---
description: Удаляет параметры компонентов из Ethernet-подключения виртуальной машины.
ms.assetid: 457056d0-7e69-47e4-8744-0136a1816f4a
title: Метод Ремовефеатуресеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c29151f6544d7eb803ec72ee49e455556d8b2d70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663852"
---
# <a name="removefeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="c230f-103">Метод Ремовефеатуресеттингс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="c230f-103">RemoveFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="c230f-104">Удаляет параметры компонентов из Ethernet-подключения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c230f-104">Removes feature settings from a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c230f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c230f-105">Syntax</span></span>


```mof
uint32 RemoveFeatureSettings(
  [in]  Msvm_EthernetSwitchPortFeatureSettingData REF FeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c230f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c230f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c230f-107">*Феатуресеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c230f-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c230f-108">Массив строк, содержащий внедренный экземпляр класса, производного от класса [**мсвм \_ есернетсвитчфеатуресеттингдата**](msvm-ethernetswitchfeaturesettingdata.md) , который определяет удаляемые параметры компонентов.</span><span class="sxs-lookup"><span data-stu-id="c230f-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class, that defines the feature settings to be removed.</span></span> <span data-ttu-id="c230f-109">Свойство **InstanceId** каждого из этих экземпляров определяет удаляемые параметры компонентов.</span><span class="sxs-lookup"><span data-stu-id="c230f-109">The **InstanceID** property of each of these instances identifies the feature settings to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="c230f-110">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c230f-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c230f-111">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c230f-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c230f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c230f-112">Return value</span></span>

<span data-ttu-id="c230f-113">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c230f-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c230f-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="c230f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c230f-115">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="c230f-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c230f-116">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="c230f-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c230f-117">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="c230f-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c230f-118">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="c230f-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c230f-119">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="c230f-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c230f-120">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="c230f-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c230f-121">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="c230f-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c230f-122">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="c230f-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="c230f-123">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="c230f-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c230f-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c230f-124">Requirements</span></span>



| <span data-ttu-id="c230f-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c230f-125">Requirement</span></span> | <span data-ttu-id="c230f-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c230f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c230f-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c230f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c230f-128">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c230f-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c230f-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c230f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c230f-130">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c230f-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c230f-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c230f-131">Namespace</span></span><br/>                | <span data-ttu-id="c230f-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c230f-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c230f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c230f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c230f-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c230f-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c230f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c230f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c230f-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c230f-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c230f-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c230f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c230f-138">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="c230f-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

