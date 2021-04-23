---
title: /рпксс, параметр
description: Если указан параметр/рпксс, он действует так, как если бы \_ для всех операций интерфейса был указан атрибут включения выделения. Использование этого атрибута не рекомендуется.
ms.assetid: a4507779-7d07-4517-8592-39f0d9460bc3
keywords:
- MIDL/рпксс Switch
topic_type:
- apiref
api_name:
- /rpcss
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dabdd6340005c4e56080dc91bdd372a858e0e7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068850"
---
# <a name="rpcss-switch"></a><span data-ttu-id="d0a21-105">/рпксс, параметр</span><span class="sxs-lookup"><span data-stu-id="d0a21-105">/rpcss switch</span></span>

<span data-ttu-id="d0a21-106">Если указан параметр **/рпксс** , он действует так, как если бы для всех операций интерфейса был указан атрибут [**включения \_ выделения**](enable-allocate.md) .</span><span class="sxs-lookup"><span data-stu-id="d0a21-106">The **/rpcss** switch, when specified, acts as though the [**enable\_allocate**](enable-allocate.md) attribute was specified on all operations of the interface.</span></span> <span data-ttu-id="d0a21-107">Использование этого атрибута не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d0a21-107">The usage of this attribute is not recommended.</span></span>

``` syntax
midl /rpcss
```

## <a name="switch-options"></a><span data-ttu-id="d0a21-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="d0a21-108">Switch Options</span></span>

<span data-ttu-id="d0a21-109">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d0a21-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0a21-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0a21-110">Remarks</span></span>

<span data-ttu-id="d0a21-111">В режиме по умолчанию пакет RPCSS включается только в том случае, если для процедуры или интерфейса установлен атрибут [**Enable \_ allocate**](enable-allocate.md) или параметр **/рпксс** указан в командной строке.</span><span class="sxs-lookup"><span data-stu-id="d0a21-111">In default mode, the RpcSs package is enabled only if either the procedure or interface has the [**enable\_allocate**](enable-allocate.md) attribute or the **/rpcss** switch is specified on the command line.</span></span> <span data-ttu-id="d0a21-112">В режиме **/ОСФ** заглушка на стороне сервера включает пакет выделения RPCSS.</span><span class="sxs-lookup"><span data-stu-id="d0a21-112">In **/osf** mode, the server-side stub enables the RpcSs allocation package.</span></span>

## <a name="examples"></a><span data-ttu-id="d0a21-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="d0a21-113">Examples</span></span>

<span data-ttu-id="d0a21-114">**MIDL/рпксс filename. idl**</span><span class="sxs-lookup"><span data-stu-id="d0a21-114">**midl /rpcss filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="d0a21-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0a21-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0a21-116">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="d0a21-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="d0a21-117">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="d0a21-117">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="d0a21-118">**включить \_ выделение**</span><span class="sxs-lookup"><span data-stu-id="d0a21-118">**enable\_allocate**</span></span>](enable-allocate.md)
</dt> <dt>

[<span data-ttu-id="d0a21-119">**/осф**</span><span class="sxs-lookup"><span data-stu-id="d0a21-119">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 




