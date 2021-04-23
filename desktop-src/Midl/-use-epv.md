---
title: use_epv Switch
description: '\_Параметр ЕПВ/TestCleanup используется указывает компилятору MIDL создать код заглушки сервера, вызывающий серверную подпрограмму с помощью вектора точки входа (ЕПВ), а не статического вызова. Использовать этот атрибут не рекомендуется.'
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /use_epv параметр MIDL
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec73b5cb9833c15a77c96a784e1ded88d266f9a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105681605"
---
# <a name="use_epv-switch"></a><span data-ttu-id="80277-105">/TestCleanup используется \_ ЕПВ Switch</span><span class="sxs-lookup"><span data-stu-id="80277-105">/use\_epv switch</span></span>

<span data-ttu-id="80277-106">Параметр **\_ ЕПВ/TestCleanup используется** указывает компилятору MIDL создать код заглушки сервера, вызывающий серверную подпрограмму с помощью вектора точки входа (ЕПВ), а не статического вызова.</span><span class="sxs-lookup"><span data-stu-id="80277-106">The **/use\_epv** switch directs the MIDL compiler to generate server stub code that calls the server application routine through an entry-point vector (epv), rather than by a static call.</span></span> <span data-ttu-id="80277-107">Использовать этот атрибут не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="80277-107">The use of this attribute is not recommended.</span></span>

``` syntax
midl /use_epv
```

## <a name="switch-options"></a><span data-ttu-id="80277-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="80277-108">Switch Options</span></span>

<span data-ttu-id="80277-109">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="80277-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="80277-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80277-110">Remarks</span></span>

<span data-ttu-id="80277-111">Как правило, приложениям требуется статическая связь с серверным приложением.</span><span class="sxs-lookup"><span data-stu-id="80277-111">Typically, applications require static linkage to the server application routine.</span></span> <span data-ttu-id="80277-112">Компилятор MIDL по умолчанию создает такой вызов.</span><span class="sxs-lookup"><span data-stu-id="80277-112">The MIDL compiler generates such a call by default.</span></span> <span data-ttu-id="80277-113">Однако если приложению требуется, чтобы серверная заглушка вызывала серверную подпрограмму с помощью ЕПВ, необходимо указать параметр **/TestCleanup используется \_ ЕПВ** .</span><span class="sxs-lookup"><span data-stu-id="80277-113">However, if an application requires the server stub to call the server application routine by using the epv, the **/use\_epv** switch must be specified.</span></span> <span data-ttu-id="80277-114">Если указан **параметр \_ ЕПВ/TestCleanup используется** , компилятор MIDL создает значение по умолчанию ЕПВ.</span><span class="sxs-lookup"><span data-stu-id="80277-114">When the **/use\_epv** switch is specified, the MIDL compiler generates a default epv.</span></span> <span data-ttu-id="80277-115">Этот ЕПВ по умолчанию используется, если приложение не регистрирует другой ЕПВ через вызов [**рпксерверрегистериф**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) .</span><span class="sxs-lookup"><span data-stu-id="80277-115">This default epv is then used if the application does not register another epv through the [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) call.</span></span>

## <a name="examples"></a><span data-ttu-id="80277-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="80277-116">Examples</span></span>

<span data-ttu-id="80277-117">**MIDL/TestCleanup используется \_ ЕПВ** *filename \* \* *. idl**</span><span class="sxs-lookup"><span data-stu-id="80277-117">**midl /use\_epv** *filename\*\*\*.idl*\*</span></span>

## <a name="see-also"></a><span data-ttu-id="80277-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80277-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80277-119">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="80277-119">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="80277-120">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="80277-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="80277-121">**/но \_ по умолчанию \_ ЕПВ**</span><span class="sxs-lookup"><span data-stu-id="80277-121">**/no\_default\_epv**</span></span>](-no-default-epv.md)
</dt> <dt>

[<span data-ttu-id="80277-122">**рпксерверрегистериф**</span><span class="sxs-lookup"><span data-stu-id="80277-122">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 