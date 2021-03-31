---
title: /IID, параметр
description: Параметр/IID указывает имя файла идентификатора интерфейса для COM-интерфейса, переопределяя имя по умолчанию, полученное путем добавления \_ i. c к имени IDL-файла.
ms.assetid: 051593f5-e612-4b19-94e5-d7885dbede21
keywords:
- MIDL/IID Switch
topic_type:
- apiref
api_name:
- /iid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631a28f1bc5a1a24253c9416104df9941cd8da33
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411896"
---
# <a name="iid-switch"></a><span data-ttu-id="0c34b-104">/IID, параметр</span><span class="sxs-lookup"><span data-stu-id="0c34b-104">/iid switch</span></span>

<span data-ttu-id="0c34b-105">Параметр **/IID** указывает имя файла идентификатора интерфейса для COM-интерфейса, переопределяя имя по умолчанию, полученное путем добавления \_ i. c к имени IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="0c34b-105">The **/iid** switch specifies the name of the interface identifier file for a COM interface, overriding the default name obtained by adding \_i.c to the IDL file name.</span></span>

``` syntax
midl /iid filename
```

## <a name="switch-options"></a><span data-ttu-id="0c34b-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="0c34b-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="0c34b-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="0c34b-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="0c34b-108">Указывает имя файла идентификатора интерфейса, переопределяющего имя файла идентификатора интерфейса по умолчанию для COM-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0c34b-108">Specifies an interface identifier file name that overrides the default interface identifier file name for a COM interface.</span></span> <span data-ttu-id="0c34b-109">Имена файлов можно явно заключить в кавычки с помощью двойных кавычек ("), чтобы оболочка не могла интерпретировать специальные символы.</span><span class="sxs-lookup"><span data-stu-id="0c34b-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c34b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c34b-110">Remarks</span></span>

<span data-ttu-id="0c34b-111">Параметр **/IID** не влияет на интерфейсы RPC.</span><span class="sxs-lookup"><span data-stu-id="0c34b-111">The **/iid** switch does not affect RPC interfaces.</span></span>

<span data-ttu-id="0c34b-112">Если *имя_файла* не включает явный путь, файл записывается в текущий каталог или в каталог, указанный параметром [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="0c34b-112">If *filename* does not include an explicit path, the file is written to the current directory or to the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="0c34b-113">Явный путь в *filename* переопределяет спецификацию переключателя **/out** .</span><span class="sxs-lookup"><span data-stu-id="0c34b-113">An explicit path in *filename* overrides the **/out** switch specification.</span></span>

## <a name="examples"></a><span data-ttu-id="0c34b-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="0c34b-114">Examples</span></span>

<span data-ttu-id="0c34b-115">**MIDL/IID "My \_ IID. c" имя_файла. idl**</span><span class="sxs-lookup"><span data-stu-id="0c34b-115">**midl /iid "my\_iid.c" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="0c34b-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c34b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c34b-117">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="0c34b-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="0c34b-118">**/Header**</span><span class="sxs-lookup"><span data-stu-id="0c34b-118">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="0c34b-119">**/out**</span><span class="sxs-lookup"><span data-stu-id="0c34b-119">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="0c34b-120">**/Proxy**</span><span class="sxs-lookup"><span data-stu-id="0c34b-120">**/proxy**</span></span>](-proxy.md)
</dt> </dl>

 

 




