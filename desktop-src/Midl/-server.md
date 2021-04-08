---
title: Параметр/Server
description: Параметр/Server направляет компилятор MIDL для создания исходных файлов C на стороне сервера для интерфейса RPC.
ms.assetid: c5ca6a47-e8b0-4a13-ba73-2d35a9ac8240
keywords:
- Параметр/Server MIDL
topic_type:
- apiref
api_name:
- /server
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31449133fa795a90d1f11d8c06b960b74909548d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069018"
---
# <a name="server-switch"></a><span data-ttu-id="42539-104">Параметр/Server</span><span class="sxs-lookup"><span data-stu-id="42539-104">/server switch</span></span>

<span data-ttu-id="42539-105">Параметр **/Server** направляет компилятор MIDL для создания исходных файлов C на стороне сервера для интерфейса RPC.</span><span class="sxs-lookup"><span data-stu-id="42539-105">The **/server** switch directs the MIDL compiler to generate server-side C source files for an RPC interface.</span></span>

``` syntax
midl /server { stub | none }
```

## <a name="switch-options"></a><span data-ttu-id="42539-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="42539-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span data-ttu-id="42539-107"><span id="stub"></span><span id="STUB"></span>заглушка \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="42539-107"><span id="stub"></span><span id="STUB"></span>\*\*\*\*stub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="42539-108">Создает файлы на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="42539-108">Generates the server-side files.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="42539-109"><span id="none"></span><span id="NONE"></span>нет \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="42539-109"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="42539-110">Не создает файлы на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="42539-110">Does not generate server-side files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42539-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42539-111">Remarks</span></span>

<span data-ttu-id="42539-112">Если параметр **/Server** не указан, компилятор MIDL создает файл заглушки сервера.</span><span class="sxs-lookup"><span data-stu-id="42539-112">When the **/server** switch is not specified, the MIDL compiler generates the server stub file.</span></span> <span data-ttu-id="42539-113">Этот параметр не влияет на интерфейсы OLE.</span><span class="sxs-lookup"><span data-stu-id="42539-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="42539-114">Параметр **None** не приводит к созданию файлов.</span><span class="sxs-lookup"><span data-stu-id="42539-114">The **none** option causes no files to be generated.</span></span>

<span data-ttu-id="42539-115">Параметр **/Server** имеет приоритет над параметром **/sstub** .</span><span class="sxs-lookup"><span data-stu-id="42539-115">The **/server** switch takes precedence over the **/sstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="42539-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="42539-116">Examples</span></span>

<span data-ttu-id="42539-117">**MIDL/Server нет**</span><span class="sxs-lookup"><span data-stu-id="42539-117">**midl /server none**</span></span>

<span data-ttu-id="42539-118">**заглушка с MIDL/Server**</span><span class="sxs-lookup"><span data-stu-id="42539-118">**midl /server stub**</span></span>

## <a name="see-also"></a><span data-ttu-id="42539-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42539-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42539-120">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="42539-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="42539-121">**/Client**</span><span class="sxs-lookup"><span data-stu-id="42539-121">**/client**</span></span>](-client.md)
</dt> <dt>

[<span data-ttu-id="42539-122">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="42539-122">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




