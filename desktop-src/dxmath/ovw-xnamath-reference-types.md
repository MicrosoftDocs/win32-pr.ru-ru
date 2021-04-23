---
description: Библиотека Директксмас предоставляет ряд структур и определенных типов для инкапсуляции данных для поддержки простоты использования, оптимизации и переносимости.
ms.assetid: 4b9ffc17-3917-551c-7cb5-19de505dfd21
title: Типы библиотек Директксмас
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32ac888e451fe1e1ba5cfc66184bf2eb7b6feffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898253"
---
# <a name="directxmath-library-types"></a><span data-ttu-id="0b4b5-103">Типы библиотек Директксмас</span><span class="sxs-lookup"><span data-stu-id="0b4b5-103">DirectXMath Library types</span></span>

<span data-ttu-id="0b4b5-104">Библиотека Директксмас предоставляет ряд структур и определенных типов для инкапсуляции данных для поддержки простоты использования, оптимизации и переносимости.</span><span class="sxs-lookup"><span data-stu-id="0b4b5-104">The DirectXMath Library provides a number of structures and defined types to encapsulate data to support ease of use, optimization, and portability.</span></span>

<span data-ttu-id="0b4b5-105">В приведенном ниже списке содержатся структуры, которые в настоящее время входят в библиотеку Директксмас и доступны в заголовке Директксмас. h.</span><span class="sxs-lookup"><span data-stu-id="0b4b5-105">The list below includes structures currently part of the DirectXMath Library, and available through the DirectXMath.h header.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0b4b5-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="0b4b5-106">In this section</span></span>



| <span data-ttu-id="0b4b5-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="0b4b5-107">Topic</span></span>                                                             | <span data-ttu-id="0b4b5-108">Описание</span><span class="sxs-lookup"><span data-stu-id="0b4b5-108">Description</span></span>                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b4b5-109">**ПОЛОВИНА типа данных**</span><span class="sxs-lookup"><span data-stu-id="0b4b5-109">**HALF Data Type**</span></span>](half-data-type.md)<br/>               | <span data-ttu-id="0b4b5-110">Псевдоним для **UInt16 \_ t** с 16-разрядным числом с плавающей запятой, состоящим из бита знака, 5-битного смещения и 10-разрядной мантисса.</span><span class="sxs-lookup"><span data-stu-id="0b4b5-110">An alias to **uint16\_t** packed with a 16-bit floating-point number consisting of a sign bit, a 5-bit biased exponent, and a 10-bit mantissa.</span></span><br/>                         |
| [<span data-ttu-id="0b4b5-111">**Тип данных КСМВЕКТОР**</span><span class="sxs-lookup"><span data-stu-id="0b4b5-111">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)<br/>       | <span data-ttu-id="0b4b5-112">Переносимый тип, используемый для представления вектора 4 32-разрядных компонентов с плавающей запятой или целых чисел, каждый из которых оптимально соответствует и сопоставляется с регистром аппаратного вектора.</span><span class="sxs-lookup"><span data-stu-id="0b4b5-112">A portable type used to represent a vector of four 32-bit floating-point or integer components, each aligned optimally and mapped to a hardware vector register.</span></span><br/>       |
| [<span data-ttu-id="0b4b5-113">**Тип данных XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="0b4b5-113">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)<br/> | <span data-ttu-id="0b4b5-114">Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки значений с плавающей запятой в экземпляр типа [**ксмвектор**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="0b4b5-114">An opaque, portable type to support the use of C/C++ initializer syntax to load floating-point values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span><br/> |
| [<span data-ttu-id="0b4b5-115">**Тип данных XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="0b4b5-115">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)<br/> | <span data-ttu-id="0b4b5-116">Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки целочисленных значений в экземпляр типа [**ксмвектор**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="0b4b5-116">An opaque, portable type to support the use of C/C++ initializer syntax to load integer values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span><br/>        |
| [<span data-ttu-id="0b4b5-117">**Тип данных XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="0b4b5-117">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)<br/> | <span data-ttu-id="0b4b5-118">Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки \_ значений uint32 t в экземпляр типа ксмвектор.</span><span class="sxs-lookup"><span data-stu-id="0b4b5-118">An opaque, portable type to support the use of C/C++ initializer syntax to load uint32\_t values into an instance of XMVECTOR type.</span></span><br/>                                    |
| [<span data-ttu-id="0b4b5-119">**Тип данных XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="0b4b5-119">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)<br/>   | <span data-ttu-id="0b4b5-120">Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки \_ значений Uint8 t в экземпляр типа ксмвектор.</span><span class="sxs-lookup"><span data-stu-id="0b4b5-120">An opaque, portable type to support the use of C/C++ initializer syntax to load uint8\_t values into an instance of XMVECTOR type.</span></span><br/>                                     |



 

## <a name="related-topics"></a><span data-ttu-id="0b4b5-121">См. также</span><span class="sxs-lookup"><span data-stu-id="0b4b5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b4b5-122">Справочник по программированию Директксмас</span><span class="sxs-lookup"><span data-stu-id="0b4b5-122">DirectXMath Programming Reference</span></span>](ovw-xnamath-reference.md)
</dt> </dl>

 

 




