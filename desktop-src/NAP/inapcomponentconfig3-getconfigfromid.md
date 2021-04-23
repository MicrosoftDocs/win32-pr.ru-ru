---
title: Метод INapComponentConfig3 Жетконфигфромид (Напкоммон. h)
description: Реализуется средствами проверки работоспособности системы (SHV) для предоставления данных конфигурации для определенного идентификатора конфигурации.
ms.assetid: 5c91681d-16d6-42f3-b1e0-c4b6e7561a73
keywords:
- Метод Жетконфигфромид NAP
- Метод Жетконфигфромид NAP, интерфейс INapComponentConfig3
- INapComponentConfig3 интерфейса NAP, метод Жетконфигфромид
topic_type:
- apiref
api_name:
- INapComponentConfig3.GetConfigFromID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce3a0e20f19c73271cdcba4070972649fe25aea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801853"
---
# <a name="inapcomponentconfig3getconfigfromid-method"></a><span data-ttu-id="35fb3-106">Метод INapComponentConfig3:: Жетконфигфромид</span><span class="sxs-lookup"><span data-stu-id="35fb3-106">INapComponentConfig3::GetConfigFromID method</span></span>

> [!Note]  
> <span data-ttu-id="35fb3-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="35fb3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="35fb3-108">Метод **жетконфигфромид** реализуется средствами проверки работоспособности системы (SHV) для предоставления данных конфигурации для определенного идентификатора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="35fb3-108">The **GetConfigFromID** method is implemented by system health validators (SHVs) to provide a way to obtain configuration data for a specific configuration ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="35fb3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35fb3-109">Syntax</span></span>


```C++
HRESULT GetConfigFromID(
  [in]  UINT32 configID,
  [out] UINT16 *count,
  [out] BYTE   **outdata
);
```



## <a name="parameters"></a><span data-ttu-id="35fb3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="35fb3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35fb3-111">*конфигид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35fb3-111">*configID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35fb3-112">Значение, представляющее конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="35fb3-112">A value that represents the configuration.</span></span> <span data-ttu-id="35fb3-113">Если *конфигид* имеет значение **0**, SHV должен вернуть данные конфигурации по умолчанию в *данные*.</span><span class="sxs-lookup"><span data-stu-id="35fb3-113">If *ConfigID* is **0**, the SHV should return the default configuration data in *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="35fb3-114">*количество* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="35fb3-114">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35fb3-115">Размер (в байтах) данных конфигурации, возвращаемых в *данных*.</span><span class="sxs-lookup"><span data-stu-id="35fb3-115">The size, in bytes, of the configuration data returned in *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="35fb3-116">*данные* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="35fb3-116">*outdata* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35fb3-117">При возвращении — массив БАЙТОВ, содержащий данные конфигурации, представленные параметром *конфигид*.</span><span class="sxs-lookup"><span data-stu-id="35fb3-117">On return, a BYTE array that contains the configuration data represented by *ConfigID*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35fb3-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35fb3-118">Return value</span></span>

<span data-ttu-id="35fb3-119">Возвращает один из следующих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="35fb3-119">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="35fb3-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="35fb3-120">Return code</span></span>                                                                                                    | <span data-ttu-id="35fb3-121">Описание</span><span class="sxs-lookup"><span data-stu-id="35fb3-121">Description</span></span>                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="35fb3-122"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="35fb3-122"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="35fb3-123">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="35fb3-123">The operation is successful.</span></span><br/> |
| <dl> <span data-ttu-id="35fb3-124"><dt>**\_ \_ \_ \_ не \_ найдена Конфигурация NAP E SHV**</dt></span><span class="sxs-lookup"><span data-stu-id="35fb3-124"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="35fb3-125">Не удается найти *конфигид* .</span><span class="sxs-lookup"><span data-stu-id="35fb3-125">*ConfigID* cannot be found.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="35fb3-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35fb3-126">Remarks</span></span>

<span data-ttu-id="35fb3-127">Перед вызовом этого метода необходимо использовать метод [**документе newconfig**](inapcomponentconfig3-newconfig.md) для выделения данных конфигурации для *конфигид* .</span><span class="sxs-lookup"><span data-stu-id="35fb3-127">The [**NewConfig**](inapcomponentconfig3-newconfig.md) method must be used to allocate configuration data for *ConfigID* before this method can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="35fb3-128">Требования</span><span class="sxs-lookup"><span data-stu-id="35fb3-128">Requirements</span></span>



| <span data-ttu-id="35fb3-129">Требование</span><span class="sxs-lookup"><span data-stu-id="35fb3-129">Requirement</span></span> | <span data-ttu-id="35fb3-130">Значение</span><span class="sxs-lookup"><span data-stu-id="35fb3-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="35fb3-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35fb3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="35fb3-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="35fb3-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="35fb3-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35fb3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="35fb3-134">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="35fb3-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="35fb3-135">Header</span><span class="sxs-lookup"><span data-stu-id="35fb3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="35fb3-136"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="35fb3-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="35fb3-137">IDL</span><span class="sxs-lookup"><span data-stu-id="35fb3-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="35fb3-138"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="35fb3-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35fb3-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35fb3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35fb3-140">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="35fb3-140">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





