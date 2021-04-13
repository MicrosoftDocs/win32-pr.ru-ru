---
title: Метод Инапкомпонентинфо-Version (Напкоммон. h)
description: Используется системой защиты доступа к сети для получения версии клиента работоспособности.
ms.assetid: aabd13d9-d2ad-4554-a9f6-7845e6775ccd
keywords:
- Метод method NAP
- Метод method NAP, интерфейс Инапкомпонентинфо
- Инапкомпонентинфо интерфейса NAP, метод метода WebMethod
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVersion
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa1d62c22acf778430bfc2f9dc0e969887c7b306
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535534"
---
# <a name="inapcomponentinfogetversion-method"></a><span data-ttu-id="15470-106">Метод Инапкомпонентинфо:: метода Version</span><span class="sxs-lookup"><span data-stu-id="15470-106">INapComponentInfo::GetVersion method</span></span>

> [!Note]  
> <span data-ttu-id="15470-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="15470-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="15470-108">Метод обратного вызова **инапкомпонентинфо::-Version** используется системой защиты доступа к сети для получения версии клиента работоспособности.</span><span class="sxs-lookup"><span data-stu-id="15470-108">The **INapComponentInfo::GetVersion** callback method is used by the NAP System to get the version of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="15470-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15470-109">Syntax</span></span>


```C++
HRESULT GetVersion(
  [out] MessageId *version
);
```



## <a name="parameters"></a><span data-ttu-id="15470-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="15470-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15470-111">*версия* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="15470-111">*version* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15470-112">Указатель на [**MessageId**](nap-datatypes.md) , содержащий идентификатор ресурса версии.</span><span class="sxs-lookup"><span data-stu-id="15470-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15470-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15470-113">Return value</span></span>

<span data-ttu-id="15470-114">Возвращает один из этих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="15470-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="15470-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="15470-115">Return code</span></span>                                                                                     | <span data-ttu-id="15470-116">Описание</span><span class="sxs-lookup"><span data-stu-id="15470-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="15470-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="15470-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="15470-118">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="15470-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="15470-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="15470-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="15470-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="15470-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="15470-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="15470-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="15470-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="15470-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="15470-123">Требования</span><span class="sxs-lookup"><span data-stu-id="15470-123">Requirements</span></span>



| <span data-ttu-id="15470-124">Требование</span><span class="sxs-lookup"><span data-stu-id="15470-124">Requirement</span></span> | <span data-ttu-id="15470-125">Значение</span><span class="sxs-lookup"><span data-stu-id="15470-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="15470-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15470-126">Minimum supported client</span></span><br/> | <span data-ttu-id="15470-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="15470-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="15470-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15470-128">Minimum supported server</span></span><br/> | <span data-ttu-id="15470-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="15470-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="15470-130">Header</span><span class="sxs-lookup"><span data-stu-id="15470-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="15470-131"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="15470-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="15470-132">IDL</span><span class="sxs-lookup"><span data-stu-id="15470-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="15470-133"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="15470-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15470-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15470-134">See also</span></span>

<dl> <span data-ttu-id="15470-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="15470-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="15470-136">**инапкомпонентинфо**</span><span class="sxs-lookup"><span data-stu-id="15470-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





