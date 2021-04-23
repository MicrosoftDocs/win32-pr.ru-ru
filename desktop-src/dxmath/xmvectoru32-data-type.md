---
description: Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки \_ значений uint32 t в экземпляр типа ксмвектор.
ms.assetid: 1ac1f48a-cd7f-7741-933f-c341fc42a21c
title: Тип данных XMVECTORU32 (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c7a64d42bc4638573b987642c0cd77c37cc12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704539"
---
# <a name="xmvectoru32-data-type"></a><span data-ttu-id="85796-103">Тип данных XMVECTORU32</span><span class="sxs-lookup"><span data-stu-id="85796-103">XMVECTORU32 Data Type</span></span>

<span data-ttu-id="85796-104">Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки \_ значений uint32 t в экземпляр типа [**ксмвектор**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="85796-104">An opaque, portable type to support the use of C/C++ initializer syntax to load uint32\_t values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTOR32 vectoru32;
```



## <a name="remarks"></a><span data-ttu-id="85796-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85796-105">Remarks</span></span>

<span data-ttu-id="85796-106">Список дополнительных функций, таких как конструкторы и операторы, доступных при использовании XMVECTORU32 при программировании в C++, см. в разделе [расширения XMVECTORU32](ovw-xmvectoru32-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="85796-106">For a list of additional functionality, such as constructors and operators, available using XMVECTORU32 when programming in C++, see [XMVECTORU32 Extensions](ovw-xmvectoru32-extensions.md).</span></span>

<span data-ttu-id="85796-107">Структуры [**XMVECTORF32**](xmvectorf32-data-type.md), **XMVECTORU32**, [**XMVECTORI32**](xmvectori32-data-type.md)и [**XMVECTORU8**](xmvectoru8-data-type.md) предоставляются в качестве механизма создания [**ксмвектор**](xmvector-data-type.md) из различных типов данных констант (с плавающей запятой, целым числом, целым числом и байтом) с помощью инициализаторов.</span><span class="sxs-lookup"><span data-stu-id="85796-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), **XMVECTORU32**, [**XMVECTORI32**](xmvectori32-data-type.md), and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="85796-108">Это необходимо для поддержки [**ксмвектор**](xmvector-data-type.md), так как сам по себе не поддерживает инициализаторы в целях обеспечения переносимости и оптимизации.</span><span class="sxs-lookup"><span data-stu-id="85796-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="85796-109">Пример:</span><span class="sxs-lookup"><span data-stu-id="85796-109">For example:</span></span>

``` syntax
XMVECTOR data;
XMVECTORU32 uintVector = { 0xf7000000, 0x8310000, 0x1000000, 0 };
data = uintVector;
```

<span data-ttu-id="85796-110">**Пространство имен**. Использование DirectX</span><span class="sxs-lookup"><span data-stu-id="85796-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="85796-111">Требования к платформе</span><span class="sxs-lookup"><span data-stu-id="85796-111">Platform Requirements</span></span>

<span data-ttu-id="85796-112">Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="85796-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="85796-113">Поддерживается для классических приложений Win32, приложений для Магазина Windows и Windows Phone 8 приложений.</span><span class="sxs-lookup"><span data-stu-id="85796-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="85796-114">Требования</span><span class="sxs-lookup"><span data-stu-id="85796-114">Requirements</span></span>



| <span data-ttu-id="85796-115">Требование</span><span class="sxs-lookup"><span data-stu-id="85796-115">Requirement</span></span> | <span data-ttu-id="85796-116">Значение</span><span class="sxs-lookup"><span data-stu-id="85796-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="85796-117">Header</span><span class="sxs-lookup"><span data-stu-id="85796-117">Header</span></span><br/> | <dl> <span data-ttu-id="85796-118"><dt>Директксмас. h</dt></span><span class="sxs-lookup"><span data-stu-id="85796-118"><dt>Directxmath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85796-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85796-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85796-120">Типы библиотек Директксмас</span><span class="sxs-lookup"><span data-stu-id="85796-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="85796-121">**Тип данных XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="85796-121">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="85796-122">**Тип данных XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="85796-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="85796-123">**Тип данных КСМВЕКТОР**</span><span class="sxs-lookup"><span data-stu-id="85796-123">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="85796-124">**Тип данных XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="85796-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="85796-125">Расширения XMVECTORU32</span><span class="sxs-lookup"><span data-stu-id="85796-125">XMVECTORU32 Extensions</span></span>](ovw-xmvectoru32-extensions.md)
</dt> </dl>

 

 




