---
title: any
description: Определяет, являются ли какие-либо компоненты указанного значения ненулевыми.
ms.assetid: 69a30478-662a-47de-babc-3cc67f89809c
keywords:
- любой HLSL
topic_type:
- apiref
api_name:
- any
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6bc5a908336f011973690bd3ca3d598583b0d32d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984084"
---
# <a name="any"></a><span data-ttu-id="645fe-104">any</span><span class="sxs-lookup"><span data-stu-id="645fe-104">any</span></span>

<span data-ttu-id="645fe-105">Определяет, являются ли какие-либо компоненты указанного значения ненулевыми.</span><span class="sxs-lookup"><span data-stu-id="645fe-105">Determines if any components of the specified value are non-zero.</span></span>



| <span data-ttu-id="645fe-106">*RET* Any (*x*)</span><span class="sxs-lookup"><span data-stu-id="645fe-106">*ret* any(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="645fe-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="645fe-107">Parameters</span></span>



| <span data-ttu-id="645fe-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="645fe-108">Item</span></span>                                                   | <span data-ttu-id="645fe-109">Описание</span><span class="sxs-lookup"><span data-stu-id="645fe-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="645fe-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="645fe-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="645fe-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="645fe-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="645fe-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="645fe-112">Return Value</span></span>

<span data-ttu-id="645fe-113">**Значение true** , если какие-либо компоненты параметра *x* не равны нулю; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="645fe-113">**True** if any components of the *x* parameter are non-zero; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="645fe-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="645fe-114">Remarks</span></span>

<span data-ttu-id="645fe-115">Эта функция похожа на встроенную функцию [**ALL**](dx-graphics-hlsl-all.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="645fe-115">This function is similar to the [**all**](dx-graphics-hlsl-all.md) HLSL intrinsic function.</span></span> <span data-ttu-id="645fe-116">Функция **ANY** определяет, являются ли какие-либо компоненты указанного значения ненулевыми, тогда как функция **ALL** определяет, являются ли все компоненты указанного значения ненулевыми.</span><span class="sxs-lookup"><span data-stu-id="645fe-116">The **any** function determines if any components of the specified value are non-zero, while the **all** function determines if all components of the specified value are non-zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="645fe-117">Описание типа</span><span class="sxs-lookup"><span data-stu-id="645fe-117">Type Description</span></span>



| <span data-ttu-id="645fe-118">Имя</span><span class="sxs-lookup"><span data-stu-id="645fe-118">Name</span></span>  | [<span data-ttu-id="645fe-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="645fe-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="645fe-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="645fe-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="645fe-121">Размер</span><span class="sxs-lookup"><span data-stu-id="645fe-121">Size</span></span> |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="645fe-122">*x*</span><span class="sxs-lookup"><span data-stu-id="645fe-122">*x*</span></span>   | <span data-ttu-id="645fe-123">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="645fe-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="645fe-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="645fe-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="645fe-125">any</span><span class="sxs-lookup"><span data-stu-id="645fe-125">any</span></span>  |
| <span data-ttu-id="645fe-126">*обратно*</span><span class="sxs-lookup"><span data-stu-id="645fe-126">*ret*</span></span> | [<span data-ttu-id="645fe-127">**скаляр**</span><span class="sxs-lookup"><span data-stu-id="645fe-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                            | [<span data-ttu-id="645fe-128">**bool**</span><span class="sxs-lookup"><span data-stu-id="645fe-128">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                 | <span data-ttu-id="645fe-129">1</span><span class="sxs-lookup"><span data-stu-id="645fe-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="645fe-130">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="645fe-130">Minimum Shader Model</span></span>

<span data-ttu-id="645fe-131">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="645fe-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="645fe-132">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="645fe-132">Shader Model</span></span>                                                                       | <span data-ttu-id="645fe-133">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="645fe-133">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="645fe-134">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="645fe-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="645fe-135">да</span><span class="sxs-lookup"><span data-stu-id="645fe-135">yes</span></span>                   |
| [<span data-ttu-id="645fe-136">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="645fe-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="645fe-137">VS \_ 1 \_ 1 и PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="645fe-137">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="645fe-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="645fe-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="645fe-139">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="645fe-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

