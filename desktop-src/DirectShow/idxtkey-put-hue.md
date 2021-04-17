---
description: Метод «разместить \_ оттенок» задает значение оттенка, по которому будет указывать ключ. Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙный \_ тон.
ms.assetid: 90c8c610-7ceb-479b-bb0e-d8753d0d7dac
title: 'Идксткэй: метод ut_Hue:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Hue
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9d2b08f3e805edc8b8860495fc105f0cfdf6768f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675321"
---
# <a name="idxtkeyput_hue-method"></a><span data-ttu-id="88171-104">Идксткэй::p \_ метод оттенок метода UT</span><span class="sxs-lookup"><span data-stu-id="88171-104">IDxtKey::put\_Hue method</span></span>

> [!Note]  
> <span data-ttu-id="88171-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="88171-105">\[Deprecated.</span></span> <span data-ttu-id="88171-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="88171-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="88171-107">`put_Hue`Метод задает значение оттенка ключа.</span><span class="sxs-lookup"><span data-stu-id="88171-107">The `put_Hue` method specifies the hue value on which to key.</span></span> <span data-ttu-id="88171-108">Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙный \_ тон.</span><span class="sxs-lookup"><span data-stu-id="88171-108">This property applies only when the key type is DXTKEY\_HUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="88171-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88171-109">Syntax</span></span>


```C++
HRESULT put_Hue(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="88171-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="88171-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88171-111">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88171-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88171-112">Значение оттенка ключа.</span><span class="sxs-lookup"><span data-stu-id="88171-112">The hue value on which to key.</span></span> <span data-ttu-id="88171-113">Допустимый диапазон: от 0 до 360.</span><span class="sxs-lookup"><span data-stu-id="88171-113">The valid range is from 0 to 360.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88171-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88171-114">Return value</span></span>

<span data-ttu-id="88171-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="88171-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88171-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88171-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="88171-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88171-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="88171-118">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="88171-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="88171-119">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="88171-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="88171-120">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="88171-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="88171-121">Требования</span><span class="sxs-lookup"><span data-stu-id="88171-121">Requirements</span></span>



| <span data-ttu-id="88171-122">Требование</span><span class="sxs-lookup"><span data-stu-id="88171-122">Requirement</span></span> | <span data-ttu-id="88171-123">Значение</span><span class="sxs-lookup"><span data-stu-id="88171-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88171-124">Header</span><span class="sxs-lookup"><span data-stu-id="88171-124">Header</span></span><br/>  | <dl> <span data-ttu-id="88171-125"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="88171-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="88171-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="88171-126">Library</span></span><br/> | <dl> <span data-ttu-id="88171-127"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88171-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88171-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88171-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88171-129">**Интерфейс Идксткэй**</span><span class="sxs-lookup"><span data-stu-id="88171-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="88171-130">**Идксткэй::p UT \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="88171-130">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




