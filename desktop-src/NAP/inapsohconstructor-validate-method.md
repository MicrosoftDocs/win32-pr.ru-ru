---
title: Метод Validate Инапсохконструктор (Наппротокол. h)
description: Проверяет допустимость пакета SoH.
ms.assetid: 66338213-43c0-461a-a794-5f18d56bd505
keywords:
- Проверка метода NAP
- Проверка метода NAP, интерфейс Инапсохконструктор
- Инапсохконструктор интерфейса NAP, метод Validate
topic_type:
- apiref
api_name:
- INapSoHConstructor.Validate
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7db8a52d7986348e85c724171b6d417996c7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803106"
---
# <a name="inapsohconstructorvalidate-method"></a><span data-ttu-id="fde71-106">Метод Инапсохконструктор:: Validate</span><span class="sxs-lookup"><span data-stu-id="fde71-106">INapSoHConstructor::Validate method</span></span>

> [!Note]  
> <span data-ttu-id="fde71-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="fde71-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fde71-108">Метод **инапсохконструктор:: Validate** проверяет допустимость пакета SoH.</span><span class="sxs-lookup"><span data-stu-id="fde71-108">The **INapSoHConstructor::Validate** method checks the validity of the SoH packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="fde71-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fde71-109">Syntax</span></span>


```C++
HRESULT Validate(
  [in] const SoH  *soh,
  [in]       BOOL isRequest
);
```



## <a name="parameters"></a><span data-ttu-id="fde71-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="fde71-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fde71-111">*состояние работоспособности* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fde71-111">*soh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde71-112">Указатель на сконструированный пакет [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="fde71-112">A pointer to the constructed [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="fde71-113">*запрос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fde71-113">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde71-114">**Логическое** **значение** , равное true, если пакет является [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) , и **false** , если это **сохреспонсе**.</span><span class="sxs-lookup"><span data-stu-id="fde71-114">A **BOOL** that is **TRUE** if the packet is an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is an **SoHResponse**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fde71-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fde71-115">Return value</span></span>

<span data-ttu-id="fde71-116">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="fde71-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="fde71-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fde71-117">Return code</span></span>                                                                                            | <span data-ttu-id="fde71-118">Описание</span><span class="sxs-lookup"><span data-stu-id="fde71-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="fde71-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fde71-119"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="fde71-120">Пакет SoH является допустимым.</span><span class="sxs-lookup"><span data-stu-id="fde71-120">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="fde71-121"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="fde71-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="fde71-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="fde71-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="fde71-123"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fde71-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="fde71-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fde71-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="fde71-125"><dt>**\_ \_ Недопустимый \_ пакет NAP E**</dt></span><span class="sxs-lookup"><span data-stu-id="fde71-125"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="fde71-126">Недопустимый пакет SoH.</span><span class="sxs-lookup"><span data-stu-id="fde71-126">The SoH packet is invalid.</span></span><br/>                              |



 

## <a name="requirements"></a><span data-ttu-id="fde71-127">Требования</span><span class="sxs-lookup"><span data-stu-id="fde71-127">Requirements</span></span>



| <span data-ttu-id="fde71-128">Требование</span><span class="sxs-lookup"><span data-stu-id="fde71-128">Requirement</span></span> | <span data-ttu-id="fde71-129">Значение</span><span class="sxs-lookup"><span data-stu-id="fde71-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="fde71-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fde71-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fde71-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fde71-131">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fde71-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fde71-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fde71-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fde71-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fde71-134">Header</span><span class="sxs-lookup"><span data-stu-id="fde71-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fde71-135"><dt>Наппротокол. h</dt></span><span class="sxs-lookup"><span data-stu-id="fde71-135"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="fde71-136">IDL</span><span class="sxs-lookup"><span data-stu-id="fde71-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fde71-137"><dt>Наппротокол. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fde71-137"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="fde71-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fde71-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fde71-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fde71-139"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="fde71-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fde71-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde71-141">**инапсохконструктор**</span><span class="sxs-lookup"><span data-stu-id="fde71-141">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





