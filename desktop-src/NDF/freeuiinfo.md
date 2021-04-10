---
title: Функция Фриуиинфо (Ндаттрибутилс. h)
description: Освобождает выделенную память для внутренней структуры Уиинфо.
ms.assetid: 41d923fd-2fb3-406e-a5cf-f3ba475685f6
keywords:
- Фриуиинфо функция NDF
topic_type:
- apiref
api_name:
- FreeUiInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a96d859faa80e3e2269981d206c96e780d05c37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135519"
---
# <a name="freeuiinfo-function"></a><span data-ttu-id="55a8d-104">Функция Фриуиинфо</span><span class="sxs-lookup"><span data-stu-id="55a8d-104">FreeUiInfo function</span></span>

<span data-ttu-id="55a8d-105">Функция **фриуиинфо** освобождает выделенную для внутренней памяти память для структуры [**уиинфо**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) .</span><span class="sxs-lookup"><span data-stu-id="55a8d-105">The **FreeUiInfo** function deallocates the memory allocated internally to a [**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) structure.</span></span> <span data-ttu-id="55a8d-106">Эта функция вызывает [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="55a8d-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="55a8d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55a8d-107">Syntax</span></span>


```C++
VOID FreeUiInfo(
  _In_ UiInfo *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="55a8d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="55a8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55a8d-109">*пинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55a8d-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55a8d-110">Тип: \**[**уиинфо**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="55a8d-110">Type: \**[**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)\** _</span></span>

<span data-ttu-id="55a8d-111">Структура.</span><span class="sxs-lookup"><span data-stu-id="55a8d-111">The structure.</span></span> <span data-ttu-id="55a8d-112">Выделенная память, на которую указывает эта структура, будет освобождена.</span><span class="sxs-lookup"><span data-stu-id="55a8d-112">The allocated memory pointed to by this structure will be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55a8d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55a8d-113">Return value</span></span>

<span data-ttu-id="55a8d-114">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="55a8d-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="55a8d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="55a8d-115">Requirements</span></span>



| <span data-ttu-id="55a8d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="55a8d-116">Requirement</span></span> | <span data-ttu-id="55a8d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="55a8d-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="55a8d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55a8d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="55a8d-119">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="55a8d-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="55a8d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55a8d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="55a8d-121">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="55a8d-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="55a8d-122">Header</span><span class="sxs-lookup"><span data-stu-id="55a8d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="55a8d-123"><dt>Ндаттрибутилс. h</dt></span><span class="sxs-lookup"><span data-stu-id="55a8d-123"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55a8d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55a8d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a8d-125">_ *Уиинфо*\*</span><span class="sxs-lookup"><span data-stu-id="55a8d-125">_ *UiInfo*\*</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)
</dt> <dt>

[<span data-ttu-id="55a8d-126">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="55a8d-126">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

