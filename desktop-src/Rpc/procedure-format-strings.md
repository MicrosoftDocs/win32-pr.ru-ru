---
title: Строки формата процедур
description: Ниже приведено полное описание строки формата. Он собирает все уровни, связанные с разными этапами развития интерпретатора.
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e58a9acf10caad23063bdba117dc402e411638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987745"
---
# <a name="procedure-format-strings"></a><span data-ttu-id="3d865-104">Строки формата процедур</span><span class="sxs-lookup"><span data-stu-id="3d865-104">Procedure Format Strings</span></span>

<span data-ttu-id="3d865-105">Ниже приведено полное описание строки формата.</span><span class="sxs-lookup"><span data-stu-id="3d865-105">The following is a complete format string description.</span></span> <span data-ttu-id="3d865-106">Он собирает все уровни, связанные с разными этапами развития интерпретатора.</span><span class="sxs-lookup"><span data-stu-id="3d865-106">It assembles all layers related to different stages of the interpreter evolution.</span></span>

## <a name="procedure-descriptor-overview"></a><span data-ttu-id="3d865-107">Обзор дескрипторов процедур</span><span class="sxs-lookup"><span data-stu-id="3d865-107">Procedure Descriptor Overview</span></span>

<span data-ttu-id="3d865-108">Дескриптор процедуры состоит из описательов заголовков и описательных параметров.</span><span class="sxs-lookup"><span data-stu-id="3d865-108">A procedure descriptor consists of the header descriptors and the parameter descriptors.</span></span> <span data-ttu-id="3d865-109">Описание стиля [**– Oi**](/windows/desktop/Midl/-oi) считается устаревшим, в терминах общего использования в текущем программировании RPC.</span><span class="sxs-lookup"><span data-stu-id="3d865-109">The [**–Oi**](/windows/desktop/Midl/-oi) style description is considered outdated, in terms of common usage in current RPC programming.</span></span> <span data-ttu-id="3d865-110">Параметр **– ОИФ** считается более актуальным.</span><span class="sxs-lookup"><span data-stu-id="3d865-110">The **–Oif** is considered more current.</span></span>

## <a name="the-oi-style-description"></a><span data-ttu-id="3d865-111">Описание стиля – OI</span><span class="sxs-lookup"><span data-stu-id="3d865-111">The –Oi Style Description</span></span>

<span data-ttu-id="3d865-112">Это описание состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="3d865-112">This description consists of the following:</span></span>

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

<span data-ttu-id="3d865-113">Заголовок будет содержать от 6 до 16 байт.</span><span class="sxs-lookup"><span data-stu-id="3d865-113">The header would have from 6 to 16 bytes.</span></span>

<span data-ttu-id="3d865-114">Полное описание создается при компиляции в режиме [**– Oi**](/windows/desktop/Midl/-oi) .</span><span class="sxs-lookup"><span data-stu-id="3d865-114">The complete description is generated when compiling in [**–Oi**](/windows/desktop/Midl/-oi) mode.</span></span> <span data-ttu-id="3d865-115">В режиме [**операционной системы**](/windows/desktop/Midl/-os) создаются только дескрипторы параметров, которые используются для преобразования.</span><span class="sxs-lookup"><span data-stu-id="3d865-115">In [**–Os**](/windows/desktop/Midl/-os) mode, only the parameter descriptors are generated, which are used for conversion.</span></span> <span data-ttu-id="3d865-116">Интерпретатор в поле выбора использует устаревшие дескрипторы параметров стиля.</span><span class="sxs-lookup"><span data-stu-id="3d865-116">The pickling interpreter uses old style parameter descriptors.</span></span>

## <a name="the-oif-style-description"></a><span data-ttu-id="3d865-117">Описание стиля – ОИФ</span><span class="sxs-lookup"><span data-stu-id="3d865-117">The –Oif Style Description</span></span>

<span data-ttu-id="3d865-118">Описание состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="3d865-118">The description consists of the following:</span></span>

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

<span data-ttu-id="3d865-119">Дескриптор заголовка стиля [**– ОИФ**](/windows/desktop/Midl/-oi) состоит из</span><span class="sxs-lookup"><span data-stu-id="3d865-119">The [**–Oif**](/windows/desktop/Midl/-oi) style header descriptor consists of</span></span>

<span data-ttu-id="3d865-120">Описание стиля – ОИФ создается при компиляции в режиме компилятора [**– ОИФ**](/windows/desktop/Midl/-oi) или **– оикф** .</span><span class="sxs-lookup"><span data-stu-id="3d865-120">The –Oif style description is generated when compiling in [**–Oif**](/windows/desktop/Midl/-oi) or **–Oicf** mode of the compiler.</span></span>

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

<span data-ttu-id="3d865-121">Некоторые более новые функции, такие как pipe, async и [**/robust**](/windows/desktop/Midl/-robust) , принудительно используют режим [**– оикф**](/windows/desktop/Midl/-oi) компилятора при его использовании.</span><span class="sxs-lookup"><span data-stu-id="3d865-121">Some more recent features like pipe, async, and [**/robust**](/windows/desktop/Midl/-robust) force the [**–Oicf**](/windows/desktop/Midl/-oi) mode of the compiler, when used.</span></span>

## <a name="the-extended-oif-description"></a><span data-ttu-id="3d865-122">Расширенное описание – ОИФ</span><span class="sxs-lookup"><span data-stu-id="3d865-122">The Extended –Oif Description</span></span>

<span data-ttu-id="3d865-123">Описание состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="3d865-123">The description consists of the following:</span></span>

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 