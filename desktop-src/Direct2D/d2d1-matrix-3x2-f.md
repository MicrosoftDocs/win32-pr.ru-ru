---
title: D2D1_MATRIX_3X2_F (D2d1. h)
description: Представляет матрицу размером 3 на 2.
ms.assetid: f05d7555-6482-4eea-950f-7b443892cc1f
keywords:
- D2D1_MATRIX_3X2_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb252e35508c48570c96f251205fc8a54755687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672565"
---
# <a name="d2d1_matrix_3x2_f"></a><span data-ttu-id="52cbe-104">D2D1 \_ Матрица \_ 3X2 \_ F</span><span class="sxs-lookup"><span data-stu-id="52cbe-104">D2D1\_MATRIX\_3X2\_F</span></span>

<span data-ttu-id="52cbe-105">Представляет матрицу размером 3 на 2.</span><span class="sxs-lookup"><span data-stu-id="52cbe-105">Represents a 3-by-2 matrix.</span></span>


```C++
typedef D2D_MATRIX_3X2_F D2D1_MATRIX_3X2_F;
```



## <a name="remarks"></a><span data-ttu-id="52cbe-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52cbe-106">Remarks</span></span>

<span data-ttu-id="52cbe-107">**D2D1 \_ MATRIX \_ 3X2** — это новое имя для структуры [**\_ матрицы D2D \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) .</span><span class="sxs-lookup"><span data-stu-id="52cbe-107">**D2D1\_MATRIX\_3X2** is a new name for the [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure.</span></span> <span data-ttu-id="52cbe-108">Список полей, предоставляемых матрицей, см. в [**разделе \_ Таблица D2D \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).</span><span class="sxs-lookup"><span data-stu-id="52cbe-108">For a list of fields provided by the matrix, see [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).</span></span>

<span data-ttu-id="52cbe-109">Для упрощения общих операций матрицы Direct2D предоставляет класс [**D2D1:: Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) , который является производным от структуры [**D2D1 \_ Matrix \_ 3X2**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) .</span><span class="sxs-lookup"><span data-stu-id="52cbe-109">To simplify common matrix operations, Direct2D provides the [**D2D1::Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) class, which is derived from the [**D2D1\_MATRIX\_3X2**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure.</span></span> <span data-ttu-id="52cbe-110">Класс **Matrix3x2F** предоставляет набор вспомогательных методов для выполнения общих задач, таких как создание матрицы перевода или смещения.</span><span class="sxs-lookup"><span data-stu-id="52cbe-110">The **Matrix3x2F** class provides a set of helper methods for performing common tasks, such as creating a translation or skew matrix.</span></span>

## <a name="examples"></a><span data-ttu-id="52cbe-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="52cbe-111">Examples</span></span>

<span data-ttu-id="52cbe-112">В следующем примере используется метод [**D2D1:: Matrix3x2F:: вращение**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) для создания матрицы вращения, которая поворачивает квадрат по часовой стрелке 45 градусов относительно центра квадрата и передает матрицу методу [**сеттрансформ**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) целевого объекта отрисовки (*m \_ прендертаржет*).</span><span class="sxs-lookup"><span data-stu-id="52cbe-112">The following example uses the [**D2D1::Matrix3x2F::Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) method to create a rotation matrix that rotates a square clockwise 45 degrees about the center of the square and passes the matrix to the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) method of the render target (*m\_pRenderTarget*).</span></span>

<span data-ttu-id="52cbe-113">На следующем рисунке показан результат применения предыдущего преобразования вращения к квадрату.</span><span class="sxs-lookup"><span data-stu-id="52cbe-113">The following illustration shows the effect of applying the preceding rotation transformation to the square.</span></span> <span data-ttu-id="52cbe-114">Исходный квадрат является пунктирным контуром, а повернутый квадрат — сплошной контур.</span><span class="sxs-lookup"><span data-stu-id="52cbe-114">The original square is a dotted outline, and the rotated square is a solid outline.</span></span>

![Иллюстрация квадрата, повернутого по часовой стрелке 45 градусов относительно центра исходного квадрата](images/rotate-ovw.png)


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



<span data-ttu-id="52cbe-116">В этом примере код пропущен.</span><span class="sxs-lookup"><span data-stu-id="52cbe-116">Code has been omitted from this example.</span></span> <span data-ttu-id="52cbe-117">Дополнительные сведения о преобразованиях см. в разделе [Общие сведения о преобразованиях](direct2d-transforms-overview.md).</span><span class="sxs-lookup"><span data-stu-id="52cbe-117">For more information about transforms, see the [Transforms Overview](direct2d-transforms-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52cbe-118">Требования</span><span class="sxs-lookup"><span data-stu-id="52cbe-118">Requirements</span></span>



| <span data-ttu-id="52cbe-119">Требование</span><span class="sxs-lookup"><span data-stu-id="52cbe-119">Requirement</span></span> | <span data-ttu-id="52cbe-120">Значение</span><span class="sxs-lookup"><span data-stu-id="52cbe-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52cbe-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52cbe-121">Minimum supported client</span></span><br/> | <span data-ttu-id="52cbe-122">Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]</span><span class="sxs-lookup"><span data-stu-id="52cbe-122">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="52cbe-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52cbe-123">Minimum supported server</span></span><br/> | <span data-ttu-id="52cbe-124">Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="52cbe-124">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="52cbe-125">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="52cbe-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="52cbe-126">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="52cbe-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="52cbe-127">Header</span><span class="sxs-lookup"><span data-stu-id="52cbe-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="52cbe-128"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="52cbe-128"><dt>D2d1.h</dt></span></span> </dl>                                                        |



## <a name="see-also"></a><span data-ttu-id="52cbe-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52cbe-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52cbe-130">**D2D1::Matrix3x2F**</span><span class="sxs-lookup"><span data-stu-id="52cbe-130">**D2D1::Matrix3x2F**</span></span>](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)
</dt> <dt>

[<span data-ttu-id="52cbe-131">Общие сведения о преобразованиях</span><span class="sxs-lookup"><span data-stu-id="52cbe-131">Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="52cbe-132">Поворот объекта</span><span class="sxs-lookup"><span data-stu-id="52cbe-132">How to Rotate an Object</span></span>](how-to-rotate.md)
</dt> <dt>

[<span data-ttu-id="52cbe-133">Масштабирование объекта</span><span class="sxs-lookup"><span data-stu-id="52cbe-133">How to Scale an Object</span></span>](how-to-scale.md)
</dt> <dt>

[<span data-ttu-id="52cbe-134">Как наклон объекта</span><span class="sxs-lookup"><span data-stu-id="52cbe-134">How to Skew an Object</span></span>](how-to-skew.md)
</dt> <dt>

[<span data-ttu-id="52cbe-135">Преобразование объекта</span><span class="sxs-lookup"><span data-stu-id="52cbe-135">How to Translate an Object</span></span>](how-to-translate.md)
</dt> <dt>

[<span data-ttu-id="52cbe-136">**\_Матрица D2D \_ 3X2 \_ F**</span><span class="sxs-lookup"><span data-stu-id="52cbe-136">**D2D\_MATRIX\_3X2\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f)
</dt> </dl>

 

