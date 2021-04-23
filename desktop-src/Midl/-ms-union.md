---
title: ms_union Switch
description: '\_Параметр объединения/МС управляет выравниванием ОНД неинкапсулированных объединений. Обратите внимание, что этот атрибут предоставляется для обеспечения обратной совместимости.'
ms.assetid: 683d1498-6419-4600-ad5b-c0b6ea44a8e1
keywords:
- /ms_union параметр MIDL
topic_type:
- apiref
api_name:
- /ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968618af5c2bb5b32ec14b293225bc09c2997aa5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889784"
---
# <a name="ms_union-switch"></a><span data-ttu-id="1ba43-104">\_коммутатор объединения/МС</span><span class="sxs-lookup"><span data-stu-id="1ba43-104">/ms\_union switch</span></span>

<span data-ttu-id="1ba43-105">Параметр **\_ объединения/МС** управляет выравниванием ОНД неинкапсулированных объединений.</span><span class="sxs-lookup"><span data-stu-id="1ba43-105">The **/ms\_union** switch controls the NDR alignment of nonencapsulated unions.</span></span>

> [!Note]  
> <span data-ttu-id="1ba43-106">Этот атрибут предоставляется для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="1ba43-106">This attribute is provided for backwards compatibility.</span></span> <span data-ttu-id="1ba43-107">Не рекомендуется использовать в новом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="1ba43-107">It is not recommended for use in a new interface.</span></span>

 

``` syntax
midl /ms_union
```

## <a name="switch-options"></a><span data-ttu-id="1ba43-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="1ba43-108">Switch Options</span></span>

<span data-ttu-id="1ba43-109">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1ba43-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ba43-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ba43-110">Remarks</span></span>

<span data-ttu-id="1ba43-111">Компилятор MIDL отражает поведение компилятора IDL использование-DCE для неинкапсулированных объединений.</span><span class="sxs-lookup"><span data-stu-id="1ba43-111">The MIDL compiler mirrors the behavior of the OSF-DCE IDL compiler for nonencapsulated unions.</span></span> <span data-ttu-id="1ba43-112">Однако, поскольку более ранние версии компилятора MIDL не сделали этого, коммутатор **/МС \_ Union** обеспечивает совместимость с интерфейсами, созданными в предыдущих версиях компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="1ba43-112">However, because earlier versions of the MIDL compiler did not do so, the **/ms\_union** switch provides compatibility with interfaces built on previous versions of the MIDL compiler.</span></span>

<span data-ttu-id="1ba43-113">Функцию MS \_ Union можно использовать в качестве параметра командной строки (**/МС \_ Union**), атрибута интерфейса IDL или в качестве атрибута IDL-Type.</span><span class="sxs-lookup"><span data-stu-id="1ba43-113">The ms\_union feature can be used as a command-line switch (**/ms\_union**), an IDL interface attribute, or as an IDL-type attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="1ba43-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="1ba43-114">Examples</span></span>

<span data-ttu-id="1ba43-115">**MIDL- \_ файл/МС Union File. idl**</span><span class="sxs-lookup"><span data-stu-id="1ba43-115">**midl /ms\_union file.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="1ba43-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ba43-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ba43-117">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="1ba43-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="1ba43-118">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="1ba43-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




