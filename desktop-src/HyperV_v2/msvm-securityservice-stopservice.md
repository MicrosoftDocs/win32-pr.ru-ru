---
description: останавливает службу.
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
ms.openlocfilehash: 68e88e2c88d4f75f4d7671c389bab0cd81d0deb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265248"
---
# <a name="stopservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="8ea3c-103">Метод «начало» \_ класса мсвм SecurityService</span><span class="sxs-lookup"><span data-stu-id="8ea3c-103">StopService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="8ea3c-104">останавливает службу.</span><span class="sxs-lookup"><span data-stu-id="8ea3c-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea3c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ea3c-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="8ea3c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ea3c-106">Parameters</span></span>

<span data-ttu-id="8ea3c-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8ea3c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8ea3c-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ea3c-108">Return value</span></span>

<span data-ttu-id="8ea3c-109">При успешном выполнении возвращает 0; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="8ea3c-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="8ea3c-110">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="8ea3c-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8ea3c-111">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="8ea3c-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8ea3c-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8ea3c-112">Requirements</span></span>



| <span data-ttu-id="8ea3c-113">Требование</span><span class="sxs-lookup"><span data-stu-id="8ea3c-113">Requirement</span></span> | <span data-ttu-id="8ea3c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8ea3c-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea3c-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ea3c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8ea3c-116">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="8ea3c-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8ea3c-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ea3c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8ea3c-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8ea3c-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8ea3c-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8ea3c-119">Namespace</span></span><br/>                | <span data-ttu-id="8ea3c-120">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="8ea3c-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8ea3c-121">MOF</span><span class="sxs-lookup"><span data-stu-id="8ea3c-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ea3c-122"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ea3c-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ea3c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8ea3c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ea3c-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8ea3c-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8ea3c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ea3c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ea3c-126">**Мсвм \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="8ea3c-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




