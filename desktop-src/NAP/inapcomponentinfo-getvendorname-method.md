---
title: Метод Инапкомпонентинфо Жетвендорнаме (Напкоммон. h)
description: Используется системой защиты доступа к сети для получения имени поставщика клиента работоспособности.
ms.assetid: 7083b0b6-38fc-4c24-a5f7-fe0a1ebd5e88
keywords:
- Метод Жетвендорнаме NAP
- Метод Жетвендорнаме NAP, интерфейс Инапкомпонентинфо
- Инапкомпонентинфо интерфейса NAP, метод Жетвендорнаме
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVendorName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3c82f4e7e4f76d827e71421c467a8a223428a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493251"
---
# <a name="inapcomponentinfogetvendorname-method"></a><span data-ttu-id="e2481-106">Метод Инапкомпонентинфо:: Жетвендорнаме</span><span class="sxs-lookup"><span data-stu-id="e2481-106">INapComponentInfo::GetVendorName method</span></span>

> [!Note]  
> <span data-ttu-id="e2481-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="e2481-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e2481-108">Метод обратного вызова **инапкомпонентинфо:: жетвендорнаме** используется системой защиты доступа к сети для получения имени поставщика клиента работоспособности.</span><span class="sxs-lookup"><span data-stu-id="e2481-108">The **INapComponentInfo::GetVendorName** callback method is used by the NAP System to get the vendor name of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2481-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2481-109">Syntax</span></span>


```C++
HRESULT GetVendorName(
  [out] MessageId *vendorName
);
```



## <a name="parameters"></a><span data-ttu-id="e2481-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2481-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2481-111">*ИмяПоставщика* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e2481-111">*vendorName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2481-112">Указатель на [**MessageId**](nap-datatypes.md) , содержащий идентификатор ресурса для имени поставщика.</span><span class="sxs-lookup"><span data-stu-id="e2481-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the vendor name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2481-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2481-113">Return value</span></span>

<span data-ttu-id="e2481-114">Возвращает один из этих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="e2481-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="e2481-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e2481-115">Return code</span></span>                                                                                     | <span data-ttu-id="e2481-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e2481-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e2481-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e2481-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="e2481-118">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="e2481-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="e2481-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e2481-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="e2481-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="e2481-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="e2481-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e2481-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="e2481-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2481-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e2481-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e2481-123">Requirements</span></span>



| <span data-ttu-id="e2481-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e2481-124">Requirement</span></span> | <span data-ttu-id="e2481-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e2481-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2481-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2481-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e2481-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2481-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e2481-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2481-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e2481-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e2481-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e2481-130">Header</span><span class="sxs-lookup"><span data-stu-id="e2481-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2481-131"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2481-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="e2481-132">IDL</span><span class="sxs-lookup"><span data-stu-id="e2481-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e2481-133"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e2481-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2481-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2481-134">See also</span></span>

<dl> <span data-ttu-id="e2481-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="e2481-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="e2481-136">**инапкомпонентинфо**</span><span class="sxs-lookup"><span data-stu-id="e2481-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





