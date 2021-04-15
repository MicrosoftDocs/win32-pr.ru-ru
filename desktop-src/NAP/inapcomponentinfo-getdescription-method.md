---
title: Метод Инапкомпонентинфо-Description (Напкоммон. h)
description: Используется системой защиты доступа к сети для получения описания клиента работоспособности.
ms.assetid: f8d1d5ea-0de6-426d-90eb-b035b5bd0bfd
keywords:
- Метод описания NAP
- Метод Description NAP, интерфейс Инапкомпонентинфо
- Инапкомпонентинфо интерфейса NAP, метод методаического описания
topic_type:
- apiref
api_name:
- INapComponentInfo.GetDescription
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499aee6f7805925cc68c08b580db7b1b72763165
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661833"
---
# <a name="inapcomponentinfogetdescription-method"></a><span data-ttu-id="63af1-106">Инапкомпонентинфо:: метод Description</span><span class="sxs-lookup"><span data-stu-id="63af1-106">INapComponentInfo::GetDescription method</span></span>

> [!Note]  
> <span data-ttu-id="63af1-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="63af1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="63af1-108">Метод обратного вызова **инапкомпонентинфо::-Description** используется системой защиты доступа к сети для получения описания клиента работоспособности.</span><span class="sxs-lookup"><span data-stu-id="63af1-108">The **INapComponentInfo::GetDescription** callback method is used by the NAP System to get the description of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="63af1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63af1-109">Syntax</span></span>


```C++
HRESULT GetDescription(
  [out] MessageId *description
);
```



## <a name="parameters"></a><span data-ttu-id="63af1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="63af1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63af1-111">*Описание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="63af1-111">*description* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63af1-112">Указатель на [**MessageId**](nap-datatypes.md) , содержащий идентификатор ресурса описания.</span><span class="sxs-lookup"><span data-stu-id="63af1-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the description.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63af1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63af1-113">Return value</span></span>

<span data-ttu-id="63af1-114">Возвращает один из этих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="63af1-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="63af1-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="63af1-115">Return code</span></span>                                                                                     | <span data-ttu-id="63af1-116">Описание</span><span class="sxs-lookup"><span data-stu-id="63af1-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="63af1-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="63af1-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="63af1-118">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="63af1-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="63af1-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="63af1-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="63af1-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="63af1-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="63af1-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="63af1-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="63af1-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63af1-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="63af1-123">Требования</span><span class="sxs-lookup"><span data-stu-id="63af1-123">Requirements</span></span>



| <span data-ttu-id="63af1-124">Требование</span><span class="sxs-lookup"><span data-stu-id="63af1-124">Requirement</span></span> | <span data-ttu-id="63af1-125">Значение</span><span class="sxs-lookup"><span data-stu-id="63af1-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="63af1-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63af1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="63af1-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63af1-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="63af1-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63af1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="63af1-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63af1-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="63af1-130">Header</span><span class="sxs-lookup"><span data-stu-id="63af1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="63af1-131"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="63af1-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="63af1-132">IDL</span><span class="sxs-lookup"><span data-stu-id="63af1-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63af1-133"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="63af1-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63af1-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63af1-134">See also</span></span>

<dl> <span data-ttu-id="63af1-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="63af1-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="63af1-136">**инапкомпонентинфо**</span><span class="sxs-lookup"><span data-stu-id="63af1-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





