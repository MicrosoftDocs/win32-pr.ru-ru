---
description: Останавливает гостевую службу.
ms.assetid: 67FFA46C-0B61-4845-A617-BA10F4D42CBC
title: 'Метод Msvm_GuestService:: No'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6c396078e2bd623a768f391a645091679694f453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897130"
---
# <a name="msvm_guestservicestopservice-method"></a><span data-ttu-id="4bff9-103">Мсвм \_ гуестсервице:: метод "</span><span class="sxs-lookup"><span data-stu-id="4bff9-103">Msvm\_GuestService::StopService method</span></span>

<span data-ttu-id="4bff9-104">Останавливает гостевую службу.</span><span class="sxs-lookup"><span data-stu-id="4bff9-104">Stops the guest service.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bff9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4bff9-105">Syntax</span></span>


```C++
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="4bff9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4bff9-106">Parameters</span></span>

<span data-ttu-id="4bff9-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4bff9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4bff9-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4bff9-108">Return value</span></span>

<span data-ttu-id="4bff9-109">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4bff9-109">This method returns one of the following values.</span></span>



| <span data-ttu-id="4bff9-110">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="4bff9-110">Return code/value</span></span>                                                                                                                                             | <span data-ttu-id="4bff9-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4bff9-111">Description</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="4bff9-112"><dt>**Завершено без ошибки**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4bff9-112"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="4bff9-113">Успешно.</span><span class="sxs-lookup"><span data-stu-id="4bff9-113">Success.</span></span><br/> |
| <dl> <span data-ttu-id="4bff9-114"><dt>**Не поддерживается**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4bff9-114"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>           |                     |



 

## <a name="requirements"></a><span data-ttu-id="4bff9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4bff9-115">Requirements</span></span>



| <span data-ttu-id="4bff9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4bff9-116">Requirement</span></span> | <span data-ttu-id="4bff9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4bff9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bff9-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4bff9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4bff9-119">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4bff9-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4bff9-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4bff9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4bff9-121">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4bff9-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4bff9-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4bff9-122">Namespace</span></span><br/>                | <span data-ttu-id="4bff9-123">\\\\Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4bff9-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="4bff9-124">MOF</span><span class="sxs-lookup"><span data-stu-id="4bff9-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4bff9-125"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4bff9-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4bff9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4bff9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bff9-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4bff9-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4bff9-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4bff9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bff9-129">**Мсвм \_ гуестсервице**</span><span class="sxs-lookup"><span data-stu-id="4bff9-129">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




