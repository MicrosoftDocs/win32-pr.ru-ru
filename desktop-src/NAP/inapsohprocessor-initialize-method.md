---
title: Метод Initialize Инапсохпроцессор (Наппротокол. h)
description: Инициализирует пакет протокола и систему процессора работоспособности. Этот метод должен вызываться только один раз.
ms.assetid: 4fccc847-3c4d-4fc5-935d-28fb2964a9be
keywords:
- Инициализация метода NAP
- Инициализация метода NAP, интерфейс Инапсохпроцессор
- Инапсохпроцессор интерфейса NAP, метод Initialize
topic_type:
- apiref
api_name:
- INapSoHProcessor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ff3a32bb213caf19964ccea8175a43e5016f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988655"
---
# <a name="inapsohprocessorinitialize-method"></a><span data-ttu-id="1cba9-107">Метод Инапсохпроцессор:: Initialize</span><span class="sxs-lookup"><span data-stu-id="1cba9-107">INapSoHProcessor::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="1cba9-108">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="1cba9-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1cba9-109">Метод **инапсохпроцессор:: Initialize** инициализирует пакет протокола и систему процессора работоспособности.</span><span class="sxs-lookup"><span data-stu-id="1cba9-109">The **INapSoHProcessor::Initialize** method initializes the protocol packet and SoH processor system.</span></span> <span data-ttu-id="1cba9-110">Этот метод должен вызываться только один раз.</span><span class="sxs-lookup"><span data-stu-id="1cba9-110">This method must be called exactly once.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cba9-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1cba9-111">Syntax</span></span>


```C++
HRESULT Initialize(
  [in]  const SoH                  *soh,
  [in]        BOOL                 isRequest,
  [out]       SystemHealthEntityId *id
);
```



## <a name="parameters"></a><span data-ttu-id="1cba9-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="1cba9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cba9-113">*состояние работоспособности* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1cba9-113">*soh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cba9-114">Указатель на пакет [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) для обработки.</span><span class="sxs-lookup"><span data-stu-id="1cba9-114">A pointer to the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="1cba9-115">*запрос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1cba9-115">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cba9-116">**Логическое** **значение** , равное true, если пакет является [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) , и **false** , если это **сохреспонсе**.</span><span class="sxs-lookup"><span data-stu-id="1cba9-116">A **BOOL** that is **TRUE** if the packet is an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is an **SoHResponse**.</span></span>

</dd> <dt>

<span data-ttu-id="1cba9-117">*идентификатор* \[ исходящей\]</span><span class="sxs-lookup"><span data-stu-id="1cba9-117">*id* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cba9-118">Уникальный [системхеалсентитид](nap-datatypes.md) , СОДЕРЖАЩИЙ идентификатор SHA или SHV, который разстроил пакет.</span><span class="sxs-lookup"><span data-stu-id="1cba9-118">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA or SHV that constructed the packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cba9-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1cba9-119">Return value</span></span>

<span data-ttu-id="1cba9-120">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="1cba9-120">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="1cba9-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1cba9-121">Return code</span></span>                                                                                            | <span data-ttu-id="1cba9-122">Описание</span><span class="sxs-lookup"><span data-stu-id="1cba9-122">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1cba9-123"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1cba9-123"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="1cba9-124">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="1cba9-124">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1cba9-125"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="1cba9-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="1cba9-126">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="1cba9-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="1cba9-127"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1cba9-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="1cba9-128">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1cba9-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="1cba9-129"><dt>**\_ \_ Недопустимый \_ пакет NAP E**</dt></span><span class="sxs-lookup"><span data-stu-id="1cba9-129"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="1cba9-130">Недопустимый пакет SoH.</span><span class="sxs-lookup"><span data-stu-id="1cba9-130">The SoH packet is invalid.</span></span><br/>                              |



 

## <a name="requirements"></a><span data-ttu-id="1cba9-131">Требования</span><span class="sxs-lookup"><span data-stu-id="1cba9-131">Requirements</span></span>



| <span data-ttu-id="1cba9-132">Требование</span><span class="sxs-lookup"><span data-stu-id="1cba9-132">Requirement</span></span> | <span data-ttu-id="1cba9-133">Значение</span><span class="sxs-lookup"><span data-stu-id="1cba9-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cba9-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1cba9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1cba9-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1cba9-135">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1cba9-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1cba9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1cba9-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1cba9-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1cba9-138">Header</span><span class="sxs-lookup"><span data-stu-id="1cba9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cba9-139"><dt>Наппротокол. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cba9-139"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="1cba9-140">IDL</span><span class="sxs-lookup"><span data-stu-id="1cba9-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1cba9-141"><dt>Наппротокол. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1cba9-141"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="1cba9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1cba9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cba9-143"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cba9-143"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="1cba9-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1cba9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cba9-145">**инапсохпроцессор**</span><span class="sxs-lookup"><span data-stu-id="1cba9-145">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





