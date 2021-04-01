---
title: readonly - атрибут
description: Атрибут \ ReadOnly \ запрещает Присваивание переменной.
ms.assetid: b81064e6-e788-48d1-9958-203f1e3c7e4d
keywords:
- атрибут ReadOnly MIDL
topic_type:
- apiref
api_name:
- readonly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4ef4ca5f32b96146ed5ab0ec085d32b24dca3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987461"
---
# <a name="readonly-attribute"></a><span data-ttu-id="c6abe-104">readonly - атрибут</span><span class="sxs-lookup"><span data-stu-id="c6abe-104">readonly attribute</span></span>

<span data-ttu-id="c6abe-105">Атрибут **\[ ReadOnly \]** запрещает Присваивание переменной.</span><span class="sxs-lookup"><span data-stu-id="c6abe-105">The **\[readonly\]** attribute prohibits assignment to a variable.</span></span>

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a><span data-ttu-id="c6abe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6abe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6abe-107">*необязательные атрибуты*</span><span class="sxs-lookup"><span data-stu-id="c6abe-107">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="c6abe-108">Ноль или несколько атрибутов MIDL.</span><span class="sxs-lookup"><span data-stu-id="c6abe-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="c6abe-109">*тип данных*</span><span class="sxs-lookup"><span data-stu-id="c6abe-109">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="c6abe-110">Тип данных, содержащихся в *идентификаторе*.</span><span class="sxs-lookup"><span data-stu-id="c6abe-110">The type of the data contained by *identifier*.</span></span>

</dd> <dt>

<span data-ttu-id="c6abe-111">*identifier*</span><span class="sxs-lookup"><span data-stu-id="c6abe-111">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="c6abe-112">Имя, по которому программное обеспечение может ссылаться на место хранения данных.</span><span class="sxs-lookup"><span data-stu-id="c6abe-112">A name by which the software can refer to the data storage location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6abe-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6abe-113">Remarks</span></span>

<span data-ttu-id="c6abe-114">Атрибут **\[ ReadOnly \]** запрещает Присваивание переменной.</span><span class="sxs-lookup"><span data-stu-id="c6abe-114">The **\[readonly\]** attribute prohibits assignment to a variable.</span></span> <span data-ttu-id="c6abe-115">**\[ ReadOnly \]** поддерживается только на уровне параметров, а не на уровне метода.</span><span class="sxs-lookup"><span data-stu-id="c6abe-115">**\[readonly\]** is only supported at the parameter level, not at the method level.</span></span>

### <a name="flags"></a><span data-ttu-id="c6abe-116">Флаги</span><span class="sxs-lookup"><span data-stu-id="c6abe-116">Flags</span></span>

<span data-ttu-id="c6abe-117">ВАРФЛАГ \_ фреадонли</span><span class="sxs-lookup"><span data-stu-id="c6abe-117">VARFLAG\_FREADONLY</span></span>

## <a name="examples"></a><span data-ttu-id="c6abe-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="c6abe-118">Examples</span></span>

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
```

## <a name="see-also"></a><span data-ttu-id="c6abe-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6abe-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6abe-120">типефлагс</span><span class="sxs-lookup"><span data-stu-id="c6abe-120">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="c6abe-121">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="c6abe-121">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="c6abe-122">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="c6abe-122">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="c6abe-123">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="c6abe-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 