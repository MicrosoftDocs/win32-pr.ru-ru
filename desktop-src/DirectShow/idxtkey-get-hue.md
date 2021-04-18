---
description: Метод получения \_ оттенок получает значение оттенка, по которому следует подключаться. Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙный \_ тон.
ms.assetid: d37fedd6-f29f-4f16-821b-c5f8520c4e12
title: 'Метод Идксткэй:: get_Hue (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Hue
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72058076e87f1a8738f3153ee8095eefb4ebce8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675330"
---
# <a name="idxtkeyget_hue-method"></a><span data-ttu-id="c1d59-104">Метод Идксткэй:: Get \_ оттенок</span><span class="sxs-lookup"><span data-stu-id="c1d59-104">IDxtKey::get\_Hue method</span></span>

> [!Note]  
> <span data-ttu-id="c1d59-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="c1d59-105">\[Deprecated.</span></span> <span data-ttu-id="c1d59-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c1d59-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c1d59-107">`get_Hue`Метод получает значение оттенка, по которому следует подключаться.</span><span class="sxs-lookup"><span data-stu-id="c1d59-107">The `get_Hue` method retrieves the hue value on which to key.</span></span> <span data-ttu-id="c1d59-108">Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙный \_ тон.</span><span class="sxs-lookup"><span data-stu-id="c1d59-108">This property applies only when the key type is DXTKEY\_HUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1d59-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1d59-109">Syntax</span></span>


```C++
HRESULT get_Hue(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="c1d59-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1d59-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1d59-111">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c1d59-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d59-112">Получает значение оттенка ключа.</span><span class="sxs-lookup"><span data-stu-id="c1d59-112">Receives the hue value on which to key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1d59-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1d59-113">Return value</span></span>

<span data-ttu-id="c1d59-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c1d59-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c1d59-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c1d59-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1d59-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1d59-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c1d59-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="c1d59-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c1d59-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c1d59-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c1d59-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c1d59-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c1d59-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c1d59-120">Requirements</span></span>



| <span data-ttu-id="c1d59-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c1d59-121">Requirement</span></span> | <span data-ttu-id="c1d59-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c1d59-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d59-123">Header</span><span class="sxs-lookup"><span data-stu-id="c1d59-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c1d59-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1d59-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c1d59-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c1d59-125">Library</span></span><br/> | <dl> <span data-ttu-id="c1d59-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1d59-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1d59-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1d59-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1d59-128">**Интерфейс Идксткэй**</span><span class="sxs-lookup"><span data-stu-id="c1d59-128">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="c1d59-129">**Идксткэй:: Get \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="c1d59-129">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




