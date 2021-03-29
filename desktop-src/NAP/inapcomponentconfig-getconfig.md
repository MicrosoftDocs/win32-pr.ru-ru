---
title: Метод Инапкомпонентконфиг-config (Напкоммон. h)
description: Извлекает конфигурацию компонента средства проверки работоспособности системы (SHV).
ms.assetid: 57a1d3a7-05c0-4e0f-91b8-b3cf8982d04f
keywords:
- Метод config NAP
- Метод config NAP, интерфейс Инапкомпонентконфиг
- Инапкомпонентконфиг интерфейса NAP, метод config
topic_type:
- apiref
api_name:
- INapComponentConfig.GetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e07465d768c8902166150e53d4200e775e2597
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492336"
---
# <a name="inapcomponentconfiggetconfig-method"></a><span data-ttu-id="60e99-106">Метод Инапкомпонентконфиг:: config</span><span class="sxs-lookup"><span data-stu-id="60e99-106">INapComponentConfig::GetConfig method</span></span>

> [!Note]  
> <span data-ttu-id="60e99-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="60e99-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="60e99-108">Метод **config** извлекает конфигурацию компонента средства проверки работоспособности системы (SHV).</span><span class="sxs-lookup"><span data-stu-id="60e99-108">The **GetConfig** method retrieves the system health validator (SHV) component configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="60e99-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60e99-109">Syntax</span></span>


```C++
HRESULT GetConfig(
  [out] UINT16 *bCount,
  [out] BYTE   **data
) const;
```



## <a name="parameters"></a><span data-ttu-id="60e99-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="60e99-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60e99-111">*бкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="60e99-111">*bCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60e99-112">Размер большого двоичного объекта конфигурации *данных* (в байтах).</span><span class="sxs-lookup"><span data-stu-id="60e99-112">The size, in bytes, of the *data* configuration blob.</span></span>

</dd> <dt>

<span data-ttu-id="60e99-113">*данные* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="60e99-113">*data* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60e99-114">Указатель на адрес данных конфигурации компонента SHV.</span><span class="sxs-lookup"><span data-stu-id="60e99-114">A pointer to the address of the SHV component configuration data.</span></span>

> [!Note]  
> <span data-ttu-id="60e99-115">Данные конфигурации, экспортированные с компьютера x86 с помощью метода **config** , можно импортировать на компьютер x64 с помощью метода [**сетконфиг**](inapcomponentconfig-setconfig.md) и наоборот.</span><span class="sxs-lookup"><span data-stu-id="60e99-115">Configuration data exported from an x86 machine using the **GetConfig** method may be imported onto an x64 machine using the [**SetConfig**](inapcomponentconfig-setconfig.md) method, and vice versa.</span></span> <span data-ttu-id="60e99-116">Поэтому данные конфигурации должны быть в независимом от архитектуры формате, таком как XML.</span><span class="sxs-lookup"><span data-stu-id="60e99-116">Therefore, configuration data must be in an architecture-agnostic format such as XML.</span></span> <span data-ttu-id="60e99-117">Использование XML вместо байтового потока упрощает использование данных конфигурации в различных архитектурах.</span><span class="sxs-lookup"><span data-stu-id="60e99-117">Using XML instead of a byte stream makes it easier to use configuration data on different architectures.</span></span> <span data-ttu-id="60e99-118">Элементы XML, используемые в данных конфигурации, определяются разработчиком.</span><span class="sxs-lookup"><span data-stu-id="60e99-118">The XML elements used in the configuration data are determined by the implementer.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60e99-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60e99-119">Return value</span></span>

<span data-ttu-id="60e99-120">Возвращает один из следующих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="60e99-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="60e99-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="60e99-121">Return code</span></span>                                                                                     | <span data-ttu-id="60e99-122">Описание</span><span class="sxs-lookup"><span data-stu-id="60e99-122">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="60e99-123"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="60e99-123"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="60e99-124">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="60e99-124">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="60e99-125"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="60e99-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="60e99-126">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="60e99-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="60e99-127"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="60e99-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="60e99-128">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60e99-128">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="60e99-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60e99-129">Remarks</span></span>

<span data-ttu-id="60e99-130">Параметр данных должен выделяться вызываемым объектом (реализующим компонентом) с помощью функции **CoTaskMemAlloc** и освобождены вызывающей стороной с помощью **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="60e99-130">The data parameter must be allocated by the callee (component implementor) using **CoTaskMemAlloc** and freed by the caller using **CoTaskMemFree**.</span></span>

## <a name="requirements"></a><span data-ttu-id="60e99-131">Требования</span><span class="sxs-lookup"><span data-stu-id="60e99-131">Requirements</span></span>



| <span data-ttu-id="60e99-132">Требование</span><span class="sxs-lookup"><span data-stu-id="60e99-132">Requirement</span></span> | <span data-ttu-id="60e99-133">Значение</span><span class="sxs-lookup"><span data-stu-id="60e99-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="60e99-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60e99-134">Minimum supported client</span></span><br/> | <span data-ttu-id="60e99-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="60e99-135">None supported</span></span><br/>                                                                |
| <span data-ttu-id="60e99-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60e99-136">Minimum supported server</span></span><br/> | <span data-ttu-id="60e99-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="60e99-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="60e99-138">Header</span><span class="sxs-lookup"><span data-stu-id="60e99-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="60e99-139"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="60e99-139"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="60e99-140">IDL</span><span class="sxs-lookup"><span data-stu-id="60e99-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="60e99-141"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="60e99-141"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60e99-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60e99-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e99-143">**инапкомпонентконфиг**</span><span class="sxs-lookup"><span data-stu-id="60e99-143">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="60e99-144">**Инапкомпонентконфиг:: Сетконфиг**</span><span class="sxs-lookup"><span data-stu-id="60e99-144">**INapComponentConfig::SetConfig**</span></span>](inapcomponentconfig-setconfig.md)
</dt> </dl>

 

 





