---
title: IDWriteTextLayout3 ЖетлинеспаЦинг, метод
description: Возвращает сведения о межстрочном промежутке.
ms.assetid: 6b93a3ec-c8ea-2e64-45b5-51565d6de173
keywords:
- Непосредственная запись метода ЖетлинеспаЦинг
- Прямая запись метода ЖетлинеспаЦинг, интерфейс IDWriteTextLayout3
- Прямая запись интерфейса IDWriteTextLayout3, метод ЖетлинеспаЦинг
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303030a5674f39c160804ae2dad5b91050d82f37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988889"
---
# <a name="idwritetextlayout3getlinespacing-method"></a><span data-ttu-id="05291-106">Метод IDWriteTextLayout3:: ЖетлинеспаЦинг</span><span class="sxs-lookup"><span data-stu-id="05291-106">IDWriteTextLayout3::GetLineSpacing method</span></span>

<span data-ttu-id="05291-107">Возвращает сведения о межстрочном промежутке.</span><span class="sxs-lookup"><span data-stu-id="05291-107">Gets line spacing information.</span></span>

## <a name="syntax"></a><span data-ttu-id="05291-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05291-108">Syntax</span></span>


```C++
HRESULT GetLineSpacing(
  [out] DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="05291-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="05291-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05291-110">*линеспаЦингоптионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="05291-110">*lineSpacingOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05291-111">Управление пространством между строками.</span><span class="sxs-lookup"><span data-stu-id="05291-111">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05291-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05291-112">Return value</span></span>

<span data-ttu-id="05291-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="05291-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="05291-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="05291-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="05291-115">Требования</span><span class="sxs-lookup"><span data-stu-id="05291-115">Requirements</span></span>



| <span data-ttu-id="05291-116">Требование</span><span class="sxs-lookup"><span data-stu-id="05291-116">Requirement</span></span> | <span data-ttu-id="05291-117">Значение</span><span class="sxs-lookup"><span data-stu-id="05291-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05291-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="05291-118">Minimum supported client</span></span><br/> | <span data-ttu-id="05291-119">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="05291-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="05291-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="05291-120">Minimum supported server</span></span><br/> | <span data-ttu-id="05291-121">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="05291-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="05291-122">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="05291-122">Minimum supported phone</span></span><br/>  | <span data-ttu-id="05291-123">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="05291-123">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="05291-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="05291-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="05291-125"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05291-125"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="05291-126">DLL</span><span class="sxs-lookup"><span data-stu-id="05291-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05291-127"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05291-127"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="05291-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05291-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05291-129">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="05291-129">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





