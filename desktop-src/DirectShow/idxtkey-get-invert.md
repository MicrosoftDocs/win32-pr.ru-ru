---
description: '\_Метод инверсии получает логическое значение, указывающее, выполняется ли обратная операция с ключом. Это свойство применяется ко всем типам ключей, за исключением ДКСТКЭЙ \_ Alpha.'
ms.assetid: 2ccf2066-3d9c-493b-bc54-a03e7d075531
title: 'Метод Идксткэй:: get_Invert (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 51b95758adf6690f6d4fa479ac1cc2c585fa9352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675329"
---
# <a name="idxtkeyget_invert-method"></a><span data-ttu-id="6665b-104">Метод Идксткэй:: Get \_ инверсия</span><span class="sxs-lookup"><span data-stu-id="6665b-104">IDxtKey::get\_Invert method</span></span>

> [!Note]  
> <span data-ttu-id="6665b-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="6665b-105">\[Deprecated.</span></span> <span data-ttu-id="6665b-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6665b-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6665b-107">`get_Invert`Метод получает логическое значение, указывающее, выполняется ли обратная операция с ключом.</span><span class="sxs-lookup"><span data-stu-id="6665b-107">The `get_Invert` method retrieves a Boolean value indicating whether the key operation is inverted.</span></span> <span data-ttu-id="6665b-108">Это свойство применяется ко всем типам ключей, за исключением ДКСТКЭЙ \_ Alpha.</span><span class="sxs-lookup"><span data-stu-id="6665b-108">This property applies to all key types except DXTKEY\_ALPHA.</span></span>

## <a name="syntax"></a><span data-ttu-id="6665b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6665b-109">Syntax</span></span>


```C++
HRESULT get_Invert(
  [out, retval] BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="6665b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6665b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6665b-111">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6665b-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6665b-112">Получает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6665b-112">Receives one of the following values.</span></span>



| <span data-ttu-id="6665b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6665b-113">Value</span></span>     | <span data-ttu-id="6665b-114">Описание</span><span class="sxs-lookup"><span data-stu-id="6665b-114">Description</span></span>                                                                       |
|-----------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6665b-115">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="6665b-115">**TRUE**</span></span>  | <span data-ttu-id="6665b-116">Пикселы в перевернутом изображении инвертированы по отношению к операции по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6665b-116">Pixels in the overlying image are inverted with respect to the default operation.</span></span> |
| <span data-ttu-id="6665b-117">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="6665b-117">**FALSE**</span></span> | <span data-ttu-id="6665b-118">Пикселы в изображении с чрезмерной назначением становятся прозрачными по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6665b-118">Pixels in the overlying image are made transparent in the default manner.</span></span>         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6665b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6665b-119">Return value</span></span>

<span data-ttu-id="6665b-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6665b-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6665b-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6665b-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6665b-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6665b-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6665b-123">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="6665b-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6665b-124">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6665b-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6665b-125">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="6665b-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6665b-126">Требования</span><span class="sxs-lookup"><span data-stu-id="6665b-126">Requirements</span></span>



| <span data-ttu-id="6665b-127">Требование</span><span class="sxs-lookup"><span data-stu-id="6665b-127">Requirement</span></span> | <span data-ttu-id="6665b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6665b-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6665b-129">Header</span><span class="sxs-lookup"><span data-stu-id="6665b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6665b-130"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="6665b-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6665b-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6665b-131">Library</span></span><br/> | <dl> <span data-ttu-id="6665b-132"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6665b-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6665b-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6665b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6665b-134">**Интерфейс Идксткэй**</span><span class="sxs-lookup"><span data-stu-id="6665b-134">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="6665b-135">**Идксткэй:: Get \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="6665b-135">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




