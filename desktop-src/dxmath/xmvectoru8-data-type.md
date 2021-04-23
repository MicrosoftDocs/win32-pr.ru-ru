---
description: Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки \_ значений Uint8 t в экземпляр типа ксмвектор.
ms.assetid: ab73ac2c-f178-1bb9-910d-9eef5fc6f5df
title: Тип данных XMVECTORU8 (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4428cdd78206bfa17c295a9578653bb0a66f0c6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704105"
---
# <a name="xmvectoru8-data-type"></a><span data-ttu-id="4bcef-103">Тип данных XMVECTORU8</span><span class="sxs-lookup"><span data-stu-id="4bcef-103">XMVECTORU8 Data Type</span></span>

<span data-ttu-id="4bcef-104">Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки \_ значений Uint8 t в экземпляр типа [**ксмвектор**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="4bcef-104">An opaque, portable type to support the use of C/C++ initializer syntax to load uint8\_t values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORU8 vectoru8;
```



## <a name="remarks"></a><span data-ttu-id="4bcef-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4bcef-105">Remarks</span></span>

<span data-ttu-id="4bcef-106">Список дополнительных функций, таких как конструкторы и операторы, доступных при использовании XMVECTORU8 при программировании в C++, см. в разделе [расширения XMVECTORU8](ovw-xmvectoru8-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="4bcef-106">For a list of additional functionality, such as constructors and operators, available using XMVECTORU8 when programming in C++, see [XMVECTORU8 Extensions](ovw-xmvectoru8-extensions.md).</span></span>

<span data-ttu-id="4bcef-107">Структуры [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)и **XMVECTORU8** предоставляются в качестве механизма создания [**ксмвектор**](xmvector-data-type.md) из различных типов данных констант (с плавающей запятой, целым числом, целым числом и байтом) с помощью инициализаторов.</span><span class="sxs-lookup"><span data-stu-id="4bcef-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md), and **XMVECTORU8** structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="4bcef-108">Это необходимо для поддержки [**ксмвектор**](xmvector-data-type.md), так как сам по себе не поддерживает инициализаторы в целях обеспечения переносимости и оптимизации.</span><span class="sxs-lookup"><span data-stu-id="4bcef-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="4bcef-109">Пример:</span><span class="sxs-lookup"><span data-stu-id="4bcef-109">For example:</span></span>

``` syntax
XMVECTOR data;
XMVECTORU8  byteVector = { (uint8_t)  1,(uint8_t) 16,(uint8_t)101,(uint8_t) 62,
                           (uint8_t)  4,(uint8_t)  0,(uint8_t)  2,(uint8_t) 99,
                           (uint8_t)  9,(uint8_t) 18,(uint8_t)  0,(uint8_t)  0,
                           (uint8_t)100,(uint8_t) 51,(uint8_t) 23,(uint8_t)117};

data = floatingVector;
```

<span data-ttu-id="4bcef-110">**Пространство имен**. Использование DirectX</span><span class="sxs-lookup"><span data-stu-id="4bcef-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="4bcef-111">Требования к платформе</span><span class="sxs-lookup"><span data-stu-id="4bcef-111">Platform Requirements</span></span>

<span data-ttu-id="4bcef-112">Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4bcef-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="4bcef-113">Поддерживается для классических приложений Win32, приложений для Магазина Windows и Windows Phone 8 приложений.</span><span class="sxs-lookup"><span data-stu-id="4bcef-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bcef-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4bcef-114">Requirements</span></span>



| <span data-ttu-id="4bcef-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4bcef-115">Requirement</span></span> | <span data-ttu-id="4bcef-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4bcef-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bcef-117">Header</span><span class="sxs-lookup"><span data-stu-id="4bcef-117">Header</span></span><br/> | <dl> <span data-ttu-id="4bcef-118"><dt>Директксмас. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bcef-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bcef-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4bcef-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bcef-120">Типы библиотек Директксмас</span><span class="sxs-lookup"><span data-stu-id="4bcef-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="4bcef-121">**Тип данных КСМВЕКТОР**</span><span class="sxs-lookup"><span data-stu-id="4bcef-121">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="4bcef-122">**Тип данных XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="4bcef-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="4bcef-123">**Тип данных XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="4bcef-123">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="4bcef-124">**Тип данных XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="4bcef-124">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="4bcef-125">Расширения XMVECTORU8</span><span class="sxs-lookup"><span data-stu-id="4bcef-125">XMVECTORU8 Extensions</span></span>](ovw-xmvectoru8-extensions.md)
</dt> </dl>

 

 




