---
title: Метод INapComponentConfig3 Сетконфигтоид (Напкоммон. h)
description: Реализуется средствами проверки работоспособности системы (SHV) для предоставления способа установки данных конфигурации для конкретного идентификатора конфигурации.
ms.assetid: 1fa0b8e7-b597-4ab1-bb61-2cab47b92ce3
keywords:
- Метод Сетконфигтоид NAP
- Метод Сетконфигтоид NAP, интерфейс INapComponentConfig3
- INapComponentConfig3 интерфейса NAP, метод Сетконфигтоид
topic_type:
- apiref
api_name:
- INapComponentConfig3.SetConfigToID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3158a216ba4fd4f82f3e4fc21fc1e0043b16a46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661992"
---
# <a name="inapcomponentconfig3setconfigtoid-method"></a><span data-ttu-id="e6e78-106">Метод INapComponentConfig3:: Сетконфигтоид</span><span class="sxs-lookup"><span data-stu-id="e6e78-106">INapComponentConfig3::SetConfigToID method</span></span>

> [!Note]  
> <span data-ttu-id="e6e78-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="e6e78-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e6e78-108">Метод **сетконфигтоид** реализуется средствами проверки работоспособности системы (SHV) для предоставления способа установки данных конфигурации для конкретного идентификатора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e6e78-108">The **SetConfigToID** method is implemented by system health validators (SHVs) to provide a way to set the configuration data for a specific configuration ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e78-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6e78-109">Syntax</span></span>


```C++
HRESULT SetConfigToID(
  [in] UINT32 configID,
  [in] UINT16 count,
  [in] BYTE   *data
);
```



## <a name="parameters"></a><span data-ttu-id="e6e78-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6e78-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6e78-111">*конфигид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6e78-111">*configID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e78-112">Значение, представляющее конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="e6e78-112">A value that represents the configuration.</span></span> <span data-ttu-id="e6e78-113">*Конфигид* назначается службой сервера политики сети (NPS) и уникальна в SHV.</span><span class="sxs-lookup"><span data-stu-id="e6e78-113">*ConfigID* is assigned by the Network Policy Server (NPS) service and is unique within the SHV.</span></span> <span data-ttu-id="e6e78-114">Если *конфигид* имеет значение 0, задается конфигурация по умолчанию SHV.</span><span class="sxs-lookup"><span data-stu-id="e6e78-114">If *ConfigID* is 0, the default configuration of the SHV is set.</span></span>

</dd> <dt>

<span data-ttu-id="e6e78-115">*количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6e78-115">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e78-116">Размер (в байтах) данных конфигурации в *данных*.</span><span class="sxs-lookup"><span data-stu-id="e6e78-116">The size, in bytes, of the configuration data in *data*.</span></span>

</dd> <dt>

<span data-ttu-id="e6e78-117">*данные* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6e78-117">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e78-118">На входе — массив БАЙТОВ, который содержит набор данных конфигурации для *конфигид*.</span><span class="sxs-lookup"><span data-stu-id="e6e78-118">On input, a BYTE array that contains the configuration data set to *ConfigID*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6e78-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6e78-119">Return value</span></span>

<span data-ttu-id="e6e78-120">Возвращает один из следующих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="e6e78-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="e6e78-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e6e78-121">Return code</span></span>                                                                                                    | <span data-ttu-id="e6e78-122">Описание</span><span class="sxs-lookup"><span data-stu-id="e6e78-122">Description</span></span>                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="e6e78-123"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e6e78-123"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="e6e78-124">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="e6e78-124">The operation is successful.</span></span><br/> |
| <dl> <span data-ttu-id="e6e78-125"><dt>**\_ \_ \_ \_ не \_ найдена Конфигурация NAP E SHV**</dt></span><span class="sxs-lookup"><span data-stu-id="e6e78-125"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="e6e78-126">Не удается найти *конфигид* .</span><span class="sxs-lookup"><span data-stu-id="e6e78-126">*ConfigID* cannot be found.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="e6e78-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6e78-127">Remarks</span></span>

<span data-ttu-id="e6e78-128">Перед вызовом этого метода необходимо использовать метод [**документе newconfig**](inapcomponentconfig3-newconfig.md) для выделения данных конфигурации для *конфигид* .</span><span class="sxs-lookup"><span data-stu-id="e6e78-128">The [**NewConfig**](inapcomponentconfig3-newconfig.md) method must be used to allocate configuration data for *ConfigID* before this method can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6e78-129">Требования</span><span class="sxs-lookup"><span data-stu-id="e6e78-129">Requirements</span></span>



| <span data-ttu-id="e6e78-130">Требование</span><span class="sxs-lookup"><span data-stu-id="e6e78-130">Requirement</span></span> | <span data-ttu-id="e6e78-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e6e78-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e78-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6e78-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e6e78-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e6e78-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e6e78-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6e78-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e6e78-135">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e6e78-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6e78-136">Header</span><span class="sxs-lookup"><span data-stu-id="e6e78-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6e78-137"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6e78-137"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="e6e78-138">IDL</span><span class="sxs-lookup"><span data-stu-id="e6e78-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e6e78-139"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e6e78-139"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6e78-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6e78-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e78-141">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="e6e78-141">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





