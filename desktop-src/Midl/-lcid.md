---
title: /LCID, параметр
description: Параметр компилятора/LCID MIDL позволяет использовать международные символы во входных файлах, именах файлов и путях к каталогам.
ms.assetid: 2ab4ba67-4414-4889-8ed7-83f4888caf8b
keywords:
- MIDL/LCID Switch
topic_type:
- apiref
api_name:
- /lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370548bb9899ce84173f2321a129aaeda1c6fe81
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334560"
---
# <a name="lcid-switch"></a><span data-ttu-id="fd396-104">/LCID, параметр</span><span class="sxs-lookup"><span data-stu-id="fd396-104">/lcid switch</span></span>

<span data-ttu-id="fd396-105">Параметр компилятора **/LCID** MIDL позволяет использовать международные символы во входных файлах, именах файлов и путях к каталогам.</span><span class="sxs-lookup"><span data-stu-id="fd396-105">The **/lcid** MIDL compiler option lets you use international characters in your input files, file names, and directory paths.</span></span>

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a><span data-ttu-id="fd396-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="fd396-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="fd396-107">*localeID*</span><span class="sxs-lookup"><span data-stu-id="fd396-107">*localeID*</span></span> 
</dt> <dd>

<span data-ttu-id="fd396-108">Указывает 32-разрядный идентификатор локали, используемый в поддержке национальных языков Windows.</span><span class="sxs-lookup"><span data-stu-id="fd396-108">Specifies the 32-bit locale identifier used in Windows National Language Support.</span></span> <span data-ttu-id="fd396-109">Код локали должен быть указан в десятичном формате.</span><span class="sxs-lookup"><span data-stu-id="fd396-109">The locale identifier should be specified in decimal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd396-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd396-110">Remarks</span></span>

<span data-ttu-id="fd396-111">Во входных файлах можно использовать локализованные комментарии, строки, хелпстрингс и идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="fd396-111">Within the input files, you can use localized comments, strings, helpstrings and identifiers.</span></span> <span data-ttu-id="fd396-112">В частности, параметр **/LCID** обеспечивает полную поддержку DBCS для представления азиатских языков, таких как японский, китайский и корейский.</span><span class="sxs-lookup"><span data-stu-id="fd396-112">In particular, the **/lcid** switch provides full DBCS support, to represent Asian languages such as Japanese, Chinese, and Korean.</span></span>

> [!Note]  
> <span data-ttu-id="fd396-113">Параметр **/LCID** доступен в MIDL версии 3.01.75 и более поздних.</span><span class="sxs-lookup"><span data-stu-id="fd396-113">The **/lcid** switch is available with MIDL version 3.01.75 and later.</span></span>

 

## <a name="examples"></a><span data-ttu-id="fd396-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd396-114">Examples</span></span>

<span data-ttu-id="fd396-115">**MIDL/LCID 1041 iface. idl**</span><span class="sxs-lookup"><span data-stu-id="fd396-115">**midl /lcid 1041 iface.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="fd396-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd396-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd396-117">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="fd396-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="fd396-118">**намного**</span><span class="sxs-lookup"><span data-stu-id="fd396-118">**lcid**</span></span>](lcid.md)
</dt> </dl>

 

 




