---
title: Метод Инапсерверманажемент Сетфаилурекатегоримаппингс (Напсерверманажемент. h)
description: Используется для задания сопоставлений категорий сбоев SHV.
ms.assetid: be482f82-c79c-405c-b619-9bcb9b4dc349
keywords:
- Метод Сетфаилурекатегоримаппингс NAP
- Метод Сетфаилурекатегоримаппингс NAP, интерфейс Инапсерверманажемент
- Инапсерверманажемент интерфейса NAP, метод Сетфаилурекатегоримаппингс
topic_type:
- apiref
api_name:
- INapServerManagement.SetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a220d6603ef5bbb49377ac0e212d5d98afa4bdd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988955"
---
# <a name="inapservermanagementsetfailurecategorymappings-method"></a><span data-ttu-id="4f420-106">Метод Инапсерверманажемент:: Сетфаилурекатегоримаппингс</span><span class="sxs-lookup"><span data-stu-id="4f420-106">INapServerManagement::SetFailureCategoryMappings method</span></span>

> [!Note]  
> <span data-ttu-id="4f420-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="4f420-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4f420-108">Метод **инапсерверманажемент:: сетфаилурекатегоримаппингс** используется для задания сопоставлений категорий сбоев SHV.</span><span class="sxs-lookup"><span data-stu-id="4f420-108">The **INapServerManagement::SetFailureCategoryMappings** method is used to set the SHV's failure category mappings.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f420-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f420-109">Syntax</span></span>


```C++
HRESULT SetFailureCategoryMappings(
  [in]       SystemHealthEntityId   id,
  [in] const FailureCategoryMapping mapping
);
```



## <a name="parameters"></a><span data-ttu-id="4f420-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f420-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f420-111">*идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="4f420-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f420-112">Объект [**системхеалсентитид**](nap-type-constants.md) , содержащий уникальный идентификатор SHV.</span><span class="sxs-lookup"><span data-stu-id="4f420-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHV.</span></span>

</dd> <dt>

<span data-ttu-id="4f420-113">*сопоставление* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4f420-113">*mapping* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f420-114">Структура [**фаилурекатегоримаппинг**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) , содержащая данные сопоставления категорий сбоев.</span><span class="sxs-lookup"><span data-stu-id="4f420-114">A [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure that contains the failure category mapping data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f420-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f420-115">Return value</span></span>

<span data-ttu-id="4f420-116">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="4f420-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="4f420-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4f420-117">Return code</span></span>                                                                                     | <span data-ttu-id="4f420-118">Описание</span><span class="sxs-lookup"><span data-stu-id="4f420-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="4f420-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4f420-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="4f420-120">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="4f420-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4f420-121"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="4f420-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="4f420-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="4f420-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="4f420-123"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4f420-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="4f420-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4f420-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4f420-125">Требования</span><span class="sxs-lookup"><span data-stu-id="4f420-125">Requirements</span></span>



| <span data-ttu-id="4f420-126">Требование</span><span class="sxs-lookup"><span data-stu-id="4f420-126">Requirement</span></span> | <span data-ttu-id="4f420-127">Значение</span><span class="sxs-lookup"><span data-stu-id="4f420-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f420-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f420-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4f420-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4f420-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="4f420-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f420-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4f420-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4f420-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4f420-132">Header</span><span class="sxs-lookup"><span data-stu-id="4f420-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f420-133"><dt>Напсерверманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f420-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f420-134">IDL</span><span class="sxs-lookup"><span data-stu-id="4f420-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4f420-135"><dt>Напсерверманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4f420-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="4f420-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4f420-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f420-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f420-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="4f420-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f420-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f420-139">**инапсерверманажемент**</span><span class="sxs-lookup"><span data-stu-id="4f420-139">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





