---
title: Функция Мпманажерверсионкуери (Мпклиент. h)
description: Возвращает сведения о версии различных компонентов диспетчера защиты от вредоносных программ.
ms.assetid: 47DE12BF-D7A4-468B-B0E7-79B5C27E56F5
keywords:
- Функции Мпманажерверсионкуери устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MpManagerVersionQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a841a83d8ceb828de0a5a9cd80f5f5bdc7f5c914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682000"
---
# <a name="mpmanagerversionquery-function"></a><span data-ttu-id="f07f5-104">Функция Мпманажерверсионкуери</span><span class="sxs-lookup"><span data-stu-id="f07f5-104">MpManagerVersionQuery function</span></span>

<span data-ttu-id="f07f5-105">Возвращает сведения о версии различных компонентов диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="f07f5-105">Returns version information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="f07f5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f07f5-106">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerVersionQuery(
  _In_  MPHANDLE        hMpHandle,
  _Out_ PMPVERSION_INFO pVersionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="f07f5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f07f5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f07f5-108">*хмфандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f07f5-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f07f5-109">Тип: **мфандле**</span><span class="sxs-lookup"><span data-stu-id="f07f5-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="f07f5-110">Обработчик для интерфейса диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="f07f5-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="f07f5-111">Этот маркер возвращается функцией [**мпманажеропен**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="f07f5-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f07f5-112">*пверсионинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f07f5-112">*pVersionInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f07f5-113">Тип: **пмпверсион \_ info** .</span><span class="sxs-lookup"><span data-stu-id="f07f5-113">Type: **PMPVERSION\_INFO**</span></span>

<span data-ttu-id="f07f5-114">Указатель на структуру, содержащую сведения о версии различных компонентов диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="f07f5-114">Pointer to a structure that contains version information about various components of the malware protection manager.</span></span> <span data-ttu-id="f07f5-115">См [**. \_ сведения о MPVERSION**](mpversion-info.md).</span><span class="sxs-lookup"><span data-stu-id="f07f5-115">See [**MPVERSION\_INFO**](mpversion-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f07f5-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f07f5-116">Return value</span></span>

<span data-ttu-id="f07f5-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f07f5-117">Type: **HRESULT**</span></span>

<span data-ttu-id="f07f5-118">Если функция выполнена успешно, возвращается значение **S \_**.</span><span class="sxs-lookup"><span data-stu-id="f07f5-118">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="f07f5-119">Если функция завершается ошибкой, возвращаемое значение является неудачным кодом **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f07f5-119">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="f07f5-120">Вызывающий объект может использовать функцию [**мперрормессажеформат**](mperrormessageformat.md) для получения общего описания сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="f07f5-120">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f07f5-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f07f5-121">Requirements</span></span>



| <span data-ttu-id="f07f5-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f07f5-122">Requirement</span></span> | <span data-ttu-id="f07f5-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f07f5-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f07f5-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f07f5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f07f5-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f07f5-125">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f07f5-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f07f5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f07f5-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f07f5-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f07f5-128">Header</span><span class="sxs-lookup"><span data-stu-id="f07f5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f07f5-129"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="f07f5-129"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="f07f5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f07f5-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f07f5-131"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f07f5-131"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f07f5-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f07f5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f07f5-133">**мперрормессажеформат**</span><span class="sxs-lookup"><span data-stu-id="f07f5-133">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="f07f5-134">**мпманажеропен**</span><span class="sxs-lookup"><span data-stu-id="f07f5-134">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="f07f5-135">**\_сведения о MPVERSION**</span><span class="sxs-lookup"><span data-stu-id="f07f5-135">**MPVERSION\_INFO**</span></span>](mpversion-info.md)
</dt> </dl>

 

 





