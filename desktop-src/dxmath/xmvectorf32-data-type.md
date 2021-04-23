---
description: Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки значений с плавающей запятой в экземпляр типа КСМВЕКТОР.
ms.assetid: bafaa59f-fd1b-e252-cbbd-903df796fde0
title: Тип данных XMVECTORF32 (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e56e79ea678ede0afcac3523c09da725ede00d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648813"
---
# <a name="xmvectorf32-data-type"></a><span data-ttu-id="bc1a5-103">Тип данных XMVECTORF32</span><span class="sxs-lookup"><span data-stu-id="bc1a5-103">XMVECTORF32 Data Type</span></span>

<span data-ttu-id="bc1a5-104">Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки значений с плавающей запятой в экземпляр типа [**ксмвектор**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="bc1a5-104">An opaque, portable type to support the use of C/C++ initializer syntax to load floating-point values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORF32 vectorf32;
```



## <a name="remarks"></a><span data-ttu-id="bc1a5-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc1a5-105">Remarks</span></span>

<span data-ttu-id="bc1a5-106">Список дополнительных функций, таких как конструкторы и операторы, доступных `XMVECTORF32` при использовании при программировании в C++, см. в разделе [расширения XMVECTORF32](ovw-xmvectorf32-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="bc1a5-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTORF32` when programming in C++, see [XMVECTORF32 Extensions](ovw-xmvectorf32-extensions.md).</span></span>

<span data-ttu-id="bc1a5-107">Структуры **XMVECTORF32**, [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)и [**XMVECTORU8**](xmvectoru8-data-type.md) предоставляются в качестве механизма создания [**ксмвектор**](xmvector-data-type.md) из различных типов данных констант (с плавающей запятой, целым числом, целым числом и байтом) с помощью инициализаторов.</span><span class="sxs-lookup"><span data-stu-id="bc1a5-107">The **XMVECTORF32**, [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md), and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="bc1a5-108">Это необходимо для поддержки [**ксмвектор**](xmvector-data-type.md), так как сам по себе не поддерживает инициализаторы в целях обеспечения переносимости и оптимизации.</span><span class="sxs-lookup"><span data-stu-id="bc1a5-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="bc1a5-109">Пример:</span><span class="sxs-lookup"><span data-stu-id="bc1a5-109">For example:</span></span>


```
XMVECTOR data;
XMVECTORF32 floatingVector = { 0.f, 0.f, 0.1f, 1.f };
data = floatingVector;
```



<span data-ttu-id="bc1a5-110">**Пространство имен**. Использование DirectX</span><span class="sxs-lookup"><span data-stu-id="bc1a5-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="bc1a5-111">Требования к платформе</span><span class="sxs-lookup"><span data-stu-id="bc1a5-111">Platform Requirements</span></span>

<span data-ttu-id="bc1a5-112">Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bc1a5-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="bc1a5-113">Поддерживается для классических приложений Win32, приложений для Магазина Windows и Windows Phone 8 приложений.</span><span class="sxs-lookup"><span data-stu-id="bc1a5-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc1a5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bc1a5-114">Requirements</span></span>



| <span data-ttu-id="bc1a5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="bc1a5-115">Requirement</span></span> | <span data-ttu-id="bc1a5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="bc1a5-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc1a5-117">Header</span><span class="sxs-lookup"><span data-stu-id="bc1a5-117">Header</span></span><br/> | <dl> <span data-ttu-id="bc1a5-118"><dt>Директксмас. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc1a5-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc1a5-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc1a5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc1a5-120">Типы библиотек Директксмас</span><span class="sxs-lookup"><span data-stu-id="bc1a5-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="bc1a5-121">**Тип данных XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="bc1a5-121">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="bc1a5-122">**Тип данных КСМВЕКТОР**</span><span class="sxs-lookup"><span data-stu-id="bc1a5-122">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="bc1a5-123">**Тип данных XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="bc1a5-123">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="bc1a5-124">**Тип данных XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="bc1a5-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="bc1a5-125">**Тип данных XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="bc1a5-125">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> </dl>

 

 




