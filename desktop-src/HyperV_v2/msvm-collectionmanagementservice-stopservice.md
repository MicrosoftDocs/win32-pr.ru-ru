---
description: Метод «начало» класса Msvm_CollectionManagementService — останавливает службу.
ms.assetid: 26d0aa9f-f5ca-481f-9bed-6788b0dc2803
title: Метод «начало» класса Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f46b7416a3f17788cbfc0af5aacba014d680dbf6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119252"
---
# <a name="stopservice-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="7e279-103">Метод «начало» \_ класса мсвм коллектионманажементсервице</span><span class="sxs-lookup"><span data-stu-id="7e279-103">StopService method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="7e279-104">останавливает службу.</span><span class="sxs-lookup"><span data-stu-id="7e279-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e279-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e279-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="7e279-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e279-106">Parameters</span></span>

<span data-ttu-id="7e279-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7e279-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7e279-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e279-108">Return value</span></span>

<span data-ttu-id="7e279-109">При успешном выполнении возвращает 0. в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="7e279-109">Returns 0 if successful; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="7e279-110">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="7e279-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7e279-111">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="7e279-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7e279-112">Требования</span><span class="sxs-lookup"><span data-stu-id="7e279-112">Requirements</span></span>



| <span data-ttu-id="7e279-113">Требование</span><span class="sxs-lookup"><span data-stu-id="7e279-113">Requirement</span></span> | <span data-ttu-id="7e279-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7e279-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e279-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e279-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7e279-116">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7e279-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="7e279-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e279-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7e279-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7e279-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7e279-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7e279-119">Namespace</span></span><br/>                | <span data-ttu-id="7e279-120">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7e279-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7e279-121">MOF</span><span class="sxs-lookup"><span data-stu-id="7e279-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e279-122"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e279-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e279-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7e279-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e279-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7e279-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7e279-125">См. также</span><span class="sxs-lookup"><span data-stu-id="7e279-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e279-126">**Мсвм \_ коллектионманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="7e279-126">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




