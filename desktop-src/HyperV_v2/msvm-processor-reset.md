---
description: Метод Reset класса Msvm_Processor — запрашивает сброс.
ms.assetid: c69b5c65-8f00-48ed-8602-7e0c5a76653d
title: Метод Reset класса Msvm_Processor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Processor.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: eecd8f240f2d5c7dc1c2c1b98c0503f54a5c8050
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111572"
---
# <a name="reset-method-of-the-msvm_processor-class"></a><span data-ttu-id="e2594-103">Метод Reset \_ класса процессора мсвм</span><span class="sxs-lookup"><span data-stu-id="e2594-103">Reset method of the Msvm\_Processor class</span></span>

<span data-ttu-id="e2594-104">Запрашивает сброс.</span><span class="sxs-lookup"><span data-stu-id="e2594-104">Requests a reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2594-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2594-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="e2594-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2594-106">Parameters</span></span>

<span data-ttu-id="e2594-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e2594-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e2594-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2594-108">Return value</span></span>

<span data-ttu-id="e2594-109">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="e2594-109">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="e2594-110">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="e2594-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e2594-111">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="e2594-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e2594-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e2594-112">Requirements</span></span>



| <span data-ttu-id="e2594-113">Требование</span><span class="sxs-lookup"><span data-stu-id="e2594-113">Requirement</span></span> | <span data-ttu-id="e2594-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e2594-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2594-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2594-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e2594-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e2594-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="e2594-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2594-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e2594-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e2594-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e2594-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e2594-119">Namespace</span></span><br/>                | <span data-ttu-id="e2594-120">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e2594-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e2594-121">MOF</span><span class="sxs-lookup"><span data-stu-id="e2594-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2594-122"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2594-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2594-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e2594-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2594-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e2594-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e2594-125">См. также</span><span class="sxs-lookup"><span data-stu-id="e2594-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2594-126">**\_Процессор мсвм**</span><span class="sxs-lookup"><span data-stu-id="e2594-126">**Msvm\_Processor**</span></span>](msvm-processor.md)
</dt> </dl>

 

 




