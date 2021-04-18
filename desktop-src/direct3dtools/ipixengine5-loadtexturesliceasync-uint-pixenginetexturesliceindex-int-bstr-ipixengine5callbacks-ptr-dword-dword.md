---
description: Загружает срез текстуры и уведомляет асинчрнаусли узла о завершении.
MS-HAID: vspixengine.IPixEngine5\_LoadTextureSliceAsync\_UINT\_PixEngineTextureSliceIndex\_int\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine5:: Лоадтекстуреслицеасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 520DBB6D-D8F3-451F-942C-BE8428B9ADFF
api_name:
- IPixEngine5.LoadTextureSliceAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 505ccfd6668cbe08b4f62878b5f51e9c20185b41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701129"
---
# <a name="span-idvspixengineipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadtexturesliceasync-method"></a><span data-ttu-id="5e9cf-103"><span id="vspixengine.ipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Метод IPixEngine5:: Лоадтекстуреслицеасинк</span><span class="sxs-lookup"><span data-stu-id="5e9cf-103"><span id="vspixengine.ipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadTextureSliceAsync method</span></span>

<span data-ttu-id="5e9cf-104">Загружает срез текстуры и уведомляет асинчрнаусли узла о завершении.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-104">Loads a texture slice and notifies the host asynchrnously when it completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e9cf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e9cf-105">Syntax</span></span>


```C++
HRESULT LoadTextureSliceAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="5e9cf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e9cf-106">Parameters</span></span>

<span data-ttu-id="5e9cf-107">*текстуреид* </span><span class="sxs-lookup"><span data-stu-id="5e9cf-107">*textureId* </span></span>  
<span data-ttu-id="5e9cf-108">Идентификатор текстуры, для которой загружается срез.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-108">The ID of the texture to load the slice for.</span></span>

<span data-ttu-id="5e9cf-109">*слицеиндекс* </span><span class="sxs-lookup"><span data-stu-id="5e9cf-109">*sliceIndex* </span></span>  
<span data-ttu-id="5e9cf-110">Индекс загружаемого среза.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-110">The index of the slice to load.</span></span>

<span data-ttu-id="5e9cf-111">*форматоверриде* </span><span class="sxs-lookup"><span data-stu-id="5e9cf-111">*formatOverride* </span></span>  
<span data-ttu-id="5e9cf-112">Задает переопределение формата.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-112">Specifies the format override.</span></span>

<span data-ttu-id="5e9cf-113">*хистограмдатафиленаме* </span><span class="sxs-lookup"><span data-stu-id="5e9cf-113">*histogramDataFileName* </span></span>  
<span data-ttu-id="5e9cf-114">Строка COM, содержащая имя файла данных гистограммы, связанного с срезом текстуры.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-114">A COM string containing the name of the histogram data file associated with the texture slice.</span></span>

<span data-ttu-id="5e9cf-115">*обратные вызовы* </span><span class="sxs-lookup"><span data-stu-id="5e9cf-115">*callbacks* </span></span>  
<span data-ttu-id="5e9cf-116">Адрес объекта, который предоставляет интерфейс обратных вызовов IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-116">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="5e9cf-117">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="5e9cf-117">*requestCookie* </span></span>  
<span data-ttu-id="5e9cf-118">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="5e9cf-119">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="5e9cf-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="5e9cf-120">Не используется.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e9cf-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e9cf-121">Return value</span></span>

<span data-ttu-id="5e9cf-122">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5e9cf-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5e9cf-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e9cf-124">Требования</span><span class="sxs-lookup"><span data-stu-id="5e9cf-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5e9cf-125">Header</span><span class="sxs-lookup"><span data-stu-id="5e9cf-125">Header</span></span></p></td><td><span data-ttu-id="5e9cf-126">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="5e9cf-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5e9cf-127"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="5e9cf-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5e9cf-128">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="5e9cf-128">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
