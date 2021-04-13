---
title: Перенос моделей заливки
description: Как и IRI GL, OpenGL позволяет переключаться между плавной заливкой (Гуро) и плоской заливкой. В следующей таблице перечислены функции заливки и сглаживания в ГК, а также их эквивалентные функции OpenGL.
ms.assetid: 93e8f437-381f-4620-ad6f-52ce830d99b6
keywords:
- Перенос GL по IRI, заливка
- Перенос из ДИАФРАГМы в ГК, заливка
- перенос в OpenGL из IRI GL, заливка
- Перенос по стандарту OpenGL из IRI GL, заливка
- Плавная Заливка
- Заливка по методу Гуро
- Плоская заливка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124bb002f6f133b4d47dd40e1a0e8738c512ce99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331003"
---
# <a name="porting-shading-models"></a><span data-ttu-id="19569-111">Перенос моделей заливки</span><span class="sxs-lookup"><span data-stu-id="19569-111">Porting Shading Models</span></span>

<span data-ttu-id="19569-112">Как и IRI GL, OpenGL позволяет переключаться между плавной заливкой (Гуро) и плоской заливкой.</span><span class="sxs-lookup"><span data-stu-id="19569-112">Like IRIS GL, OpenGL lets you switch between smooth (Gouraud) shading and flat shading.</span></span> <span data-ttu-id="19569-113">В следующей таблице перечислены функции заливки и сглаживания в ГК, а также их эквивалентные функции OpenGL.</span><span class="sxs-lookup"><span data-stu-id="19569-113">The following table lists the IRIS GL shading and dithering functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="19569-114">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="19569-114">IRIS GL function</span></span>                                   | <span data-ttu-id="19569-115">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="19569-115">OpenGL function</span></span>                                                                                    | <span data-ttu-id="19569-116">Значение</span><span class="sxs-lookup"><span data-stu-id="19569-116">Meaning</span></span>                      |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="19569-117">**шадемодел**(плоский)</span><span class="sxs-lookup"><span data-stu-id="19569-117">**shademodel**(FLAT)</span></span>                               | <span data-ttu-id="19569-118">[**глшадемодел**](glshademodel.md) ( \_ Flat GL)</span><span class="sxs-lookup"><span data-stu-id="19569-118">[**glShadeModel**](glshademodel.md) ( GL\_FLAT )</span></span>                                                  | <span data-ttu-id="19569-119">Выполняет плоскую заливку.</span><span class="sxs-lookup"><span data-stu-id="19569-119">Does flat shading.</span></span>           |
| <span data-ttu-id="19569-120">**шадемодел**(метод Гуро)</span><span class="sxs-lookup"><span data-stu-id="19569-120">**shademodel**(GOURAUD)</span></span>                            | <span data-ttu-id="19569-121">**глшадемодел**( \_ Smooth GL)</span><span class="sxs-lookup"><span data-stu-id="19569-121">**glShadeModel**( GL\_SMOOTH )</span></span>                                                                     | <span data-ttu-id="19569-122">Плавное затенение.</span><span class="sxs-lookup"><span data-stu-id="19569-122">Does smooth shading.</span></span>         |
| <span data-ttu-id="19569-123">**жетсм**</span><span class="sxs-lookup"><span data-stu-id="19569-123">**getsm**</span></span>                                          | <span data-ttu-id="19569-124">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ модель шейдера GL \_ )</span><span class="sxs-lookup"><span data-stu-id="19569-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_SHADE\_MODEL )</span></span>      | <span data-ttu-id="19569-125">Возвращает текущую модель затенения.</span><span class="sxs-lookup"><span data-stu-id="19569-125">Returns current shade model.</span></span> |
| <span data-ttu-id="19569-126">**дизеринг (** \_ вкл.) **смешение**(DT \_ Off)</span><span class="sxs-lookup"><span data-stu-id="19569-126">**dither**(DT\_ON) **dither**(DT\_OFF)</span></span> <br/> | <span data-ttu-id="19569-127">[**гленабле**](glenable.md) ( \_ дизеринг GL)[**глдисабле**](gldisable.md)( \_ дизеринг GL)</span><span class="sxs-lookup"><span data-stu-id="19569-127">[**glEnable**](glenable.md) ( GL\_DITHER )[**glDisable**](gldisable.md)( GL\_DITHER )</span></span><br/> | <span data-ttu-id="19569-128">Включает или выключает Дизеринг.</span><span class="sxs-lookup"><span data-stu-id="19569-128">Turns dithering on/off.</span></span>      |



 

<span data-ttu-id="19569-129">??</span><span class="sxs-lookup"><span data-stu-id="19569-129">??</span></span>

 

 





