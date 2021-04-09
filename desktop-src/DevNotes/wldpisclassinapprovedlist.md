---
description: Вызывает библиотеку, чтобы проверить, является ли определенный идентификатор CLSID надежным для вызова.
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: Функция Влдписклассинаппроведлист (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsClassInApprovedList
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 01762c60a3f1aef1574cc218ace9988669175efe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140890"
---
# <a name="wldpisclassinapprovedlist-function"></a><span data-ttu-id="77227-103">Функция Влдписклассинаппроведлист</span><span class="sxs-lookup"><span data-stu-id="77227-103">WldpIsClassInApprovedList function</span></span>

<span data-ttu-id="77227-104">Вызывает библиотеку, чтобы проверить, является ли определенный **идентификатор CLSID** надежным для вызова.</span><span class="sxs-lookup"><span data-stu-id="77227-104">Calls the library to validate if a particular **CLSID** is safe to be called.</span></span> <span data-ttu-id="77227-105">У функции нет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="77227-105">The function has no associated import library.</span></span> <span data-ttu-id="77227-106">Для динамической привязки к wldp.dll необходимо использовать функции LoadLibrary и GetProcAddress.</span><span class="sxs-lookup"><span data-stu-id="77227-106">You must use the LoadLibrary and GetProcAddress functions to dynamically link to wldp.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="77227-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77227-107">Syntax</span></span>


```C++
HRESULT WINAPI WldpIsClassInApprovedList(
        REFCLSID               classID,
  _In_  PWLDP_HOST_INFORMATION hostInformation,
  _Out_ PBOOL                  isApproved,
        DWORD                  optionalFlags
);
```



## <a name="parameters"></a><span data-ttu-id="77227-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="77227-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77227-109">*Класса*</span><span class="sxs-lookup"><span data-stu-id="77227-109">*classID*</span></span> 
</dt> <dd>

<span data-ttu-id="77227-110">Идентификатор класса COM для проверки на одобрение.</span><span class="sxs-lookup"><span data-stu-id="77227-110">The COM class ID to check for approval.</span></span>

</dd> <dt>

<span data-ttu-id="77227-111">*хостинформатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="77227-111">*hostInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77227-112">Структура [**\_ \_ информации узла WLDP**](wldp-host-information.md) , определяющая оцениваемый узел.</span><span class="sxs-lookup"><span data-stu-id="77227-112">A [**WLDP\_HOST\_INFORMATION**](wldp-host-information.md) structure identifying the host to be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="77227-113">*утверждено* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="77227-113">*isApproved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77227-114">При успешном завершении содержит **значение true** , если идентификатор класса утвержден. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="77227-114">On successful completion, contains **TRUE** if the class ID is approved; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="77227-115">*оптионалфлагс*</span><span class="sxs-lookup"><span data-stu-id="77227-115">*optionalFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="77227-116">Этот параметр зарезервирован и должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="77227-116">This parameter is reserved and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77227-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77227-117">Return value</span></span>

<span data-ttu-id="77227-118">Этот метод возвращает **значение \_ ОК** в случае успеха или код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="77227-118">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="77227-119">Требования</span><span class="sxs-lookup"><span data-stu-id="77227-119">Requirements</span></span>



| <span data-ttu-id="77227-120">Требование</span><span class="sxs-lookup"><span data-stu-id="77227-120">Requirement</span></span> | <span data-ttu-id="77227-121">Значение</span><span class="sxs-lookup"><span data-stu-id="77227-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="77227-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77227-122">Minimum supported client</span></span><br/> | <span data-ttu-id="77227-123">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="77227-123">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="77227-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77227-124">Minimum supported server</span></span><br/> | <span data-ttu-id="77227-125">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="77227-125">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="77227-126">Header</span><span class="sxs-lookup"><span data-stu-id="77227-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="77227-127"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="77227-127"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="77227-128">DLL</span><span class="sxs-lookup"><span data-stu-id="77227-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77227-129"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77227-129"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




