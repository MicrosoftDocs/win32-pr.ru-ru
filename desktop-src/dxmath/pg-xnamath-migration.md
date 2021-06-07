---
description: В этом обзоре описываются изменения, необходимые для переноса существующего кода с помощью библиотеки XNA Math в библиотеку Директксмас.
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: Перенос кода из библиотеки XNA Math
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc7a48d30711a870c28b677e458a4f72c3b3c40
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549966"
---
# <a name="code-migration-from-the-xna-math-library"></a>Перенос кода из библиотеки XNA Math

В этом обзоре описываются изменения, необходимые для переноса существующего кода с помощью библиотеки XNA Math в библиотеку Директксмас.

## <a name="header-changes"></a>Изменения заголовка

Библиотека Директксмас использует новый набор заголовков.

Замените `xnamath.h` заголовок на `DirectXMath.h` и добавьте `DirectXPackedVector.h` для *упакованных типов GPU* .

Ограничивающие типы из примера конфликта DirectX SDK в `xnacollision.h` теперь входят в библиотеку директксмас в `DirectXCollision.h` . Они были изменены для использования классов C++, а не API-интерфейсов в стиле языка C.

## <a name="constant-changes"></a>Постоянные изменения

\_Версия кснамас (200, 201, 202, 203, 204 и т. д.) заменена диреккстмас \_ версией (300, 301, 302, 303 и т. д.).

> [!NOTE]  
> Директксмас 3,00 и 3,02 поставляются с предварительными версиями Windows SDK. Директксмас 3,03 в финальной версии пакета SDK для Windows 8.

## <a name="namespaces"></a>Пространства имен

Библиотека Директксмас использует пространства имен C++ для организации типов. XNA Math использовал только глобальное пространство имен. Типы Директксмас, общие с XNA Math, находятся в **DirectX** или в пространстве имен **DirectX::P аккедвектор** .

В исходных файлах C++ простое решение заключается в добавлении `using` инструкций.

```cpp
#include "DirectXMath.h"
#include "DirectXPackedVector.h"

using namespace DirectX; 
using namespace DirectX::PackedVector;
```

Для заголовков не рекомендуется добавлять операторы using. Вместо этого добавьте полные пространства имен.

```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```

## <a name="partial-loads"></a>Частичные загрузки

Для различных функций, которые загружают менее 4 элементов КСМВЕКТОР, в библиотеке XNA Math не определены дополнительные элементы. Директксмас всегда будет заполнять эти дополнительные элементы 0.

## <a name="removal-of-xbox-360-specific-types"></a>Удаление специальных типов для Xbox 360

Следующие типы, функции и константы XNA Math Library недоступны в Директксмас.

-   HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3
-   XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()
-   XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()
-   g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ ксмадддхен, g \_ XMMulHenD3, g \_ XMMulDHen3, g \_ XMXorHenD3, g \_ XMXorDHen3
-   XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4
-   XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()
-   XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()
-   g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g \_ XMAddIco4, g \_ XMMulIco4

\_\_vector4i является устаревшим. Вместо этого используйте [**XMVECTORI32**](xmvectori32-data-type.md) или [**XMVECTORU32**](xmvectoru32-data-type.md) .

Следующие функции и типы являются устаревшими, так как они являются только Xbox 360: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.

## <a name="arm-neon-intrinsics"></a>Встроенные функции ARM-NEON

Объявление векторной константы с этим кодом будет компилироваться для XNA Math для SSE и без встроенных функций, но не будет выполняться для Директксмас с помощью ARM-NEON.

```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```

Как правило, не рекомендуется использовать этот метод инициализации [**ксмвектор**](xmvector-data-type.md). Однако, если требуется константа Vector, класс [**XMVECTORF32**](xmvectorf32-data-type.md) поддерживает этот стиль инициализации и возвращает тип **ксмвектор** автоматически, чтобы можно было использовать **XMVECTORF32** в большинстве тех же контекстов. Для выполнения любых операций записи в класс **XMVECTORF32** требуется явная ссылка на элемент **ксмвектор** . v.

## <a name="permute"></a>Переставляют

Библиотека XNA Math имела следующую форму для общих векторных переставляют:

```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```

Для Директксмас было устранено **ксмвекторпермутеконтрол** , а XM \_ переставляют \_ 0x. \_ \_ Константы 1Z переставляют XM были переопределены, чтобы они были простыми индексами 0-7. Вот новая сигнатура для [**ксмвекторпермуте**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):

```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```

Вместо управляющего слова эта функция непосредственно принимает 4 индекса в качестве параметров, что также делает ее аналогом функции [**ксмвекторсвиззле**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) , используя новый XM \_ свиззле \_ X. \_ \_ Константы XM свиззле W определены как простые индексы 0-3.

```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```

> [!NOTE]
> Для постоянных значений существует гораздо более эффективный способ реализации переставляют. Вместо использования формы функции [**ксмвекторпермуте**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)используйте форму **шаблона** :

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
```

## <a name="template-forms"></a>Формы шаблонов

Как правило, использование формы шаблона в форме функции следующих функций значительно более эффективно и позволяет библиотеке выполнять оптимизацию для конкретной платформы с помощью специализации шаблонов.

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
    XMVECTOR XMVectorSwizzle(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateLeft(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateRight(FXMVECTOR V)

template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
    XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
```

## <a name="eliminated-functions"></a>Исключенные функции

| Функция исключена        | Замена                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| XMStoreFloat3x3NC          | [**XMStoreFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
| XMStoreFloat4NC            | [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
| XMStoreFloat4x3NC          | [**XMStoreFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
| XMStoreFloat4x4NC          | [**XMStoreFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
| XMStoreInt4NC              | [**XMStoreInt4**](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
| XMVector2InBoundsR         | [**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ? [XM \_ КРМАСК \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0 |
| XMVector2TransformStreamNC | [**XMVector2TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
| XMVector3InBoundsR         | [**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ? [XM \_ КРМАСК \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0 |
| XMVector3TransformStreamNC | [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
| XMVector4InBoundsR         | [**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ? [XM \_ КРМАСК \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0 |
| ксмвекторкошест            | [**ксмвекторкош**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
| ксмвекторекспест             | [**ксмвекторексп**](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
| ксмвекторложест             | [**ксмвекторлог**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
| ксмвекторповест             | [**ксмвекторпов**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
| ксмвекторсинхест            | [**ксмвекторсинх**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
| ксмвектортанхест            | [**ксмвектортанх**](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |

## <a name="related-topics"></a>Связанные темы

[Директксмас по программированию](ovw-xnamath-progguide.md)
