---
description: Метод Get \_ RGB извлекает цвет RGB для ключа. Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ RGB.
ms.assetid: 7b1b22ff-457a-48c8-9221-ca38601874a9
title: 'Метод Идксткэй:: get_RGB (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ef521b28c232f8247ef38858931ae56be6bf2d25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675324"
---
# <a name="idxtkeyget_rgb-method"></a><span data-ttu-id="f2447-104">Метод Идксткэй:: Get \_ RGB</span><span class="sxs-lookup"><span data-stu-id="f2447-104">IDxtKey::get\_RGB method</span></span>

> [!Note]  
> <span data-ttu-id="f2447-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f2447-105">\[Deprecated.</span></span> <span data-ttu-id="f2447-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f2447-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f2447-107">`get_RGB`Метод извлекает цвет RGB, по которому следует подключаться.</span><span class="sxs-lookup"><span data-stu-id="f2447-107">The `get_RGB` method retrieves the RGB color on which to key.</span></span> <span data-ttu-id="f2447-108">Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ RGB.</span><span class="sxs-lookup"><span data-stu-id="f2447-108">This property applies only when the key type is DXTKEY\_RGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2447-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2447-109">Syntax</span></span>


```C++
HRESULT get_RGB(
  [out, retval] DWORD *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f2447-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2447-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2447-111">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f2447-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f2447-112">Получает цвет.</span><span class="sxs-lookup"><span data-stu-id="f2447-112">Receives the color.</span></span> <span data-ttu-id="f2447-113">Возвращаемое значение представляет собой шестнадцатеричное число в формате 0xRRGGBB, где RR — это значение красного цвета, а параметр GG — зеленое значение, а BB — синий.</span><span class="sxs-lookup"><span data-stu-id="f2447-113">The returned value is a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2447-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2447-114">Return value</span></span>

<span data-ttu-id="f2447-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2447-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f2447-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f2447-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2447-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2447-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f2447-118">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f2447-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f2447-119">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f2447-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f2447-120">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f2447-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f2447-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f2447-121">Requirements</span></span>



| <span data-ttu-id="f2447-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f2447-122">Requirement</span></span> | <span data-ttu-id="f2447-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f2447-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2447-124">Header</span><span class="sxs-lookup"><span data-stu-id="f2447-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f2447-125"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2447-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f2447-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f2447-126">Library</span></span><br/> | <dl> <span data-ttu-id="f2447-127"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2447-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2447-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2447-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2447-129">**Интерфейс Идксткэй**</span><span class="sxs-lookup"><span data-stu-id="f2447-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="f2447-130">**Идксткэй:: Get \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="f2447-130">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




