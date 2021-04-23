---
description: Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки целочисленных значений в экземпляр типа КСМВЕКТОР.
ms.assetid: 6564030e-b6e9-0c4f-4e2a-4132e4264c94
title: Тип данных XMVECTORI32 (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ac36caf97a62037223840e9220876f1c7a1f09a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649095"
---
# <a name="xmvectori32-data-type"></a><span data-ttu-id="abe31-103">Тип данных XMVECTORI32</span><span class="sxs-lookup"><span data-stu-id="abe31-103">XMVECTORI32 Data Type</span></span>

<span data-ttu-id="abe31-104">Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки целочисленных значений в экземпляр типа [**ксмвектор**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="abe31-104">An opaque, portable type to support the use of C/C++ initializer syntax to load integer values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORI32 vectori32;
```



## <a name="remarks"></a><span data-ttu-id="abe31-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="abe31-105">Remarks</span></span>

<span data-ttu-id="abe31-106">Список дополнительных функций, таких как конструкторы и операторы, доступных `XMVECTORI32` при использовании при программировании в C++, см. в разделе [расширения XMVECTORI32](ovw-xmvectori32-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="abe31-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTORI32` when programming in C++, see [XMVECTORI32 Extensions](ovw-xmvectori32-extensions.md).</span></span>

<span data-ttu-id="abe31-107">Структуры [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32** и [**XMVECTORU8**](xmvectoru8-data-type.md) предоставляются в качестве механизма создания [**ксмвектор**](xmvector-data-type.md) из различных типов данных констант (с плавающей запятой, целым числом, целым числом и байтом) с помощью инициализаторов.</span><span class="sxs-lookup"><span data-stu-id="abe31-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32**, and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="abe31-108">Это необходимо для поддержки [**ксмвектор**](xmvector-data-type.md), так как сам по себе не поддерживает инициализаторы в целях обеспечения переносимости и оптимизации.</span><span class="sxs-lookup"><span data-stu-id="abe31-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="abe31-109">Пример:</span><span class="sxs-lookup"><span data-stu-id="abe31-109">For example:</span></span>


```
XMVECTOR data;
XMVECTORI32 intVector = { -1, 5, 33, 0 };
data = intVector;
```



<span data-ttu-id="abe31-110">**Пространство имен**. Использование DirectX</span><span class="sxs-lookup"><span data-stu-id="abe31-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="abe31-111">Требования к платформе</span><span class="sxs-lookup"><span data-stu-id="abe31-111">Platform Requirements</span></span>

<span data-ttu-id="abe31-112">Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="abe31-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="abe31-113">Поддерживается для классических приложений Win32, приложений для Магазина Windows и Windows Phone 8 приложений.</span><span class="sxs-lookup"><span data-stu-id="abe31-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="abe31-114">Требования</span><span class="sxs-lookup"><span data-stu-id="abe31-114">Requirements</span></span>



| <span data-ttu-id="abe31-115">Требование</span><span class="sxs-lookup"><span data-stu-id="abe31-115">Requirement</span></span> | <span data-ttu-id="abe31-116">Значение</span><span class="sxs-lookup"><span data-stu-id="abe31-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="abe31-117">Header</span><span class="sxs-lookup"><span data-stu-id="abe31-117">Header</span></span><br/> | <dl> <span data-ttu-id="abe31-118"><dt>Директксмас. h</dt></span><span class="sxs-lookup"><span data-stu-id="abe31-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abe31-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abe31-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe31-120">Типы библиотек Директксмас</span><span class="sxs-lookup"><span data-stu-id="abe31-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="abe31-121">**Тип данных КСМВЕКТОР**</span><span class="sxs-lookup"><span data-stu-id="abe31-121">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="abe31-122">**Тип данных XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="abe31-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="abe31-123">**Тип данных XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="abe31-123">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="abe31-124">**Тип данных XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="abe31-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="abe31-125">**Тип данных XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="abe31-125">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> </dl>

 

 




