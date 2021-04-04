---
title: Метод Инапсистемхеалсвалидатионрекуест Сетприватедата (Напсистемхеалсвалидатор. h)
description: Позволяет Напсервер хранить сведения о состоянии.
ms.assetid: 128f9beb-e5da-4b20-bf5e-fcf064209da3
keywords:
- Метод Сетприватедата NAP
- Метод Сетприватедата NAP, интерфейс Инапсистемхеалсвалидатионрекуест
- Инапсистемхеалсвалидатионрекуест интерфейса NAP, метод Сетприватедата
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da50ca236c08388632e17916decee162b3b71743
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802818"
---
# <a name="inapsystemhealthvalidationrequestsetprivatedata-method"></a><span data-ttu-id="d16b3-106">Метод Инапсистемхеалсвалидатионрекуест:: Сетприватедата</span><span class="sxs-lookup"><span data-stu-id="d16b3-106">INapSystemHealthValidationRequest::SetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="d16b3-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="d16b3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d16b3-108">Метод **инапсистемхеалсвалидатионрекуест:: сетприватедата** позволяет напсервер хранить сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="d16b3-108">The **INapSystemHealthValidationRequest::SetPrivateData** method allows the NapServer to store state information.</span></span>

## <a name="syntax"></a><span data-ttu-id="d16b3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d16b3-109">Syntax</span></span>


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="d16b3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d16b3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d16b3-111">*privateData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d16b3-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d16b3-112">Указатель на большой двоичный объект данных [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) , содержащий сведения о непрозрачном состоянии.</span><span class="sxs-lookup"><span data-stu-id="d16b3-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) data blob that contains the opaque state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d16b3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d16b3-113">Return value</span></span>

<span data-ttu-id="d16b3-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="d16b3-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="d16b3-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d16b3-115">Return code</span></span>                                                                                     | <span data-ttu-id="d16b3-116">Описание</span><span class="sxs-lookup"><span data-stu-id="d16b3-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d16b3-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d16b3-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="d16b3-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="d16b3-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d16b3-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="d16b3-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="d16b3-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="d16b3-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="d16b3-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d16b3-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="d16b3-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d16b3-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d16b3-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d16b3-123">Remarks</span></span>

<span data-ttu-id="d16b3-124">Только Напсервер может интерпретировать большой двоичный объект данных.</span><span class="sxs-lookup"><span data-stu-id="d16b3-124">Only the NapServer can interpret the data blob.</span></span>

## <a name="requirements"></a><span data-ttu-id="d16b3-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d16b3-125">Requirements</span></span>



| <span data-ttu-id="d16b3-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d16b3-126">Requirement</span></span> | <span data-ttu-id="d16b3-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d16b3-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d16b3-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d16b3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d16b3-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d16b3-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="d16b3-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d16b3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d16b3-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d16b3-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d16b3-132">Header</span><span class="sxs-lookup"><span data-stu-id="d16b3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d16b3-133"><dt>Напсистемхеалсвалидатор. h</dt></span><span class="sxs-lookup"><span data-stu-id="d16b3-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="d16b3-134">IDL</span><span class="sxs-lookup"><span data-stu-id="d16b3-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d16b3-135"><dt>Напсистемхеалсвалидатор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d16b3-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="d16b3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d16b3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d16b3-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d16b3-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="d16b3-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d16b3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d16b3-139">**инапсистемхеалсвалидатионрекуест**</span><span class="sxs-lookup"><span data-stu-id="d16b3-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





