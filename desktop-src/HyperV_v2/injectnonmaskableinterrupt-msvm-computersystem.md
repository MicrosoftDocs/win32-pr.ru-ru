---
description: Внедряет немаскируемое прерывание в виртуальную машину.
ms.assetid: 897AD1B9-0EDD-4DCE-963D-D5DE03AF55A9
title: 'Метод Msvm_ComputerSystem:: Инжектнонмаскаблеинтеррупт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.InjectNonMaskableInterrupt
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5798079a8866d9fb67356adff43c0ac1e993e6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662243"
---
# <a name="msvm_computersysteminjectnonmaskableinterrupt-method"></a><span data-ttu-id="957c3-103">Мсвм \_ ComputerSystem:: инжектнонмаскаблеинтеррупт, метод</span><span class="sxs-lookup"><span data-stu-id="957c3-103">Msvm\_ComputerSystem::InjectNonMaskableInterrupt method</span></span>

<span data-ttu-id="957c3-104">Внедряет немаскируемое прерывание в виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="957c3-104">Injects a non-maskable interrupt into the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="957c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="957c3-105">Syntax</span></span>


```C++
uint32 InjectNonMaskableInterrupt(
  [out] CIM_ConcreteJob Job
);
```



## <a name="parameters"></a><span data-ttu-id="957c3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="957c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="957c3-107">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="957c3-107">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="957c3-108">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)) , чтобы отвести состояние внедрения прерываний.</span><span class="sxs-lookup"><span data-stu-id="957c3-108">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) to track the status of the interrupt injection.</span></span> <span data-ttu-id="957c3-109">Если задача завершена, ссылка может иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="957c3-109">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="957c3-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="957c3-110">Return value</span></span>

<span data-ttu-id="957c3-111">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="957c3-111">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="957c3-112">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="957c3-112">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="957c3-113">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="957c3-113">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="957c3-114">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="957c3-114">**Access Denied** (32769)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="957c3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="957c3-115">Requirements</span></span>



| <span data-ttu-id="957c3-116">Требование</span><span class="sxs-lookup"><span data-stu-id="957c3-116">Requirement</span></span> | <span data-ttu-id="957c3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="957c3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="957c3-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="957c3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="957c3-119">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="957c3-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="957c3-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="957c3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="957c3-121">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="957c3-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="957c3-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="957c3-122">Namespace</span></span><br/>                | <span data-ttu-id="957c3-123">\\\\Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="957c3-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="957c3-124">MOF</span><span class="sxs-lookup"><span data-stu-id="957c3-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="957c3-125"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="957c3-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="957c3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="957c3-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="957c3-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="957c3-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="957c3-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="957c3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="957c3-129">**Мсвм \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="957c3-129">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

