---
Description: Значение COLORREF используется для указания цвета RGB.
ms.assetid: b87d3de2-7a13-44ef-8253-c6851a75fa54
title: COLORREF (Виндеф. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 6836cfcc1b18d0b20d5e347fb83206551b27de06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104998882"
---
# <a name="colorref"></a><span data-ttu-id="4727e-103">COLORREF</span><span class="sxs-lookup"><span data-stu-id="4727e-103">COLORREF</span></span>

<span data-ttu-id="4727e-104">Значение COLORREF используется для указания цвета [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="4727e-104">The COLORREF value is used to specify an [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) color.</span></span>


```C++
typedef DWORD COLORREF;
typedef DWORD* LPCOLORREF;
```



## <a name="remarks"></a><span data-ttu-id="4727e-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="4727e-105">Remarks</span></span>

<span data-ttu-id="4727e-106">При указании явного цвета [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) значение **COLORREF** имеет следующую шестнадцатеричную форму:</span><span class="sxs-lookup"><span data-stu-id="4727e-106">When specifying an explicit [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) color, the **COLORREF** value has the following hexadecimal form:</span></span>

`0x00bbggrr`

<span data-ttu-id="4727e-107">Байт нижнего порядка содержит значение для относительной интенсивности красного цвета; второй байт содержит значение для зеленого цвета; третий байт содержит значение синего.</span><span class="sxs-lookup"><span data-stu-id="4727e-107">The low-order byte contains a value for the relative intensity of red; the second byte contains a value for green; and the third byte contains a value for blue.</span></span> <span data-ttu-id="4727e-108">Байт высокого порядка должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="4727e-108">The high-order byte must be zero.</span></span> <span data-ttu-id="4727e-109">Максимальное значение для одного байта — 0xFF.</span><span class="sxs-lookup"><span data-stu-id="4727e-109">The maximum value for a single byte is 0xFF.</span></span>

<span data-ttu-id="4727e-110">Чтобы создать значение цвета **COLORREF** , используйте макрос [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="4727e-110">To create a **COLORREF** color value, use the [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro.</span></span> <span data-ttu-id="4727e-111">Чтобы извлечь отдельные значения для красного, зеленого и синего компонентов значения цвета, используйте макросы [**rvalue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [жетгвалуе](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)и [жетбвалуе](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) соответственно.</span><span class="sxs-lookup"><span data-stu-id="4727e-111">To extract the individual values for the red, green, and blue components of a color value, use the [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue), and [GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) macros, respectively.</span></span>

## <a name="example"></a><span data-ttu-id="4727e-112">Например, .</span><span class="sxs-lookup"><span data-stu-id="4727e-112">Example</span></span>

```cpp
// Color constants.
const COLORREF rgbRed   =  0x000000FF;
const COLORREF rgbGreen =  0x0000FF00;
const COLORREF rgbBlue  =  0x00FF0000;
const COLORREF rgbBlack =  0x00000000;
const COLORREF rgbWhite =  0x00FFFFFF;
```

<span data-ttu-id="4727e-113">Пример из [классической выборки Windows](https://github.com/microsoft/Windows-classic-samples) на сайте GitHub.</span><span class="sxs-lookup"><span data-stu-id="4727e-113">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

## <a name="requirements"></a><span data-ttu-id="4727e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4727e-114">Requirements</span></span>



| <span data-ttu-id="4727e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4727e-115">Requirement</span></span> | <span data-ttu-id="4727e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4727e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4727e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4727e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4727e-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4727e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="4727e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4727e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4727e-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4727e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4727e-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4727e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4727e-122"><dt>Виндеф. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4727e-122"><dt>Windef.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4727e-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4727e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4727e-124">Общие сведения о цветах</span><span class="sxs-lookup"><span data-stu-id="4727e-124">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="4727e-125">Цветовые структуры</span><span class="sxs-lookup"><span data-stu-id="4727e-125">Color Structures</span></span>](color-structures.md)
</dt> <dt>

[<span data-ttu-id="4727e-126">жетбвалуе</span><span class="sxs-lookup"><span data-stu-id="4727e-126">GetBValue</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue)
</dt> <dt>

[<span data-ttu-id="4727e-127">жетгвалуе</span><span class="sxs-lookup"><span data-stu-id="4727e-127">GetGValue</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)
</dt> <dt>

[<span data-ttu-id="4727e-128">**RValue**</span><span class="sxs-lookup"><span data-stu-id="4727e-128">**GetRValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)
</dt> <dt>

[<span data-ttu-id="4727e-129">RGB</span><span class="sxs-lookup"><span data-stu-id="4727e-129">RGB</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-rgb)
</dt> </dl>

 

 




