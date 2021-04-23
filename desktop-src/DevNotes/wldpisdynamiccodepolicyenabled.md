---
description: Извлекает значение, описывающее состояние принудительного применения политики Device Guard для динамического кода .NET.
ms.assetid: 11E6C631-0FF8-4DB2-931A-1012B3CA4357
title: Функция Влдписдинамиккодеполициенаблед (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsDynamicCodePolicyEnabled
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 4df0555f89e9c575a7d97b69a5252c17936eb3d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140887"
---
# <a name="wldpisdynamiccodepolicyenabled-function"></a><span data-ttu-id="853bd-103">Функция Влдписдинамиккодеполициенаблед</span><span class="sxs-lookup"><span data-stu-id="853bd-103">WldpIsDynamicCodePolicyEnabled function</span></span>

<span data-ttu-id="853bd-104">Извлекает значение, описывающее состояние принудительного применения политики Device Guard для динамического кода .NET.</span><span class="sxs-lookup"><span data-stu-id="853bd-104">Retrieves a value that describes the Device Guard policy enforcement status for .NET dynamic code.</span></span>

## <a name="syntax"></a><span data-ttu-id="853bd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="853bd-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpIsDynamicCodePolicyEnabled(
  _Out_ PBOOL  isEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="853bd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="853bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="853bd-107">*включено* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="853bd-107">*isEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="853bd-108">При успешном выполнении возвращает **значение true** , если политика Device Guard обеспечивает применение политики динамического кода .NET. в противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="853bd-108">On success, returns **true** if the Device Guard policy enforces .NET Dynamic Code policy; otherwise, returns **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="853bd-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="853bd-109">Return value</span></span>

<span data-ttu-id="853bd-110">Этот метод возвращает **значение \_ ОК** в случае успеха или код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="853bd-110">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="853bd-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="853bd-111">Remarks</span></span>

<span data-ttu-id="853bd-112">Динамический код относится к динамически созданному коду .NET CRL.</span><span class="sxs-lookup"><span data-stu-id="853bd-112">Dynamic code refers to .NET CRL dynamically-generated code.</span></span>

## <a name="requirements"></a><span data-ttu-id="853bd-113">Требования</span><span class="sxs-lookup"><span data-stu-id="853bd-113">Requirements</span></span>



| <span data-ttu-id="853bd-114">Требование</span><span class="sxs-lookup"><span data-stu-id="853bd-114">Requirement</span></span> | <span data-ttu-id="853bd-115">Значение</span><span class="sxs-lookup"><span data-stu-id="853bd-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="853bd-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="853bd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="853bd-117">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="853bd-117">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="853bd-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="853bd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="853bd-119">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="853bd-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="853bd-120">Header</span><span class="sxs-lookup"><span data-stu-id="853bd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="853bd-121"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="853bd-121"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="853bd-122">DLL</span><span class="sxs-lookup"><span data-stu-id="853bd-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="853bd-123"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="853bd-123"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




