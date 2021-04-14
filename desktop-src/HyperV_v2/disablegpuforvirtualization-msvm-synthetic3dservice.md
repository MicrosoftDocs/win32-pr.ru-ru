---
description: Отключает физический GPU для виртуализации.
ms.assetid: 280a3c25-7b8f-4113-bf35-171d15f4aea7
title: Метод Дисаблегпуфорвиртуализатион класса Msvm_Synthetic3DService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.DisableGPUForVirtualization
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2634a3196e0c59368002151426e6f1407a13db8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342635"
---
# <a name="disablegpuforvirtualization-method-of-the-msvm_synthetic3dservice-class"></a><span data-ttu-id="1dc0d-103">Метод Дисаблегпуфорвиртуализатион \_ класса Synthetic3DService мсвм</span><span class="sxs-lookup"><span data-stu-id="1dc0d-103">DisableGPUForVirtualization method of the Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="1dc0d-104">Отключает физический GPU для виртуализации.</span><span class="sxs-lookup"><span data-stu-id="1dc0d-104">Disables a physical GPU for virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dc0d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1dc0d-105">Syntax</span></span>


```mof
uint32 DisableGPUForVirtualization(
  [in]  Msvm_Physical3dGraphicsProcessor REF PhysicalGPU,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1dc0d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1dc0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dc0d-107">*Фисикалгпу* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1dc0d-107">*PhysicalGPU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dc0d-108">Ссылка на экземпляр класса [**мсвм \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) , который представляет физический GPU для отключения.</span><span class="sxs-lookup"><span data-stu-id="1dc0d-108">A reference to an instance of the [**Msvm\_Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) class that represents the physical GPU to be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="1dc0d-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1dc0d-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1dc0d-110">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1dc0d-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dc0d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1dc0d-111">Return value</span></span>

<span data-ttu-id="1dc0d-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1dc0d-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1dc0d-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="1dc0d-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1dc0d-114">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="1dc0d-114">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1dc0d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="1dc0d-115">Requirements</span></span>



| <span data-ttu-id="1dc0d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="1dc0d-116">Requirement</span></span> | <span data-ttu-id="1dc0d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1dc0d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc0d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1dc0d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1dc0d-119">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1dc0d-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1dc0d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1dc0d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1dc0d-121">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1dc0d-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1dc0d-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1dc0d-122">Namespace</span></span><br/>                | <span data-ttu-id="1dc0d-123">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="1dc0d-123">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1dc0d-124">MOF</span><span class="sxs-lookup"><span data-stu-id="1dc0d-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1dc0d-125"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1dc0d-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1dc0d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1dc0d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dc0d-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1dc0d-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1dc0d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1dc0d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dc0d-129">**Мсвм \_ Synthetic3DService**</span><span class="sxs-lookup"><span data-stu-id="1dc0d-129">**Msvm\_Synthetic3DService**</span></span>](msvm-synthetic3dservice.md)
</dt> </dl>

 

