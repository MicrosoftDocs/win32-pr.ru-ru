---
title: importlib - атрибут
description: Директива \ importlib \ делает типы, которые уже были скомпилированы в другую библиотеку типов, доступными для создаваемой библиотеки типов.
ms.assetid: d5f15a77-c6b1-4918-be86-07d2995ca2d4
keywords:
- атрибут importlib MIDL
topic_type:
- apiref
api_name:
- importlib
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b9c233103330e9f8ae7318a613cbc5103315a74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487545"
---
# <a name="importlib-attribute"></a><span data-ttu-id="6cff9-104">importlib - атрибут</span><span class="sxs-lookup"><span data-stu-id="6cff9-104">importlib attribute</span></span>

<span data-ttu-id="6cff9-105">Директива **\[ importlib \]** делает типы, которые уже были скомпилированы в другую библиотеку типов, доступными для создаваемой библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="6cff9-105">The **\[importlib\]** directive makes types that have already been compiled into another type library available to the type library being created.</span></span>

``` syntax
[
    library-attributes
]
library (library-name)
{
    importlib(file-to-import); 
    ... 
}
```

## <a name="parameters"></a><span data-ttu-id="6cff9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6cff9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cff9-107">*атрибуты библиотеки*</span><span class="sxs-lookup"><span data-stu-id="6cff9-107">*library-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="6cff9-108">Ноль или более атрибутов, которые будут применены к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="6cff9-108">Zero or more attributes that will be applied to the library.</span></span>

</dd> <dt>

<span data-ttu-id="6cff9-109">*имя библиотеки*</span><span class="sxs-lookup"><span data-stu-id="6cff9-109">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6cff9-110">Идентификатор, который программные компоненты будут использовать для обозначения этой [**библиотеки**](library.md).</span><span class="sxs-lookup"><span data-stu-id="6cff9-110">The identifier that software components will use to denote this [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cff9-111">*файл для импорта*</span><span class="sxs-lookup"><span data-stu-id="6cff9-111">*file-to-import*</span></span> 
</dt> <dd>

<span data-ttu-id="6cff9-112">Имя и расположение импортируемого файла во время компиляции MIDL.</span><span class="sxs-lookup"><span data-stu-id="6cff9-112">The name and location of the imported file at MIDL compile-time.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6cff9-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6cff9-113">Remarks</span></span>

<span data-ttu-id="6cff9-114">Все директивы **\[ importlib \]** должны предшествовать описаниям других типов в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="6cff9-114">All **\[importlib\]** directives must precede the other type descriptions in the library.</span></span> <span data-ttu-id="6cff9-115">Обратите внимание, что Импортированная библиотека, а также созданная библиотека, должна быть распространена вместе с приложением, чтобы она была доступна во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="6cff9-115">Note that the imported library, as well as the generated library, must be distributed with the application so that it is available at run time.</span></span>

<span data-ttu-id="6cff9-116">В большинстве случаев директиву импорта MIDL следует использовать **\[** [](import.md) **\]** для ссылки на определения из другого. IDL-файл в. IDL-файл.</span><span class="sxs-lookup"><span data-stu-id="6cff9-116">In most cases you should use the MIDL **\[**[**import**](import.md)**\]** directive to reference definitions from another .IDL file in your .IDL file.</span></span> <span data-ttu-id="6cff9-117">Этот метод предоставляет библиотеке типов все данные из исходного файла, тогда как **\[ importlib \]** помещает только содержимое библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="6cff9-117">This method provides your type library with all the information from the original file, whereas **\[importlib\]** only brings in the contents of the type library.</span></span>

> [!Note]  
> <span data-ttu-id="6cff9-118">Директива **\[ importlib \]** делает любой тип, определенный в импортируемой библиотеке, доступным в компилируемой библиотеке.</span><span class="sxs-lookup"><span data-stu-id="6cff9-118">The **\[importlib\]** directive makes any type defined in the imported library accessible from within the library being compiled.</span></span> <span data-ttu-id="6cff9-119">Чтобы избежать неоднозначности при наличии повторяющихся ссылок, рекомендуется определить каждую из этих ссылок с использованием соответствующего имени библиотеки, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="6cff9-119">To avoid ambiguity when there are duplicate references, we recommend that you qualify each such reference with the appropriate library name, as follows:</span></span>

 

``` syntax
library_name.type
```

<span data-ttu-id="6cff9-120">В отсутствие такой квалификации MIDL разрешает неоднозначность повторяющейся ссылки следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6cff9-120">In the absence of such qualification, MIDL resolves duplicate reference ambiguity as follows:</span></span>

-   <span data-ttu-id="6cff9-121">Начиная с версии 3,1, MIDL использует первую найденную ссылку.</span><span class="sxs-lookup"><span data-stu-id="6cff9-121">Effective with version 3.1, MIDL uses the first reference it finds.</span></span>
-   <span data-ttu-id="6cff9-122">Версия 3,0 MIDL, первая версия MIDL, способная формировать библиотеки типов, использует последнюю найденную ссылку.</span><span class="sxs-lookup"><span data-stu-id="6cff9-122">Version 3.0 of MIDL, the first version of MIDL that could generate type libraries, uses the last reference it found.</span></span>

## <a name="examples"></a><span data-ttu-id="6cff9-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="6cff9-123">Examples</span></span>

``` syntax
library BrowseHelper 
{ 
    importlib("stdole32.tlb"); 
    importlib("mydisp.tlb"); 
    //Remainder of library definition 
};
```

## <a name="see-also"></a><span data-ttu-id="6cff9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6cff9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cff9-125">**библиотека**</span><span class="sxs-lookup"><span data-stu-id="6cff9-125">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="6cff9-126">**импортиру**</span><span class="sxs-lookup"><span data-stu-id="6cff9-126">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="6cff9-127">Импорт системных файлов заголовков</span><span class="sxs-lookup"><span data-stu-id="6cff9-127">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> <dt>

[<span data-ttu-id="6cff9-128">Импорт файлов и библиотек типов</span><span class="sxs-lookup"><span data-stu-id="6cff9-128">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="6cff9-129">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="6cff9-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="6cff9-130">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="6cff9-130">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="6cff9-131">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="6cff9-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 