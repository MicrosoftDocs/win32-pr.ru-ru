---
title: helpfile - атрибут
description: Атрибут \ HelpFile \ задает имя файла справки для библиотеки типов. Все типы в библиотеке совместно используют один и тот же файл справки.
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- атрибут HelpFile MIDL
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b4283b0285631a710af774d364a01b82c9d44b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790021"
---
# <a name="helpfile-attribute"></a><span data-ttu-id="c6f1d-105">helpfile - атрибут</span><span class="sxs-lookup"><span data-stu-id="c6f1d-105">helpfile attribute</span></span>

<span data-ttu-id="c6f1d-106">Атрибут **\[ HelpFile \]** задает имя файла справки для библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="c6f1d-106">The **\[helpfile\]** attribute sets the name of the Help file for a type library.</span></span> <span data-ttu-id="c6f1d-107">Все типы в библиотеке совместно используют один и тот же файл справки.</span><span class="sxs-lookup"><span data-stu-id="c6f1d-107">All types in a library share the same Help file.</span></span>

``` syntax
[
    uuid(uuid-number), 
    helpfile("filename") 
    [, optional-attribute-list]
] 
library 
{
    library statements
};
```

## <a name="parameters"></a><span data-ttu-id="c6f1d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6f1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6f1d-109">*UUID — номер*</span><span class="sxs-lookup"><span data-stu-id="c6f1d-109">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="c6f1d-110">Задает универсальный уникальный идентификационный номер для [**библиотеки**](library.md).</span><span class="sxs-lookup"><span data-stu-id="c6f1d-110">Specifies a universally unique identification number for the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6f1d-111">*filename*</span><span class="sxs-lookup"><span data-stu-id="c6f1d-111">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="c6f1d-112">Указывает имя файла, содержащего текст справки.</span><span class="sxs-lookup"><span data-stu-id="c6f1d-112">Specifies the name of the file containing the help text.</span></span>

</dd> <dt>

<span data-ttu-id="c6f1d-113">*список необязательных атрибутов*</span><span class="sxs-lookup"><span data-stu-id="c6f1d-113">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c6f1d-114">Указывает ноль или более атрибутов, которые компилятор MIDL будет применять к [**библиотеке**](library.md).</span><span class="sxs-lookup"><span data-stu-id="c6f1d-114">Specifies zero or more attributes that the MIDL compiler will apply to the [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6f1d-115">*библиотечные операторы*</span><span class="sxs-lookup"><span data-stu-id="c6f1d-115">*library statements*</span></span> 
</dt> <dd>

<span data-ttu-id="c6f1d-116">Задает одну или несколько инструкций MIDL, определяющих интерфейс библиотеки.</span><span class="sxs-lookup"><span data-stu-id="c6f1d-116">Specifies one or more MIDL statements that define the library interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6f1d-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6f1d-117">Remarks</span></span>

<span data-ttu-id="c6f1d-118">Для получения имени файла используйте функции **Кодокумента** в интерфейсах **ITypeLib** и **ITypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="c6f1d-118">Use the **GetDocumentation** functions in the **ITypeLib** and **ITypeInfo** interfaces to retrieve the file name.</span></span>

## <a name="examples"></a><span data-ttu-id="c6f1d-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="c6f1d-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpfile("filename.hlp"),
    lcid(0x0409), 
    version(2.0)
]
library Hello
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a><span data-ttu-id="c6f1d-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6f1d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6f1d-121">**библиотека**</span><span class="sxs-lookup"><span data-stu-id="c6f1d-121">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="c6f1d-122">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="c6f1d-122">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="c6f1d-123">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="c6f1d-123">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="c6f1d-124">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="c6f1d-124">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 