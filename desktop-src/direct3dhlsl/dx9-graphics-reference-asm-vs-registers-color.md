---
title: Регистр цвета
description: Эти регистры выходных данных шейдера вершин содержат значение цвета.
ms.assetid: fd36e207-7312-4c7e-b664-b2de9ba1ebcf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38ee29ebafd9e7374fa868c6d84ad45f6c07dedf
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "104350872"
---
# <a name="color-register"></a><span data-ttu-id="e3c00-103">Регистр цвета</span><span class="sxs-lookup"><span data-stu-id="e3c00-103">Color Register</span></span>

<span data-ttu-id="e3c00-104">Эти регистры выходных данных шейдера вершин содержат значение цвета.</span><span class="sxs-lookup"><span data-stu-id="e3c00-104">These vertex shader output registers contain a color value.</span></span> 

| <span data-ttu-id="e3c00-105">Регистрация</span><span class="sxs-lookup"><span data-stu-id="e3c00-105">Register</span></span> | <span data-ttu-id="e3c00-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e3c00-106">Description</span></span>              |
|----------|--------------------------|
| <span data-ttu-id="e3c00-107">oD0</span><span class="sxs-lookup"><span data-stu-id="e3c00-107">oD0</span></span>      | <span data-ttu-id="e3c00-108">Регистр цветов диффузии.</span><span class="sxs-lookup"><span data-stu-id="e3c00-108">diffuse color register.</span></span>  |
| <span data-ttu-id="e3c00-109">oD1</span><span class="sxs-lookup"><span data-stu-id="e3c00-109">oD1</span></span>      | <span data-ttu-id="e3c00-110">Регистр отраженного цвета.</span><span class="sxs-lookup"><span data-stu-id="e3c00-110">specular color register.</span></span> |



 

<span data-ttu-id="e3c00-111">Значение oD0 интерполяции и записывается в цветовую область шейдера пикселей 0 (v0).</span><span class="sxs-lookup"><span data-stu-id="e3c00-111">The oD0 value is interpolated and is written to the pixel shader color register 0 (v0).</span></span> <span data-ttu-id="e3c00-112">Значение oD1 интерполяции и записывается в цветовой реестр построителя текстуры 1 (v1).</span><span class="sxs-lookup"><span data-stu-id="e3c00-112">The oD1 value is interpolated and written to the pixel shader color register 1 (v1).</span></span> <span data-ttu-id="e3c00-113">Дополнительные сведения о цветовых регистрах шейдера пикселей см. в разделе [регистр цветов ввода](dx9-graphics-reference-asm-ps-registers-input-color.md) построителя текстуры.</span><span class="sxs-lookup"><span data-stu-id="e3c00-113">For more information about pixel shader color registers, see the pixel shader [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3c00-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="e3c00-114">Remarks</span></span>

<span data-ttu-id="e3c00-115">Пример</span><span class="sxs-lookup"><span data-stu-id="e3c00-115">Example</span></span>


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a><span data-ttu-id="e3c00-116">См. также</span><span class="sxs-lookup"><span data-stu-id="e3c00-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3c00-117">Регистры шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="e3c00-117">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




