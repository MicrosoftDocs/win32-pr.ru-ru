---
title: Выходные данные компилятора MIDL
description: Используя файлы IDL и ACF в качестве входных данных, компилятор MIDL создает до пяти исходных файлов C-Language.
ms.assetid: 151bd643-1da0-4b33-b8a3-3d7037e63319
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb45bb369ea9d5faa695bf2658f3bafe2b3cb3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067608"
---
# <a name="midl-compiler-output"></a><span data-ttu-id="a9d0c-103">Выходные данные компилятора MIDL</span><span class="sxs-lookup"><span data-stu-id="a9d0c-103">MIDL Compiler Output</span></span>

<span data-ttu-id="a9d0c-104">Используя файлы IDL и ACF в качестве входных данных, компилятор MIDL создает до пяти исходных файлов C-Language.</span><span class="sxs-lookup"><span data-stu-id="a9d0c-104">With the IDL and ACF files as input, the MIDL compiler generates up to five C-language source files.</span></span> <span data-ttu-id="a9d0c-105">По умолчанию компилятор MIDL использует базовое имя файла IDL-файла в составе созданных файлов заглушек.</span><span class="sxs-lookup"><span data-stu-id="a9d0c-105">By default, the MIDL compiler uses the base file name of the IDL file as part of the generated stub files.</span></span> <span data-ttu-id="a9d0c-106">Если в базовом имени файла имеется более шести символов, некоторые файловые системы могут не принимать полное имя заглушки.</span><span class="sxs-lookup"><span data-stu-id="a9d0c-106">When more than six characters are present in the base file name, some file systems may not accept the full stub name.</span></span> <span data-ttu-id="a9d0c-107">В следующей таблице показаны соглашения, используемые для имен файлов.</span><span class="sxs-lookup"><span data-stu-id="a9d0c-107">The following table shows conventions used for file names.</span></span>



| <span data-ttu-id="a9d0c-108">Файл</span><span class="sxs-lookup"><span data-stu-id="a9d0c-108">File</span></span>        | <span data-ttu-id="a9d0c-109">Часть имени базового файла по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a9d0c-109">Default portion of base file name</span></span> | <span data-ttu-id="a9d0c-110">Пример</span><span class="sxs-lookup"><span data-stu-id="a9d0c-110">Example</span></span>      |
|-------------|-----------------------------------|--------------|
| <span data-ttu-id="a9d0c-111">IDL-файл</span><span class="sxs-lookup"><span data-stu-id="a9d0c-111">IDL file</span></span>    | ---                               | <span data-ttu-id="a9d0c-112">Абкдефгх. idl</span><span class="sxs-lookup"><span data-stu-id="a9d0c-112">Abcdefgh.idl</span></span> |
| <span data-ttu-id="a9d0c-113">Header</span><span class="sxs-lookup"><span data-stu-id="a9d0c-113">Header</span></span>      | <span data-ttu-id="a9d0c-114">.h</span><span class="sxs-lookup"><span data-stu-id="a9d0c-114">.h</span></span>                                | <span data-ttu-id="a9d0c-115">Abcdef. h</span><span class="sxs-lookup"><span data-stu-id="a9d0c-115">Abcdef.h</span></span>     |
| <span data-ttu-id="a9d0c-116">Заглушка клиента</span><span class="sxs-lookup"><span data-stu-id="a9d0c-116">Client stub</span></span> | <span data-ttu-id="a9d0c-117">\_c. c</span><span class="sxs-lookup"><span data-stu-id="a9d0c-117">\_c.c</span></span>                             | <span data-ttu-id="a9d0c-118">Abcdef \_ c. c</span><span class="sxs-lookup"><span data-stu-id="a9d0c-118">Abcdef\_c.c</span></span>  |
| <span data-ttu-id="a9d0c-119">Заглушка сервера</span><span class="sxs-lookup"><span data-stu-id="a9d0c-119">Server stub</span></span> | <span data-ttu-id="a9d0c-120">\_s. c</span><span class="sxs-lookup"><span data-stu-id="a9d0c-120">\_s.c</span></span>                             | <span data-ttu-id="a9d0c-121">Abcdef \_ s. c</span><span class="sxs-lookup"><span data-stu-id="a9d0c-121">Abcdef\_s.c</span></span>  |



 

 

 




