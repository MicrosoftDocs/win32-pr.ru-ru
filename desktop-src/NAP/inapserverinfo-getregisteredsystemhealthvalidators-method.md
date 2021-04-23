---
title: Метод Инапсерверинфо Жетрегистередсистемхеалсвалидаторс (Напсерверманажемент. h)
description: Извлекает список зарегистрированных SHV.
ms.assetid: 029c7d5c-b397-415c-a530-0096de1ef771
keywords:
- Метод Жетрегистередсистемхеалсвалидаторс NAP
- Метод Жетрегистередсистемхеалсвалидаторс NAP, интерфейс Инапсерверинфо
- Инапсерверинфо интерфейса NAP, метод Жетрегистередсистемхеалсвалидаторс
topic_type:
- apiref
api_name:
- INapServerInfo.GetRegisteredSystemHealthValidators
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ffdd4d363c994efbecdb57fe4ad7203393fd1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071891"
---
# <a name="inapserverinfogetregisteredsystemhealthvalidators-method"></a><span data-ttu-id="08813-106">Метод Инапсерверинфо:: Жетрегистередсистемхеалсвалидаторс</span><span class="sxs-lookup"><span data-stu-id="08813-106">INapServerInfo::GetRegisteredSystemHealthValidators method</span></span>

> [!Note]  
> <span data-ttu-id="08813-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="08813-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="08813-108">Метод **инапсерверинфо:: жетрегистередсистемхеалсвалидаторс** извлекает список зарегистрированных SHV.</span><span class="sxs-lookup"><span data-stu-id="08813-108">The **INapServerInfo::GetRegisteredSystemHealthValidators** method retrieves a list of registered SHVs.</span></span>

## <a name="syntax"></a><span data-ttu-id="08813-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08813-109">Syntax</span></span>


```C++
HRESULT GetRegisteredSystemHealthValidators(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **validators,
  [out] CLSID                        **validatorClsids
);
```



## <a name="parameters"></a><span data-ttu-id="08813-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="08813-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08813-111">*количество* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="08813-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08813-112">Указатель на [**системхеалсентитикаунт**](nap-type-constants.md) , содержащий число зарегистрированных SHV.</span><span class="sxs-lookup"><span data-stu-id="08813-112">A pointer to a [**SystemHealthEntityCount**](nap-type-constants.md) that contains the number of registered SHVs.</span></span>

</dd> <dt>

<span data-ttu-id="08813-113">*проверяющие элементы управления* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="08813-113">*validators* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08813-114">Указатель на указатель на структуру [**напкомпонентрегистратионинфо**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) , содержащую сведения о регистрации SHV.</span><span class="sxs-lookup"><span data-stu-id="08813-114">A pointer to a pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the SHV registration information.</span></span>

</dd> <dt>

<span data-ttu-id="08813-115">*валидаторклсидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="08813-115">*validatorClsids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08813-116">Указатель на массив идентификаторов зарегистрированных SHV.</span><span class="sxs-lookup"><span data-stu-id="08813-116">Pointer to an array of IDs for the registered SHVs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08813-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08813-117">Return value</span></span>

<span data-ttu-id="08813-118">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="08813-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="08813-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="08813-119">Return code</span></span>                                                                                     | <span data-ttu-id="08813-120">Описание</span><span class="sxs-lookup"><span data-stu-id="08813-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="08813-121"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="08813-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="08813-122">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="08813-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="08813-123"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="08813-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="08813-124">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="08813-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="08813-125"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="08813-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="08813-126">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="08813-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="08813-127">Требования</span><span class="sxs-lookup"><span data-stu-id="08813-127">Requirements</span></span>



| <span data-ttu-id="08813-128">Требование</span><span class="sxs-lookup"><span data-stu-id="08813-128">Requirement</span></span> | <span data-ttu-id="08813-129">Значение</span><span class="sxs-lookup"><span data-stu-id="08813-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08813-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08813-130">Minimum supported client</span></span><br/> | <span data-ttu-id="08813-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="08813-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="08813-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08813-132">Minimum supported server</span></span><br/> | <span data-ttu-id="08813-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="08813-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="08813-134">Header</span><span class="sxs-lookup"><span data-stu-id="08813-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="08813-135"><dt>Напсерверманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="08813-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="08813-136">IDL</span><span class="sxs-lookup"><span data-stu-id="08813-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="08813-137"><dt>Напсерверманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="08813-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="08813-138">DLL</span><span class="sxs-lookup"><span data-stu-id="08813-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08813-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08813-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="08813-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08813-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08813-141">**напкомпонентрегистратионинфо**</span><span class="sxs-lookup"><span data-stu-id="08813-141">**NapComponentRegistrationInfo**</span></span>](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)
</dt> <dt>

[<span data-ttu-id="08813-142">**инапсерверинфо**</span><span class="sxs-lookup"><span data-stu-id="08813-142">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> </dl>

 

 





