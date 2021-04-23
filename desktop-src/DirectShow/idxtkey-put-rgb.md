---
description: Метод постановки \_ RGB задает цвет RGB для ключа. Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ RGB.
ms.assetid: 7a0b794e-bea6-4061-98a0-3f70521e89a3
title: 'Идксткэй: метод ut_RGB:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0b7d282ceb4a693d5a390b8df9b935f0e415d150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675810"
---
# <a name="idxtkeyput_rgb-method"></a><span data-ttu-id="b89cf-104">Идксткэй: метод:p UT \_ RGB</span><span class="sxs-lookup"><span data-stu-id="b89cf-104">IDxtKey::put\_RGB method</span></span>

> [!Note]  
> <span data-ttu-id="b89cf-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="b89cf-105">\[Deprecated.</span></span> <span data-ttu-id="b89cf-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b89cf-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b89cf-107">`put_RGB`Метод задает цвет RGB для ключа.</span><span class="sxs-lookup"><span data-stu-id="b89cf-107">The `put_RGB` method specifies the RGB color on which to key.</span></span> <span data-ttu-id="b89cf-108">Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ RGB.</span><span class="sxs-lookup"><span data-stu-id="b89cf-108">This property applies only when the key type is DXTKEY\_RGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="b89cf-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b89cf-109">Syntax</span></span>


```C++
HRESULT put_RGB(
  [in] DWORD newVal
);
```



## <a name="parameters"></a><span data-ttu-id="b89cf-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b89cf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b89cf-111">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b89cf-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b89cf-112">Задает цвет в виде шестнадцатеричного числа в формате 0xRRGGBB, где RR — это красная величина, а параметр GG — зеленое значение, а BB — синий.</span><span class="sxs-lookup"><span data-stu-id="b89cf-112">Specifies the color as a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b89cf-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b89cf-113">Return value</span></span>

<span data-ttu-id="b89cf-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b89cf-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b89cf-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b89cf-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b89cf-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b89cf-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b89cf-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="b89cf-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b89cf-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b89cf-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b89cf-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="b89cf-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b89cf-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b89cf-120">Requirements</span></span>



| <span data-ttu-id="b89cf-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b89cf-121">Requirement</span></span> | <span data-ttu-id="b89cf-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b89cf-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b89cf-123">Header</span><span class="sxs-lookup"><span data-stu-id="b89cf-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b89cf-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="b89cf-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b89cf-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b89cf-125">Library</span></span><br/> | <dl> <span data-ttu-id="b89cf-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b89cf-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b89cf-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b89cf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b89cf-128">**Интерфейс Идксткэй**</span><span class="sxs-lookup"><span data-stu-id="b89cf-128">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="b89cf-129">**Идксткэй::p UT \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="b89cf-129">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




