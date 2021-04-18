---
description: Метод Жетклассвиндовстилес извлекает стили окон и стили окна.
ms.assetid: 6eec7912-c654-4e4f-b6f1-ec94c7284575
title: Кбасевиндов. Жетклассвиндовстилес, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetClassWindowStyles
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a34332f84a91ee88d61ee5f29f0b6a0b0cc44714
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675476"
---
# <a name="cbasewindowgetclasswindowstyles-method"></a><span data-ttu-id="45b09-103">Кбасевиндов. Жетклассвиндовстилес, метод</span><span class="sxs-lookup"><span data-stu-id="45b09-103">CBaseWindow.GetClassWindowStyles method</span></span>

<span data-ttu-id="45b09-104">`GetClassWindowStyles`Метод получает стили окна и стили окна.</span><span class="sxs-lookup"><span data-stu-id="45b09-104">The `GetClassWindowStyles` method retrieves the window's class styles and window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b09-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45b09-105">Syntax</span></span>


```C++
virtual LPTSTR GetClassWindowStyles(
   DWORD *pClassStyles,
   DWORD *pWindowStyles,
   DWORD *pWindowStylesEx
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="45b09-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="45b09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45b09-107">*пклассстилес*</span><span class="sxs-lookup"><span data-stu-id="45b09-107">*pClassStyles*</span></span> 
</dt> <dd>

<span data-ttu-id="45b09-108">Указатель на переменную, которая получает стили класса.</span><span class="sxs-lookup"><span data-stu-id="45b09-108">Pointer to a variable that receives the class styles.</span></span>

</dd> <dt>

<span data-ttu-id="45b09-109">*пвиндовстилес*</span><span class="sxs-lookup"><span data-stu-id="45b09-109">*pWindowStyles*</span></span> 
</dt> <dd>

<span data-ttu-id="45b09-110">Указатель на переменную, которая получает стили окна.</span><span class="sxs-lookup"><span data-stu-id="45b09-110">Pointer to a variable that receives the window styles.</span></span>

</dd> <dt>

<span data-ttu-id="45b09-111">*пвиндовстилесекс*</span><span class="sxs-lookup"><span data-stu-id="45b09-111">*pWindowStylesEx*</span></span> 
</dt> <dd>

<span data-ttu-id="45b09-112">Указатель на переменную, которая получает расширенные стили окна.</span><span class="sxs-lookup"><span data-stu-id="45b09-112">Pointer to a variable that receives the extended window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45b09-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45b09-113">Return value</span></span>

<span data-ttu-id="45b09-114">Возвращает статическую текстовую строку, содержащую имя класса.</span><span class="sxs-lookup"><span data-stu-id="45b09-114">Returns a static text string that contains the class name.</span></span>

## <a name="remarks"></a><span data-ttu-id="45b09-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45b09-115">Remarks</span></span>

<span data-ttu-id="45b09-116">Метод [**кбасевиндов::P репаревиндов**](cbasewindow-preparewindow.md) вызывает этот метод, чтобы получить стили окна и стили окон.</span><span class="sxs-lookup"><span data-stu-id="45b09-116">The [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method calls this method to retrieve the window's class styles and window styles.</span></span>

<span data-ttu-id="45b09-117">Этот метод является чисто виртуальным; производный класс должен реализовать его.</span><span class="sxs-lookup"><span data-stu-id="45b09-117">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="45b09-118">В следующем примере показана возможная реализация:</span><span class="sxs-lookup"><span data-stu-id="45b09-118">The following example shows a possible implementation:</span></span>


```C++
LPTSTR CMyWindowClass::GetClassWindowStyles(DWORD *pClassStyles,
                                            DWORD *pWindowStyles,
                                            DWORD *pWindowStylesEx)
{
    *pClassStyles = CS_HREDRAW | CS_VREDRAW;
    *pWindowStyles = WS_OVERLAPPEDWINDOW | WS_CLIPCHILDREN;
    *pWindowStylesEx = WS_EX_WINDOWEDGE;
    return TEXT("MyWindowClass");
}
```



<span data-ttu-id="45b09-119">Объект использует стиль класса для элемента **лпсзкласснаме** структуры вндкласс, который передается функции **registerClass** .</span><span class="sxs-lookup"><span data-stu-id="45b09-119">The object uses the class style for the **lpszClassName** member of a WNDCLASS structure, which it passes to the **RegisterClass** function.</span></span> <span data-ttu-id="45b09-120">Объект использует стили окна для параметров *двексстиле* и *двстиле* функции **CreateWindowEx** .</span><span class="sxs-lookup"><span data-stu-id="45b09-120">The object uses the window styles for the *dwExStyle* and *dwStyle* parameters of the **CreateWindowEx** function.</span></span> <span data-ttu-id="45b09-121">Дополнительные сведения см. в разделе пакет SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="45b09-121">For more information, see the Platform SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="45b09-122">Требования</span><span class="sxs-lookup"><span data-stu-id="45b09-122">Requirements</span></span>



| <span data-ttu-id="45b09-123">Требование</span><span class="sxs-lookup"><span data-stu-id="45b09-123">Requirement</span></span> | <span data-ttu-id="45b09-124">Значение</span><span class="sxs-lookup"><span data-stu-id="45b09-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45b09-125">Header</span><span class="sxs-lookup"><span data-stu-id="45b09-125">Header</span></span><br/>  | <dl> <span data-ttu-id="45b09-126"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45b09-126"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="45b09-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="45b09-127">Library</span></span><br/> | <dl> <span data-ttu-id="45b09-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="45b09-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45b09-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45b09-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45b09-130">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="45b09-130">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




