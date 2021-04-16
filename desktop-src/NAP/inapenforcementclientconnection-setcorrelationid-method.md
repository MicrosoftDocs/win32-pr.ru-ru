---
title: Метод Инапенфорцементклиентконнектион Сеткоррелатионид (Напенфорцементклиент. h)
description: Задает идентификатор, используемый для корреляции запросов SoH и ответов о состоянии работоспособности.
ms.assetid: 8f9d5bde-95b1-4566-84ee-31c6ed5e8986
keywords:
- Метод Сеткоррелатионид NAP
- Метод Сеткоррелатионид NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Сеткоррелатионид
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c99576b8302f7fcf949f132cf110a5ac5f675ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533962"
---
# <a name="inapenforcementclientconnectionsetcorrelationid-method"></a><span data-ttu-id="aa4e9-106">Метод Инапенфорцементклиентконнектион:: Сеткоррелатионид</span><span class="sxs-lookup"><span data-stu-id="aa4e9-106">INapEnforcementClientConnection::SetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="aa4e9-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="aa4e9-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="aa4e9-108">Метод **инапенфорцементклиентконнектион:: сеткоррелатионид** задает идентификатор, используемый для корреляции запросов SoH и состояний работоспособности.</span><span class="sxs-lookup"><span data-stu-id="aa4e9-108">The **INapEnforcementClientConnection::SetCorrelationId** method sets the ID used to correlate SoH-requests and SoH-responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa4e9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa4e9-109">Syntax</span></span>


```C++
HRESULT SetCorrelationId(
  [in] CorrelationId correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="aa4e9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa4e9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa4e9-111">*correlationId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aa4e9-111">*correlationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa4e9-112">Уникальная структура [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) , идентифицирующая конкретный обмен SoH.</span><span class="sxs-lookup"><span data-stu-id="aa4e9-112">A unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure that identifies a specific SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa4e9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa4e9-113">Return value</span></span>

<span data-ttu-id="aa4e9-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="aa4e9-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="aa4e9-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="aa4e9-115">Return code</span></span>                                                                                     | <span data-ttu-id="aa4e9-116">Описание</span><span class="sxs-lookup"><span data-stu-id="aa4e9-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa4e9-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="aa4e9-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="aa4e9-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="aa4e9-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="aa4e9-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="aa4e9-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="aa4e9-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="aa4e9-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="aa4e9-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="aa4e9-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="aa4e9-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa4e9-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aa4e9-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa4e9-123">Remarks</span></span>

<span data-ttu-id="aa4e9-124">Корреляционный идентификатор задается Напажент и основывается на идентификаторе Connection-ID.</span><span class="sxs-lookup"><span data-stu-id="aa4e9-124">The correlation-id is set by the NapAgent and based on the connection-id.</span></span>

<span data-ttu-id="aa4e9-125">Этот идентификатор используется для корреляции запросов и ответов, т. е. он однозначно описывает обмен данными о состоянии работоспособности и всегда содержит идентификатор последнего набора состояний работоспособности, установленного для объекта соединения.</span><span class="sxs-lookup"><span data-stu-id="aa4e9-125">This id is used to correlate requests and responses, i.e. it uniquely describes an SoH exchange and always contains the id of the most recent SoH set on the connection object.</span></span>

<span data-ttu-id="aa4e9-126">При получении SoH-Response Напажент сначала проверяет соответствие идентификаторов. Если это не так, то возвращается ошибка, и принудительно удаляется пакет.</span><span class="sxs-lookup"><span data-stu-id="aa4e9-126">When an SoH-Response is received, the NapAgent first ensures the IDs match; if not, an error is returned and the enforcer must drop the packet.</span></span> <span data-ttu-id="aa4e9-127">Дополнительные сведения см. в разделе [**инапенфорцементклиентбиндинг::P роцесссохреспонсе**](inapenforcementclientbinding-processsohresponse-method.md) .</span><span class="sxs-lookup"><span data-stu-id="aa4e9-127">See [**INapEnforcementClientBinding::ProcessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md) for more details.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa4e9-128">Требования</span><span class="sxs-lookup"><span data-stu-id="aa4e9-128">Requirements</span></span>



| <span data-ttu-id="aa4e9-129">Требование</span><span class="sxs-lookup"><span data-stu-id="aa4e9-129">Requirement</span></span> | <span data-ttu-id="aa4e9-130">Значение</span><span class="sxs-lookup"><span data-stu-id="aa4e9-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa4e9-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa4e9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="aa4e9-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa4e9-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="aa4e9-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa4e9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="aa4e9-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa4e9-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="aa4e9-135">Header</span><span class="sxs-lookup"><span data-stu-id="aa4e9-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa4e9-136"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa4e9-136"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="aa4e9-137">IDL</span><span class="sxs-lookup"><span data-stu-id="aa4e9-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aa4e9-138"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aa4e9-138"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="aa4e9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="aa4e9-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa4e9-140"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa4e9-140"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="aa4e9-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa4e9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa4e9-142">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="aa4e9-142">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





