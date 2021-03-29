---
title: Метод Инапсерверманажемент Регистерсистемхеалсвалидатор (Напсерверманажемент. h)
description: Регистрирует SHV.
ms.assetid: 23f147d5-3c4e-48ca-940a-c4350ad6ecb3
keywords:
- Метод Регистерсистемхеалсвалидатор NAP
- Метод Регистерсистемхеалсвалидатор NAP, интерфейс Инапсерверманажемент
- Инапсерверманажемент интерфейса NAP, метод Регистерсистемхеалсвалидатор
topic_type:
- apiref
api_name:
- INapServerManagement.RegisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abd8d42da196caa804a8919c6425fda9fcb950c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262232"
---
# <a name="inapservermanagementregistersystemhealthvalidator-method"></a><span data-ttu-id="d6815-106">Метод Инапсерверманажемент:: Регистерсистемхеалсвалидатор</span><span class="sxs-lookup"><span data-stu-id="d6815-106">INapServerManagement::RegisterSystemHealthValidator method</span></span>

> [!Note]  
> <span data-ttu-id="d6815-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="d6815-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d6815-108">Метод **инапсерверманажемент:: регистерсистемхеалсвалидатор** регистрирует SHV.</span><span class="sxs-lookup"><span data-stu-id="d6815-108">The **INapServerManagement::RegisterSystemHealthValidator** method registers an SHV.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6815-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6815-109">Syntax</span></span>


```C++
HRESULT RegisterSystemHealthValidator(
  [in] const NapComponentRegistrationInfo *validator,
  [in] const CLSID                        *validatorClsid
);
```



## <a name="parameters"></a><span data-ttu-id="d6815-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6815-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6815-111">*проверяющий элемент управления* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6815-111">*validator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6815-112">Указатель на структуру [**напкомпонентрегистратионинфо**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) , содержащую сведения о регистрации SHV.</span><span class="sxs-lookup"><span data-stu-id="d6815-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the SHV registration information.</span></span>

</dd> <dt>

<span data-ttu-id="d6815-113">*валидаторклсид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6815-113">*validatorClsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6815-114">Указатель на идентификатор CLSID класса COM, который реализует интерфейс [**инапсистемхеалсвалидатор**](inapsystemhealthvalidator.md) .</span><span class="sxs-lookup"><span data-stu-id="d6815-114">A pointer to the CLSID of the COM class that implements the [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6815-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6815-115">Return value</span></span>

<span data-ttu-id="d6815-116">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="d6815-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="d6815-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d6815-117">Return code</span></span>                                                                                            | <span data-ttu-id="d6815-118">Описание</span><span class="sxs-lookup"><span data-stu-id="d6815-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d6815-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d6815-119"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="d6815-120">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="d6815-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d6815-121"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="d6815-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="d6815-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="d6815-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="d6815-123"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d6815-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="d6815-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6815-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="d6815-125"><dt>**\_ \_ конфликтующий идентификатор NAP \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="d6815-125"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="d6815-126">Идентификатор SHV уже зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="d6815-126">SHV id is already registered.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="d6815-127">Требования</span><span class="sxs-lookup"><span data-stu-id="d6815-127">Requirements</span></span>



| <span data-ttu-id="d6815-128">Требование</span><span class="sxs-lookup"><span data-stu-id="d6815-128">Requirement</span></span> | <span data-ttu-id="d6815-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d6815-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6815-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6815-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d6815-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d6815-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="d6815-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6815-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d6815-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d6815-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d6815-134">Header</span><span class="sxs-lookup"><span data-stu-id="d6815-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6815-135"><dt>Напсерверманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6815-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6815-136">IDL</span><span class="sxs-lookup"><span data-stu-id="d6815-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d6815-137"><dt>Напсерверманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d6815-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="d6815-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d6815-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6815-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6815-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="d6815-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6815-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6815-141">**инапсерверманажемент**</span><span class="sxs-lookup"><span data-stu-id="d6815-141">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





