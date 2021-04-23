---
title: IDWriteTextLayout3 Инвалидателайаут, метод
description: Делает макет недействительным, принудительно перемера макета перед вызовом метрик или функций рисования. Это полезно в том случае, если изменяется расположение шрифта, а макет должен быть перерисован или если размер, реализуемый клиентом, Идвритеинлинеобжект изменения.
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
keywords:
- Непосредственная запись метода Инвалидателайаут
- Прямая запись метода Инвалидателайаут, интерфейс IDWriteTextLayout3
- Прямая запись интерфейса IDWriteTextLayout3, метод Инвалидателайаут
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.InvalidateLayout
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5df97d4590f62f586a570d52428b6560a7d88df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136382"
---
# <a name="idwritetextlayout3invalidatelayout-method"></a><span data-ttu-id="4515f-107">Метод IDWriteTextLayout3:: Инвалидателайаут</span><span class="sxs-lookup"><span data-stu-id="4515f-107">IDWriteTextLayout3::InvalidateLayout method</span></span>

<span data-ttu-id="4515f-108">Делает макет недействительным, принудительно перемера макета перед вызовом метрик или функций рисования.</span><span class="sxs-lookup"><span data-stu-id="4515f-108">Invalidates the layout, forcing layout to remeasure before calling the metrics or drawing functions.</span></span> <span data-ttu-id="4515f-109">Это полезно в том случае, если изменяется расположение шрифта, а макет должен быть перерисован или если размер, реализуемый клиентом, Идвритеинлинеобжект изменения.</span><span class="sxs-lookup"><span data-stu-id="4515f-109">This is useful if the locality of a font changes, and layout should be redrawn, or if the size of a client implemented IDWriteInlineObject changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4515f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4515f-110">Syntax</span></span>


```C++
HRESULT InvalidateLayout();
```



## <a name="parameters"></a><span data-ttu-id="4515f-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="4515f-111">Parameters</span></span>

<span data-ttu-id="4515f-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4515f-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4515f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4515f-113">Return value</span></span>

<span data-ttu-id="4515f-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4515f-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4515f-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4515f-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4515f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4515f-116">Requirements</span></span>



| <span data-ttu-id="4515f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4515f-117">Requirement</span></span> | <span data-ttu-id="4515f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4515f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4515f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4515f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4515f-120">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4515f-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4515f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4515f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4515f-122">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4515f-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4515f-123">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="4515f-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="4515f-124">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="4515f-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="4515f-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4515f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="4515f-126"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4515f-126"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4515f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4515f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4515f-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4515f-128"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4515f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4515f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4515f-130">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="4515f-130">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





