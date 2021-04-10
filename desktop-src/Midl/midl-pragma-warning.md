---
title: midl_pragma атрибут предупреждения
description: Используйте параметр компилятора MIDL \_ pragma warning, чтобы временно переопределить поведение сообщения о предупреждении MIDL во время компиляции.
ms.assetid: d32a3d3f-5c4d-4f93-a72a-2224ceed0012
keywords:
- midl_pragma атрибута предупреждения MIDL
topic_type:
- apiref
api_name:
- midl_pragma warning
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b7e1e2c2a1d818216245e45a9129018a3ba2e1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889460"
---
# <a name="midl_pragma-warning-attribute"></a><span data-ttu-id="b3b23-104">MIDL \_ pragma, атрибут Warning</span><span class="sxs-lookup"><span data-stu-id="b3b23-104">midl\_pragma warning attribute</span></span>

<span data-ttu-id="b3b23-105">Используйте параметр **компилятора MIDL \_ pragma warning** , чтобы временно переопределить поведение сообщения о предупреждении MIDL во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="b3b23-105">Use the **midl\_pragma warning** option to temporarily override MIDL's warning message behavior at compile time.</span></span>

``` syntax
midl_pragma warning ( warning_option : message_list )
```

## <a name="parameters"></a><span data-ttu-id="b3b23-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3b23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3b23-107">*\_параметр предупреждения*</span><span class="sxs-lookup"><span data-stu-id="b3b23-107">*warning\_option*</span></span> 
</dt> <dd>

<span data-ttu-id="b3b23-108">Параметр warning может принимать одно из следующих значений: Disable, Enable, Default.</span><span class="sxs-lookup"><span data-stu-id="b3b23-108">The warning option can be one of the following: disable, enable, default.</span></span>

</dd> <dt>

<span data-ttu-id="b3b23-109">*\_список сообщений*</span><span class="sxs-lookup"><span data-stu-id="b3b23-109">*message\_list*</span></span> 
</dt> <dd>

<span data-ttu-id="b3b23-110">Список номеров сообщений, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="b3b23-110">A list of message numbers separated by spaces.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3b23-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3b23-111">Remarks</span></span>

<span data-ttu-id="b3b23-112">Директиву pragma можно использовать как директиву pragma C-Compiler.</span><span class="sxs-lookup"><span data-stu-id="b3b23-112">The pragma can be used like a C-compiler pragma.</span></span> <span data-ttu-id="b3b23-113">То есть он отключает, включает или возвращает поведение по умолчанию для данного предупреждения MIDL.</span><span class="sxs-lookup"><span data-stu-id="b3b23-113">That is, it disables, enables, or returns to the default behavior for a given MIDL warning.</span></span>

## <a name="examples"></a><span data-ttu-id="b3b23-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="b3b23-114">Examples</span></span>

``` syntax
#if (__midl >= 501)
midl_pragma warning( disable: 2007 )   // file already imported midl_pragma warning( disable: 2209 )   // ignored redundant attr
#endif
```

## <a name="see-also"></a><span data-ttu-id="b3b23-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3b23-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3b23-116">**pragma**</span><span class="sxs-lookup"><span data-stu-id="b3b23-116">**pragma**</span></span>](pragma.md)
</dt> </dl>

 

 




