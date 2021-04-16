---
title: /Сал, параметр
description: Параметр/Сал направляет MIDL для создания аннотаций SAL в создаваемых файлах-заглушках.
ms.assetid: 452A19CA-6F72-416F-8059-77937412DA88
keywords:
- MIDL/Сал Switch
topic_type:
- apiref
api_name:
- /sal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef52eb510c71bfdb153b95a5d05e992359e39b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105650312"
---
# <a name="sal-switch"></a><span data-ttu-id="b78e7-104">/Сал, параметр</span><span class="sxs-lookup"><span data-stu-id="b78e7-104">/sal switch</span></span>

<span data-ttu-id="b78e7-105">Параметр **/Сал** направляет MIDL для создания аннотаций SAL в создаваемых файлах-заглушках.</span><span class="sxs-lookup"><span data-stu-id="b78e7-105">The **/sal** switch directs MIDL to generate SAL annotations in the generated stub files.</span></span>

``` syntax
midl /sal
```

## <a name="switch-options"></a><span data-ttu-id="b78e7-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="b78e7-106">Switch Options</span></span>

<span data-ttu-id="b78e7-107">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b78e7-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="b78e7-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b78e7-108">Remarks</span></span>

<span data-ttu-id="b78e7-109">MIDL помечает параметры указателя и массива с заметками, отражающими описание параметра в IDL-файле в соответствии с применением RPC и подсистемой маршалирования NDR.</span><span class="sxs-lookup"><span data-stu-id="b78e7-109">MIDL will mark pointer and array parameters with annotations that reflect the parameter description in the IDL file as enforced by RPC and the NDR marshaling engine.</span></span> <span data-ttu-id="b78e7-110">MIDL не создает аннотации для параметров в методах интерфейса, помеченных [**\[ локальным \]**](local.md)атрибутом, если в командной строке также отсутствует [**/Сал \_ Local**](-sal-local.md) .</span><span class="sxs-lookup"><span data-stu-id="b78e7-110">MIDL does not create annotations for parameters in interface methods marked with the [**\[local\]**](local.md)attribute unless [**/sal\_local**](-sal-local.md) is also present on the command line.</span></span> <span data-ttu-id="b78e7-111">Чтобы переопределить созданную с помощью MIDL аннотацию, используйте атрибут [**\[ аннотации \]**](annotate.md) .</span><span class="sxs-lookup"><span data-stu-id="b78e7-111">To override the MIDL-generated annotation, use the [**\[annotate\]**](annotate.md) attribute.</span></span>

<span data-ttu-id="b78e7-112">Созданные MIDL-заметки всегда имеют префикс \_ \_ RPC \_ и должны использовать заголовок **RPCSS. h** для преобразования аннотации в стандартные аннотации SAL.</span><span class="sxs-lookup"><span data-stu-id="b78e7-112">MIDL-generated annotations are always prefixed with \_\_RPC\_, and require use of the **rpcsal.h** header to translate the annotation into standard SAL annotations.</span></span>

## <a name="see-also"></a><span data-ttu-id="b78e7-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b78e7-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b78e7-114">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="b78e7-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="b78e7-115">**/Сал \_ локальный**</span><span class="sxs-lookup"><span data-stu-id="b78e7-115">**/sal\_local**</span></span>](-sal-local.md)
</dt> <dt>

<span data-ttu-id="b78e7-116">[**\[комментировани\]**](annotate.md)</span><span class="sxs-lookup"><span data-stu-id="b78e7-116">[**\[annotate\]**](annotate.md)</span></span>
</dt> </dl>

 

 




