---
title: Параметр/d
description: Параметр/D определяет имя и необязательное значение, передаваемое препроцессору C, как при помощи директивы \ define. В командной строке можно использовать несколько директив/D.
ms.assetid: 65642bf6-8e25-400b-8b1c-43513ab6b313
keywords:
- Параметр/d Switch
topic_type:
- apiref
api_name:
- /D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d51cdcbecb5386acb1a97d933be8b25f68720ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104133203"
---
# <a name="d-switch"></a><span data-ttu-id="5bc19-105">Параметр/d</span><span class="sxs-lookup"><span data-stu-id="5bc19-105">/D switch</span></span>

<span data-ttu-id="5bc19-106">Параметр **/d** определяет имя и необязательное значение, передаваемое препроцессору C, как при помощи директивы **\# define** .</span><span class="sxs-lookup"><span data-stu-id="5bc19-106">The **/D** switch defines a name and an optional value to be passed to the C preprocessor as if by a **\#define** directive.</span></span> <span data-ttu-id="5bc19-107">В командной строке можно использовать несколько директив **/d** .</span><span class="sxs-lookup"><span data-stu-id="5bc19-107">Multiple **/D** directives can be used in a command line.</span></span>

``` syntax
midl /Dname[=definition]
```

## <a name="switch-options"></a><span data-ttu-id="5bc19-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="5bc19-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="5bc19-109">*name*</span><span class="sxs-lookup"><span data-stu-id="5bc19-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="5bc19-110">Указывает определенное имя, которое передается препроцессору C при наличии ключа [**/КПП \_ cmd**](-cpp-cmd.md) и [**/КПП \_ OPT**](-cpp-opt.md) .</span><span class="sxs-lookup"><span data-stu-id="5bc19-110">Specifies a defined name that is passed to the C preprocessor when the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not present.</span></span>

</dd> <dt>

<span data-ttu-id="5bc19-111">*definition*</span><span class="sxs-lookup"><span data-stu-id="5bc19-111">*definition*</span></span> 
</dt> <dd>

<span data-ttu-id="5bc19-112">Указывает значение, связанное с определенным именем.</span><span class="sxs-lookup"><span data-stu-id="5bc19-112">Specifies a value associated with the defined name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5bc19-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5bc19-113">Remarks</span></span>

<span data-ttu-id="5bc19-114">Пробел между параметром **/d** и определенным именем является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5bc19-114">White space between the **/D** switch and the defined name is optional.</span></span>

<span data-ttu-id="5bc19-115">Если параметр [**\_ cmd/КПП**](-cpp-cmd.md) имеет значение, а параметр [**/КПП \_ OPT**](-cpp-opt.md) — нет, компилятор MIDL объединяет строку, указанную параметром **/КПП \_ cmd** , с параметрами [**/i**](-i.md), **/d** и [**/u**](-u.md) и использует эту объединенную строку для вызова препроцессора C для каждого исходного файла IDL и ACF.</span><span class="sxs-lookup"><span data-stu-id="5bc19-115">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the [**/I**](-i.md), **/D**, and [**/U**](-u.md) options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span>

<span data-ttu-id="5bc19-116">Параметр компилятора MIDL **/d** игнорируется, если указан параметр компилятора MIDL [/но \_ cpp](-no-cpp-nocpp.md) или [**/КПП \_ OPT**](-cpp-opt.md) .</span><span class="sxs-lookup"><span data-stu-id="5bc19-116">The MIDL compiler switch **/D** is ignored when the MIDL compiler switch [/no\_cpp](-no-cpp-nocpp.md) or [**/cpp\_opt**](-cpp-opt.md) is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="5bc19-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="5bc19-117">Examples</span></span>

<span data-ttu-id="5bc19-118">**MIDL-ДУНИКОДЕ filename. idl**</span><span class="sxs-lookup"><span data-stu-id="5bc19-118">**midl -DUNICODE filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="5bc19-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5bc19-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bc19-120">**/КПП \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="5bc19-120">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="5bc19-121">**/КПП \_ OPT**</span><span class="sxs-lookup"><span data-stu-id="5bc19-121">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="5bc19-122">**/I**</span><span class="sxs-lookup"><span data-stu-id="5bc19-122">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="5bc19-123">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="5bc19-123">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="5bc19-124">**/но \_ cpp**</span><span class="sxs-lookup"><span data-stu-id="5bc19-124">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="5bc19-125">**/U**</span><span class="sxs-lookup"><span data-stu-id="5bc19-125">**/U**</span></span>](-u.md)
</dt> </dl>

 

 




