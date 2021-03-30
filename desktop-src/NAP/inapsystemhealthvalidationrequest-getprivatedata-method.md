---
title: Метод Инапсистемхеалсвалидатионрекуест Жетприватедата (Напсистемхеалсвалидатор. h)
description: Позволяет Напсервер получать сведения о состоянии.
ms.assetid: f85026ca-852b-4eb1-9a8c-7e03cd1765f2
keywords:
- Метод Жетприватедата NAP
- Метод Жетприватедата NAP, интерфейс Инапсистемхеалсвалидатионрекуест
- Инапсистемхеалсвалидатионрекуест интерфейса NAP, метод Жетприватедата
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d78cceba42cd503ef8a875ece8f4ed196eaeff8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803659"
---
# <a name="inapsystemhealthvalidationrequestgetprivatedata-method"></a><span data-ttu-id="5ada9-106">Метод Инапсистемхеалсвалидатионрекуест:: Жетприватедата</span><span class="sxs-lookup"><span data-stu-id="5ada9-106">INapSystemHealthValidationRequest::GetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="5ada9-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="5ada9-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5ada9-108">Метод **инапсистемхеалсвалидатионрекуест:: жетприватедата** позволяет напсервер получить сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="5ada9-108">The **INapSystemHealthValidationRequest::GetPrivateData** method allows the NapServer to retrieve state information.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ada9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ada9-109">Syntax</span></span>


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="5ada9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ada9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ada9-111">*privateData* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5ada9-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ada9-112">Указатель на указатель на [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) непрозрачный большой двоичный объект данных, содержащий сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="5ada9-112">A pointer to a pointer to [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that contains state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ada9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ada9-113">Return value</span></span>

<span data-ttu-id="5ada9-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="5ada9-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5ada9-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5ada9-115">Return code</span></span>                                                                                     | <span data-ttu-id="5ada9-116">Описание</span><span class="sxs-lookup"><span data-stu-id="5ada9-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ada9-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5ada9-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="5ada9-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="5ada9-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5ada9-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5ada9-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="5ada9-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="5ada9-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="5ada9-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5ada9-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="5ada9-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ada9-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5ada9-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ada9-123">Remarks</span></span>

<span data-ttu-id="5ada9-124">Только Напсервер может интерпретировать большой двоичный объект данных.</span><span class="sxs-lookup"><span data-stu-id="5ada9-124">Only the NapServer can interpret the data blob.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ada9-125">Требования</span><span class="sxs-lookup"><span data-stu-id="5ada9-125">Requirements</span></span>



| <span data-ttu-id="5ada9-126">Требование</span><span class="sxs-lookup"><span data-stu-id="5ada9-126">Requirement</span></span> | <span data-ttu-id="5ada9-127">Значение</span><span class="sxs-lookup"><span data-stu-id="5ada9-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ada9-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ada9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5ada9-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5ada9-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="5ada9-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ada9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5ada9-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5ada9-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5ada9-132">Header</span><span class="sxs-lookup"><span data-stu-id="5ada9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ada9-133"><dt>Напсистемхеалсвалидатор. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ada9-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ada9-134">IDL</span><span class="sxs-lookup"><span data-stu-id="5ada9-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5ada9-135"><dt>Напсистемхеалсвалидатор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5ada9-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="5ada9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5ada9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ada9-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ada9-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="5ada9-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ada9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ada9-139">**инапсистемхеалсвалидатионрекуест**</span><span class="sxs-lookup"><span data-stu-id="5ada9-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





