---
title: Метод Инапкомпонентконфиг Сетконфиг (Напкоммон. h)
description: Задает конфигурацию компонента средства проверки работоспособности системы (SHV).
ms.assetid: ec27e30b-4205-40bc-a24b-61072a746e53
keywords:
- Метод Сетконфиг NAP
- Метод Сетконфиг NAP, интерфейс Инапкомпонентконфиг
- Инапкомпонентконфиг интерфейса NAP, метод Сетконфиг
topic_type:
- apiref
api_name:
- INapComponentConfig.SetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1f3d557517ec27f9537a7cbcd46be9e2cd107e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535612"
---
# <a name="inapcomponentconfigsetconfig-method"></a><span data-ttu-id="e7c58-106">Метод Инапкомпонентконфиг:: Сетконфиг</span><span class="sxs-lookup"><span data-stu-id="e7c58-106">INapComponentConfig::SetConfig method</span></span>

> [!Note]  
> <span data-ttu-id="e7c58-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="e7c58-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e7c58-108">Метод **сетконфиг** задает конфигурацию компонента средства проверки работоспособности системы (SHV).</span><span class="sxs-lookup"><span data-stu-id="e7c58-108">The **SetConfig** method sets the system health validator (SHV) component configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7c58-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7c58-109">Syntax</span></span>


```C++
HRESULT SetConfig(
  [in] UINT16 bCount,
  [in] BYTE   *data
);
```



## <a name="parameters"></a><span data-ttu-id="e7c58-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7c58-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7c58-111">*бкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e7c58-111">*bCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7c58-112">Размер большого двоичного объекта конфигурации *данных* (в байтах).</span><span class="sxs-lookup"><span data-stu-id="e7c58-112">The size, in bytes, of the *data* configuration blob.</span></span>

</dd> <dt>

<span data-ttu-id="e7c58-113">*данные* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e7c58-113">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7c58-114">Указатель на данные конфигурации компонента SHV.</span><span class="sxs-lookup"><span data-stu-id="e7c58-114">A pointer to the SHV component configuration data.</span></span>

> [!Note]  
> <span data-ttu-id="e7c58-115">Данные конфигурации, экспортированные с компьютера x86 с помощью метода [**config**](inapcomponentconfig-getconfig.md) , можно импортировать на компьютер x64 с помощью метода **сетконфиг** и наоборот.</span><span class="sxs-lookup"><span data-stu-id="e7c58-115">Configuration data exported from an x86 machine using the [**GetConfig**](inapcomponentconfig-getconfig.md) method may be imported onto an x64 machine using the **SetConfig** method, and vice versa.</span></span> <span data-ttu-id="e7c58-116">Поэтому данные конфигурации должны быть в независимом от архитектуры формате, таком как XML.</span><span class="sxs-lookup"><span data-stu-id="e7c58-116">Therefore, configuration data must be in an architecture-agnostic format such as XML.</span></span> <span data-ttu-id="e7c58-117">Использование XML вместо байтового потока упрощает использование данных конфигурации в различных архитектурах.</span><span class="sxs-lookup"><span data-stu-id="e7c58-117">Using XML instead of a byte stream makes it easier to use configuration data on different architectures.</span></span> <span data-ttu-id="e7c58-118">Элементы XML, используемые в данных конфигурации, определяются разработчиком.</span><span class="sxs-lookup"><span data-stu-id="e7c58-118">The XML elements used in the configuration data are determined by the implementer.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7c58-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7c58-119">Return value</span></span>

<span data-ttu-id="e7c58-120">Возвращает один из следующих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="e7c58-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="e7c58-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e7c58-121">Return code</span></span>                                                                                     | <span data-ttu-id="e7c58-122">Описание</span><span class="sxs-lookup"><span data-stu-id="e7c58-122">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e7c58-123"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e7c58-123"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="e7c58-124">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="e7c58-124">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="e7c58-125"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e7c58-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="e7c58-126">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="e7c58-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="e7c58-127"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e7c58-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="e7c58-128">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e7c58-128">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e7c58-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7c58-129">Remarks</span></span>

<span data-ttu-id="e7c58-130">Сведения об управлении версиями компонентов должны включаться в большой двоичный объект конфигурации *данных* .</span><span class="sxs-lookup"><span data-stu-id="e7c58-130">Component versioning information should be included in the *data* configuration blob.</span></span> <span data-ttu-id="e7c58-131">Сведения об управлении версиями могут использоваться при переходе с одной версии SHV на другую.</span><span class="sxs-lookup"><span data-stu-id="e7c58-131">The versioning information may be used when migrating from one SHV version to another.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7c58-132">Требования</span><span class="sxs-lookup"><span data-stu-id="e7c58-132">Requirements</span></span>



| <span data-ttu-id="e7c58-133">Требование</span><span class="sxs-lookup"><span data-stu-id="e7c58-133">Requirement</span></span> | <span data-ttu-id="e7c58-134">Значение</span><span class="sxs-lookup"><span data-stu-id="e7c58-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7c58-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7c58-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e7c58-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e7c58-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e7c58-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7c58-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e7c58-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e7c58-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e7c58-139">Header</span><span class="sxs-lookup"><span data-stu-id="e7c58-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7c58-140"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7c58-140"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7c58-141">IDL</span><span class="sxs-lookup"><span data-stu-id="e7c58-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e7c58-142"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e7c58-142"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7c58-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7c58-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7c58-144">**инапкомпонентконфиг**</span><span class="sxs-lookup"><span data-stu-id="e7c58-144">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="e7c58-145">**Инапконпонентконфиг:: config**</span><span class="sxs-lookup"><span data-stu-id="e7c58-145">**INapConponentConfig::GetConfig**</span></span>](inapcomponentconfig-getconfig.md)
</dt> </dl>

 

 





