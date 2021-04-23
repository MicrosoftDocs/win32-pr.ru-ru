---
title: Использование C/C++-препроцессора с помощью MIDL
description: Компилятор MIDL не выполняет предварительную обработку исходных файлов.
ms.assetid: 0f62d2a4-cfc3-42a7-b3a6-4e5c67c7c849
keywords:
- MIDL компилятора MIDL, C-препроцессор
- C-препроцессор MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5752bd64ee9a9b5fc26d586b5bc33c1a1fb96e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329563"
---
# <a name="using-cc-preprocessor-with-midl"></a><span data-ttu-id="d1169-105">Использование C/C++-препроцессора с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="d1169-105">Using C/C++-Preprocessor with MIDL</span></span>

<span data-ttu-id="d1169-106">Компилятор MIDL не выполняет предварительную обработку исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="d1169-106">The MIDL compiler does not preprocess source files.</span></span> <span data-ttu-id="d1169-107">Вместо этого компилятор MIDL использует доступный препроцессор для подготовки входного потока для синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="d1169-107">Rather, the MIDL compiler uses an available preprocessor to prepare the input stream for parsing.</span></span> <span data-ttu-id="d1169-108">По умолчанию MIDL использует препроцессор для компилятора Microsoft C/C++ из той же среды разработки, что и MIDL.</span><span class="sxs-lookup"><span data-stu-id="d1169-108">By default, MIDL uses the preprocessor for the Microsoft C/C++ compiler from the same building environment as MIDL.</span></span> <span data-ttu-id="d1169-109">При необходимости пользователь может указать другой препроцессор, который будет использоваться MIDL.</span><span class="sxs-lookup"><span data-stu-id="d1169-109">The user can indicate a different preprocessor to be used by MIDL, if needed.</span></span>

<span data-ttu-id="d1169-110">MIDL порождает отдельные запуски препроцессора для файлов IDL и ACF верхнего уровня, а также для каждого файла, импортированного с помощью директивы MIDL Import.</span><span class="sxs-lookup"><span data-stu-id="d1169-110">MIDL spawns separate preprocessor runs for top-level IDL and ACF files, and for each file imported with the MIDL import directive.</span></span> <span data-ttu-id="d1169-111">Файлы, включенные в директиву **\# include** , обрабатываются препроцессором напрямую.</span><span class="sxs-lookup"><span data-stu-id="d1169-111">Files included with the **\#include** directive are handled by the preprocessor directly.</span></span>

<span data-ttu-id="d1169-112">В следующих разделах описываются различные аспекты взаимодействия с препроцессором MIDL:</span><span class="sxs-lookup"><span data-stu-id="d1169-112">The following topics describe various aspects of MIDL-preprocessor interactions:</span></span>

-   [<span data-ttu-id="d1169-113">Требования к препроцессору C-препроцессор для MIDL</span><span class="sxs-lookup"><span data-stu-id="d1169-113">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
-   [<span data-ttu-id="d1169-114">Проверка параметров препроцессора</span><span class="sxs-lookup"><span data-stu-id="d1169-114">Verifying Preprocessor Options</span></span>](verifying-preprocessor-options.md)
-   [<span data-ttu-id="d1169-115">Сохранение выходных данных препроцессора</span><span class="sxs-lookup"><span data-stu-id="d1169-115">Saving Preprocessor Output</span></span>](saving-preprocessor-output.md)
-   [<span data-ttu-id="d1169-116">Работа с \# определениями в IDL-файлах</span><span class="sxs-lookup"><span data-stu-id="d1169-116">Dealing with \#defines in IDL Files</span></span>](dealing-with-defines-in-idl-files-2.md)

 

 




