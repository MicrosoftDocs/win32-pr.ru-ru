---
description: Уничтожает виртуальный коммутатор.
ms.assetid: f0b6b4cc-e9b7-4255-a9e1-a2a826b8f119
title: Метод Дестройсистем класса Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d8f01a3f72d15fba908c7891f76b4128a1ee8200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683980"
---
# <a name="destroysystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="55332-103">Метод Дестройсистем \_ класса Виртуалесернетсвитчманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="55332-103">DestroySystem method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="55332-104">Уничтожает виртуальный коммутатор.</span><span class="sxs-lookup"><span data-stu-id="55332-104">Destroys a virtual switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="55332-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55332-105">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="55332-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="55332-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55332-107">*Аффектедсистем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55332-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55332-108">Ссылка на экземпляр класса [**мсвм \_ виртуалесернетсвитч**](msvm-virtualethernetswitch.md) , представляющий виртуальный коммутатор, который необходимо уничтожить.</span><span class="sxs-lookup"><span data-stu-id="55332-108">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch that is to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="55332-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="55332-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55332-110">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="55332-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55332-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55332-111">Return value</span></span>

<span data-ttu-id="55332-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="55332-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="55332-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="55332-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="55332-114">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="55332-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="55332-115">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="55332-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="55332-116">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="55332-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="55332-117">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="55332-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="55332-118">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="55332-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="55332-119">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="55332-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="55332-120">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="55332-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="55332-121">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="55332-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="55332-122">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="55332-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="55332-123">Требования</span><span class="sxs-lookup"><span data-stu-id="55332-123">Requirements</span></span>



| <span data-ttu-id="55332-124">Требование</span><span class="sxs-lookup"><span data-stu-id="55332-124">Requirement</span></span> | <span data-ttu-id="55332-125">Значение</span><span class="sxs-lookup"><span data-stu-id="55332-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55332-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55332-126">Minimum supported client</span></span><br/> | <span data-ttu-id="55332-127">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="55332-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="55332-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55332-128">Minimum supported server</span></span><br/> | <span data-ttu-id="55332-129">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="55332-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="55332-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="55332-130">Namespace</span></span><br/>                | <span data-ttu-id="55332-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="55332-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="55332-132">MOF</span><span class="sxs-lookup"><span data-stu-id="55332-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55332-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55332-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="55332-134">DLL</span><span class="sxs-lookup"><span data-stu-id="55332-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55332-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="55332-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="55332-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55332-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55332-137">**Мсвм \_ виртуалесернетсвитчманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="55332-137">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

