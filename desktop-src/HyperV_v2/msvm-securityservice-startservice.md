---
description: запускает службу.
ms.assetid: 59918c15-7216-4cf7-9215-b27532febc72
title: Метод StartService класса Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bff2721b942b6bb145f2d57492f27d1cabb722bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664757"
---
# <a name="startservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="e9a6f-103">Метод StartService \_ класса мсвм SecurityService</span><span class="sxs-lookup"><span data-stu-id="e9a6f-103">StartService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="e9a6f-104">запускает службу.</span><span class="sxs-lookup"><span data-stu-id="e9a6f-104">Starts the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9a6f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9a6f-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="e9a6f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9a6f-106">Parameters</span></span>

<span data-ttu-id="e9a6f-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e9a6f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9a6f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9a6f-108">Return value</span></span>

<span data-ttu-id="e9a6f-109">При успешном выполнении возвращает 0; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e9a6f-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="e9a6f-110">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="e9a6f-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e9a6f-111">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="e9a6f-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e9a6f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e9a6f-112">Requirements</span></span>



| <span data-ttu-id="e9a6f-113">Требование</span><span class="sxs-lookup"><span data-stu-id="e9a6f-113">Requirement</span></span> | <span data-ttu-id="e9a6f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e9a6f-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a6f-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9a6f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e9a6f-116">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="e9a6f-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e9a6f-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9a6f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e9a6f-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e9a6f-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e9a6f-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e9a6f-119">Namespace</span></span><br/>                | <span data-ttu-id="e9a6f-120">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e9a6f-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e9a6f-121">MOF</span><span class="sxs-lookup"><span data-stu-id="e9a6f-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9a6f-122"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9a6f-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9a6f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e9a6f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9a6f-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e9a6f-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e9a6f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9a6f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9a6f-126">**Мсвм \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="e9a6f-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




