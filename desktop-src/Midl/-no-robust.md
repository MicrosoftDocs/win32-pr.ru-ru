---
title: no_robust Switch
description: /Но \_ надежный коммутатор направляет КОМПИЛЯТОР MIDL явным образом отключить функцию командной строки/robust. Параметр командной строки/robust и связанные с ним компоненты являются параметрами компилятора по умолчанию для MIDL версии 6.0.359 и более поздних.
ms.assetid: 17ece05a-d39d-4465-8553-199a45c8c073
keywords:
- /no_robust параметр MIDL
topic_type:
- apiref
api_name:
- /no_robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90691aede68f8e43ae95a4bd6c6f7fb4e2ecad29
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784308"
---
# <a name="no_robust-switch"></a><span data-ttu-id="17a4b-105">/но \_ надежный коммутатор</span><span class="sxs-lookup"><span data-stu-id="17a4b-105">/no\_robust switch</span></span>

<span data-ttu-id="17a4b-106">**/Но \_ надежный** коммутатор направляет компилятор MIDL явным образом отключить функцию командной строки [**/robust**](-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="17a4b-106">The **/no\_robust** switch directs the MIDL compiler to explicitly disable the [**/robust**](-robust.md) command line feature.</span></span> <span data-ttu-id="17a4b-107">Параметр командной строки **/robust** и связанные с ним компоненты являются параметрами компилятора по умолчанию для MIDL версии 6.0.359 и более поздних.</span><span class="sxs-lookup"><span data-stu-id="17a4b-107">The **/robust** command line switch and its associated features is the default compiler setting for MIDL version 6.0.359 and later.</span></span>

``` syntax
midl /no_robust
```

## <a name="switch-options"></a><span data-ttu-id="17a4b-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="17a4b-108">Switch Options</span></span>

<span data-ttu-id="17a4b-109">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="17a4b-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="17a4b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17a4b-110">Remarks</span></span>

<span data-ttu-id="17a4b-111">В MIDL версии 6.0.359 и более поздних компилятор MIDL устанавливает [**/robust**](-robust.md) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="17a4b-111">With MIDL version 6.0.359 and later, the MIDL compiler sets [**/robust**](-robust.md) by default.</span></span> <span data-ttu-id="17a4b-112">**/Но \_ надежный** параметр командной строки должен использоваться для отключения функции **/robust** , если созданные заглушки должны выполняться в Microsoft Windows NT, Windows 95/98 или Windows.</span><span class="sxs-lookup"><span data-stu-id="17a4b-112">The **/no\_robust** command line switch must be used to disable the **/robust** feature if generated stubs need to run on Microsoft WindowsÂ NT, WindowsÂ 95/98, or WindowsÂ Me.</span></span>

## <a name="examples"></a><span data-ttu-id="17a4b-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="17a4b-113">Examples</span></span>

<span data-ttu-id="17a4b-114">**MIDL/но \_ надежность filename. idl**</span><span class="sxs-lookup"><span data-stu-id="17a4b-114">**midl /no\_robust filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="17a4b-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17a4b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a4b-116">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="17a4b-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="17a4b-117">**/robust**</span><span class="sxs-lookup"><span data-stu-id="17a4b-117">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




