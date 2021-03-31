---
title: IDWriteTextFormat2 СетлинеспаЦинг, метод
description: Задать Междустрочный зазор. | IDWriteTextFormat2 СетлинеспаЦинг, метод
ms.assetid: 71d8c6c4-920f-a1b5-5a13-9985a7aca41e
keywords:
- Непосредственная запись метода СетлинеспаЦинг
- Прямая запись метода СетлинеспаЦинг, интерфейс IDWriteTextFormat2
- Прямая запись интерфейса IDWriteTextFormat2, метод СетлинеспаЦинг
topic_type:
- apiref
api_name:
- IDWriteTextFormat2.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d3514c52c9b8a51666d36eec7ce893735635f3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273630"
---
# <a name="idwritetextformat2setlinespacing-method"></a><span data-ttu-id="b7d5a-107">Метод IDWriteTextFormat2:: СетлинеспаЦинг</span><span class="sxs-lookup"><span data-stu-id="b7d5a-107">IDWriteTextFormat2::SetLineSpacing method</span></span>

<span data-ttu-id="b7d5a-108">Задать Междустрочный зазор.</span><span class="sxs-lookup"><span data-stu-id="b7d5a-108">Set line spacing.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d5a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7d5a-109">Syntax</span></span>


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="b7d5a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7d5a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7d5a-111">*линеспаЦингоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7d5a-111">*lineSpacingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d5a-112">Тип: **const [**дврите \_ \_ Междустрочный зазор**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing) \***</span><span class="sxs-lookup"><span data-stu-id="b7d5a-112">Type: **const [**DWRITE\_LINE\_SPACING**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing)\***</span></span>

<span data-ttu-id="b7d5a-113">Управление пространством между строками.</span><span class="sxs-lookup"><span data-stu-id="b7d5a-113">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7d5a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7d5a-114">Return value</span></span>

<span data-ttu-id="b7d5a-115">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b7d5a-115">Type: **HRESULT**</span></span>

<span data-ttu-id="b7d5a-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b7d5a-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b7d5a-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b7d5a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d5a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b7d5a-118">Requirements</span></span>



| <span data-ttu-id="b7d5a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b7d5a-119">Requirement</span></span> | <span data-ttu-id="b7d5a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b7d5a-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d5a-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7d5a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b7d5a-122">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b7d5a-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b7d5a-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7d5a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b7d5a-124">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b7d5a-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b7d5a-125">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="b7d5a-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="b7d5a-126">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="b7d5a-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="b7d5a-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b7d5a-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7d5a-128"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7d5a-128"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b7d5a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b7d5a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7d5a-130"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7d5a-130"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b7d5a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7d5a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d5a-132">**IDWriteTextFormat2**</span><span class="sxs-lookup"><span data-stu-id="b7d5a-132">**IDWriteTextFormat2**</span></span>](idwritetextformat2.md)
</dt> </dl>

 

 





