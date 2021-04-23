---
description: Блокирует или освобождает носитель.
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
ms.openlocfilehash: 4f9bce4e9e46d76c3426271af16c28026c242fa9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914151"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a><span data-ttu-id="bc8eb-103">Метод Локкмедиа \_ класса Дискеттедриве мсвм</span><span class="sxs-lookup"><span data-stu-id="bc8eb-103">LockMedia method of the Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="bc8eb-104">Блокирует или освобождает носитель.</span><span class="sxs-lookup"><span data-stu-id="bc8eb-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8eb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc8eb-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="bc8eb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc8eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc8eb-107">*Блокировка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bc8eb-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8eb-108">**значение true** , чтобы заблокировать носитель; **значение false** , чтобы освободить носитель.</span><span class="sxs-lookup"><span data-stu-id="bc8eb-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc8eb-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc8eb-109">Return value</span></span>

<span data-ttu-id="bc8eb-110">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="bc8eb-110">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="bc8eb-111">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="bc8eb-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc8eb-112">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="bc8eb-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bc8eb-113">Требования</span><span class="sxs-lookup"><span data-stu-id="bc8eb-113">Requirements</span></span>



| <span data-ttu-id="bc8eb-114">Требование</span><span class="sxs-lookup"><span data-stu-id="bc8eb-114">Requirement</span></span> | <span data-ttu-id="bc8eb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="bc8eb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8eb-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc8eb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bc8eb-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="bc8eb-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="bc8eb-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc8eb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bc8eb-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bc8eb-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="bc8eb-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bc8eb-120">Namespace</span></span><br/>                | <span data-ttu-id="bc8eb-121">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="bc8eb-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bc8eb-122">MOF</span><span class="sxs-lookup"><span data-stu-id="bc8eb-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc8eb-123"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc8eb-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc8eb-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bc8eb-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc8eb-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bc8eb-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bc8eb-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc8eb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc8eb-127">**Мсвм \_ дискеттедриве**</span><span class="sxs-lookup"><span data-stu-id="bc8eb-127">**Msvm\_DisketteDrive**</span></span>](msvm-diskettedrive.md)
</dt> </dl>

 

 




