---
description: Считывает значение шаг текселя и возвращает результат в асинчрнаусли узла.
MS-HAID: vspixengine.IPixEngine5\_ReadTexelValueAsync\_UINT\_PixEngineTextureSliceIndex\_int\_int\_int\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine5:: Реадтекселвалуеасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 28C44D12-383D-4E91-8BB1-12869782533C
api_name:
- IPixEngine5.ReadTexelValueAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ca3510b01038df3b07b3033364902f76f2e05b4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701149"
---
# <a name="span-idvspixengineipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dwordspanipixengine5readtexelvalueasync-method"></a><span data-ttu-id="c0d08-103"><span id="vspixengine.ipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dword"></span>Метод IPixEngine5:: Реадтекселвалуеасинк</span><span class="sxs-lookup"><span data-stu-id="c0d08-103"><span id="vspixengine.ipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::ReadTexelValueAsync method</span></span>

<span data-ttu-id="c0d08-104">Считывает значение шаг текселя и возвращает результат в асинчрнаусли узла.</span><span class="sxs-lookup"><span data-stu-id="c0d08-104">Reads a texel value and returns the result to the host asynchrnously.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0d08-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0d08-105">Syntax</span></span>


```C++
HRESULT ReadTexelValueAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        x,
   int                        y,
   int                        formatOverride,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="c0d08-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0d08-106">Parameters</span></span>

<span data-ttu-id="c0d08-107">*текстуреид* </span><span class="sxs-lookup"><span data-stu-id="c0d08-107">*textureId* </span></span>  
<span data-ttu-id="c0d08-108">Идентификатор текстуры, из которой считывается значение шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="c0d08-108">The ID of the texture to read the texel value from.</span></span>

<span data-ttu-id="c0d08-109">*слицеиндекс* </span><span class="sxs-lookup"><span data-stu-id="c0d08-109">*sliceIndex* </span></span>  
<span data-ttu-id="c0d08-110">Индекс среза в текстуре, из которого считывается значение шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="c0d08-110">The index of the slice within the texture to read the texel value from.</span></span>

<span data-ttu-id="c0d08-111">*x* </span><span class="sxs-lookup"><span data-stu-id="c0d08-111">*x* </span></span>  
<span data-ttu-id="c0d08-112">Координата x шаг текселя для чтения.</span><span class="sxs-lookup"><span data-stu-id="c0d08-112">The x texel coordinate to read.</span></span>

<span data-ttu-id="c0d08-113">*&* </span><span class="sxs-lookup"><span data-stu-id="c0d08-113">*y* </span></span>  
<span data-ttu-id="c0d08-114">Координата y шаг текселя для чтения.</span><span class="sxs-lookup"><span data-stu-id="c0d08-114">The y texel coordinate to read.</span></span>

<span data-ttu-id="c0d08-115">*форматоверриде* </span><span class="sxs-lookup"><span data-stu-id="c0d08-115">*formatOverride* </span></span>  
<span data-ttu-id="c0d08-116">Переопределение формата цвета.</span><span class="sxs-lookup"><span data-stu-id="c0d08-116">The color format override.</span></span>

<span data-ttu-id="c0d08-117">*обратные вызовы* </span><span class="sxs-lookup"><span data-stu-id="c0d08-117">*callbacks* </span></span>  
<span data-ttu-id="c0d08-118">Адрес объекта, который предоставляет интерфейс обратных вызовов IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="c0d08-118">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="c0d08-119">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="c0d08-119">*requestCookie* </span></span>  
<span data-ttu-id="c0d08-120">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="c0d08-120">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="c0d08-121">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="c0d08-121">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="c0d08-122">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c0d08-122">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="c0d08-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0d08-123">Return value</span></span>

<span data-ttu-id="c0d08-124">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c0d08-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c0d08-125">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c0d08-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0d08-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c0d08-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c0d08-127">Header</span><span class="sxs-lookup"><span data-stu-id="c0d08-127">Header</span></span></p></td><td><span data-ttu-id="c0d08-128">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="c0d08-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c0d08-129"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="c0d08-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c0d08-130">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="c0d08-130">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
