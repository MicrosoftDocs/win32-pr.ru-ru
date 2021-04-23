---
title: IDWriteTextLayout3 Жетлинеметрикс, метод
description: Извлекает свойства каждой строки.
ms.assetid: 352ca3e3-7b08-823c-0881-0b051d4ce574
keywords:
- Непосредственная запись метода Жетлинеметрикс
- Прямая запись метода Жетлинеметрикс, интерфейс IDWriteTextLayout3
- Прямая запись интерфейса IDWriteTextLayout3, метод Жетлинеметрикс
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d10a06cbf123b71e1308b45c747ac8a840a5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491409"
---
# <a name="idwritetextlayout3getlinemetrics-method"></a><span data-ttu-id="98ef7-106">Метод IDWriteTextLayout3:: Жетлинеметрикс</span><span class="sxs-lookup"><span data-stu-id="98ef7-106">IDWriteTextLayout3::GetLineMetrics method</span></span>

<span data-ttu-id="98ef7-107">Извлекает свойства каждой строки.</span><span class="sxs-lookup"><span data-stu-id="98ef7-107">Retrieves properties of each line.</span></span>

## <a name="syntax"></a><span data-ttu-id="98ef7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98ef7-108">Syntax</span></span>


```C++
HRESULT GetLineMetrics(
  [out] DWRITE_LINE_METRICS1 *lineMetrics,
        UINT32               maxLineCount,
  [out] UINT32               *actualLineCount
);
```



## <a name="parameters"></a><span data-ttu-id="98ef7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ef7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98ef7-110">*линеметрикс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="98ef7-110">*lineMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98ef7-111">Массив, который заполняется сведениями о строке.</span><span class="sxs-lookup"><span data-stu-id="98ef7-111">The array to fill with line information.</span></span>

</dd> <dt>

<span data-ttu-id="98ef7-112">*макслинекаунт*</span><span class="sxs-lookup"><span data-stu-id="98ef7-112">*maxLineCount*</span></span> 
</dt> <dd>

<span data-ttu-id="98ef7-113">Максимальный размер массива Линеметрикс.</span><span class="sxs-lookup"><span data-stu-id="98ef7-113">The maximum size of the lineMetrics array.</span></span>

</dd> <dt>

<span data-ttu-id="98ef7-114">*актуаллинекаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="98ef7-114">*actualLineCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98ef7-115">Фактический размер требуемого массива Линеметрикс.</span><span class="sxs-lookup"><span data-stu-id="98ef7-115">The actual size of the lineMetrics array that is needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98ef7-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98ef7-116">Return value</span></span>

<span data-ttu-id="98ef7-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="98ef7-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="98ef7-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="98ef7-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="98ef7-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98ef7-119">Remarks</span></span>

<span data-ttu-id="98ef7-120">Если размер Макслинекаунт не достаточен \_ \_ для недостаточного размера \_ буфера, что эквивалентно значению HRESULT \_ из \_ Win32 (ошибка \_ недостаточна для \_ буфера), возвращается значение, а для актуаллинекаунт задается необходимое количество строк.</span><span class="sxs-lookup"><span data-stu-id="98ef7-120">If maxLineCount is not large enough E\_NOT\_SUFFICIENT\_BUFFER, which is equivalent to HRESULT\_FROM\_WIN32(ERROR\_INSUFFICIENT\_BUFFER), is returned and actualLineCount is set to the number of lines needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="98ef7-121">Требования</span><span class="sxs-lookup"><span data-stu-id="98ef7-121">Requirements</span></span>



| <span data-ttu-id="98ef7-122">Требование</span><span class="sxs-lookup"><span data-stu-id="98ef7-122">Requirement</span></span> | <span data-ttu-id="98ef7-123">Значение</span><span class="sxs-lookup"><span data-stu-id="98ef7-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98ef7-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98ef7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="98ef7-125">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="98ef7-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="98ef7-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98ef7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="98ef7-127">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="98ef7-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="98ef7-128">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="98ef7-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="98ef7-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="98ef7-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="98ef7-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="98ef7-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="98ef7-131"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98ef7-131"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="98ef7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="98ef7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98ef7-133"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98ef7-133"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="98ef7-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98ef7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98ef7-135">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="98ef7-135">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





