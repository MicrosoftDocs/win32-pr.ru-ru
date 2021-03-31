---
title: Метод Инапсистемхеалсаженткаллбакк Процесссохреспонсе (Напсистемхеалсажент. h)
description: Вызывается, когда Напажент получает Сохреспонсе, предназначенный для этого агента работоспособности.
ms.assetid: 860b1012-7df8-456f-8f21-eb0e1abd2b3b
keywords:
- Метод Процесссохреспонсе NAP
- Метод Процесссохреспонсе NAP, интерфейс Инапсистемхеалсаженткаллбакк
- Инапсистемхеалсаженткаллбакк интерфейса NAP, метод Процесссохреспонсе
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.ProcessSoHResponse
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c62c585c36680dde2c54c95c255a85f69fc5ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988795"
---
# <a name="inapsystemhealthagentcallbackprocesssohresponse-method"></a><span data-ttu-id="62d4e-106">Инапсистемхеалсаженткаллбакк: метод:P Роцесссохреспонсе</span><span class="sxs-lookup"><span data-stu-id="62d4e-106">INapSystemHealthAgentCallback::ProcessSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="62d4e-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="62d4e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="62d4e-108">Метод **инапсистемхеалсаженткаллбакк::P роцесссохреспонсе** вызывается, когда Напажент получает [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh) , предназначенный для этого агента работоспособности.</span><span class="sxs-lookup"><span data-stu-id="62d4e-108">The **INapSystemHealthAgentCallback::ProcessSoHResponse** method is called when the NapAgent receives an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destined for this health agent.</span></span>

## <a name="syntax"></a><span data-ttu-id="62d4e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62d4e-109">Syntax</span></span>


```C++
HRESULT ProcessSoHResponse(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a><span data-ttu-id="62d4e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="62d4e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62d4e-111">*запрос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="62d4e-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62d4e-112">Указатель COM на объект [**инапсистемхеалсажентрекуест**](inapsystemhealthagentrequest.md) , который идентифицирует объект запроса.</span><span class="sxs-lookup"><span data-stu-id="62d4e-112">A COM pointer to a [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object that identifies the request object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62d4e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62d4e-113">Return value</span></span>

<span data-ttu-id="62d4e-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="62d4e-114">This method can return one of these values.</span></span>



| <span data-ttu-id="62d4e-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="62d4e-115">Return code</span></span>                                                                                            | <span data-ttu-id="62d4e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="62d4e-116">Description</span></span>                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="62d4e-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="62d4e-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="62d4e-118">Указывает на успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="62d4e-118">Indicates success.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="62d4e-119"><dt>**\_ \_ Недопустимый \_ пакет NAP E**</dt></span><span class="sxs-lookup"><span data-stu-id="62d4e-119"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="62d4e-120">Возвращается этой реализацией, если ответ имеет неправильный формат.</span><span class="sxs-lookup"><span data-stu-id="62d4e-120">Returned by this implementation if the response is not in the correct format.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62d4e-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62d4e-121">Remarks</span></span>

<span data-ttu-id="62d4e-122">Этот метод обратного вызова объявляется системой защиты доступа к сети и реализуется модулем записи SHA.</span><span class="sxs-lookup"><span data-stu-id="62d4e-122">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="62d4e-123">Когда Напажент получает [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh) , предназначенный для этого агента работоспособности, он вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="62d4e-123">When the NapAgent receives an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destined for this health agent, it invokes this method.</span></span> <span data-ttu-id="62d4e-124">Агент работоспособности должен запросить Сохреспонсе из объекта Request.</span><span class="sxs-lookup"><span data-stu-id="62d4e-124">The health agent must query the SoHResponse from the request object.</span></span> <span data-ttu-id="62d4e-125">После завершения этого вызова он не должен содержать ссылки на объект запроса.</span><span class="sxs-lookup"><span data-stu-id="62d4e-125">It must not hold references to the request object once this call has completed.</span></span>

<span data-ttu-id="62d4e-126">Метод **инапсистемхеалсаженткаллбакк::P роцесссохреспонсе** не должен блокироваться.</span><span class="sxs-lookup"><span data-stu-id="62d4e-126">The **INapSystemHealthAgentCallback::ProcessSoHResponse** method must not block.</span></span> <span data-ttu-id="62d4e-127">Если требуется обработка исправления, любая реализация **процесссохреспонсе** должна запустить новый поток для выполнения процесса исправления.</span><span class="sxs-lookup"><span data-stu-id="62d4e-127">If any fix-up processing is required, any implementation of **ProcessSoHResponse** must start a new thread to perform fix-up processing.</span></span> <span data-ttu-id="62d4e-128">Напажент должен вызвать [**инапсистемхеалсаженткаллбакк:: жетфиксупинфо**](inapsystemhealthagentcallback-getfixupinfo-method.md) , чтобы определить состояние исправления SHA.</span><span class="sxs-lookup"><span data-stu-id="62d4e-128">The NapAgent must call [**INapSystemHealthAgentCallBack::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) to determine the fix-up status of the SHA.</span></span>

<span data-ttu-id="62d4e-129">Этот метод должен возвращать **\_ \_ Недопустимый \_ пакет NAP E** , если ответ имеет неправильный формат.</span><span class="sxs-lookup"><span data-stu-id="62d4e-129">This method must return **NAP\_E\_INVALID\_PACKET** if the response is not in the correct format.</span></span>

## <a name="requirements"></a><span data-ttu-id="62d4e-130">Требования</span><span class="sxs-lookup"><span data-stu-id="62d4e-130">Requirements</span></span>



| <span data-ttu-id="62d4e-131">Требование</span><span class="sxs-lookup"><span data-stu-id="62d4e-131">Requirement</span></span> | <span data-ttu-id="62d4e-132">Значение</span><span class="sxs-lookup"><span data-stu-id="62d4e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62d4e-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62d4e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="62d4e-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62d4e-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="62d4e-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62d4e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="62d4e-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="62d4e-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="62d4e-137">Header</span><span class="sxs-lookup"><span data-stu-id="62d4e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="62d4e-138"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="62d4e-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="62d4e-139">IDL</span><span class="sxs-lookup"><span data-stu-id="62d4e-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="62d4e-140"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="62d4e-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62d4e-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62d4e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62d4e-142">**инапсистемхеалсаженткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="62d4e-142">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





