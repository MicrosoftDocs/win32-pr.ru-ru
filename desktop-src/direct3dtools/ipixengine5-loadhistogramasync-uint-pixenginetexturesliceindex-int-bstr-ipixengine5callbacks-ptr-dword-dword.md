---
description: Асинхронный запрос на загрузку данных гистограммы.
MS-HAID: vspixengine.IPixEngine5\_LoadHistogramAsync\_UINT\_PixEngineTextureSliceIndex\_int\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine5:: Лоадхистограмасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A23CB3E0-B299-40FD-899E-9FE6E9177551
api_name:
- IPixEngine5.LoadHistogramAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7c7128743c2086c0ddc2875c493dac98617986a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701150"
---
# <a name="span-idvspixengineipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadhistogramasync-method"></a><span data-ttu-id="5167f-103"><span id="vspixengine.ipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Метод IPixEngine5:: Лоадхистограмасинк</span><span class="sxs-lookup"><span data-stu-id="5167f-103"><span id="vspixengine.ipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadHistogramAsync method</span></span>

<span data-ttu-id="5167f-104">Асинхронный запрос на загрузку данных гистограммы.</span><span class="sxs-lookup"><span data-stu-id="5167f-104">An asynchronous request to load histogram data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5167f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5167f-105">Syntax</span></span>


```C++
HRESULT LoadHistogramAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="5167f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5167f-106">Parameters</span></span>

<span data-ttu-id="5167f-107">*текстуреид* </span><span class="sxs-lookup"><span data-stu-id="5167f-107">*textureId* </span></span>  
<span data-ttu-id="5167f-108">Идентификатор текстуры, для которой загружаются данные гистограммы.</span><span class="sxs-lookup"><span data-stu-id="5167f-108">The ID of the texture to load histogram data for.</span></span>

<span data-ttu-id="5167f-109">*слицеиндекс* </span><span class="sxs-lookup"><span data-stu-id="5167f-109">*sliceIndex* </span></span>  
<span data-ttu-id="5167f-110">Индекс среза, для которого загружаются данные гистограммы.</span><span class="sxs-lookup"><span data-stu-id="5167f-110">The index of the slice to load histogram data for.</span></span>

<span data-ttu-id="5167f-111">*форматоверриде* </span><span class="sxs-lookup"><span data-stu-id="5167f-111">*formatOverride* </span></span>  
<span data-ttu-id="5167f-112">Задает переопределение формата.</span><span class="sxs-lookup"><span data-stu-id="5167f-112">Specifies the format override.</span></span>

<span data-ttu-id="5167f-113">*хистограмдатафиленаме* </span><span class="sxs-lookup"><span data-stu-id="5167f-113">*histogramDataFileName* </span></span>  
<span data-ttu-id="5167f-114">Строка COM, содержащая имя файла данных гистограммы.</span><span class="sxs-lookup"><span data-stu-id="5167f-114">A COM string containing the name of the histogram data file.</span></span>

<span data-ttu-id="5167f-115">*обратные вызовы* </span><span class="sxs-lookup"><span data-stu-id="5167f-115">*callbacks* </span></span>  
<span data-ttu-id="5167f-116">Адрес объекта, который предоставляет интерфейс обратных вызовов IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="5167f-116">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="5167f-117">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="5167f-117">*requestCookie* </span></span>  
<span data-ttu-id="5167f-118">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="5167f-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="5167f-119">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="5167f-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="5167f-120">Не используется.</span><span class="sxs-lookup"><span data-stu-id="5167f-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="5167f-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5167f-121">Return value</span></span>

<span data-ttu-id="5167f-122">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5167f-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5167f-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5167f-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5167f-124">Требования</span><span class="sxs-lookup"><span data-stu-id="5167f-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5167f-125">Header</span><span class="sxs-lookup"><span data-stu-id="5167f-125">Header</span></span></p></td><td><span data-ttu-id="5167f-126">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="5167f-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5167f-127"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="5167f-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5167f-128">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="5167f-128">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
