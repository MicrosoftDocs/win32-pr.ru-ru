---
description: Изменяет параметры виртуального коммутатора.
ms.assetid: 8d323578-990f-483c-8515-8a21479767b1
title: Метод Модифисистемсеттингс класса Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3512debfd6d49e3c09cb8a508a7f0d748ab128e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683966"
---
# <a name="modifysystemsettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="ad3c9-103">Метод Модифисистемсеттингс \_ класса Виртуалесернетсвитчманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="ad3c9-103">ModifySystemSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="ad3c9-104">Изменяет параметры виртуального коммутатора.</span><span class="sxs-lookup"><span data-stu-id="ad3c9-104">Modifies virtual switch settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad3c9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad3c9-105">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ad3c9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad3c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad3c9-107">*SystemSettings* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad3c9-107">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad3c9-108">Встроенный экземпляр класса [**мсвм \_ виртуалесернетсвитчсеттингдата**](msvm-virtualethernetswitchsettingdata.md) , который содержит измененные аспекты виртуального коммутатора.</span><span class="sxs-lookup"><span data-stu-id="ad3c9-108">An embedded instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that contains the modified aspects of the virtual switch.</span></span> <span data-ttu-id="ad3c9-109">Свойство **InstanceId** определяет параметр виртуального коммутатора, который необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="ad3c9-109">The **InstanceID** property identifies the virtual switch setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="ad3c9-110">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ad3c9-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad3c9-111">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ad3c9-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad3c9-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad3c9-112">Return value</span></span>

<span data-ttu-id="ad3c9-113">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ad3c9-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ad3c9-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="ad3c9-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ad3c9-115">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="ad3c9-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ad3c9-116">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="ad3c9-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ad3c9-117">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="ad3c9-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ad3c9-118">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="ad3c9-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ad3c9-119">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="ad3c9-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ad3c9-120">**Несовместимые параметры** (6)</span><span class="sxs-lookup"><span data-stu-id="ad3c9-120">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ad3c9-121">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ad3c9-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ad3c9-122">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="ad3c9-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ad3c9-123">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="ad3c9-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="ad3c9-124">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="ad3c9-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ad3c9-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ad3c9-125">Requirements</span></span>



| <span data-ttu-id="ad3c9-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ad3c9-126">Requirement</span></span> | <span data-ttu-id="ad3c9-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ad3c9-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad3c9-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad3c9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ad3c9-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ad3c9-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ad3c9-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad3c9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ad3c9-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ad3c9-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ad3c9-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ad3c9-132">Namespace</span></span><br/>                | <span data-ttu-id="ad3c9-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ad3c9-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ad3c9-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ad3c9-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad3c9-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad3c9-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad3c9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ad3c9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad3c9-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ad3c9-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ad3c9-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad3c9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad3c9-139">**Мсвм \_ виртуалесернетсвитчманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="ad3c9-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

