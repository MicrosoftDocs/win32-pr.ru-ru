---
description: Расширения интерфейса IPixEngine4, содержащие дополнения для просмотра текстур.
MS-HAID: vspixengine.IPixEngine5
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс IPixEngine5
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8995B617-6830-4A07-8C83-B5925E033967
api_name:
- IPixEngine5
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 300ed31eae5d8ff4009f28691c5348db7cd89d6e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537190"
---
# <a name="span-idvspixengineipixengine5spanipixengine5-interface"></a><span data-ttu-id="830f8-103"><span id="vspixengine.ipixengine5"></span>Интерфейс IPixEngine5</span><span class="sxs-lookup"><span data-stu-id="830f8-103"><span id="vspixengine.ipixengine5"></span>IPixEngine5 interface</span></span>

<span data-ttu-id="830f8-104">Расширения интерфейса IPixEngine4, содержащие дополнения для просмотра текстур.</span><span class="sxs-lookup"><span data-stu-id="830f8-104">Extensions to the IPixEngine4 interface containing additions for viewing textures.</span></span>

## <a name="members"></a><span data-ttu-id="830f8-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="830f8-105">Members</span></span>

<span data-ttu-id="830f8-106">Интерфейс **IPixEngine5** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="830f8-106">The **IPixEngine5** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="830f8-107">**IPixEngine5** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="830f8-107">**IPixEngine5** also has these types of members:</span></span>

-   [<span data-ttu-id="830f8-108">Методы</span><span class="sxs-lookup"><span data-stu-id="830f8-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="830f8-109"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="830f8-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="830f8-110">Интерфейс **IPixEngine5** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="830f8-110">The **IPixEngine5** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="830f8-111">Метод</span><span class="sxs-lookup"><span data-stu-id="830f8-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="830f8-112">Описание</span><span class="sxs-lookup"><span data-stu-id="830f8-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="830f8-113"><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>фритекстуреасинк</strong></a></span><span class="sxs-lookup"><span data-stu-id="830f8-113"><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>FreeTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="830f8-114">Освобождает текстуру и уведомляет узел асинхронно.</span><span class="sxs-lookup"><span data-stu-id="830f8-114">Frees a texture and notifies the host asynchronously.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="830f8-115"><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>лоадхистограмасинк</strong></a></span><span class="sxs-lookup"><span data-stu-id="830f8-115"><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadHistogramAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="830f8-116">Асинхронный запрос на загрузку данных гистограммы.</span><span class="sxs-lookup"><span data-stu-id="830f8-116">An asynchronous request to load histogram data.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="830f8-117"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>лоадтекстурефромфилеасинк</strong></a></span><span class="sxs-lookup"><span data-stu-id="830f8-117"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureFromFileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="830f8-118">Загружает текстуру из файла и уведомляет узел асинхронно по завершении.</span><span class="sxs-lookup"><span data-stu-id="830f8-118">Loads a texture from a file and notifies the host asynchronously when it completes.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="830f8-119"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>лоадтекстуреслицеасинк</strong></a></span><span class="sxs-lookup"><span data-stu-id="830f8-119"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureSliceAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="830f8-120">Загружает срез текстуры и уведомляет асинчрнаусли узла о завершении.</span><span class="sxs-lookup"><span data-stu-id="830f8-120">Loads a texture slice and notifies the host asynchrnously when it completes.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="830f8-121"><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>реадтекселвалуеасинк</strong></a></span><span class="sxs-lookup"><span data-stu-id="830f8-121"><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>ReadTexelValueAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="830f8-122">Считывает значение шаг текселя и возвращает результат в асинчрнаусли узла.</span><span class="sxs-lookup"><span data-stu-id="830f8-122">Reads a texel value and returns the result to the host asynchrnously.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="830f8-123"><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>рендертекстуреасинк</strong></a></span><span class="sxs-lookup"><span data-stu-id="830f8-123"><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>RenderTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="830f8-124">Визуализирует текстуру в файл и возвращает результат в асинчрнаусли узла.</span><span class="sxs-lookup"><span data-stu-id="830f8-124">Renders a texture to a file and returns the result to the host asynchrnously.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="830f8-125"><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>саветекстуреасинк</strong></a></span><span class="sxs-lookup"><span data-stu-id="830f8-125"><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>SaveTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="830f8-126">Сохраняет текстуру.</span><span class="sxs-lookup"><span data-stu-id="830f8-126">Saves a texture.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="830f8-127">Требования</span><span class="sxs-lookup"><span data-stu-id="830f8-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="830f8-128">Header</span><span class="sxs-lookup"><span data-stu-id="830f8-128">Header</span></span></p></td><td><span data-ttu-id="830f8-129">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="830f8-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
