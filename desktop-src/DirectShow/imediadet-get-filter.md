---
description: Метод получения \_ фильтра получает указатель на фильтр источника, который сейчас используется средством обнаружения мультимедиа.
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: 'Метод Имедиадет:: get_Filter (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f80b5d5021ca7f04cd56dc319fb5416c3361108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679712"
---
# <a name="imediadetget_filter-method"></a><span data-ttu-id="88dbf-103">Метод фильтра Имедиадет:: Get \_</span><span class="sxs-lookup"><span data-stu-id="88dbf-103">IMediaDet::get\_Filter method</span></span>

> [!Note]  
> <span data-ttu-id="88dbf-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="88dbf-104">\[Deprecated.</span></span> <span data-ttu-id="88dbf-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="88dbf-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="88dbf-106">`get_Filter`Метод получает указатель на фильтр источника, который сейчас используется средством обнаружения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="88dbf-106">The `get_Filter` method retrieves a pointer to the source filter currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="88dbf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88dbf-107">Syntax</span></span>


```C++
HRESULT get_Filter(
  [out, retval] IUnknown **ppVal
);
```



## <a name="parameters"></a><span data-ttu-id="88dbf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="88dbf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88dbf-109">*ппвал* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="88dbf-109">*ppVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="88dbf-110">Получает указатель на интерфейс **IUnknown** фильтра.</span><span class="sxs-lookup"><span data-stu-id="88dbf-110">Receives a pointer to the filter's **IUnknown** interface.</span></span> <span data-ttu-id="88dbf-111">Если фильтр источника не используется, устанавливается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="88dbf-111">If no source filter is in use, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88dbf-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88dbf-112">Return value</span></span>

<span data-ttu-id="88dbf-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="88dbf-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88dbf-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88dbf-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="88dbf-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88dbf-115">Remarks</span></span>

<span data-ttu-id="88dbf-116">Если метод возвращает значение, если *\* ппвал* не равен **null**, то интерфейс **IUnknown** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="88dbf-116">When the method returns, if *\*ppVal* is not **NULL**, the **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="88dbf-117">Освободите интерфейс по окончании его использования.</span><span class="sxs-lookup"><span data-stu-id="88dbf-117">Release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="88dbf-118">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="88dbf-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="88dbf-119">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="88dbf-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="88dbf-120">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="88dbf-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="88dbf-121">Требования</span><span class="sxs-lookup"><span data-stu-id="88dbf-121">Requirements</span></span>



| <span data-ttu-id="88dbf-122">Требование</span><span class="sxs-lookup"><span data-stu-id="88dbf-122">Requirement</span></span> | <span data-ttu-id="88dbf-123">Значение</span><span class="sxs-lookup"><span data-stu-id="88dbf-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88dbf-124">Header</span><span class="sxs-lookup"><span data-stu-id="88dbf-124">Header</span></span><br/>  | <dl> <span data-ttu-id="88dbf-125"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="88dbf-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="88dbf-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="88dbf-126">Library</span></span><br/> | <dl> <span data-ttu-id="88dbf-127"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88dbf-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88dbf-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88dbf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88dbf-129">**Интерфейс Имедиадет**</span><span class="sxs-lookup"><span data-stu-id="88dbf-129">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="88dbf-130">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="88dbf-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




