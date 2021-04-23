---
title: Метод Инапсистемхеалсажентрекуест Жетсохреспонсе (Напсистемхеалсажент. h)
description: Используется агентом работоспособности для извлечения своего большого двоичного объекта Сохреспонсе, когда Напажент вызывает Инапсистемхеалсаженткаллбакк Процесссохреспонсе.
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- Метод Жетсохреспонсе NAP
- Метод Жетсохреспонсе NAP, интерфейс Инапсистемхеалсажентрекуест
- Инапсистемхеалсажентрекуест интерфейса NAP, метод Жетсохреспонсе
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHResponse
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d593ff897e69b86b554365561e43308adead5250
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135527"
---
# <a name="inapsystemhealthagentrequestgetsohresponse-method"></a><span data-ttu-id="859b1-106">Метод Инапсистемхеалсажентрекуест:: Жетсохреспонсе</span><span class="sxs-lookup"><span data-stu-id="859b1-106">INapSystemHealthAgentRequest::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="859b1-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="859b1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="859b1-108">Метод **инапсистемхеалсажентрекуест:: жетсохреспонсе** используется агентом работоспособности для получения своего большого двоичного объекта сохреспонсе, когда Напажент вызывает [**Инапсистемхеалсаженткаллбакк::P rocesssohresponse**](inapsystemhealthagentcallback-processsohresponse-method.md).</span><span class="sxs-lookup"><span data-stu-id="859b1-108">The **INapSystemHealthAgentRequest::GetSoHResponse** method is used by the health agent to retrieve their SoHResponse blob when the NapAgent calls [**INapSystemHealthAgentCallback::ProcessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="859b1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="859b1-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse,
  [out] UINT8       *flags
);
```



## <a name="parameters"></a><span data-ttu-id="859b1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="859b1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="859b1-111">*сохреспонсе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="859b1-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="859b1-112">Указатель на указатель на пакет [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="859b1-112">A pointer to a pointer to a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="859b1-113">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="859b1-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="859b1-114">Указатель на флаг, позволяющий выполнять исправление SHA, если установлен бит [**шафиксуп**](nap-type-constants.md) , в противном случае — исправление отключено.</span><span class="sxs-lookup"><span data-stu-id="859b1-114">A pointer to a flag that enables fix-up by the SHA if the [**shaFixup**](nap-type-constants.md) bit is set, otherwise fix-up is disabled.</span></span>



| <span data-ttu-id="859b1-115">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="859b1-115">Possible Values</span></span>                                                                                                                                                          | <span data-ttu-id="859b1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="859b1-116">Meaning</span></span>                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <span data-ttu-id="859b1-117"><dt>**шафиксуп**</dt></span><span class="sxs-lookup"><span data-stu-id="859b1-117"><dt>**shaFixup**</dt></span></span> </dl> | <span data-ttu-id="859b1-118">Ожидается, что SHA будет выполнять исправление на основе ответа.</span><span class="sxs-lookup"><span data-stu-id="859b1-118">The SHA is expected to perform the fixup based on the response.</span></span> <span data-ttu-id="859b1-119">Если этот флаг не установлен, SHA не должен выполнять исправление, даже если [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh) указывает на неработоспособность.</span><span class="sxs-lookup"><span data-stu-id="859b1-119">If this flag is not set, the SHA should not perform a fix-up even though the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indicates that it is unhealthy.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="859b1-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="859b1-120">Return value</span></span>

<span data-ttu-id="859b1-121">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="859b1-121">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="859b1-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="859b1-122">Return code</span></span>                                                                                     | <span data-ttu-id="859b1-123">Описание</span><span class="sxs-lookup"><span data-stu-id="859b1-123">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="859b1-124"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="859b1-124"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="859b1-125">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="859b1-125">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="859b1-126"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="859b1-126"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="859b1-127">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="859b1-127">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="859b1-128"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="859b1-128"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="859b1-129">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="859b1-129">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="859b1-130">Требования</span><span class="sxs-lookup"><span data-stu-id="859b1-130">Requirements</span></span>



| <span data-ttu-id="859b1-131">Требование</span><span class="sxs-lookup"><span data-stu-id="859b1-131">Requirement</span></span> | <span data-ttu-id="859b1-132">Значение</span><span class="sxs-lookup"><span data-stu-id="859b1-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="859b1-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="859b1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="859b1-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="859b1-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="859b1-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="859b1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="859b1-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="859b1-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="859b1-137">Header</span><span class="sxs-lookup"><span data-stu-id="859b1-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="859b1-138"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="859b1-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="859b1-139">IDL</span><span class="sxs-lookup"><span data-stu-id="859b1-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="859b1-140"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="859b1-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="859b1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="859b1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="859b1-142"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="859b1-142"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="859b1-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="859b1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="859b1-144">**инапсистемхеалсажентрекуест**</span><span class="sxs-lookup"><span data-stu-id="859b1-144">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





