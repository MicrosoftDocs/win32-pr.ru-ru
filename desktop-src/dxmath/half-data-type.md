---
description: Псевдоним для UInt16 \_ t с 16-разрядным числом с плавающей запятой, состоящим из бита знака, 5-битного смещения и 10-разрядной мантисса.
ms.assetid: E84E0EBA-5C34-41AA-84DB-7A65EBDCAD15
title: ПОЛОВИНА типа данных (Директкспаккедвектор. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9651b84675be68bd433fdeaaae588cb01dc745ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718025"
---
# <a name="half-data-type"></a><span data-ttu-id="cfa05-103">ПОЛОВИНА типа данных</span><span class="sxs-lookup"><span data-stu-id="cfa05-103">HALF Data Type</span></span>

<span data-ttu-id="cfa05-104">Псевдоним для **UInt16 \_ t** с 16-разрядным числом с плавающей запятой, состоящим из бита знака, 5-битного смещения и 10-разрядной мантисса.</span><span class="sxs-lookup"><span data-stu-id="cfa05-104">An alias to **uint16\_t** packed with a 16-bit floating-point number consisting of a sign bit, a 5-bit biased exponent, and a 10-bit mantissa.</span></span>


```C++
typedef uint16_t HALF;
```



## <a name="remarks"></a><span data-ttu-id="cfa05-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cfa05-105">Remarks</span></span>

<span data-ttu-id="cfa05-106">ПОЛОВИНА типа данных эквивалентна формату binary16 в формате IEEE 754.</span><span class="sxs-lookup"><span data-stu-id="cfa05-106">The HALF data type is equivalent to the IEEE 754 binary16 format.</span></span>

<span data-ttu-id="cfa05-107">ПОЛОВИНная \_ минута = 6.10352 e-5F</span><span class="sxs-lookup"><span data-stu-id="cfa05-107">HALF\_MIN = 6.10352e-5f</span></span>

<span data-ttu-id="cfa05-108">ПОЛОВИНА \_ Max = 65504. f</span><span class="sxs-lookup"><span data-stu-id="cfa05-108">HALF\_MAX = 65504.f</span></span>

<span data-ttu-id="cfa05-109">Дополнительные сведения о половина типа данных см. в разделе [Формат с плавающей запятой половинной точности](https://en.wikipedia.org/wiki/Half_precision_floating-point_format).</span><span class="sxs-lookup"><span data-stu-id="cfa05-109">For more info about the HALF data type, see [Half-precision floating-point format](https://en.wikipedia.org/wiki/Half_precision_floating-point_format).</span></span>

<span data-ttu-id="cfa05-110">**Пространство имен**: Используйте DirectX::P аккедвектор</span><span class="sxs-lookup"><span data-stu-id="cfa05-110">**Namespace**: Use DirectX::PackedVector</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="cfa05-111">Требования к платформе</span><span class="sxs-lookup"><span data-stu-id="cfa05-111">Platform Requirements</span></span>

<span data-ttu-id="cfa05-112">Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cfa05-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="cfa05-113">Поддерживается для классических приложений Win32, приложений для Магазина Windows и Windows Phone 8 приложений.</span><span class="sxs-lookup"><span data-stu-id="cfa05-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfa05-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cfa05-114">Requirements</span></span>



| <span data-ttu-id="cfa05-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cfa05-115">Requirement</span></span> | <span data-ttu-id="cfa05-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cfa05-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa05-117">Header</span><span class="sxs-lookup"><span data-stu-id="cfa05-117">Header</span></span><br/> | <dl> <span data-ttu-id="cfa05-118"><dt>Директкспаккедвектор. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfa05-118"><dt>DirectXPackedVector.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfa05-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cfa05-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfa05-120">Типы библиотек Директксмас</span><span class="sxs-lookup"><span data-stu-id="cfa05-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> </dl>

 

 




