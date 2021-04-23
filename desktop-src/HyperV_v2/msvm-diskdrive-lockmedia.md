---
description: Блокирует или разблокирует носитель.
ms.assetid: 805efb2d-71a7-4c74-821f-942644928ff9
title: Метод Локкмедиа класса Msvm_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7ddc082ca6ceb7141eaa42bdfddf7a97897a9240
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684776"
---
# <a name="lockmedia-method-of-the-msvm_diskdrive-class"></a><span data-ttu-id="8058e-103">Метод Локкмедиа \_ класса Дискдриве мсвм</span><span class="sxs-lookup"><span data-stu-id="8058e-103">LockMedia method of the Msvm\_DiskDrive class</span></span>

<span data-ttu-id="8058e-104">Блокирует или разблокирует носитель.</span><span class="sxs-lookup"><span data-stu-id="8058e-104">Locks or unlocks the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="8058e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8058e-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="8058e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8058e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8058e-107">*Блокировка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8058e-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8058e-108">**значение true** , чтобы заблокировать носитель; **значение false** , чтобы освободить носитель.</span><span class="sxs-lookup"><span data-stu-id="8058e-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8058e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8058e-109">Return value</span></span>

<span data-ttu-id="8058e-110">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="8058e-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="8058e-111">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="8058e-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8058e-112">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="8058e-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8058e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8058e-113">Requirements</span></span>



| <span data-ttu-id="8058e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8058e-114">Requirement</span></span> | <span data-ttu-id="8058e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8058e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8058e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8058e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8058e-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8058e-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="8058e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8058e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8058e-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8058e-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="8058e-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8058e-120">Namespace</span></span><br/>                | <span data-ttu-id="8058e-121">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="8058e-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8058e-122">MOF</span><span class="sxs-lookup"><span data-stu-id="8058e-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8058e-123"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8058e-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8058e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8058e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8058e-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8058e-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8058e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8058e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8058e-127">**Мсвм \_ дискдриве**</span><span class="sxs-lookup"><span data-stu-id="8058e-127">**Msvm\_DiskDrive**</span></span>](msvm-diskdrive.md)
</dt> </dl>

 

 




