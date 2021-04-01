---
description: Извлекает текущий безопасный режим Windows. Windows может находиться в заблокированном режиме, в незаблокированном нормальном режиме или в режиме пробной версии.
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: Функция Влдпкуеривиндовслоккдовнмоде (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryWindowsLockdownMode
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: fc746270a0634525154417cfba7e1529bee7edfb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262721"
---
# <a name="wldpquerywindowslockdownmode-function"></a><span data-ttu-id="9bb01-104">Функция Влдпкуеривиндовслоккдовнмоде</span><span class="sxs-lookup"><span data-stu-id="9bb01-104">WldpQueryWindowsLockdownMode function</span></span>

<span data-ttu-id="9bb01-105">Извлекает текущий безопасный режим Windows.</span><span class="sxs-lookup"><span data-stu-id="9bb01-105">Retrieves the current Windows secure mode.</span></span> <span data-ttu-id="9bb01-106">Windows может находиться в заблокированном режиме, в незаблокированном нормальном режиме или в режиме пробной версии.</span><span class="sxs-lookup"><span data-stu-id="9bb01-106">Windows can be in locked mode, unlocked normal mode, or trial mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bb01-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bb01-107">Syntax</span></span>


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a><span data-ttu-id="9bb01-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bb01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bb01-109">*локкдовнмоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9bb01-109">*lockdownMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bb01-110">При успешном выполнении возвращает [**пвлдп \_ \_ \_ режим блокировки Windows**](wldp-windows-lockdown-mode.md) , который указывает безопасный режим для текущего устройства Windows 10.</span><span class="sxs-lookup"><span data-stu-id="9bb01-110">On success, returns a [**PWLDP\_WINDOWS\_LOCKDOWN\_MODE**](wldp-windows-lockdown-mode.md) that indicates the secure mode for the current Windows 10 device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bb01-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9bb01-111">Return value</span></span>

<span data-ttu-id="9bb01-112">Этот метод возвращает **значение \_ ОК** в случае успеха или код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9bb01-112">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bb01-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9bb01-113">Requirements</span></span>



| <span data-ttu-id="9bb01-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9bb01-114">Requirement</span></span> | <span data-ttu-id="9bb01-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9bb01-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9bb01-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9bb01-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9bb01-117">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="9bb01-117">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9bb01-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9bb01-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9bb01-119">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="9bb01-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9bb01-120">Header</span><span class="sxs-lookup"><span data-stu-id="9bb01-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bb01-121"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bb01-121"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9bb01-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9bb01-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bb01-123"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bb01-123"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




