---
title: Метод Идкомпоситионматрикстрансформ Сетматрикселемент (int, int, Идкомпоситионаниматион)
description: Анимируется значение одного элемента матрицы данного 2D-преобразования.
ms.assetid: 16A9E136-5F0C-4F34-A127-BF06C4530499
keywords:
- Метод Сетматрикселемент DirectComposition
- Метод Сетматрикселемент DirectComposition, интерфейс Идкомпоситионматрикстрансформ
- Интерфейс Идкомпоситионматрикстрансформ DirectComposition, метод Сетматрикселемент
topic_type:
- apiref
api_name:
- IDCompositionMatrixTransform.SetMatrixElement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b4bf2a43e762b85b8b8cfd0c15468b3dc438221
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413395"
---
# <a name="idcompositionmatrixtransformsetmatrixelementint-int-idcompositionanimation-method"></a><span data-ttu-id="1c094-106">Метод Идкомпоситионматрикстрансформ:: Сетматрикселемент (int, int, Идкомпоситионаниматион \* )</span><span class="sxs-lookup"><span data-stu-id="1c094-106">IDCompositionMatrixTransform::SetMatrixElement(int, int, IDCompositionAnimation\*) method</span></span>

<span data-ttu-id="1c094-107">Анимируется значение одного элемента матрицы данного 2D-преобразования.</span><span class="sxs-lookup"><span data-stu-id="1c094-107">Animates the value of one element of the matrix of this 2D transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c094-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c094-108">Syntax</span></span>


```C++
HRESULT SetMatrixElement(
  [in] int                    row,
  [in] int                    column,
  [in] IDCompositionAnimation *animation
);
```



## <a name="parameters"></a><span data-ttu-id="1c094-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c094-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c094-110">*строка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c094-110">*row* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c094-111">Индекс строки изменяемого элемента.</span><span class="sxs-lookup"><span data-stu-id="1c094-111">The row index of the element to change.</span></span> <span data-ttu-id="1c094-112">Это значение должно находиться в диапазоне от 0 до 2 включительно.</span><span class="sxs-lookup"><span data-stu-id="1c094-112">This value must be between 0 and 2, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="1c094-113">*столбец* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c094-113">*column* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c094-114">Индекс столбца изменяемого элемента.</span><span class="sxs-lookup"><span data-stu-id="1c094-114">The column index of the element to change.</span></span> <span data-ttu-id="1c094-115">Это значение должно находиться в диапазоне от 0 до 1 включительно.</span><span class="sxs-lookup"><span data-stu-id="1c094-115">This value must be between 0 and 1, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="1c094-116">*анимация* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c094-116">*animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c094-117">Анимация, представляющая изменение значения указанного элемента с течением времени.</span><span class="sxs-lookup"><span data-stu-id="1c094-117">An animation that represents how the value of the specified element changes over time.</span></span> <span data-ttu-id="1c094-118">Этот параметр не может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="1c094-118">This parameter must not be NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c094-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c094-119">Return value</span></span>

<span data-ttu-id="1c094-120">Если функция завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1c094-120">If the function succeeds, it returns S\_OK.</span></span> <span data-ttu-id="1c094-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1c094-121">Otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="1c094-122">Список кодов ошибок см. в разделе [коды ошибок DirectComposition](directcomposition-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="1c094-122">See [DirectComposition Error Codes](directcomposition-error-codes.md) for a list of error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c094-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c094-123">Remarks</span></span>

<span data-ttu-id="1c094-124">Этот метод создает копию указанной анимации.</span><span class="sxs-lookup"><span data-stu-id="1c094-124">This method makes a copy of the specified animation.</span></span> <span data-ttu-id="1c094-125">Если объект, на который ссылается параметр *анимации* , изменяется после вызова этого метода, это изменение не влияет на элемент, если этот метод не вызывается снова.</span><span class="sxs-lookup"><span data-stu-id="1c094-125">If the object referenced by the *animation* parameter is changed after calling this method, the change does not affect the element unless this method is called again.</span></span> <span data-ttu-id="1c094-126">Если элемент был анимирован ранее, вызов этого метода заменяет предыдущую анимацию новой анимацией.</span><span class="sxs-lookup"><span data-stu-id="1c094-126">If the element was previously animated, calling this method replaces the previous animation with the new animation.</span></span>

<span data-ttu-id="1c094-127">Этот метод завершается ошибкой, если *анимация* является недопустимым указателем, или если она не была создана с помощью того же интерфейса [**идкомпоситиондевице**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) , что и затронутое преобразование.</span><span class="sxs-lookup"><span data-stu-id="1c094-127">This method fails if *animation* is an invalid pointer or if it was not created by the same [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) interface as the affected transform.</span></span> <span data-ttu-id="1c094-128">Интерфейс не может быть пользовательской реализацией; с этим методом можно использовать только интерфейсы, созданные с помощью Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="1c094-128">The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c094-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c094-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c094-130">**идкомпоситионматрикстрансформ**</span><span class="sxs-lookup"><span data-stu-id="1c094-130">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> </dl>

 

 