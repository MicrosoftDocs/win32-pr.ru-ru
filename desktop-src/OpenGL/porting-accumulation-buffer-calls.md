---
title: Вызовы буфера накопления при переносе
description: Необходимо выделить буфер накопления, запросив соответствующий формат пикселей с помощью функции OpenGL Ауксинитдисплаймоде или Чусепикселформат.
ms.assetid: 523728ce-4aae-4247-a3dc-23864231cad1
keywords:
- Перенос GL в ГК, буферы накопления
- Перенос из IRI GL, буферы накопления
- перенос в OpenGL из IRI GL, буферы накопления
- Перенос по стандарту OpenGL из IRI GL, буферы накопления
- накопление буферов OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca91cb3ba35535ba2470297070dffc932a1c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104259067"
---
# <a name="porting-accumulation-buffer-calls"></a><span data-ttu-id="e6399-108">Вызовы буфера накопления при переносе</span><span class="sxs-lookup"><span data-stu-id="e6399-108">Porting Accumulation Buffer Calls</span></span>

<span data-ttu-id="e6399-109">Необходимо выделить буфер накопления, запросив соответствующий формат пикселей с помощью функции OpenGL **ауксинитдисплаймоде** или [**чусепикселформат**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) .</span><span class="sxs-lookup"><span data-stu-id="e6399-109">You must allocate your accumulation buffer by requesting the appropriate pixel format with the OpenGL **auxInitDisplayMode** or [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) function.</span></span> <span data-ttu-id="e6399-110">В следующей таблице перечислены функции IRI GL, влияющие на буфер накопления и их эквивалентные функции OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e6399-110">The following table lists IRIS GL functions that affect the accumulation buffer and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="e6399-111">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="e6399-111">IRIS GL function</span></span>       | <span data-ttu-id="e6399-112">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="e6399-112">OpenGL function</span></span>                                       | <span data-ttu-id="e6399-113">Значение</span><span class="sxs-lookup"><span data-stu-id="e6399-113">Meaning</span></span>                                                                       |
|------------------------|-------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="e6399-114">**аксизе**</span><span class="sxs-lookup"><span data-stu-id="e6399-114">**acsize**</span></span>             | <span data-ttu-id="e6399-115">**ауксинитдисплаймоде** или **чусепикселформат**</span><span class="sxs-lookup"><span data-stu-id="e6399-115">**auxInitDisplayMode** or **ChoosePixelFormat**</span></span>       | <span data-ttu-id="e6399-116">Указывает число битпланес на каждый компонент цвета в буфере накопления.</span><span class="sxs-lookup"><span data-stu-id="e6399-116">Specifies number of bitplanes per color component in the accumulation buffer.</span></span> |
| <span data-ttu-id="e6399-117">**акбуф**</span><span class="sxs-lookup"><span data-stu-id="e6399-117">**acbuf**</span></span>              | [<span data-ttu-id="e6399-118">**глаккум**</span><span class="sxs-lookup"><span data-stu-id="e6399-118">**glAccum**</span></span>](glaccum.md)                            | <span data-ttu-id="e6399-119">Работает с буфером накопления.</span><span class="sxs-lookup"><span data-stu-id="e6399-119">Operates on the accumulation buffer.</span></span>                                          |
|                        | [<span data-ttu-id="e6399-120">**глклеараккум**</span><span class="sxs-lookup"><span data-stu-id="e6399-120">**glClearAccum**</span></span>](glclearaccum.md)                  | <span data-ttu-id="e6399-121">Задает сброс значений для буфера накопления.</span><span class="sxs-lookup"><span data-stu-id="e6399-121">Sets clear values for accumulation buffer.</span></span>                                    |
| <span data-ttu-id="e6399-122">**акбуф**(AC \_ clear)</span><span class="sxs-lookup"><span data-stu-id="e6399-122">**acbuf**( AC\_CLEAR )</span></span> | <span data-ttu-id="e6399-123">[**глклеар**](glclear.md) ( \_ бит накопленного \_ буфера GL \_ )</span><span class="sxs-lookup"><span data-stu-id="e6399-123">[**glClear**](glclear.md) ( GL\_ACCUM\_BUFFER\_BIT )</span></span> | <span data-ttu-id="e6399-124">Очищает буфер накопления.</span><span class="sxs-lookup"><span data-stu-id="e6399-124">Clears the accumulation buffer.</span></span>                                               |



 

<span data-ttu-id="e6399-125">В следующей таблице перечислены параметры **АКБУФ** GL, а также эквивалентные параметры [**Глаккум**](glaccum.md) OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e6399-125">The following table lists the IRIS GL **acbuf** parameters along with the equivalent OpenGL [**glAccum**](glaccum.md) parameters.</span></span>



| <span data-ttu-id="e6399-126">Параметр IRI GL</span><span class="sxs-lookup"><span data-stu-id="e6399-126">IRIS GL parameter</span></span>     | <span data-ttu-id="e6399-127">Параметр OpenGL</span><span class="sxs-lookup"><span data-stu-id="e6399-127">OpenGL parameter</span></span> |
|-----------------------|------------------|
| <span data-ttu-id="e6399-128">\_накопленный ток</span><span class="sxs-lookup"><span data-stu-id="e6399-128">AC\_ACCUMULATE</span></span>        | <span data-ttu-id="e6399-129">\_накопленный счет ГК</span><span class="sxs-lookup"><span data-stu-id="e6399-129">GL\_ACCUM</span></span>        |
| <span data-ttu-id="e6399-130">Очистка блока AC \_ \_</span><span class="sxs-lookup"><span data-stu-id="e6399-130">AC\_CLEAR\_ACCUMULATE</span></span> | <span data-ttu-id="e6399-131">\_Загрузка GL</span><span class="sxs-lookup"><span data-stu-id="e6399-131">GL\_LOAD</span></span>         |
| <span data-ttu-id="e6399-132">\_Возврат AC</span><span class="sxs-lookup"><span data-stu-id="e6399-132">AC\_RETURN</span></span>            | <span data-ttu-id="e6399-133">\_Возврат GL</span><span class="sxs-lookup"><span data-stu-id="e6399-133">GL\_RETURN</span></span>       |
| <span data-ttu-id="e6399-134">AC \_ mult</span><span class="sxs-lookup"><span data-stu-id="e6399-134">AC\_MULT</span></span>              | <span data-ttu-id="e6399-135">\_mult GL</span><span class="sxs-lookup"><span data-stu-id="e6399-135">GL\_MULT</span></span>         |
| <span data-ttu-id="e6399-136">\_Добавление AC</span><span class="sxs-lookup"><span data-stu-id="e6399-136">AC\_ADD</span></span>               | <span data-ttu-id="e6399-137">Добавление в ГК \_</span><span class="sxs-lookup"><span data-stu-id="e6399-137">GL\_ADD</span></span>          |



 

 

 




