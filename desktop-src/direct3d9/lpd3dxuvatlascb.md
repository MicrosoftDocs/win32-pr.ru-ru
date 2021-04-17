---
description: Функция обратного вызова для Уватлас.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda7c58ef001a936b01f3af2027f9207c3d2770
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710637"
---
# <a name="lpd3dxuvatlascb"></a><span data-ttu-id="63e88-103">LPD3DXUVATLASCB</span><span class="sxs-lookup"><span data-stu-id="63e88-103">LPD3DXUVATLASCB</span></span>

<span data-ttu-id="63e88-104">Функция обратного вызова для Уватлас.</span><span class="sxs-lookup"><span data-stu-id="63e88-104">Callback function for UVAtlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e88-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63e88-105">Syntax</span></span>


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="63e88-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="63e88-106">Parameters</span></span>

<span data-ttu-id="63e88-107">\[out \] фперцентдоне — число с плавающей запятой от 0 до 1,0, представляющее процент выполненных вычислений (от 0 до 100 процентов).</span><span class="sxs-lookup"><span data-stu-id="63e88-107">\[out\] fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="63e88-108">\[в \] лпусерконтекст — указатель на определяемое пользователем значение, которое передается функции обратного вызова; обычно используется приложением для передачи указателя на структуру данных, которая предоставляет сведения о контексте для функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="63e88-108">\[in\] lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="63e88-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63e88-109">Return Value</span></span>

<span data-ttu-id="63e88-110">Эта функция должна быть реализована, чтобы вернуть значение \_ ОК для сохранения запуска симулятора.</span><span class="sxs-lookup"><span data-stu-id="63e88-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="63e88-111">Любое другое значение остановит симулятор.</span><span class="sxs-lookup"><span data-stu-id="63e88-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="63e88-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63e88-112">Remarks</span></span>

<span data-ttu-id="63e88-113">Не забудьте указать соглашение о вызовах [**типов данных Windows**](../winprog/windows-data-types.md) при объявлении функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="63e88-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="63e88-114">В противном случае могут возникать переполняется стек.</span><span class="sxs-lookup"><span data-stu-id="63e88-114">Otherwise, stack overflows can occur.</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="63e88-115">Header</span><span class="sxs-lookup"><span data-stu-id="63e88-115">Header</span></span>                   | <span data-ttu-id="63e88-116">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="63e88-116">d3dx9mesh.h</span></span> |
| <span data-ttu-id="63e88-117">Библиотека импорта</span><span class="sxs-lookup"><span data-stu-id="63e88-117">Import Library</span></span>           | <span data-ttu-id="63e88-118">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="63e88-118">d3dx9.lib</span></span>   |
| <span data-ttu-id="63e88-119">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="63e88-119">Minimum Operating System</span></span> | <span data-ttu-id="63e88-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="63e88-120">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="63e88-121">См. также</span><span class="sxs-lookup"><span data-stu-id="63e88-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63e88-122">Функции обратного вызова</span><span class="sxs-lookup"><span data-stu-id="63e88-122">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
