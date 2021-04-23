---
title: атрибут хелпстрингдлл
description: Атрибут \ хелпстрингдлл \ задает имя библиотеки DLL, используемой для поиска строки документа.
ms.assetid: 1b9b962c-c355-4428-b5ea-dc7fd48b50a9
keywords:
- атрибут хелпстрингдлл MIDL
topic_type:
- apiref
api_name:
- helpstringdll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dace4fb9ddc3908ce637cd2d8521a1ab4671d620
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987409"
---
# <a name="helpstringdll-attribute"></a><span data-ttu-id="86778-104">атрибут хелпстрингдлл</span><span class="sxs-lookup"><span data-stu-id="86778-104">helpstringdll attribute</span></span>

<span data-ttu-id="86778-105">Атрибут **\[ хелпстрингдлл \]** задает имя библиотеки DLL, используемой для поиска строки документа.</span><span class="sxs-lookup"><span data-stu-id="86778-105">The **\[helpstringdll\]** attribute sets the name of the DLL to use to perform a document string lookup.</span></span>

``` syntax
[
    helpstringdll(help-text-string)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
};
```

## <a name="parameters"></a><span data-ttu-id="86778-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="86778-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86778-107">*Справка-текстовая строка*</span><span class="sxs-lookup"><span data-stu-id="86778-107">*help-text-string*</span></span> 
</dt> <dd>

<span data-ttu-id="86778-108">Строка символов с нулевым нулем, указывающая полное имя файла DLL.</span><span class="sxs-lookup"><span data-stu-id="86778-108">A zero-terminated string of characters specifying the fully qualified file name of a DLL.</span></span>

</dd> <dt>

<span data-ttu-id="86778-109">*список необязательных атрибутов*</span><span class="sxs-lookup"><span data-stu-id="86778-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="86778-110">Другие атрибуты, применяемые к оператору Library в целом.</span><span class="sxs-lookup"><span data-stu-id="86778-110">Other attributes that apply to the library statement as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="86778-111">*имя библиотеки*</span><span class="sxs-lookup"><span data-stu-id="86778-111">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="86778-112">Идентификатор, который программные компоненты будут использовать для обозначения этой [**библиотеки**](library.md).</span><span class="sxs-lookup"><span data-stu-id="86778-112">The identifier that software components will use to denote this [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="86778-113">*Library-операторы определения*</span><span class="sxs-lookup"><span data-stu-id="86778-113">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="86778-114">Одна или несколько инструкций MIDL, которые определяют интерфейс [**библиотеки**](library.md).</span><span class="sxs-lookup"><span data-stu-id="86778-114">One or more MIDL statement which define the interface of the [**library**](library.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86778-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86778-115">Remarks</span></span>

<span data-ttu-id="86778-116">Используйте атрибут **\[ хелпстрингдлл \]** в операторе Library, чтобы указать в виде символьной строки полное имя файла библиотеки динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="86778-116">Use the **\[helpstringdll\]** attribute on a library statement to specify, as a character string, the fully qualified file name of a dynamic link library.</span></span> <span data-ttu-id="86778-117">Это позволяет пользователю просматривать описание библиотеки DLL с помощью средства просмотра объектов.</span><span class="sxs-lookup"><span data-stu-id="86778-117">This allows a user to view a description of the DLL with the object viewer.</span></span>

<span data-ttu-id="86778-118">Используйте функции **GetDocumentation2** в интерфейсах **ITypeLib2** и **ITypeInfo2** , чтобы получить строку справки.</span><span class="sxs-lookup"><span data-stu-id="86778-118">Use the **GetDocumentation2** functions in the **ITypeLib2** and **ITypeInfo2** interfaces to retrieve the help string.</span></span>

## <a name="see-also"></a><span data-ttu-id="86778-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86778-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86778-120">**библиотека**</span><span class="sxs-lookup"><span data-stu-id="86778-120">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="86778-121">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="86778-121">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="86778-122">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="86778-122">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="86778-123">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="86778-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 