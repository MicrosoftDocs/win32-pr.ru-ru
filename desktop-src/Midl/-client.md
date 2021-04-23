---
title: /Client, параметр
description: Параметр/Client направляет компилятор MIDL для создания исходных файлов C на стороне клиента для интерфейса RPC.
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- MIDL/Client Switch
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf7e17e1893b918d926cd94a93eb8b1c372ee75
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334576"
---
# <a name="client-switch"></a><span data-ttu-id="f7213-104">/Client, параметр</span><span class="sxs-lookup"><span data-stu-id="f7213-104">/client switch</span></span>

<span data-ttu-id="f7213-105">Параметр **/Client** направляет компилятор MIDL для создания исходных файлов C на стороне клиента для интерфейса RPC.</span><span class="sxs-lookup"><span data-stu-id="f7213-105">The **/client** switch directs the MIDL compiler to generate client-side C source files for an RPC interface.</span></span>

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a><span data-ttu-id="f7213-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="f7213-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span data-ttu-id="f7213-107"><span id="stub"></span><span id="STUB"></span>заглушка \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="f7213-107"><span id="stub"></span><span id="STUB"></span>\*\*\*\*stub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="f7213-108">Создает файлы на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="f7213-108">Generates the client-side files.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="f7213-109"><span id="none"></span><span id="NONE"></span>нет \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="f7213-109"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="f7213-110">Не создает файлы на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="f7213-110">Does not generate any client-side files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7213-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7213-111">Remarks</span></span>

<span data-ttu-id="f7213-112">Если параметр **/Client** не указан, компилятор MIDL создает файл заглушки клиента.</span><span class="sxs-lookup"><span data-stu-id="f7213-112">When the **/client** switch is not specified, the MIDL compiler generates the client stub file.</span></span> <span data-ttu-id="f7213-113">Этот параметр не влияет на интерфейсы OLE.</span><span class="sxs-lookup"><span data-stu-id="f7213-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="f7213-114">Параметр **/Client** имеет приоритет над параметром [**/cstub**](-cstub.md) .</span><span class="sxs-lookup"><span data-stu-id="f7213-114">The **/client** switch takes precedence over the [**/cstub**](-cstub.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="f7213-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="f7213-115">Examples</span></span>

<span data-ttu-id="f7213-116">**MIDL/Client нет filename. idl**</span><span class="sxs-lookup"><span data-stu-id="f7213-116">**midl /client none filename.idl**</span></span>

<span data-ttu-id="f7213-117">**MIDL/Client заглушек filename. idl**</span><span class="sxs-lookup"><span data-stu-id="f7213-117">**midl /client stub filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="f7213-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7213-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7213-119">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="f7213-119">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="f7213-120">**/Server**</span><span class="sxs-lookup"><span data-stu-id="f7213-120">**/server**</span></span>](-server.md)
</dt> <dt>

[<span data-ttu-id="f7213-121">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="f7213-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




