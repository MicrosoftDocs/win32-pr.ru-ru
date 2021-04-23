---
title: Метод INapComponentConfig3 документе newconfig (Напкоммон. h)
description: Реализуется средствами проверки работоспособности системы (SHV) для предоставления способа создания данных конфигурации для определенного идентификатора конфигурации.
ms.assetid: cea762d3-815d-4034-94c1-5fa9a859cce8
keywords:
- Метод документе newconfig NAP
- Метод документе newconfig NAP, интерфейс INapComponentConfig3
- INapComponentConfig3 интерфейса NAP, метод документе newconfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.NewConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 924204068dbb66b22cc06d28966511d8922e0068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135531"
---
# <a name="inapcomponentconfig3newconfig-method"></a><span data-ttu-id="38172-106">Метод INapComponentConfig3:: документе newconfig</span><span class="sxs-lookup"><span data-stu-id="38172-106">INapComponentConfig3::NewConfig method</span></span>

> [!Note]  
> <span data-ttu-id="38172-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="38172-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="38172-108">Метод **документе newconfig** реализуется средствами проверки работоспособности системы (SHV) для предоставления способа создания данных конфигурации для определенного идентификатора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="38172-108">The **NewConfig** method is implemented by system health validators (SHVs) to provide a way to create configuration data for a specific configuration ID.</span></span> <span data-ttu-id="38172-109">При вызове этой функции SHV должен выделить новые данные конфигурации и заполнить ее копией данных конфигурации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="38172-109">When this function is called, an SHV must allocate new configuration data and populate it with a copy of the default configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="38172-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38172-110">Syntax</span></span>


```C++
HRESULT NewConfig(
   UINT32 configID
);
```



## <a name="parameters"></a><span data-ttu-id="38172-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="38172-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38172-112">*конфигид*</span><span class="sxs-lookup"><span data-stu-id="38172-112">*configID*</span></span> 
</dt> <dd>

<span data-ttu-id="38172-113">Значение, представляющее конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="38172-113">A value that represents the configuration.</span></span> <span data-ttu-id="38172-114">*Конфигид* назначается службой сервера политики сети (NPS) и уникальна в SHV.</span><span class="sxs-lookup"><span data-stu-id="38172-114">*ConfigID* is assigned by the Network Policy Server (NPS) service and is unique within the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38172-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38172-115">Return value</span></span>

<span data-ttu-id="38172-116">Возвращает один из следующих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="38172-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="38172-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="38172-117">Return code</span></span>                                                                                                 | <span data-ttu-id="38172-118">Описание</span><span class="sxs-lookup"><span data-stu-id="38172-118">Description</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="38172-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="38172-119"><dt>**S\_OK** </dt></span></span> </dl>                       | <span data-ttu-id="38172-120">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="38172-120">The operation is successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="38172-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="38172-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="38172-122">*Конфигид* — 0 (значение, зарезервированное для конфигурации по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="38172-122">*ConfigID* is 0 (a value reserved for the default configuration).</span></span><br/>                  |
| <dl> <span data-ttu-id="38172-123"><dt>**Конфигурация средства защиты доступа к сети (NAP) \_ \_ \_ \_ существовала**</dt></span><span class="sxs-lookup"><span data-stu-id="38172-123"><dt>**NAP\_E\_SHV\_CONFIG\_EXISTED**</dt></span></span> </dl> | <span data-ttu-id="38172-124">*Конфигид* уже существует.</span><span class="sxs-lookup"><span data-stu-id="38172-124">*ConfigID* already exists.</span></span> <span data-ttu-id="38172-125">Список идентификаторов, известных серверу NPS, отличается от SHV.</span><span class="sxs-lookup"><span data-stu-id="38172-125">The list of IDs known to NPS is different from the SHV.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="38172-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38172-126">Remarks</span></span>

<span data-ttu-id="38172-127">После создания новой конфигурации с помощью **документе newconfig** методы [**жетконфигфромид**](inapcomponentconfig3-getconfigfromid.md), [**инвокеуифромконфигблоб**](inapcomponentconfig2-invokeuifromconfigblob.md)и [**сетконфигтоид**](inapcomponentconfig3-setconfigtoid.md) следует использовать для изменения конфигурации при необходимости.</span><span class="sxs-lookup"><span data-stu-id="38172-127">After the new configuration is created by **NewConfig**, the [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md), and [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) methods should be used to alter the configuration as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="38172-128">Требования</span><span class="sxs-lookup"><span data-stu-id="38172-128">Requirements</span></span>



| <span data-ttu-id="38172-129">Требование</span><span class="sxs-lookup"><span data-stu-id="38172-129">Requirement</span></span> | <span data-ttu-id="38172-130">Значение</span><span class="sxs-lookup"><span data-stu-id="38172-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="38172-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38172-131">Minimum supported client</span></span><br/> | <span data-ttu-id="38172-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="38172-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="38172-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38172-133">Minimum supported server</span></span><br/> | <span data-ttu-id="38172-134">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="38172-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="38172-135">Header</span><span class="sxs-lookup"><span data-stu-id="38172-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="38172-136"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="38172-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="38172-137">IDL</span><span class="sxs-lookup"><span data-stu-id="38172-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="38172-138"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="38172-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38172-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38172-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38172-140">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="38172-140">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





