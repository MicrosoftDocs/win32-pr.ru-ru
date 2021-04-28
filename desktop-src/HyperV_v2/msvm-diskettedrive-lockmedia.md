---
description: Метод Локкмедиа класса Msvm_DisketteDrive — блокирует или освобождает носитель.
ms.assetid: 90f7e06c-92d0-4742-a74d-68ae6bfc00bf
title: Метод Локкмедиа класса Msvm_DisketteDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5f5f87354aa7c39534e8b32c8985c5d18b55caa9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111981"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a><span data-ttu-id="3c27d-103">Метод Локкмедиа \_ класса Дискеттедриве мсвм</span><span class="sxs-lookup"><span data-stu-id="3c27d-103">LockMedia method of the Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="3c27d-104">Блокирует или освобождает носитель.</span><span class="sxs-lookup"><span data-stu-id="3c27d-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c27d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c27d-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="3c27d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c27d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c27d-107">*Блокировка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c27d-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c27d-108">**значение true** , чтобы заблокировать носитель; **значение false** , чтобы освободить носитель.</span><span class="sxs-lookup"><span data-stu-id="3c27d-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c27d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c27d-109">Return value</span></span>

<span data-ttu-id="3c27d-110">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="3c27d-110">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="3c27d-111">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="3c27d-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3c27d-112">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="3c27d-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3c27d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3c27d-113">Requirements</span></span>



| <span data-ttu-id="3c27d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3c27d-114">Requirement</span></span> | <span data-ttu-id="3c27d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3c27d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c27d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c27d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3c27d-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3c27d-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3c27d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c27d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3c27d-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3c27d-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3c27d-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3c27d-120">Namespace</span></span><br/>                | <span data-ttu-id="3c27d-121">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3c27d-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3c27d-122">MOF</span><span class="sxs-lookup"><span data-stu-id="3c27d-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c27d-123"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c27d-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c27d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3c27d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c27d-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3c27d-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3c27d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="3c27d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c27d-127">**Мсвм \_ дискеттедриве**</span><span class="sxs-lookup"><span data-stu-id="3c27d-127">**Msvm\_DisketteDrive**</span></span>](msvm-diskettedrive.md)
</dt> </dl>

 

 




