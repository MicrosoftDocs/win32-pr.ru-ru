---
title: Метод Инапсохконструктор Жетсох (Наппротокол. h)
description: Извлекает сконструированный пакет Сохрекуест или Сохреспонсе.
ms.assetid: 402c72fd-9e23-453a-8c95-57615295e056
keywords:
- Метод Жетсох NAP
- Метод Жетсох NAP, интерфейс Инапсохконструктор
- Инапсохконструктор интерфейса NAP, метод Жетсох
topic_type:
- apiref
api_name:
- INapSoHConstructor.GetSoH
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066257aadf0ed14816efec06936d4b070087159f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135771"
---
# <a name="inapsohconstructorgetsoh-method"></a><span data-ttu-id="86869-106">Метод Инапсохконструктор:: Жетсох</span><span class="sxs-lookup"><span data-stu-id="86869-106">INapSoHConstructor::GetSoH method</span></span>

> [!Note]  
> <span data-ttu-id="86869-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="86869-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="86869-108">Метод **инапсохконструктор:: жетсох** извлекает сконструированный пакет Сохрекуест или сохреспонсе.</span><span class="sxs-lookup"><span data-stu-id="86869-108">The **INapSoHConstructor::GetSoH** method retrieves the constructed SoHRequest or SoHResponse packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="86869-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86869-109">Syntax</span></span>


```C++
HRESULT GetSoH(
  [out] SoH **soh
);
```



## <a name="parameters"></a><span data-ttu-id="86869-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="86869-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86869-111">*состояние работоспособности* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="86869-111">*soh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86869-112">Указатель на указатель на сконструированный пакет [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) или **сохреспонсе** .</span><span class="sxs-lookup"><span data-stu-id="86869-112">A pointer to a pointer to the constructed [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) or **SoHResponse** packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86869-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86869-113">Return value</span></span>

<span data-ttu-id="86869-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="86869-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="86869-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="86869-115">Return code</span></span>                                                                                     | <span data-ttu-id="86869-116">Описание</span><span class="sxs-lookup"><span data-stu-id="86869-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="86869-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="86869-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="86869-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="86869-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="86869-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="86869-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="86869-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="86869-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="86869-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="86869-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="86869-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86869-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="86869-123">Требования</span><span class="sxs-lookup"><span data-stu-id="86869-123">Requirements</span></span>



| <span data-ttu-id="86869-124">Требование</span><span class="sxs-lookup"><span data-stu-id="86869-124">Requirement</span></span> | <span data-ttu-id="86869-125">Значение</span><span class="sxs-lookup"><span data-stu-id="86869-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="86869-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86869-126">Minimum supported client</span></span><br/> | <span data-ttu-id="86869-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="86869-127">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="86869-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86869-128">Minimum supported server</span></span><br/> | <span data-ttu-id="86869-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="86869-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="86869-130">Header</span><span class="sxs-lookup"><span data-stu-id="86869-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="86869-131"><dt>Наппротокол. h</dt></span><span class="sxs-lookup"><span data-stu-id="86869-131"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="86869-132">IDL</span><span class="sxs-lookup"><span data-stu-id="86869-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="86869-133"><dt>Наппротокол. idl</dt></span><span class="sxs-lookup"><span data-stu-id="86869-133"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="86869-134">DLL</span><span class="sxs-lookup"><span data-stu-id="86869-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86869-135"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86869-135"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="86869-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86869-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86869-137">**инапсохконструктор**</span><span class="sxs-lookup"><span data-stu-id="86869-137">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





