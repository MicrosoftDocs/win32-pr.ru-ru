---
title: no_default_epv Switch
description: Параметр/но \_ по умолчанию \_ ЕПВ указывает компилятору MIDL не создавать вектор точки входа по умолчанию (ЕПВ). Использовать этот атрибут не рекомендуется.
ms.assetid: 160b5fd3-cd9c-4f51-8c35-6cddab120021
keywords:
- /no_default_epv параметр MIDL
topic_type:
- apiref
api_name:
- /no_default_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a6e39319c5f03c1cd41959a009307b07bef66f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987398"
---
# <a name="no_default_epv-switch"></a><span data-ttu-id="48fc6-105">/но \_ параметр ЕПВ по умолчанию \_</span><span class="sxs-lookup"><span data-stu-id="48fc6-105">/no\_default\_epv switch</span></span>

<span data-ttu-id="48fc6-106">Параметр **/но \_ по умолчанию \_ ЕПВ** указывает компилятору MIDL не создавать вектор точки входа по умолчанию (ЕПВ).</span><span class="sxs-lookup"><span data-stu-id="48fc6-106">The **/no\_default\_epv** switch directs the MIDL compiler not to generate a default entry-point vector (epv).</span></span> <span data-ttu-id="48fc6-107">Использовать этот атрибут не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="48fc6-107">The use of this attribute is not recommended.</span></span>

``` syntax
midl /no_default_epv
```

## <a name="switch-options"></a><span data-ttu-id="48fc6-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="48fc6-108">Switch Options</span></span>

<span data-ttu-id="48fc6-109">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="48fc6-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="48fc6-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="48fc6-110">Remarks</span></span>

<span data-ttu-id="48fc6-111">В этом случае приложение должно зарегистрировать ЕПВ с помощью вызова [**рпксерверрегистериф**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) .</span><span class="sxs-lookup"><span data-stu-id="48fc6-111">In this case, the application must register an epv with the [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) call.</span></span> <span data-ttu-id="48fc6-112">Сравните этот параметр с параметром [**\_ ЕПВ/TestCleanup используется**](-use-epv.md) .</span><span class="sxs-lookup"><span data-stu-id="48fc6-112">Compare this switch with the [**/use\_epv**](-use-epv.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="48fc6-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="48fc6-113">Examples</span></span>

<span data-ttu-id="48fc6-114">**MIDL/но \_ по умолчанию \_ ЕПВ filename. idl**</span><span class="sxs-lookup"><span data-stu-id="48fc6-114">**midl /no\_default\_epv filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="48fc6-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48fc6-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48fc6-116">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="48fc6-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="48fc6-117">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="48fc6-117">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="48fc6-118">**/TestCleanup используется \_ ЕПВ**</span><span class="sxs-lookup"><span data-stu-id="48fc6-118">**/use\_epv**</span></span>](-use-epv.md)
</dt> <dt>

[<span data-ttu-id="48fc6-119">**рпксерверрегистериф**</span><span class="sxs-lookup"><span data-stu-id="48fc6-119">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 