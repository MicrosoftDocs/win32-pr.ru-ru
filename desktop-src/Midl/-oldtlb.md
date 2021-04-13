---
title: /oldtlb, параметр
description: Параметр/oldtlb направляет компилятор MIDL для создания библиотеки типов старого формата.
ms.assetid: cf5fe000-7262-4812-a6ab-f12a558ac068
keywords:
- MIDL/oldtlb Switch
topic_type:
- apiref
api_name:
- /oldtlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a08e468d0acff16aa1df4a45fcacafeb676b00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412847"
---
# <a name="oldtlb-switch"></a><span data-ttu-id="46101-104">/oldtlb, параметр</span><span class="sxs-lookup"><span data-stu-id="46101-104">/oldtlb switch</span></span>

<span data-ttu-id="46101-105">Параметр **/oldtlb** направляет компилятор MIDL для создания библиотеки типов старого формата.</span><span class="sxs-lookup"><span data-stu-id="46101-105">The **/oldtlb** switch directs the MIDL compiler to generate an old-format type library.</span></span>

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a><span data-ttu-id="46101-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="46101-106">Switch Options</span></span>

<span data-ttu-id="46101-107">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="46101-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="46101-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46101-108">Remarks</span></span>

<span data-ttu-id="46101-109">Параметр **/oldtlb** переопределяет значение по умолчанию и направляет компилятор MIDL для создания библиотек типов старого формата даже в текущих версиях Windows с помощью [креатетипелиб](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) вместо [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).</span><span class="sxs-lookup"><span data-stu-id="46101-109">The **/oldtlb** switch overrides the default and directs the MIDL compiler to generate old-format type libraries even on current versions of Windows by using [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) instead of [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).</span></span>

## <a name="examples"></a><span data-ttu-id="46101-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="46101-110">Examples</span></span>

<span data-ttu-id="46101-111">**MIDL/oldtlb filename. idl**</span><span class="sxs-lookup"><span data-stu-id="46101-111">**midl /oldtlb filename.idl**</span></span>

<span data-ttu-id="46101-112">**MIDL/oldtlb мйолдодл. odl**</span><span class="sxs-lookup"><span data-stu-id="46101-112">**midl /oldtlb myoldodl.odl**</span></span>

## <a name="see-also"></a><span data-ttu-id="46101-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46101-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46101-114">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="46101-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="46101-115">**/newtlb**</span><span class="sxs-lookup"><span data-stu-id="46101-115">**/newtlb**</span></span>](-newtlb.md)
</dt> </dl>

 

 