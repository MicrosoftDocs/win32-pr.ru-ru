---
description: Функция обратного вызова, используемая для уведомления узла о завершении загрузки текстуры.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureFromFileComplete\_UINT\_PixEngineTextureDescriptor\_UINT\_PixEngineTextureSliceIndex\_arr\_PixEngineTextureSliceDescriptor\_arr\_UINT\_int\_arr\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine5Callbacks:: Лоадтекстурефромфилекомплете'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7fb4c38b733a7e85a237260404b5b253e3eb88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105691988"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptrspanipixengine5callbacksloadtexturefromfilecomplete-method"></a><span data-ttu-id="48213-103"><span id="vspixengine.ipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptr"></span>Метод IPixEngine5Callbacks:: Лоадтекстурефромфилекомплете</span><span class="sxs-lookup"><span data-stu-id="48213-103"><span id="vspixengine.ipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadTextureFromFileComplete method</span></span>

<span data-ttu-id="48213-104">Функция обратного вызова, используемая для уведомления узла о завершении загрузки текстуры.</span><span class="sxs-lookup"><span data-stu-id="48213-104">A callback function used to notify the host when a texture load has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="48213-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48213-105">Syntax</span></span>


```C++
HRESULT LoadTextureFromFileComplete(
   UINT                               textureId,
   PixEngineTextureDescriptor         textureDesc,
   UINT                               numSlices,
   PixEngineTextureSliceIndex []      count2_sliceIndicies,
   PixEngineTextureSliceDescriptor [] count2_sliceDescriptors,
   UINT                               numFormatOverrides,
   int []                             count5_formatOverrides,
   PixEngineHistogram*                histogram
);
```

## <a name="parameters"></a><span data-ttu-id="48213-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="48213-106">Parameters</span></span>

<span data-ttu-id="48213-107">*текстуреид* </span><span class="sxs-lookup"><span data-stu-id="48213-107">*textureId* </span></span>  
<span data-ttu-id="48213-108">Идентификатор загруженной текстуры.</span><span class="sxs-lookup"><span data-stu-id="48213-108">The ID of the loaded texture.</span></span>

<span data-ttu-id="48213-109">*текстуредеск* </span><span class="sxs-lookup"><span data-stu-id="48213-109">*textureDesc* </span></span>  
<span data-ttu-id="48213-110">Дескриптор текстуры загруженной текстуры.</span><span class="sxs-lookup"><span data-stu-id="48213-110">The texture descriptor of the loaded texture.</span></span>

<span data-ttu-id="48213-111">*нумслицес* </span><span class="sxs-lookup"><span data-stu-id="48213-111">*numSlices* </span></span>  
<span data-ttu-id="48213-112">Число срезов, которые имеет текстура.</span><span class="sxs-lookup"><span data-stu-id="48213-112">The number of slices the texture has.</span></span>

<span data-ttu-id="48213-113">*count2 \_ слицеиндиЦиес* </span><span class="sxs-lookup"><span data-stu-id="48213-113">*count2\_sliceIndicies* </span></span>  
<span data-ttu-id="48213-114">Срез индиЦиес, связанный с текстурой.</span><span class="sxs-lookup"><span data-stu-id="48213-114">Slice indicies associated with the texture.</span></span>

<span data-ttu-id="48213-115">*count2 \_ слицедескрипторс* </span><span class="sxs-lookup"><span data-stu-id="48213-115">*count2\_sliceDescriptors* </span></span>  
<span data-ttu-id="48213-116">Дескрипторы для каждого среза.</span><span class="sxs-lookup"><span data-stu-id="48213-116">Descriptors for each slice.</span></span>

<span data-ttu-id="48213-117">*нумформатоверридес* </span><span class="sxs-lookup"><span data-stu-id="48213-117">*numFormatOverrides* </span></span>  
<span data-ttu-id="48213-118">Число переопределений формата.</span><span class="sxs-lookup"><span data-stu-id="48213-118">The number of format overrides.</span></span>

<span data-ttu-id="48213-119">*count5 \_ форматоверридес* </span><span class="sxs-lookup"><span data-stu-id="48213-119">*count5\_formatOverrides* </span></span>  
<span data-ttu-id="48213-120">Формат переопределяет.</span><span class="sxs-lookup"><span data-stu-id="48213-120">The format overrides.</span></span>

<span data-ttu-id="48213-121">*отображения* </span><span class="sxs-lookup"><span data-stu-id="48213-121">*histogram* </span></span>  
<span data-ttu-id="48213-122">Адрес данных гистограммы загруженной текстуры.</span><span class="sxs-lookup"><span data-stu-id="48213-122">The address of histogram data for the loaded texture.</span></span>

## <a name="return-value"></a><span data-ttu-id="48213-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48213-123">Return value</span></span>

<span data-ttu-id="48213-124">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="48213-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="48213-125">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="48213-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="48213-126">Требования</span><span class="sxs-lookup"><span data-stu-id="48213-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="48213-127">Header</span><span class="sxs-lookup"><span data-stu-id="48213-127">Header</span></span></p></td><td><span data-ttu-id="48213-128">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="48213-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="48213-129"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="48213-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="48213-130">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="48213-130">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
