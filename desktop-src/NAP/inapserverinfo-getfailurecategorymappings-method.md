---
title: Метод Инапсерверинфо Жетфаилурекатегоримаппингс (Напсерверманажемент. h)
description: Извлекает сопоставления категорий сбоев для указанного агента SHA или SHV.
ms.assetid: 89b89003-40b3-4763-aec8-01cd0c307649
keywords:
- Метод Жетфаилурекатегоримаппингс NAP
- Метод Жетфаилурекатегоримаппингс NAP, интерфейс Инапсерверинфо
- Инапсерверинфо интерфейса NAP, метод Жетфаилурекатегоримаппингс
topic_type:
- apiref
api_name:
- INapServerInfo.GetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba830dd8a35a2c60b14c4feec14846125223e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493233"
---
# <a name="inapserverinfogetfailurecategorymappings-method"></a><span data-ttu-id="5beef-106">Метод Инапсерверинфо:: Жетфаилурекатегоримаппингс</span><span class="sxs-lookup"><span data-stu-id="5beef-106">INapServerInfo::GetFailureCategoryMappings method</span></span>

> [!Note]  
> <span data-ttu-id="5beef-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="5beef-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5beef-108">Метод **инапсерверинфо:: жетфаилурекатегоримаппингс** извлекает сопоставления категорий сбоев для указанного агента SHA или SHV.</span><span class="sxs-lookup"><span data-stu-id="5beef-108">The **INapServerInfo::GetFailureCategoryMappings** method retrieves the failure category mappings for a specified SHA or SHV.</span></span>

## <a name="syntax"></a><span data-ttu-id="5beef-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5beef-109">Syntax</span></span>


```C++
HRESULT GetFailureCategoryMappings(
  [in]  SystemHealthEntityId   id,
  [out] FailureCategoryMapping *mapping
);
```



## <a name="parameters"></a><span data-ttu-id="5beef-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5beef-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5beef-111">*идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="5beef-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5beef-112">Объект [**системхеалсентитид**](nap-type-constants.md) , содержащий уникальный идентификатор SHA или SHV.</span><span class="sxs-lookup"><span data-stu-id="5beef-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHA or the SHV.</span></span>

</dd> <dt>

<span data-ttu-id="5beef-113">*сопоставление* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5beef-113">*mapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5beef-114">Указатель на [**фаилурекатегоримаппинг**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) , содержащий данные сопоставления.</span><span class="sxs-lookup"><span data-stu-id="5beef-114">A pointer to a [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) that contains the mapping data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5beef-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5beef-115">Return value</span></span>

<span data-ttu-id="5beef-116">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="5beef-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5beef-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5beef-117">Return code</span></span>                                                                                     | <span data-ttu-id="5beef-118">Описание</span><span class="sxs-lookup"><span data-stu-id="5beef-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5beef-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5beef-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="5beef-120">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="5beef-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5beef-121"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5beef-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="5beef-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="5beef-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="5beef-123"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5beef-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="5beef-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5beef-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5beef-125">Требования</span><span class="sxs-lookup"><span data-stu-id="5beef-125">Requirements</span></span>



| <span data-ttu-id="5beef-126">Требование</span><span class="sxs-lookup"><span data-stu-id="5beef-126">Requirement</span></span> | <span data-ttu-id="5beef-127">Значение</span><span class="sxs-lookup"><span data-stu-id="5beef-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5beef-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5beef-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5beef-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5beef-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="5beef-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5beef-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5beef-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5beef-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5beef-132">Header</span><span class="sxs-lookup"><span data-stu-id="5beef-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5beef-133"><dt>Напсерверманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="5beef-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="5beef-134">IDL</span><span class="sxs-lookup"><span data-stu-id="5beef-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5beef-135"><dt>Напсерверманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5beef-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="5beef-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5beef-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5beef-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5beef-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="5beef-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5beef-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5beef-139">**инапсерверинфо**</span><span class="sxs-lookup"><span data-stu-id="5beef-139">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> </dl>

 

 





