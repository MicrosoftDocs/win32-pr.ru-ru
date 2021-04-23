---
description: Задает функцию обратного вызова, используемую при распознавании строк.
ms.assetid: 0b07ec80-328a-471b-b554-fa66f56a2871
title: Функция Сетлинерекокаллбакк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineRecoCallback
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: b256a38d6d6ee6ecf43994c6619c369ea6ca2212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265065"
---
# <a name="setlinerecocallback-function"></a><span data-ttu-id="a81a2-103">Функция Сетлинерекокаллбакк</span><span class="sxs-lookup"><span data-stu-id="a81a2-103">SetLineRecoCallback function</span></span>

<span data-ttu-id="a81a2-104">Задает функцию обратного вызова, используемую при распознавании строк.</span><span class="sxs-lookup"><span data-stu-id="a81a2-104">Sets a callback function to be used during line recognition.</span></span>

<span data-ttu-id="a81a2-105">Эта вспомогательная функция не предназначена для использования в коде приложения.</span><span class="sxs-lookup"><span data-stu-id="a81a2-105">This helper function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a81a2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a81a2-106">Syntax</span></span>


```C++
HRESULT WINAPI SetLineRecoCallback(
  _In_ INT_PTR        hDivider,
       GetLineRecoDef pfn
);
```



## <a name="parameters"></a><span data-ttu-id="a81a2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a81a2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a81a2-108">*хдивидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a81a2-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a81a2-109">Маркер объекта [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="a81a2-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="a81a2-110">*PFN*</span><span class="sxs-lookup"><span data-stu-id="a81a2-110">*pfn*</span></span> 
</dt> <dd>

<span data-ttu-id="a81a2-111">Указатель на функцию, которая вызывается при распознавании в переданном [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="a81a2-111">A pointer to a function that is called when recognition occurs on the [**InkDivider**](inkdivider-class.md) passed in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a81a2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a81a2-112">Return value</span></span>

<span data-ttu-id="a81a2-113">Эта функция может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="a81a2-113">This function can return one of these values.</span></span>



| <span data-ttu-id="a81a2-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a81a2-114">Return code</span></span>                                                                                  | <span data-ttu-id="a81a2-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a81a2-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="a81a2-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a81a2-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a81a2-117">Функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a81a2-117">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="a81a2-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a81a2-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a81a2-119">Недопустимый параметр *пдивидер* .</span><span class="sxs-lookup"><span data-stu-id="a81a2-119">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a81a2-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a81a2-120">Remarks</span></span>

<span data-ttu-id="a81a2-121">Ниже приведен синтаксис функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="a81a2-121">The following is the syntax for the callback function.</span></span>

``` syntax
public delegate void GetLineRecoDef(
        int cStrokes, 
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.I4, SizeParamIndex = 0)]int [] aStrokeIds, 
        float degrees, 
        Point point, 
        [MarshalAs(UnmanagedType.BStr)] out string lineString, 
        out int cSegment, 
        out int[] strokeIdOrdered, 
        out int[] segmentStrokes,
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.BStr)] out string [] aSegmentString
    );
```

## <a name="requirements"></a><span data-ttu-id="a81a2-122">Требования</span><span class="sxs-lookup"><span data-stu-id="a81a2-122">Requirements</span></span>



| <span data-ttu-id="a81a2-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a81a2-123">Requirement</span></span> | <span data-ttu-id="a81a2-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a81a2-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a81a2-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a81a2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a81a2-126">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a81a2-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="a81a2-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a81a2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a81a2-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a81a2-128">None supported</span></span><br/>                                                             |
| <span data-ttu-id="a81a2-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a81a2-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="a81a2-130"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a81a2-130"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




