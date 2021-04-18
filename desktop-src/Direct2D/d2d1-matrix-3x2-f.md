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
# <a name="d2d1_matrix_3x2_f"></a>D2D1 \_ Матрица \_ 3X2 \_ F

Представляет матрицу размером 3 на 2.


```C++
typedef D2D_MATRIX_3X2_F D2D1_MATRIX_3X2_F;
```



## <a name="remarks"></a>Комментарии

**D2D1 \_ MATRIX \_ 3X2** — это новое имя для структуры [**\_ матрицы D2D \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) . Список полей, предоставляемых матрицей, см. в [**разделе \_ Таблица D2D \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).

Для упрощения общих операций матрицы Direct2D предоставляет класс [**D2D1:: Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) , который является производным от структуры [**D2D1 \_ Matrix \_ 3X2**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) . Класс **Matrix3x2F** предоставляет набор вспомогательных методов для выполнения общих задач, таких как создание матрицы перевода или смещения.

## <a name="examples"></a>Примеры

В следующем примере используется метод [**D2D1:: Matrix3x2F:: вращение**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) для создания матрицы вращения, которая поворачивает квадрат по часовой стрелке 45 градусов относительно центра квадрата и передает матрицу методу [**сеттрансформ**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) целевого объекта отрисовки (*m \_ прендертаржет*).

На следующем рисунке показан результат применения предыдущего преобразования вращения к квадрату. Исходный квадрат является пунктирным контуром, а повернутый квадрат — сплошной контур.

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



В этом примере код пропущен. Дополнительные сведения о преобразованиях см. в разделе [Общие сведения о преобразованиях](direct2d-transforms-overview.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]<br/>                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]<br/> |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**D2D1::Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)
</dt> <dt>

[Общие сведения о преобразованиях](direct2d-transforms-overview.md)
</dt> <dt>

[Поворот объекта](how-to-rotate.md)
</dt> <dt>

[Масштабирование объекта](how-to-scale.md)
</dt> <dt>

[Как наклон объекта](how-to-skew.md)
</dt> <dt>

[Преобразование объекта](how-to-translate.md)
</dt> <dt>

[**\_Матрица D2D \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f)
</dt> </dl>

 

