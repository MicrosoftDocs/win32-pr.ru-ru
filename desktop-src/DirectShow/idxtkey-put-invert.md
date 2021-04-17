---
description: Метод «разместить \_ инверсию» указывает, выполняется ли обратная операция с ключом. Это свойство применяется ко всем типам ключей, за исключением ДКСТКЭЙ \_ Alpha.
ms.assetid: 06acdd9f-eb3a-49bd-961d-00966df2ccb4
title: 'Идксткэй: метод ut_Invert:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3e4b807770d0eeb985c982b61b8390695cc42327
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675319"
---
# <a name="idxtkeyput_invert-method"></a><span data-ttu-id="7698b-104">Идксткэй::p \_ метод инвертора UT</span><span class="sxs-lookup"><span data-stu-id="7698b-104">IDxtKey::put\_Invert method</span></span>

> [!Note]  
> <span data-ttu-id="7698b-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="7698b-105">\[Deprecated.</span></span> <span data-ttu-id="7698b-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7698b-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7698b-107">`put_Invert`Метод указывает, выполняется ли обратная операция с ключом.</span><span class="sxs-lookup"><span data-stu-id="7698b-107">The `put_Invert` method specifies whether the key operation is inverted.</span></span> <span data-ttu-id="7698b-108">Это свойство применяется ко всем типам ключей, за исключением ДКСТКЭЙ \_ Alpha.</span><span class="sxs-lookup"><span data-stu-id="7698b-108">This property applies to all key types except DXTKEY\_ALPHA.</span></span>

## <a name="syntax"></a><span data-ttu-id="7698b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7698b-109">Syntax</span></span>


```C++
HRESULT put_Invert(
  [in] BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="7698b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7698b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7698b-111">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7698b-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7698b-112">Задает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="7698b-112">Specifies a Boolean value.</span></span> <span data-ttu-id="7698b-113">**Значение true** показывает, что Пиксели в перевернутом изображении инвертированы по отношению к операции по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7698b-113">If **TRUE**, pixels in the overlying image are inverted with respect to the default operation.</span></span> <span data-ttu-id="7698b-114">Если **значение равно false**, Пиксели в изображении с чрезмерной назначением становятся прозрачными по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7698b-114">If **FALSE**, pixels in the overlying image are made transparent in the default manner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7698b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7698b-115">Return value</span></span>

<span data-ttu-id="7698b-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7698b-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7698b-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7698b-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7698b-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7698b-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7698b-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="7698b-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7698b-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7698b-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7698b-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="7698b-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7698b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="7698b-122">Requirements</span></span>



| <span data-ttu-id="7698b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="7698b-123">Requirement</span></span> | <span data-ttu-id="7698b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7698b-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7698b-125">Header</span><span class="sxs-lookup"><span data-stu-id="7698b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7698b-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="7698b-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7698b-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7698b-127">Library</span></span><br/> | <dl> <span data-ttu-id="7698b-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7698b-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7698b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7698b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7698b-130">**Интерфейс Идксткэй**</span><span class="sxs-lookup"><span data-stu-id="7698b-130">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="7698b-131">**Идксткэй::p UT \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="7698b-131">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




