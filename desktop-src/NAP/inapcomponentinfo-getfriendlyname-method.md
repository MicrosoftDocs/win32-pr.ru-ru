---
title: Метод Инапкомпонентинфо Жетфриендлинаме (Напкоммон. h)
description: Используется системой защиты доступа к сети для получения понятного имени клиента работоспособности.
ms.assetid: 28614f06-a250-4f92-abf2-422675efd8a0
keywords:
- Метод Жетфриендлинаме NAP
- Метод Жетфриендлинаме NAP, интерфейс Инапкомпонентинфо
- Инапкомпонентинфо интерфейса NAP, метод Жетфриендлинаме
topic_type:
- apiref
api_name:
- INapComponentInfo.GetFriendlyName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3848f8fb8365f91bceb5a44c498578f04a1776b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492807"
---
# <a name="inapcomponentinfogetfriendlyname-method"></a><span data-ttu-id="a01d7-106">Метод Инапкомпонентинфо:: Жетфриендлинаме</span><span class="sxs-lookup"><span data-stu-id="a01d7-106">INapComponentInfo::GetFriendlyName method</span></span>

> [!Note]  
> <span data-ttu-id="a01d7-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="a01d7-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a01d7-108">Метод обратного вызова **инапкомпонентинфо:: жетфриендлинаме** используется системой защиты доступа к сети для получения понятного имени клиента работоспособности.</span><span class="sxs-lookup"><span data-stu-id="a01d7-108">The **INapComponentInfo::GetFriendlyName** callback method is used by the NAP System to get the friendly name of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="a01d7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a01d7-109">Syntax</span></span>


```C++
HRESULT GetFriendlyName(
  [out] MessageId *friendlyName
);
```



## <a name="parameters"></a><span data-ttu-id="a01d7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a01d7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a01d7-111">*FriendlyName* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a01d7-111">*friendlyName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a01d7-112">Указатель на [**MessageId**](nap-datatypes.md) , содержащий идентификатор ресурса понятного имени.</span><span class="sxs-lookup"><span data-stu-id="a01d7-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a01d7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a01d7-113">Return value</span></span>

<span data-ttu-id="a01d7-114">Возвращает один из этих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="a01d7-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="a01d7-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a01d7-115">Return code</span></span>                                                                                     | <span data-ttu-id="a01d7-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a01d7-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a01d7-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a01d7-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a01d7-118">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="a01d7-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="a01d7-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a01d7-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a01d7-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="a01d7-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a01d7-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a01d7-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a01d7-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a01d7-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a01d7-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a01d7-123">Requirements</span></span>



| <span data-ttu-id="a01d7-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a01d7-124">Requirement</span></span> | <span data-ttu-id="a01d7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a01d7-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a01d7-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a01d7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a01d7-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a01d7-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a01d7-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a01d7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a01d7-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a01d7-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a01d7-130">Header</span><span class="sxs-lookup"><span data-stu-id="a01d7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a01d7-131"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="a01d7-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="a01d7-132">IDL</span><span class="sxs-lookup"><span data-stu-id="a01d7-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a01d7-133"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a01d7-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a01d7-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a01d7-134">See also</span></span>

<dl> <span data-ttu-id="a01d7-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="a01d7-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="a01d7-136">**инапкомпонентинфо**</span><span class="sxs-lookup"><span data-stu-id="a01d7-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





