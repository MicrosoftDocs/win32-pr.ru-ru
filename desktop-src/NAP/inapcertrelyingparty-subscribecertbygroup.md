---
title: Метод Инапцертрелингпарти Субскрибецертбиграуп (Напцертрелингпарти. h)
description: Подписывается на сервер сертификатов работоспособности (HCS).
ms.assetid: 6fce113d-e183-45d7-8fb5-e04b6f4afcca
keywords:
- Метод Субскрибецертбиграуп NAP
- Метод Субскрибецертбиграуп NAP, интерфейс Инапцертрелингпарти
- Инапцертрелингпарти интерфейса NAP, метод Субскрибецертбиграуп
topic_type:
- apiref
api_name:
- INapCertRelyingParty.SubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053c3c2dbf00e706003988bd5769cb2aa9201c41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650380"
---
# <a name="inapcertrelyingpartysubscribecertbygroup-method"></a><span data-ttu-id="4f337-106">Метод Инапцертрелингпарти:: Субскрибецертбиграуп</span><span class="sxs-lookup"><span data-stu-id="4f337-106">INapCertRelyingParty::SubscribeCertByGroup method</span></span>

> [!Note]  
> <span data-ttu-id="4f337-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="4f337-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4f337-108">Метод **субскрибецертбиграуп** подписывается на сервер сертификатов работоспособности (HCS).</span><span class="sxs-lookup"><span data-stu-id="4f337-108">The **SubscribeCertByGroup** method subscribes to a health certificate server (HCS).</span></span> <span data-ttu-id="4f337-109">Прежде чем подписаться на подписку, HCS уже должен быть зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="4f337-109">The HCS must already be registered before subscribing.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f337-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f337-110">Syntax</span></span>


```C++
HRESULT SubscribeCertByGroup(
  [in]        EnforcementEntityId  id,
  [in]  const BSTR                subscriberName,
  [in]  const  VARIANT            *reserved,
  [out]       BOOL                *certExists
);
```



## <a name="parameters"></a><span data-ttu-id="4f337-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f337-111">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="4f337-112">*идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="4f337-112">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f337-113">Объект [**енфорцементентитид**](nap-datatypes.md) , содержащий идентификатор клиента принудительного применения, который подписывается на подписку.</span><span class="sxs-lookup"><span data-stu-id="4f337-113">An [**EnforcementEntityId**](nap-datatypes.md) that contains the ID of the enforcement client that is subscribing.</span></span>

</dd> <dt>

<span data-ttu-id="4f337-114">*subscriberName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4f337-114">*subscriberName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f337-115">Имя подписчика.</span><span class="sxs-lookup"><span data-stu-id="4f337-115">The name of the subscriber.</span></span>

> [!Note]  
> <span data-ttu-id="4f337-116">В настоящее время этот параметр используется только в целях ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="4f337-116">This is currently only used for logging purposes.</span></span>

 

</dd> <dt>

<span data-ttu-id="4f337-117">*зарезервировано* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4f337-117">*reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f337-118">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4f337-118">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4f337-119">*цертексистс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4f337-119">*certExists* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f337-120">Указывает, что сертификат работоспособности из этого HCS уже поддерживается Напажент и имеется в хранилище компьютера.</span><span class="sxs-lookup"><span data-stu-id="4f337-120">Indicates whether a health certificate from this HCS is already being maintained by the NapAgent and is present in the machine store.</span></span> <span data-ttu-id="4f337-121">Если **значение — true**, сертификат работоспособности уже сохраняется и находится в наличии.</span><span class="sxs-lookup"><span data-stu-id="4f337-121">If **TRUE**, a health certificate is already being maintained and is present.</span></span> <span data-ttu-id="4f337-122">Если задано **значение false**, сертификат работоспособности в настоящее время не поддерживается и отсутствует.</span><span class="sxs-lookup"><span data-stu-id="4f337-122">If **FALSE**, a health certificate is not currently being maintained and present.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f337-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f337-123">Return value</span></span>

<span data-ttu-id="4f337-124">Возвращает один из следующих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="4f337-124">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="4f337-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4f337-125">Return code</span></span>                                                                                     | <span data-ttu-id="4f337-126">Описание</span><span class="sxs-lookup"><span data-stu-id="4f337-126">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="4f337-127"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4f337-127"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="4f337-128">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="4f337-128">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="4f337-129"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="4f337-129"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="4f337-130">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="4f337-130">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="4f337-131"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4f337-131"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="4f337-132">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4f337-132">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4f337-133">Требования</span><span class="sxs-lookup"><span data-stu-id="4f337-133">Requirements</span></span>



| <span data-ttu-id="4f337-134">Требование</span><span class="sxs-lookup"><span data-stu-id="4f337-134">Requirement</span></span> | <span data-ttu-id="4f337-135">Значение</span><span class="sxs-lookup"><span data-stu-id="4f337-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f337-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f337-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4f337-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4f337-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4f337-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f337-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4f337-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4f337-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4f337-140">Header</span><span class="sxs-lookup"><span data-stu-id="4f337-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f337-141"><dt>Напцертрелингпарти. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f337-141"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f337-142">IDL</span><span class="sxs-lookup"><span data-stu-id="4f337-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4f337-143"><dt>Напцертрелингпарти. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4f337-143"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f337-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f337-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f337-145">**инапцертрелингпарти**</span><span class="sxs-lookup"><span data-stu-id="4f337-145">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





