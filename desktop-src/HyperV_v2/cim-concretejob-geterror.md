---
description: Извлекает ошибку из-за невыполненного задания.
ms.assetid: d499eb91-e1cc-4792-b32d-5a8875eebbb7
title: Метод method класса CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: aa9ed87f2d484286d91d14c4183d2ce3b6f41cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682953"
---
# <a name="geterror-method-of-the-cim_concretejob-class"></a><span data-ttu-id="62c43-103">Метод \_ конкретежоб класса CIM</span><span class="sxs-lookup"><span data-stu-id="62c43-103">GetError method of the CIM\_ConcreteJob class</span></span>

<span data-ttu-id="62c43-104">Извлекает ошибку из-за невыполненного задания.</span><span class="sxs-lookup"><span data-stu-id="62c43-104">Retrieves an error due to a failed job.</span></span> <span data-ttu-id="62c43-105">При выполнении или завершении задания без ошибок этот метод не возвращает экземпляр [**\_ ошибки CIM**](cim-error.md) .</span><span class="sxs-lookup"><span data-stu-id="62c43-105">When the job is executing or has terminated without error, then this method returns no [**CIM\_Error**](cim-error.md) instance.</span></span> <span data-ttu-id="62c43-106">Однако если задание завершилось сбоем из-за внутренней проблемы или из-за завершения задания клиентом, то возвращается экземпляр **\_ ошибки CIM** .</span><span class="sxs-lookup"><span data-stu-id="62c43-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="62c43-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62c43-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="62c43-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="62c43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62c43-109">*Ошибка при* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="62c43-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62c43-110">Возвращает экземпляр [**\_ ошибки CIM**](cim-error.md) , если **OperationalStatus** в задании не имеет значение "ОК"; в противном случае возвращает **null**.</span><span class="sxs-lookup"><span data-stu-id="62c43-110">Returns a [**CIM\_Error**](cim-error.md) instance if the **OperationalStatus** on the Job is not "OK"; otherwise, returns **null**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62c43-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62c43-111">Return value</span></span>

<span data-ttu-id="62c43-112">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="62c43-112">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="62c43-113">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="62c43-113">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="62c43-114">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="62c43-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="62c43-115">**Неопределенная ошибка** (2)</span><span class="sxs-lookup"><span data-stu-id="62c43-115">**Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="62c43-116">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="62c43-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="62c43-117">**Сбой** (4)</span><span class="sxs-lookup"><span data-stu-id="62c43-117">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="62c43-118">**Недопустимый параметр** (5)</span><span class="sxs-lookup"><span data-stu-id="62c43-118">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="62c43-119">**Отказано в доступе** (6)</span><span class="sxs-lookup"><span data-stu-id="62c43-119">**Access Denied** (6)</span></span>
</dt> <dt>

<span data-ttu-id="62c43-120">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="62c43-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="62c43-121">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="62c43-121">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="62c43-122">Требования</span><span class="sxs-lookup"><span data-stu-id="62c43-122">Requirements</span></span>



| <span data-ttu-id="62c43-123">Требование</span><span class="sxs-lookup"><span data-stu-id="62c43-123">Requirement</span></span> | <span data-ttu-id="62c43-124">Значение</span><span class="sxs-lookup"><span data-stu-id="62c43-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62c43-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62c43-125">Minimum supported client</span></span><br/> | <span data-ttu-id="62c43-126">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="62c43-126">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="62c43-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62c43-127">Minimum supported server</span></span><br/> | <span data-ttu-id="62c43-128">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="62c43-128">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="62c43-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="62c43-129">Namespace</span></span><br/>                | <span data-ttu-id="62c43-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="62c43-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="62c43-131">MOF</span><span class="sxs-lookup"><span data-stu-id="62c43-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62c43-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62c43-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="62c43-133">DLL</span><span class="sxs-lookup"><span data-stu-id="62c43-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62c43-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="62c43-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="62c43-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62c43-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c43-136">**\_КОНКРЕТЕЖОБ CIM**</span><span class="sxs-lookup"><span data-stu-id="62c43-136">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

 




