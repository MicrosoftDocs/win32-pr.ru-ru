---
title: Метод Инапкомпонентинфо Конвертерроркодетомессажеид (Напкоммон. h)
description: Используется системой защиты доступа к сети для запроса клиента работоспособности о преобразовании кода ошибки HRESULT в идентификатор сообщения.
ms.assetid: 760dd039-5b9c-4227-9939-ad6ea23f5b81
keywords:
- Метод Конвертерроркодетомессажеид NAP
- Метод Конвертерроркодетомессажеид NAP, интерфейс Инапкомпонентинфо
- Инапкомпонентинфо интерфейса NAP, метод Конвертерроркодетомессажеид
topic_type:
- apiref
api_name:
- INapComponentInfo.ConvertErrorCodeToMessageId
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed8eee06ed6bd553ffcce68e76e375dd706238
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492810"
---
# <a name="inapcomponentinfoconverterrorcodetomessageid-method"></a><span data-ttu-id="5f383-106">Метод Инапкомпонентинфо:: Конвертерроркодетомессажеид</span><span class="sxs-lookup"><span data-stu-id="5f383-106">INapComponentInfo::ConvertErrorCodeToMessageId method</span></span>

> [!Note]  
> <span data-ttu-id="5f383-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="5f383-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5f383-108">Метод обратного вызова **инапкомпонентинфо:: конвертерроркодетомессажеид** используется системой защиты доступа к сети для запроса клиента работоспособности о преобразовании кода ошибки HRESULT в идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="5f383-108">The **INapComponentInfo::ConvertErrorCodeToMessageId** callback method is used by the NAP System to request the health client convert an HRESULT error code into a message ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f383-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f383-109">Syntax</span></span>


```C++
HRESULT ConvertErrorCodeToMessageId(
  [in]  HRESULT   errorCode,
  [out] MessageId *msgId
);
```



## <a name="parameters"></a><span data-ttu-id="5f383-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f383-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f383-111">*код ошибки* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f383-111">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f383-112">[**Код ошибки**](nap-error-constants.md) из системы защиты доступа к сети, который необходимо преобразовать в **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="5f383-112">The [**error code**](nap-error-constants.md) from the NAP System that is to be converted into a **MessageId**.</span></span>

</dd> <dt>

<span data-ttu-id="5f383-113">*msgid* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5f383-113">*msgId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f383-114">Указатель на [**MessageId**](nap-datatypes.md) , который содержит идентификатор ресурса соответствующей локализованной строки.</span><span class="sxs-lookup"><span data-stu-id="5f383-114">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the corresponding localized string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f383-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f383-115">Return value</span></span>

<span data-ttu-id="5f383-116">Возвращает один из этих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="5f383-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="5f383-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5f383-117">Return code</span></span>                                                                                     | <span data-ttu-id="5f383-118">Описание</span><span class="sxs-lookup"><span data-stu-id="5f383-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5f383-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5f383-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="5f383-120">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="5f383-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="5f383-121"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5f383-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="5f383-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="5f383-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="5f383-123"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5f383-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="5f383-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5f383-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5f383-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5f383-125">Remarks</span></span>

<span data-ttu-id="5f383-126">Возвращенный идентификатор **MessageId** используется системой защиты доступа к сети для получения локализованной строки.</span><span class="sxs-lookup"><span data-stu-id="5f383-126">The returned **MessageId** is used by the NAP System to retrieve a localized string.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f383-127">Требования</span><span class="sxs-lookup"><span data-stu-id="5f383-127">Requirements</span></span>



| <span data-ttu-id="5f383-128">Требование</span><span class="sxs-lookup"><span data-stu-id="5f383-128">Requirement</span></span> | <span data-ttu-id="5f383-129">Значение</span><span class="sxs-lookup"><span data-stu-id="5f383-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f383-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5f383-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5f383-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f383-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5f383-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5f383-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5f383-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5f383-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5f383-134">Header</span><span class="sxs-lookup"><span data-stu-id="5f383-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f383-135"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f383-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f383-136">IDL</span><span class="sxs-lookup"><span data-stu-id="5f383-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5f383-137"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5f383-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f383-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f383-138">See also</span></span>

<dl> <span data-ttu-id="5f383-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="5f383-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="5f383-140">**инапкомпонентинфо**</span><span class="sxs-lookup"><span data-stu-id="5f383-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





