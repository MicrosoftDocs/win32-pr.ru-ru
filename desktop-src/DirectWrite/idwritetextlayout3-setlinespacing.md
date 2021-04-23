---
title: IDWriteTextLayout3 СетлинеспаЦинг, метод
description: Задать Междустрочный зазор. | IDWriteTextLayout3 СетлинеспаЦинг, метод
ms.assetid: 1bfca257-189c-4d18-628c-aff8217d2775
keywords:
- Непосредственная запись метода СетлинеспаЦинг
- Прямая запись метода СетлинеспаЦинг, интерфейс IDWriteTextLayout3
- Прямая запись интерфейса IDWriteTextLayout3, метод СетлинеспаЦинг
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794df5b0dc993688c8bab15c927ae2c03bc18d69
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664858"
---
# <a name="idwritetextlayout3setlinespacing-method"></a><span data-ttu-id="7e1d6-107">Метод IDWriteTextLayout3:: СетлинеспаЦинг</span><span class="sxs-lookup"><span data-stu-id="7e1d6-107">IDWriteTextLayout3::SetLineSpacing method</span></span>

<span data-ttu-id="7e1d6-108">Задать Междустрочный зазор.</span><span class="sxs-lookup"><span data-stu-id="7e1d6-108">Set line spacing.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e1d6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e1d6-109">Syntax</span></span>


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="7e1d6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e1d6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e1d6-111">*линеспаЦингоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e1d6-111">*lineSpacingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e1d6-112">Управление пространством между строками.</span><span class="sxs-lookup"><span data-stu-id="7e1d6-112">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e1d6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e1d6-113">Return value</span></span>

<span data-ttu-id="7e1d6-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7e1d6-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7e1d6-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7e1d6-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e1d6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7e1d6-116">Requirements</span></span>



| <span data-ttu-id="7e1d6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7e1d6-117">Requirement</span></span> | <span data-ttu-id="7e1d6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7e1d6-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e1d6-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e1d6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7e1d6-120">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7e1d6-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7e1d6-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e1d6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7e1d6-122">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e1d6-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7e1d6-123">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="7e1d6-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="7e1d6-124">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="7e1d6-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="7e1d6-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7e1d6-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="7e1d6-126"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e1d6-126"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7e1d6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7e1d6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e1d6-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e1d6-128"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7e1d6-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e1d6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e1d6-130">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="7e1d6-130">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





