---
title: include attribute
description: Инструкция ACF include указывает один или несколько файлов заголовков, которые будут включены в созданный код-заглушку.
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- включить атрибут MIDL
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2aab7b7262bceb330e3f4645e4f16035b783197
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104133106"
---
# <a name="include-attribute"></a><span data-ttu-id="eae8d-104">include attribute</span><span class="sxs-lookup"><span data-stu-id="eae8d-104">include attribute</span></span>

<span data-ttu-id="eae8d-105">Инструкция ACF **include** указывает один или несколько файлов заголовков, которые будут включены в созданный код-заглушку.</span><span class="sxs-lookup"><span data-stu-id="eae8d-105">The ACF **include** statement specifies one or more header files to be included in the generated stub code.</span></span>

``` syntax
include filenames;
```

## <a name="parameters"></a><span data-ttu-id="eae8d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eae8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eae8d-107">*имена файлов*</span><span class="sxs-lookup"><span data-stu-id="eae8d-107">*filenames*</span></span> 
</dt> <dd>

<span data-ttu-id="eae8d-108">Указывает имя одного или нескольких файлов заголовков языка C.</span><span class="sxs-lookup"><span data-stu-id="eae8d-108">Specifies the name of one or more C-language header files.</span></span> <span data-ttu-id="eae8d-109">Используйте полное имя файла, включая. Расширение H и заключите каждое имя файла в кавычки.</span><span class="sxs-lookup"><span data-stu-id="eae8d-109">Use the full file name, including the .H extension and enclose each file name in quotation marks.</span></span> <span data-ttu-id="eae8d-110">Разделяйте имена файлов заголовков языка C запятыми.</span><span class="sxs-lookup"><span data-stu-id="eae8d-110">Separate multiple C-language header file names with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eae8d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eae8d-111">Remarks</span></span>

<span data-ttu-id="eae8d-112">В результате выполнения инструкции **include** созданный код-заглушка будет содержать инструкцию C-препроцессор **\# include** .</span><span class="sxs-lookup"><span data-stu-id="eae8d-112">As a result of the **include** statement, the generated stub code will contain a C-preprocessor **\#include** statement.</span></span> <span data-ttu-id="eae8d-113">При компиляции заглушек вы предоставляете заголовочный файл языка C.</span><span class="sxs-lookup"><span data-stu-id="eae8d-113">You supply the C-language header file when compiling the stubs.</span></span> <span data-ttu-id="eae8d-114">Инструкции include используют механизм поиска в структуре каталогов для включенных файлов.</span><span class="sxs-lookup"><span data-stu-id="eae8d-114">Include statements rely on the C-compiler mechanism of searching the directory structure for included files.</span></span>

> [!Note]  
> <span data-ttu-id="eae8d-115">Используйте директиву [**Import**](import.md) вместо директивы **include** для системных файлов, содержащих типы данных, которые необходимо сделать доступными для IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="eae8d-115">Use the [**import**](import.md) directive rather than the **include** directive for system files that contain data types you want to make available to the IDL file.</span></span> <span data-ttu-id="eae8d-116">Директива **Import** игнорирует прототипы функций и позволяет использовать параметры компилятора MIDL, которые оптимизируют создание подпрограмм поддержки.</span><span class="sxs-lookup"><span data-stu-id="eae8d-116">The **import** directive ignores function prototypes and allows you to use MIDL compiler switches that optimize the generation of support routines.</span></span>

 

## <a name="examples"></a><span data-ttu-id="eae8d-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="eae8d-117">Examples</span></span>

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a><span data-ttu-id="eae8d-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eae8d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eae8d-119">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="eae8d-119">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="eae8d-120">**импортиру**</span><span class="sxs-lookup"><span data-stu-id="eae8d-120">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="eae8d-121">Импорт файлов и библиотек типов</span><span class="sxs-lookup"><span data-stu-id="eae8d-121">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="eae8d-122">Импорт системных файлов заголовков</span><span class="sxs-lookup"><span data-stu-id="eae8d-122">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> </dl>

 

 




