---
title: Метод Инапцертрелингпарти Унсубскрибецертбиграуп (Напцертрелингпарти. h)
description: Отменяет подписывание на сервере сертификатов работоспособности (HCS).
ms.assetid: 2b26b110-8aba-487e-bd49-c6afc6af11f8
keywords:
- Метод Унсубскрибецертбиграуп NAP
- Метод Унсубскрибецертбиграуп NAP, интерфейс Инапцертрелингпарти
- Инапцертрелингпарти интерфейса NAP, метод Унсубскрибецертбиграуп
topic_type:
- apiref
api_name:
- INapCertRelyingParty.UnSubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01bbad5ef48b5f709f93f018c56b5798907d08c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988797"
---
# <a name="inapcertrelyingpartyunsubscribecertbygroup-method"></a><span data-ttu-id="e014e-106">Метод Инапцертрелингпарти:: Унсубскрибецертбиграуп</span><span class="sxs-lookup"><span data-stu-id="e014e-106">INapCertRelyingParty::UnSubscribeCertByGroup method</span></span>

> [!Note]  
> <span data-ttu-id="e014e-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="e014e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e014e-108">Метод **унсубскрибецертбиграуп** отменяет подписывание на сервере сертификатов работоспособности (HCS).</span><span class="sxs-lookup"><span data-stu-id="e014e-108">The **UnSubscribeCertByGroup** method unsubscribes from a health certificate server (HCS).</span></span>

## <a name="syntax"></a><span data-ttu-id="e014e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e014e-109">Syntax</span></span>


```C++
HRESULT UnSubscribeCertByGroup(
  [in]        EnforcementEntityId   id,
  [in] const  VARIANT             * reserved
);
```



## <a name="parameters"></a><span data-ttu-id="e014e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e014e-110">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="e014e-111">*идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="e014e-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e014e-112">Объект [**енфорцементентитид**](nap-datatypes.md) , содержащий идентификатор клиента принудительного применения, который отменяет подписку.</span><span class="sxs-lookup"><span data-stu-id="e014e-112">An [**EnforcementEntityId**](nap-datatypes.md) that contains the ID of the enforcement client that is unsubscribing.</span></span>

</dd> <dt>

 <span data-ttu-id="e014e-113">*зарезервировано* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e014e-113">*reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e014e-114">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e014e-114">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e014e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e014e-115">Return value</span></span>

<span data-ttu-id="e014e-116">Возвращает один из следующих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="e014e-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="e014e-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e014e-117">Return code</span></span>                                                                                     | <span data-ttu-id="e014e-118">Описание</span><span class="sxs-lookup"><span data-stu-id="e014e-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e014e-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e014e-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="e014e-120">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="e014e-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="e014e-121"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e014e-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="e014e-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="e014e-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="e014e-123"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e014e-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="e014e-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e014e-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e014e-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e014e-125">Remarks</span></span>

<span data-ttu-id="e014e-126">Если нет других подписчиков на HCS, Напажент удалит соответствующие сертификаты работоспособности из хранилища локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="e014e-126">If there are no other subscribers to the HCS, the NapAgent will delete the corresponding health certificates from the local machine store.</span></span>

<span data-ttu-id="e014e-127">Перед вызовом этого метода вызовите [**субскрибецертбиграуп**](inapcertrelyingparty-subscribecertbygroup.md).</span><span class="sxs-lookup"><span data-stu-id="e014e-127">Before calling this method, call [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e014e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="e014e-128">Requirements</span></span>



| <span data-ttu-id="e014e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="e014e-129">Requirement</span></span> | <span data-ttu-id="e014e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="e014e-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e014e-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e014e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e014e-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e014e-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e014e-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e014e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e014e-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e014e-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e014e-135">Header</span><span class="sxs-lookup"><span data-stu-id="e014e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e014e-136"><dt>Напцертрелингпарти. h</dt></span><span class="sxs-lookup"><span data-stu-id="e014e-136"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="e014e-137">IDL</span><span class="sxs-lookup"><span data-stu-id="e014e-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e014e-138"><dt>Напцертрелингпарти. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e014e-138"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e014e-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e014e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e014e-140">**инапцертрелингпарти**</span><span class="sxs-lookup"><span data-stu-id="e014e-140">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





