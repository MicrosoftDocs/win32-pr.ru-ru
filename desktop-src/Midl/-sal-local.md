---
title: sal_local Switch
description: '\_Локальный коммутатор/Сал направляет MIDL для создания аннотаций SAL для параметров методов интерфейса, помеченных \ Local \. Также должен присутствовать параметр/Сал.'
ms.assetid: 49AFC3F6-EAD5-45F6-8862-EFB3D9C479D1
keywords:
- /sal_local параметр MIDL
topic_type:
- apiref
api_name:
- /sal_local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03263b94b809407d1c3e55c2f3dacc5e10684bc1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105672197"
---
# <a name="sal_local-switch"></a><span data-ttu-id="14588-105">\_локальный коммутатор/Сал</span><span class="sxs-lookup"><span data-stu-id="14588-105">/sal\_local switch</span></span>

<span data-ttu-id="14588-106">**\_ Локальный коммутатор/Сал** направляет MIDL для создания аннотаций SAL для параметров методов интерфейса, помеченных как [**\[ локальные \]**](local.md).</span><span class="sxs-lookup"><span data-stu-id="14588-106">The **/sal\_local** switch directs MIDL to also generate SAL annotations for parameters of interface methods marked [**\[local\]**](local.md).</span></span> <span data-ttu-id="14588-107">Также должен присутствовать параметр [**/Сал**](-sal.md) .</span><span class="sxs-lookup"><span data-stu-id="14588-107">The [**/sal**](-sal.md) switch must also be present.</span></span>

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a><span data-ttu-id="14588-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="14588-108">Switch Options</span></span>

<span data-ttu-id="14588-109">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="14588-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="14588-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14588-110">Remarks</span></span>

<span data-ttu-id="14588-111">Изменяет поведение параметра [**/Сал**](-sal.md) , чтобы также предоставить заметки для параметров методов интерфейса, помеченных [**\[ локальным \]**](local.md) атрибутом.</span><span class="sxs-lookup"><span data-stu-id="14588-111">Modifies the behavior of the [**/sal**](-sal.md) switch to also provide annotations on the parameters of interface methods marked with the [**\[local\]**](local.md) attribute.</span></span> <span data-ttu-id="14588-112">Используйте атрибут [**\[ аннотации \]**](annotate.md), чтобы переопределить созданную с помощью MIDL аннотацию другой строкой заметки.</span><span class="sxs-lookup"><span data-stu-id="14588-112">Use the [**\[annotate\]**](annotate.md)attribute to override the MIDL-generated annotation with a different annotation string.</span></span>

## <a name="see-also"></a><span data-ttu-id="14588-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14588-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14588-114">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="14588-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="14588-115">**/сал**</span><span class="sxs-lookup"><span data-stu-id="14588-115">**/sal**</span></span>](-sal.md)
</dt> <dt>

<span data-ttu-id="14588-116">[**\[комментировани\]**](annotate.md)</span><span class="sxs-lookup"><span data-stu-id="14588-116">[**\[annotate\]**](annotate.md)</span></span>
</dt> </dl>

 

 




