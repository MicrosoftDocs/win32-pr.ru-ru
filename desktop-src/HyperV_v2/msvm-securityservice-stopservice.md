---
description: Метод «начало» класса Msvm_SecurityService — останавливает службу.
ms.assetid: cf100cea-b0e1-42e9-831e-6422aded47c5
title: Метод «начало» класса Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a9a16fef951fdee5ed7fc580da61f43d848a8dec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118712"
---
# <a name="stopservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="14334-103">Метод «начало» \_ класса мсвм SecurityService</span><span class="sxs-lookup"><span data-stu-id="14334-103">StopService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="14334-104">останавливает службу.</span><span class="sxs-lookup"><span data-stu-id="14334-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="14334-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14334-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="14334-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="14334-106">Parameters</span></span>

<span data-ttu-id="14334-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="14334-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="14334-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14334-108">Return value</span></span>

<span data-ttu-id="14334-109">При успешном выполнении возвращает 0; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="14334-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="14334-110">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="14334-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="14334-111">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="14334-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="14334-112">Требования</span><span class="sxs-lookup"><span data-stu-id="14334-112">Requirements</span></span>



| <span data-ttu-id="14334-113">Требование</span><span class="sxs-lookup"><span data-stu-id="14334-113">Requirement</span></span> | <span data-ttu-id="14334-114">Значение</span><span class="sxs-lookup"><span data-stu-id="14334-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14334-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14334-115">Minimum supported client</span></span><br/> | <span data-ttu-id="14334-116">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="14334-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="14334-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14334-117">Minimum supported server</span></span><br/> | <span data-ttu-id="14334-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="14334-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="14334-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="14334-119">Namespace</span></span><br/>                | <span data-ttu-id="14334-120">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="14334-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="14334-121">MOF</span><span class="sxs-lookup"><span data-stu-id="14334-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14334-122"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14334-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="14334-123">DLL</span><span class="sxs-lookup"><span data-stu-id="14334-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14334-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="14334-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="14334-125">См. также</span><span class="sxs-lookup"><span data-stu-id="14334-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14334-126">**Мсвм \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="14334-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




