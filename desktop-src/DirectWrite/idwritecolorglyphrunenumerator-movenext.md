---
title: Идвритеколорглифруненумератор метод MoveNext
description: Переход к следующему глифу выполняется в перечислителе.
ms.assetid: E6336C0E-F880-485C-9111-A102298257C1
keywords:
- Прямая запись метода MoveNext
- Метод MoveNext Direct Write, интерфейс Идвритеколорглифруненумератор
- Прямая запись интерфейса Идвритеколорглифруненумератор, метод MoveNext
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator.MoveNext
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c9963916c07f1df8cf3cfedb49b9e3fd66d0df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534499"
---
# <a name="idwritecolorglyphrunenumeratormovenext-method"></a><span data-ttu-id="56e8c-106">Метод Идвритеколорглифруненумератор:: MoveNext</span><span class="sxs-lookup"><span data-stu-id="56e8c-106">IDWriteColorGlyphRunEnumerator::MoveNext method</span></span>

<span data-ttu-id="56e8c-107">Переход к следующему глифу выполняется в перечислителе.</span><span class="sxs-lookup"><span data-stu-id="56e8c-107">Move to the next glyph run in the enumerator.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e8c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56e8c-108">Syntax</span></span>


```C++
HRESULT MoveNext(
  [out] BOOL *haveRun
);
```



## <a name="parameters"></a><span data-ttu-id="56e8c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="56e8c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56e8c-110">*хаверун* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="56e8c-110">*haveRun* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56e8c-111">Тип: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="56e8c-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="56e8c-112">Возвращает \*значение _ true\*\*, если выполняется следующий запуск глифа.</span><span class="sxs-lookup"><span data-stu-id="56e8c-112">Returns _ *TRUE*\* if there is a next glyph run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56e8c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56e8c-113">Return value</span></span>

<span data-ttu-id="56e8c-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="56e8c-114">Type: **HRESULT**</span></span>

<span data-ttu-id="56e8c-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="56e8c-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="56e8c-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="56e8c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="56e8c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="56e8c-117">Requirements</span></span>



| <span data-ttu-id="56e8c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="56e8c-118">Requirement</span></span> | <span data-ttu-id="56e8c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="56e8c-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56e8c-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56e8c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="56e8c-121">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="56e8c-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="56e8c-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56e8c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="56e8c-123">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="56e8c-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="56e8c-124">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="56e8c-124">Minimum supported phone</span></span><br/>  | <span data-ttu-id="56e8c-125">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="56e8c-125">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="56e8c-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="56e8c-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="56e8c-127"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56e8c-127"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="56e8c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="56e8c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56e8c-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56e8c-129"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="56e8c-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56e8c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56e8c-131">**идвритеколорглифруненумератор**</span><span class="sxs-lookup"><span data-stu-id="56e8c-131">**IDWriteColorGlyphRunEnumerator**</span></span>](idwritecolorglyphrunenumerator.md)
</dt> </dl>

 

 





