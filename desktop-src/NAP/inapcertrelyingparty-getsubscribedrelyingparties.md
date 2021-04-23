---
title: Метод Инапцертрелингпарти Жетсубскрибедрелингпартиес (Напцертрелингпарти. h)
description: Возвращает список проверяющих сторон, на которые оформлена подписка.
ms.assetid: 7eef28fd-71cd-4765-89a5-2c9ce29fdc00
keywords:
- Метод Жетсубскрибедрелингпартиес NAP
- Метод Жетсубскрибедрелингпартиес NAP, интерфейс Инапцертрелингпарти
- Инапцертрелингпарти интерфейса NAP, метод Жетсубскрибедрелингпартиес
topic_type:
- apiref
api_name:
- INapCertRelyingParty.GetSubscribedRelyingParties
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a84871838324c431278d15bb9e78471f48aa1f34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489381"
---
# <a name="inapcertrelyingpartygetsubscribedrelyingparties-method"></a><span data-ttu-id="2717e-106">Метод Инапцертрелингпарти:: Жетсубскрибедрелингпартиес</span><span class="sxs-lookup"><span data-stu-id="2717e-106">INapCertRelyingParty::GetSubscribedRelyingParties method</span></span>

> [!Note]  
> <span data-ttu-id="2717e-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="2717e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2717e-108">Метод **жетсубскрибедрелингпартиес** возвращает список проверяющих сторон, на которые оформлена подписка.</span><span class="sxs-lookup"><span data-stu-id="2717e-108">The **GetSubscribedRelyingParties** method gets a list of relying parties that have subscribed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2717e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2717e-109">Syntax</span></span>


```C++
HRESULT GetSubscribedRelyingParties(
  [out] EnforcementEntityCount *count,
  [out]  EnforcementEntityId   **relyingParties
);
```



## <a name="parameters"></a><span data-ttu-id="2717e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2717e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2717e-111">*количество* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2717e-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2717e-112">Указатель на [**енфорцементентитикаунт**](nap-datatypes.md) , содержащий количество подписанных проверяющих сторон.</span><span class="sxs-lookup"><span data-stu-id="2717e-112">A pointer to a [**EnforcementEntityCount**](nap-datatypes.md) that contains the number of subscribed relying parties.</span></span>

</dd> <dt>

<span data-ttu-id="2717e-113">*релингпартиес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2717e-113">*relyingParties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2717e-114">Указатель на указатель на [**енфорцементентитид**](nap-datatypes.md) , содержащий список проверяющих сторон с подпиской.</span><span class="sxs-lookup"><span data-stu-id="2717e-114">A pointer to a pointer to an [**EnforcementEntityId**](nap-datatypes.md) that contains the list of subscribed relying parties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2717e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2717e-115">Return value</span></span>

<span data-ttu-id="2717e-116">Возвращает один из следующих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="2717e-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="2717e-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2717e-117">Return code</span></span>                                                                                     | <span data-ttu-id="2717e-118">Описание</span><span class="sxs-lookup"><span data-stu-id="2717e-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="2717e-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2717e-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="2717e-120">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="2717e-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="2717e-121"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="2717e-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="2717e-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="2717e-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="2717e-123"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2717e-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="2717e-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2717e-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2717e-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2717e-125">Remarks</span></span>

<span data-ttu-id="2717e-126">Вызывающий объект должен освободить параметр *релингпартиес* с помощью **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="2717e-126">The caller must free the *relyingParties* parameter using **CoTaskMemFree**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2717e-127">Требования</span><span class="sxs-lookup"><span data-stu-id="2717e-127">Requirements</span></span>



| <span data-ttu-id="2717e-128">Требование</span><span class="sxs-lookup"><span data-stu-id="2717e-128">Requirement</span></span> | <span data-ttu-id="2717e-129">Значение</span><span class="sxs-lookup"><span data-stu-id="2717e-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2717e-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2717e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2717e-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2717e-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2717e-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2717e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2717e-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2717e-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2717e-134">Header</span><span class="sxs-lookup"><span data-stu-id="2717e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2717e-135"><dt>Напцертрелингпарти. h</dt></span><span class="sxs-lookup"><span data-stu-id="2717e-135"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="2717e-136">IDL</span><span class="sxs-lookup"><span data-stu-id="2717e-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2717e-137"><dt>Напцертрелингпарти. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2717e-137"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2717e-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2717e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2717e-139">**инапцертрелингпарти**</span><span class="sxs-lookup"><span data-stu-id="2717e-139">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





