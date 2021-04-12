---
title: Метод Инапсерверманажемент Унрегистерсистемхеалсвалидатор (Напсерверманажемент. h)
description: Используется для отмены регистрации SHV на сервере NAP.
ms.assetid: f4148df1-a230-4845-ac8b-9e04be9e0d6c
keywords:
- Метод Унрегистерсистемхеалсвалидатор NAP
- Метод Унрегистерсистемхеалсвалидатор NAP, интерфейс Инапсерверманажемент
- Инапсерверманажемент интерфейса NAP, метод Унрегистерсистемхеалсвалидатор
topic_type:
- apiref
api_name:
- INapServerManagement.UnregisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0715445504b862d9ae9e8478b543f8e80378f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535015"
---
# <a name="inapservermanagementunregistersystemhealthvalidator-method"></a><span data-ttu-id="22cc5-106">Метод Инапсерверманажемент:: Унрегистерсистемхеалсвалидатор</span><span class="sxs-lookup"><span data-stu-id="22cc5-106">INapServerManagement::UnregisterSystemHealthValidator method</span></span>

> [!Note]  
> <span data-ttu-id="22cc5-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="22cc5-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="22cc5-108">Метод **инапсерверманажемент:: унрегистерсистемхеалсвалидатор** используется для отмены регистрации SHV на сервере NAP.</span><span class="sxs-lookup"><span data-stu-id="22cc5-108">The **INapServerManagement::UnregisterSystemHealthValidator** method is used to unregister an SHV with the NAP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="22cc5-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22cc5-109">Syntax</span></span>


```C++
HRESULT UnregisterSystemHealthValidator(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="22cc5-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="22cc5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22cc5-111">*идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="22cc5-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22cc5-112">Объект [**системхеалсентитид**](nap-type-constants.md) , содержащий уникальный идентификатор средства SHV для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="22cc5-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHV to unregister.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22cc5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22cc5-113">Return value</span></span>

<span data-ttu-id="22cc5-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="22cc5-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="22cc5-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="22cc5-115">Return code</span></span>                                                                                     | <span data-ttu-id="22cc5-116">Описание</span><span class="sxs-lookup"><span data-stu-id="22cc5-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="22cc5-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="22cc5-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="22cc5-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="22cc5-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="22cc5-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="22cc5-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="22cc5-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="22cc5-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="22cc5-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="22cc5-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="22cc5-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="22cc5-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="22cc5-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="22cc5-123">Remarks</span></span>

<span data-ttu-id="22cc5-124">Если в SHV ожидаются асинхронные вызовы, они будут завершены позже и будут отменены.</span><span class="sxs-lookup"><span data-stu-id="22cc5-124">If there are any asynchronous calls pending on the SHV, they will complete at a later time and will be discarded.</span></span>

## <a name="requirements"></a><span data-ttu-id="22cc5-125">Требования</span><span class="sxs-lookup"><span data-stu-id="22cc5-125">Requirements</span></span>



| <span data-ttu-id="22cc5-126">Требование</span><span class="sxs-lookup"><span data-stu-id="22cc5-126">Requirement</span></span> | <span data-ttu-id="22cc5-127">Значение</span><span class="sxs-lookup"><span data-stu-id="22cc5-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22cc5-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22cc5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="22cc5-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="22cc5-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="22cc5-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22cc5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="22cc5-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="22cc5-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="22cc5-132">Header</span><span class="sxs-lookup"><span data-stu-id="22cc5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="22cc5-133"><dt>Напсерверманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="22cc5-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="22cc5-134">IDL</span><span class="sxs-lookup"><span data-stu-id="22cc5-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="22cc5-135"><dt>Напсерверманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="22cc5-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="22cc5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="22cc5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22cc5-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22cc5-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="22cc5-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22cc5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22cc5-139">**инапсерверманажемент**</span><span class="sxs-lookup"><span data-stu-id="22cc5-139">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





