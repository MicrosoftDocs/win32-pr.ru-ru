---
description: Метод StartService класса Msvm_VirtualEthernetSwitchManagementService — запускает службу.
ms.assetid: 8b232523-3311-47a9-949a-3bbb9944d80f
title: Метод StartService класса Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d58ec579d13edd87b0a952d8b9e26ad387622d3b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109412"
---
# <a name="startservice-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="2eef1-103">Метод StartService \_ класса мсвм виртуалесернетсвитчманажементсервице</span><span class="sxs-lookup"><span data-stu-id="2eef1-103">StartService method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="2eef1-104">запускает службу.</span><span class="sxs-lookup"><span data-stu-id="2eef1-104">Starts the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eef1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2eef1-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="2eef1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2eef1-106">Parameters</span></span>

<span data-ttu-id="2eef1-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2eef1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2eef1-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2eef1-108">Return value</span></span>

<span data-ttu-id="2eef1-109">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="2eef1-109">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="2eef1-110">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="2eef1-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2eef1-111">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="2eef1-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2eef1-112">Требования</span><span class="sxs-lookup"><span data-stu-id="2eef1-112">Requirements</span></span>



| <span data-ttu-id="2eef1-113">Требование</span><span class="sxs-lookup"><span data-stu-id="2eef1-113">Requirement</span></span> | <span data-ttu-id="2eef1-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2eef1-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eef1-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2eef1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2eef1-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2eef1-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2eef1-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2eef1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2eef1-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2eef1-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2eef1-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2eef1-119">Namespace</span></span><br/>                | <span data-ttu-id="2eef1-120">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="2eef1-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2eef1-121">MOF</span><span class="sxs-lookup"><span data-stu-id="2eef1-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2eef1-122"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2eef1-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2eef1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="2eef1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2eef1-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2eef1-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2eef1-125">См. также</span><span class="sxs-lookup"><span data-stu-id="2eef1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eef1-126">**Мсвм \_ виртуалесернетсвитчманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="2eef1-126">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

 




