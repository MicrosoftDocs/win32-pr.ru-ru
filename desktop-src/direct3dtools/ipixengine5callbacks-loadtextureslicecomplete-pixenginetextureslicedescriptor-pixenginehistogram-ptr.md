---
description: Функция обратного вызова, используемая для уведомления узла о завершении загрузки среза текстуры.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureSliceComplete\_PixEngineTextureSliceDescriptor\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine5Callbacks:: Лоадтекстуреслицекомплете'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CEEAB77F-0856-4DEC-991A-7CEB921C84BB
api_name:
- IPixEngine5Callbacks.LoadTextureSliceComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 674288841ea08ad38c519e88abac4c64a1f1ca7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495549"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptrspanipixengine5callbacksloadtextureslicecomplete-method"></a><span data-ttu-id="8af4c-103"><span id="vspixengine.ipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptr"></span>Метод IPixEngine5Callbacks:: Лоадтекстуреслицекомплете</span><span class="sxs-lookup"><span data-stu-id="8af4c-103"><span id="vspixengine.ipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadTextureSliceComplete method</span></span>

<span data-ttu-id="8af4c-104">Функция обратного вызова, используемая для уведомления узла о завершении загрузки среза текстуры.</span><span class="sxs-lookup"><span data-stu-id="8af4c-104">A callback function used to notify the host when a texture slice load has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8af4c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8af4c-105">Syntax</span></span>


```C++
HRESULT LoadTextureSliceComplete(
   PixEngineTextureSliceDescriptor sliceDesc,
   PixEngineHistogram*             histogram
);
```

## <a name="parameters"></a><span data-ttu-id="8af4c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8af4c-106">Parameters</span></span>

<span data-ttu-id="8af4c-107">*слицедеск* </span><span class="sxs-lookup"><span data-stu-id="8af4c-107">*sliceDesc* </span></span>  
<span data-ttu-id="8af4c-108">Дескриптор загруженного среза.</span><span class="sxs-lookup"><span data-stu-id="8af4c-108">A descriptor of the loaded slice.</span></span>

<span data-ttu-id="8af4c-109">*отображения* </span><span class="sxs-lookup"><span data-stu-id="8af4c-109">*histogram* </span></span>  
<span data-ttu-id="8af4c-110">Адрес данных гистограммы загруженного среза.</span><span class="sxs-lookup"><span data-stu-id="8af4c-110">The address of histogram data for the loaded slice.</span></span>

## <a name="return-value"></a><span data-ttu-id="8af4c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8af4c-111">Return value</span></span>

<span data-ttu-id="8af4c-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8af4c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8af4c-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8af4c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8af4c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8af4c-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8af4c-115">Header</span><span class="sxs-lookup"><span data-stu-id="8af4c-115">Header</span></span></p></td><td><span data-ttu-id="8af4c-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="8af4c-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="8af4c-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="8af4c-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="8af4c-118">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="8af4c-118">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
