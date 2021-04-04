---
title: Функция Мпсреатенумерате (Мпклиент. h)
description: Возвращает сведения о следующей угрозе в списке перечисления. Эту функцию можно вызывать повторно до тех пор, пока не завершится перечисление всех угроз.
ms.assetid: 33244F4F-4FB7-4FA7-BC56-B9A30ABC3644
keywords:
- Функции Мпсреатенумерате устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MpThreatEnumerate
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acdbb7971371015a401c1a951ace8c55869fd405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989022"
---
# <a name="mpthreatenumerate-function"></a><span data-ttu-id="a7fc4-105">Функция Мпсреатенумерате</span><span class="sxs-lookup"><span data-stu-id="a7fc4-105">MpThreatEnumerate function</span></span>

<span data-ttu-id="a7fc4-106">Возвращает сведения о следующей угрозе в списке перечисления.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-106">Returns information about the next threat in the enumeration list.</span></span> <span data-ttu-id="a7fc4-107">Эту функцию можно вызывать повторно до тех пор, пока не завершится перечисление всех угроз.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-107">This function can be called repeatedly until the enumeration of all the threats is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7fc4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7fc4-108">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatEnumerate(
  _In_  MPHANDLE       hThreatEnumHandle,
  _Out_ PMPTHREAT_INFO *ppThreatInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a7fc4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7fc4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7fc4-110">*хсреатенумхандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a7fc4-110">*hThreatEnumHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fc4-111">Тип: **мфандле**</span><span class="sxs-lookup"><span data-stu-id="a7fc4-111">Type: **MPHANDLE**</span></span>

<span data-ttu-id="a7fc4-112">Обработчик контекста перечисления угроз, возвращенный [**мпсреатопен**](mpthreatopen.md).</span><span class="sxs-lookup"><span data-stu-id="a7fc4-112">Handle to a threat enumeration context returned by [**MpThreatOpen**](mpthreatopen.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7fc4-113">*ппсреатинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a7fc4-113">*ppThreatInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fc4-114">Введите: \**пмпсреат \_ info \** _</span><span class="sxs-lookup"><span data-stu-id="a7fc4-114">Type: \**PMPTHREAT\_INFO\** _</span></span>

<span data-ttu-id="a7fc4-115">Возвращает указатель на структуру сведений об угрозе, [_ *мпсреат \_ info* \*](mpthreat-info.md).</span><span class="sxs-lookup"><span data-stu-id="a7fc4-115">Returns a pointer to a threat information structure, [_ *MPTHREAT\_INFO*\*](mpthreat-info.md).</span></span> <span data-ttu-id="a7fc4-116">Структура содержит такие сведения, как идентификатор угрозы, имя и серьезность.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-116">The structure contains information such as threat id, name, and severity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7fc4-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7fc4-117">Return value</span></span>

<span data-ttu-id="a7fc4-118">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a7fc4-118">Type: **HRESULT**</span></span>

<span data-ttu-id="a7fc4-119">Если функция выполнена успешно, возвращается значение **S \_**.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-119">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="a7fc4-120">Если больше нет элементов для возврата возвращаемого значения, возвращается значение **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-120">If there are no more items to return the return value is **S\_FALSE**.</span></span>

<span data-ttu-id="a7fc4-121">Если функция завершается ошибкой, возвращаемое значение является неудачным кодом **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a7fc4-121">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="a7fc4-122">Вызывающий объект может использовать функцию [**мперрормессажеформат**](mperrormessageformat.md) для получения общего описания сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a7fc4-122">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7fc4-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a7fc4-123">Requirements</span></span>



| <span data-ttu-id="a7fc4-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a7fc4-124">Requirement</span></span> | <span data-ttu-id="a7fc4-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a7fc4-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7fc4-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7fc4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a7fc4-127">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a7fc4-127">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="a7fc4-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7fc4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a7fc4-129">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a7fc4-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a7fc4-130">Header</span><span class="sxs-lookup"><span data-stu-id="a7fc4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7fc4-131"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7fc4-131"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7fc4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a7fc4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7fc4-133"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7fc4-133"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7fc4-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7fc4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7fc4-135">**мперрормессажеформат**</span><span class="sxs-lookup"><span data-stu-id="a7fc4-135">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="a7fc4-136">**мпсреатопен**</span><span class="sxs-lookup"><span data-stu-id="a7fc4-136">**MpThreatOpen**</span></span>](mpthreatopen.md)
</dt> <dt>

[<span data-ttu-id="a7fc4-137">**\_сведения о мпсреат**</span><span class="sxs-lookup"><span data-stu-id="a7fc4-137">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> </dl>

 

 





