---
title: Метод INapComponentConfig2 Исремотеконфигсуппортед (Напкоммон. h)
description: Реализуется с помощью средств проверки работоспособности системы (SHV), чтобы указать, поддерживается ли удаленная конфигурация.
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- Метод Исремотеконфигсуппортед NAP
- Метод Исремотеконфигсуппортед NAP, интерфейс INapComponentConfig2
- INapComponentConfig2 интерфейса NAP, метод Исремотеконфигсуппортед
topic_type:
- apiref
api_name:
- INapComponentConfig2.IsRemoteConfigSupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d144926aafff6f5ad7e243efe2a81a2955f497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988450"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a><span data-ttu-id="63b80-106">Метод INapComponentConfig2:: Исремотеконфигсуппортед</span><span class="sxs-lookup"><span data-stu-id="63b80-106">INapComponentConfig2::IsRemoteConfigSupported method</span></span>

> [!Note]  
> <span data-ttu-id="63b80-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="63b80-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="63b80-108">Метод **исремотеконфигсуппортед** реализуется средствами проверки работоспособности системы (SHV), чтобы указать, поддерживается ли удаленная конфигурация.</span><span class="sxs-lookup"><span data-stu-id="63b80-108">The **IsRemoteConfigSupported** method is implemented by system health validators (SHVs) to indicate whether remote configuration is supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="63b80-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63b80-109">Syntax</span></span>


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a><span data-ttu-id="63b80-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="63b80-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63b80-111">*поддерживается* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="63b80-111">*isSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63b80-112">Указатель на логическое значение, равное **true** , если компонент поддерживает удаленную настройку, и **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="63b80-112">A pointer to a BOOL that is set to **TRUE** if the component supports remote configuration, and **FALSE** if it does not.</span></span>

</dd> <dt>

<span data-ttu-id="63b80-113">*ремотеконфигтипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="63b80-113">*remoteConfigType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63b80-114">Указывает тип удаленной конфигурации, поддерживаемой с помощью значения из перечисления [**ремотеконфигуратионтипе**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) :</span><span class="sxs-lookup"><span data-stu-id="63b80-114">Indicates the type of remote configuration supported using value from the [**RemoteConfigurationType**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) enumeration:</span></span>



| <span data-ttu-id="63b80-115">Значение</span><span class="sxs-lookup"><span data-stu-id="63b80-115">Value</span></span>                                                                                                 | <span data-ttu-id="63b80-116">Значение</span><span class="sxs-lookup"><span data-stu-id="63b80-116">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63b80-117"><dt>ремотеконфигтипемачине</dt></span><span class="sxs-lookup"><span data-stu-id="63b80-117"><dt>remoteConfigTypeMachine</dt></span></span> </dl>    | <span data-ttu-id="63b80-118">[**Инвокеуиформачине**](inapcomponentconfig2-invokeuiformachine.md) реализован.</span><span class="sxs-lookup"><span data-stu-id="63b80-118">[**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) is implemented.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="63b80-119"><dt>ремотеконфигтипеконфигблоб</dt></span><span class="sxs-lookup"><span data-stu-id="63b80-119"><dt>remoteConfigTypeConfigBlob</dt></span></span> </dl> | <span data-ttu-id="63b80-120">[**Инвокеуифромконфигблоб**](inapcomponentconfig2-invokeuifromconfigblob.md) реализован.</span><span class="sxs-lookup"><span data-stu-id="63b80-120">[**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) is implemented.</span></span> <span data-ttu-id="63b80-121">[**Инапкомпонентконфиг:: config**](inapcomponentconfig-getconfig.md) и [**Инапкомпонентконфиг:: сетконфиг**](inapcomponentconfig-setconfig.md) можно вызывать удаленно с помощью DCOM.</span><span class="sxs-lookup"><span data-stu-id="63b80-121">[**INapComponentConfig::GetConfig**](inapcomponentconfig-getconfig.md) and [**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md) can be called remotely using DCOM.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63b80-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63b80-122">Return value</span></span>

<span data-ttu-id="63b80-123">Возвращает значение \_ ОК, если успешно, или один из стандартных кодов ошибок Windows.</span><span class="sxs-lookup"><span data-stu-id="63b80-123">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="63b80-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63b80-124">Remarks</span></span>

<span data-ttu-id="63b80-125">Если ни [**инвокеуиформачине**](inapcomponentconfig2-invokeuiformachine.md) , ни [**инвокеуифромконфигблоб**](inapcomponentconfig2-invokeuifromconfigblob.md) не реализованы, удаленная настройка SHV невозможна.</span><span class="sxs-lookup"><span data-stu-id="63b80-125">If neither [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) nor [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) are implemented, remote configuration of the SHV is not possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="63b80-126">Требования</span><span class="sxs-lookup"><span data-stu-id="63b80-126">Requirements</span></span>



| <span data-ttu-id="63b80-127">Требование</span><span class="sxs-lookup"><span data-stu-id="63b80-127">Requirement</span></span> | <span data-ttu-id="63b80-128">Значение</span><span class="sxs-lookup"><span data-stu-id="63b80-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="63b80-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63b80-129">Minimum supported client</span></span><br/> | <span data-ttu-id="63b80-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="63b80-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="63b80-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63b80-131">Minimum supported server</span></span><br/> | <span data-ttu-id="63b80-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63b80-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="63b80-133">Header</span><span class="sxs-lookup"><span data-stu-id="63b80-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="63b80-134"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="63b80-134"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="63b80-135">IDL</span><span class="sxs-lookup"><span data-stu-id="63b80-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63b80-136"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="63b80-136"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63b80-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63b80-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63b80-138">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="63b80-138">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





