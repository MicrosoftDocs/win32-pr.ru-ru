---
title: атрибут dllname (STR)
description: Атрибут \ dllname \ определяет имя библиотеки DLL, содержащей точки входа для модуля.
ms.assetid: dbf062ce-9dcc-4cc6-b7cd-cdc5945e399b
keywords:
- атрибут dllname (STR) MIDL
topic_type:
- apiref
api_name:
- dllname(str)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 990d277db855c2988021d19a0a756c49454546f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069989"
---
# <a name="dllnamestr-attribute"></a><span data-ttu-id="8b3f0-104">атрибут dllname (STR)</span><span class="sxs-lookup"><span data-stu-id="8b3f0-104">dllname(str) attribute</span></span>

<span data-ttu-id="8b3f0-105">Атрибут **\[ dllname \]** определяет имя библиотеки DLL, содержащей точки входа для модуля.</span><span class="sxs-lookup"><span data-stu-id="8b3f0-105">The **\[dllname\]** attribute defines the name of the DLL that contains the entry points for a module.</span></span>

``` syntax
[
    uuid(uuid-number), 
    dllname("filename")
    [, optional-attribute-list]
]
module modulename
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="8b3f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b3f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b3f0-107">*UUID — номер*</span><span class="sxs-lookup"><span data-stu-id="8b3f0-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="8b3f0-108">Задает универсальный уникальный идентификационный номер для [**модуля**](module.md).</span><span class="sxs-lookup"><span data-stu-id="8b3f0-108">Specifies a universally unique identification number for the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b3f0-109">*filename*</span><span class="sxs-lookup"><span data-stu-id="8b3f0-109">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="8b3f0-110">Указывает строку, завершающуюся НУЛЕМ, которая содержит полный путь к DLL-файлу.</span><span class="sxs-lookup"><span data-stu-id="8b3f0-110">Specifies a NULL-terminated string which contains the full path to the Dll file.</span></span>

</dd> <dt>

<span data-ttu-id="8b3f0-111">*список необязательных атрибутов*</span><span class="sxs-lookup"><span data-stu-id="8b3f0-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8b3f0-112">Указывает список атрибутов интерфейса MIDL, отданных от нуля или более.</span><span class="sxs-lookup"><span data-stu-id="8b3f0-112">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="8b3f0-113">*ModuleName*</span><span class="sxs-lookup"><span data-stu-id="8b3f0-113">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="8b3f0-114">Указывает имя, которое другие программные компоненты могут использовать для ссылки на модуль.</span><span class="sxs-lookup"><span data-stu-id="8b3f0-114">Specifies the name which other software components can use to refer to the module.</span></span>

</dd> <dt>

<span data-ttu-id="8b3f0-115">*елементлист*</span><span class="sxs-lookup"><span data-stu-id="8b3f0-115">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="8b3f0-116">Указывает одну или несколько инструкций определения элемента модуля.</span><span class="sxs-lookup"><span data-stu-id="8b3f0-116">Specifies one or more module element definition statements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b3f0-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b3f0-117">Remarks</span></span>

<span data-ttu-id="8b3f0-118">Атрибут **\[ dllname \]** является обязательным для модуля.</span><span class="sxs-lookup"><span data-stu-id="8b3f0-118">The **\[dllname\]** attribute is required on a module.</span></span>

## <a name="examples"></a><span data-ttu-id="8b3f0-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="8b3f0-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("A meaningful comment"),   
    dllname("HANDY.DLL")
] 
module HandyStuff
{
    /* Module content definitions */
};
```

## <a name="see-also"></a><span data-ttu-id="8b3f0-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b3f0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b3f0-121">**модуль**</span><span class="sxs-lookup"><span data-stu-id="8b3f0-121">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="8b3f0-122">**операции**</span><span class="sxs-lookup"><span data-stu-id="8b3f0-122">**entry**</span></span>](entry.md)
</dt> <dt>

[<span data-ttu-id="8b3f0-123">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="8b3f0-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="8b3f0-124">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="8b3f0-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="8b3f0-125">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="8b3f0-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 