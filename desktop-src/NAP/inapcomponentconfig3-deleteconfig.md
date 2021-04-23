---
title: Метод INapComponentConfig3 Делетеконфиг (Напкоммон. h)
description: Реализуется средствами проверки работоспособности системы (SHV) для предоставления способа удаления данных конфигурации для определенного идентификатора конфигурации.
ms.assetid: 9740c122-86c8-4b77-9268-faa90e84d8aa
keywords:
- Метод Делетеконфиг NAP
- Метод Делетеконфиг NAP, интерфейс INapComponentConfig3
- INapComponentConfig3 интерфейса NAP, метод Делетеконфиг
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a9b9a6838616f0892b45df34d9a7c5ed63ff16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801859"
---
# <a name="inapcomponentconfig3deleteconfig-method"></a><span data-ttu-id="d93b8-106">INapComponentConfig3: метод:D Елетеконфиг</span><span class="sxs-lookup"><span data-stu-id="d93b8-106">INapComponentConfig3::DeleteConfig method</span></span>

> [!Note]  
> <span data-ttu-id="d93b8-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="d93b8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d93b8-108">Метод **делетеконфиг** реализуется средствами проверки работоспособности системы (SHV) для предоставления способа удаления данных конфигурации для определенного идентификатора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d93b8-108">The **DeleteConfig** method is implemented by system health validators (SHVs) to provide a way to delete configuration data for a specific configuration ID.</span></span> <span data-ttu-id="d93b8-109">Идентификатор может быть использован повторно после удаления данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d93b8-109">The ID may be reused after the configuration data has been deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="d93b8-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d93b8-110">Syntax</span></span>


```C++
HRESULT DeleteConfig(
   UINT32 configID
);
```



## <a name="parameters"></a><span data-ttu-id="d93b8-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d93b8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d93b8-112">*конфигид*</span><span class="sxs-lookup"><span data-stu-id="d93b8-112">*configID*</span></span> 
</dt> <dd>

<span data-ttu-id="d93b8-113">Значение типа, представляющее данные конфигурации для удаления.</span><span class="sxs-lookup"><span data-stu-id="d93b8-113">A value that represents the configuration data to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d93b8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d93b8-114">Return value</span></span>

<span data-ttu-id="d93b8-115">Возвращает один из следующих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="d93b8-115">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="d93b8-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d93b8-116">Return code</span></span>                                                                                                    | <span data-ttu-id="d93b8-117">Описание</span><span class="sxs-lookup"><span data-stu-id="d93b8-117">Description</span></span>                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d93b8-118"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d93b8-118"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="d93b8-119">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="d93b8-119">The operation is successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="d93b8-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d93b8-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                   | <span data-ttu-id="d93b8-121">*Конфигид* — 0 (значение, зарезервированное для конфигурации по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="d93b8-121">*ConfigID* is 0 (a value reserved for the default configuration).</span></span><br/> |
| <dl> <span data-ttu-id="d93b8-122"><dt>**\_ \_ \_ \_ не \_ найдена Конфигурация NAP E SHV**</dt></span><span class="sxs-lookup"><span data-stu-id="d93b8-122"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="d93b8-123">Не удается найти *конфигид* .</span><span class="sxs-lookup"><span data-stu-id="d93b8-123">*ConfigID* cannot be found.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="d93b8-124">Требования</span><span class="sxs-lookup"><span data-stu-id="d93b8-124">Requirements</span></span>



| <span data-ttu-id="d93b8-125">Требование</span><span class="sxs-lookup"><span data-stu-id="d93b8-125">Requirement</span></span> | <span data-ttu-id="d93b8-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d93b8-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d93b8-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d93b8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d93b8-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d93b8-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d93b8-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d93b8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d93b8-130">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d93b8-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d93b8-131">Header</span><span class="sxs-lookup"><span data-stu-id="d93b8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d93b8-132"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="d93b8-132"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="d93b8-133">IDL</span><span class="sxs-lookup"><span data-stu-id="d93b8-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d93b8-134"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d93b8-134"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d93b8-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d93b8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d93b8-136">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="d93b8-136">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





