---
description: Функция обратного вызова для Уватлас.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe073b5e6a798ccb74421d42502b089d59be11f
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342799"
---
# <a name="lpd3dxuvatlascb"></a><span data-ttu-id="e690e-103">LPD3DXUVATLASCB</span><span class="sxs-lookup"><span data-stu-id="e690e-103">LPD3DXUVATLASCB</span></span>

<span data-ttu-id="e690e-104">Функция обратного вызова для Уватлас.</span><span class="sxs-lookup"><span data-stu-id="e690e-104">Callback function for UVAtlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="e690e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e690e-105">Syntax</span></span>


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="e690e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e690e-106">Parameters</span></span>

<span data-ttu-id="e690e-107">\[out \] фперцентдоне — число с плавающей запятой от 0 до 1,0, представляющее процент выполненных вычислений (от 0 до 100 процентов).</span><span class="sxs-lookup"><span data-stu-id="e690e-107">\[out\] fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="e690e-108">\[в \] лпусерконтекст — указатель на определяемое пользователем значение, которое передается функции обратного вызова; обычно используется приложением для передачи указателя на структуру данных, которая предоставляет сведения о контексте для функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="e690e-108">\[in\] lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="e690e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e690e-109">Return Value</span></span>

<span data-ttu-id="e690e-110">Эта функция должна быть реализована, чтобы вернуть значение \_ ОК для сохранения запуска симулятора.</span><span class="sxs-lookup"><span data-stu-id="e690e-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="e690e-111">Любое другое значение остановит симулятор.</span><span class="sxs-lookup"><span data-stu-id="e690e-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="e690e-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="e690e-112">Remarks</span></span>

<span data-ttu-id="e690e-113">Не забудьте указать соглашение о вызовах [**типов данных Windows**](../winprog/windows-data-types.md) при объявлении функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="e690e-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="e690e-114">В противном случае могут возникать переполняется стек.</span><span class="sxs-lookup"><span data-stu-id="e690e-114">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="e690e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e690e-115">Requirement</span></span>                         | <span data-ttu-id="e690e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e690e-116">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="e690e-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e690e-117">Header</span></span>                   | <span data-ttu-id="e690e-118">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="e690e-118">d3dx9mesh.h</span></span> |
| <span data-ttu-id="e690e-119">Библиотека импорта</span><span class="sxs-lookup"><span data-stu-id="e690e-119">Import Library</span></span>           | <span data-ttu-id="e690e-120">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="e690e-120">d3dx9.lib</span></span>   |
| <span data-ttu-id="e690e-121">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="e690e-121">Minimum Operating System</span></span> | <span data-ttu-id="e690e-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e690e-122">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="e690e-123">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e690e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e690e-124">Функции обратного вызова</span><span class="sxs-lookup"><span data-stu-id="e690e-124">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
