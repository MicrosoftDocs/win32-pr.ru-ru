---
description: останавливает службу.
ms.assetid: 0f9a015d-b895-496a-a4c6-2737c0742746
title: Метод StartService класса Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f76fa9e5069c2a9e19b83a8ab83136879c6657e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684627"
---
# <a name="startservice-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="451d7-103">Метод StartService \_ класса мсвм коллектионманажементсервице</span><span class="sxs-lookup"><span data-stu-id="451d7-103">StartService method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="451d7-104">останавливает службу.</span><span class="sxs-lookup"><span data-stu-id="451d7-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="451d7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="451d7-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="451d7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="451d7-106">Parameters</span></span>

<span data-ttu-id="451d7-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="451d7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="451d7-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="451d7-108">Return value</span></span>

<span data-ttu-id="451d7-109">При успешном выполнении возвращает 0. в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="451d7-109">Returns 0 if successful; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="451d7-110">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="451d7-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="451d7-111">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="451d7-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="451d7-112">Требования</span><span class="sxs-lookup"><span data-stu-id="451d7-112">Requirements</span></span>



| <span data-ttu-id="451d7-113">Требование</span><span class="sxs-lookup"><span data-stu-id="451d7-113">Requirement</span></span> | <span data-ttu-id="451d7-114">Значение</span><span class="sxs-lookup"><span data-stu-id="451d7-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="451d7-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="451d7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="451d7-116">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="451d7-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="451d7-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="451d7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="451d7-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="451d7-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="451d7-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="451d7-119">Namespace</span></span><br/>                | <span data-ttu-id="451d7-120">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="451d7-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="451d7-121">MOF</span><span class="sxs-lookup"><span data-stu-id="451d7-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="451d7-122"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="451d7-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="451d7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="451d7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="451d7-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="451d7-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="451d7-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="451d7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="451d7-126">**Мсвм \_ коллектионманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="451d7-126">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




