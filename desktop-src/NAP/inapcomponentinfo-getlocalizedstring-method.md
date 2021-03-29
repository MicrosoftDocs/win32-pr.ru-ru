---
title: Метод Инапкомпонентинфо Жетлокализедстринг (Напкоммон. h)
description: Используется системой защиты доступа к сети для получения локализованных строк.
ms.assetid: ad5be180-6329-4c91-b4d1-871a4d83c323
keywords:
- Метод Жетлокализедстринг NAP
- Метод Жетлокализедстринг NAP, интерфейс Инапкомпонентинфо
- Инапкомпонентинфо интерфейса NAP, метод Жетлокализедстринг
topic_type:
- apiref
api_name:
- INapComponentInfo.GetLocalizedString
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781e4e8c93f58039c72a98f40a529243e5722d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989419"
---
# <a name="inapcomponentinfogetlocalizedstring-method"></a><span data-ttu-id="84d8f-106">Метод Инапкомпонентинфо:: Жетлокализедстринг</span><span class="sxs-lookup"><span data-stu-id="84d8f-106">INapComponentInfo::GetLocalizedString method</span></span>

> [!Note]  
> <span data-ttu-id="84d8f-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="84d8f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="84d8f-108">Метод обратного вызова **инапкомпонентинфо:: жетлокализедстринг** используется системой защиты доступа к сети для получения локализованных строк.</span><span class="sxs-lookup"><span data-stu-id="84d8f-108">The **INapComponentInfo::GetLocalizedString** callback method is used by the NAP System to get localized strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="84d8f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84d8f-109">Syntax</span></span>


```C++
HRESULT GetLocalizedString(
  [in]  MessageId     msgId,
  [out] CountedString **string
);
```



## <a name="parameters"></a><span data-ttu-id="84d8f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="84d8f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84d8f-111">*msgid* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84d8f-111">*msgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84d8f-112">[**MessageId**](nap-datatypes.md) , содержащий идентификатор ресурса строки для локализации.</span><span class="sxs-lookup"><span data-stu-id="84d8f-112">A [**MessageId**](nap-datatypes.md) that contains the resource ID of the string to localize.</span></span>

</dd> <dt>

<span data-ttu-id="84d8f-113">*строка* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="84d8f-113">*string* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84d8f-114">Указатель на указатель на [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , содержащий локализованную версию сообщения.</span><span class="sxs-lookup"><span data-stu-id="84d8f-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) that contains the localized version of the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84d8f-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84d8f-115">Return value</span></span>

<span data-ttu-id="84d8f-116">Возвращает один из этих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="84d8f-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="84d8f-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="84d8f-117">Return code</span></span>                                                                                     | <span data-ttu-id="84d8f-118">Описание</span><span class="sxs-lookup"><span data-stu-id="84d8f-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="84d8f-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="84d8f-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="84d8f-120">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="84d8f-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="84d8f-121"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="84d8f-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="84d8f-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="84d8f-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="84d8f-123"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="84d8f-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="84d8f-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84d8f-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="84d8f-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84d8f-125">Remarks</span></span>

<span data-ttu-id="84d8f-126">Строки должны быть локализованы в соответствии с идентификатором языка вызывающего потока.</span><span class="sxs-lookup"><span data-stu-id="84d8f-126">Strings should be localized according to the calling thread's language-id.</span></span>

## <a name="requirements"></a><span data-ttu-id="84d8f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="84d8f-127">Requirements</span></span>



| <span data-ttu-id="84d8f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="84d8f-128">Requirement</span></span> | <span data-ttu-id="84d8f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="84d8f-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="84d8f-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84d8f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="84d8f-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84d8f-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="84d8f-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84d8f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="84d8f-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="84d8f-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="84d8f-134">Header</span><span class="sxs-lookup"><span data-stu-id="84d8f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="84d8f-135"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="84d8f-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="84d8f-136">IDL</span><span class="sxs-lookup"><span data-stu-id="84d8f-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="84d8f-137"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="84d8f-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84d8f-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84d8f-138">See also</span></span>

<dl> <span data-ttu-id="84d8f-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="84d8f-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="84d8f-140">**инапкомпонентинфо**</span><span class="sxs-lookup"><span data-stu-id="84d8f-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





