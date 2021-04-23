---
description: Метод «разместить \_ светимость» указывает значение светимости, к которому будет подключаться ключ. Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ светимость.
ms.assetid: 3e255423-1724-49fe-b1a1-49bc1d5fa6ae
title: 'Идксткэй: метод ut_Luminance:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Luminance
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 100f2352b88e9aae2f31ce969302f4bee0905f27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675931"
---
# <a name="idxtkeyput_luminance-method"></a><span data-ttu-id="4ad18-104">Идксткэй: \_ метод освещенности:p UT</span><span class="sxs-lookup"><span data-stu-id="4ad18-104">IDxtKey::put\_Luminance method</span></span>

> [!Note]  
> <span data-ttu-id="4ad18-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="4ad18-105">\[Deprecated.</span></span> <span data-ttu-id="4ad18-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4ad18-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4ad18-107">`put_Luminance`Метод задает значение светимости для ключа.</span><span class="sxs-lookup"><span data-stu-id="4ad18-107">The `put_Luminance` method specifies the luminance value on which to key.</span></span> <span data-ttu-id="4ad18-108">Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ светимость.</span><span class="sxs-lookup"><span data-stu-id="4ad18-108">This property applies only when the key type is DXTKEY\_LUMINANCE.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ad18-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ad18-109">Syntax</span></span>


```C++
HRESULT put_Luminance(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="4ad18-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ad18-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ad18-111">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ad18-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ad18-112">Значение светимости, на которое следует подключаться.</span><span class="sxs-lookup"><span data-stu-id="4ad18-112">The luminance value on which to key.</span></span> <span data-ttu-id="4ad18-113">Допустимый диапазон: от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="4ad18-113">The valid range is from 0 to 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ad18-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ad18-114">Return value</span></span>

<span data-ttu-id="4ad18-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4ad18-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4ad18-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4ad18-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ad18-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ad18-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4ad18-118">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="4ad18-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4ad18-119">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4ad18-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4ad18-120">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4ad18-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4ad18-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4ad18-121">Requirements</span></span>



| <span data-ttu-id="4ad18-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4ad18-122">Requirement</span></span> | <span data-ttu-id="4ad18-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4ad18-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ad18-124">Header</span><span class="sxs-lookup"><span data-stu-id="4ad18-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4ad18-125"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ad18-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4ad18-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4ad18-126">Library</span></span><br/> | <dl> <span data-ttu-id="4ad18-127"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ad18-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ad18-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ad18-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ad18-129">**Интерфейс Идксткэй**</span><span class="sxs-lookup"><span data-stu-id="4ad18-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="4ad18-130">**Идксткэй::p UT \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="4ad18-130">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




