---
title: Параметр/u
description: Параметр/U удаляет все предыдущие определения имени, передавая имя в препроцессору C, как при помощи директивы \ undefine.
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- /U переключить MIDL
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d018d47dd5cbcc8192dee490965bd06c56d0e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104133158"
---
# <a name="u-switch"></a><span data-ttu-id="865c7-104">Параметр/u</span><span class="sxs-lookup"><span data-stu-id="865c7-104">/U switch</span></span>

<span data-ttu-id="865c7-105">Параметр **/u** удаляет все предыдущие определения имени, передавая имя в препроцессору C, как при помощи директивы **\# undefine** .</span><span class="sxs-lookup"><span data-stu-id="865c7-105">The **/U** switch removes any previous definition of a name by passing the name to the C preprocessor as if by a **\#undefine** directive.</span></span>

``` syntax
midl /U name
```

## <a name="switch-options"></a><span data-ttu-id="865c7-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="865c7-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="865c7-107">*name*</span><span class="sxs-lookup"><span data-stu-id="865c7-107">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="865c7-108">Задает определенное имя, передаваемое препроцессору C, как если бы она была директивой **\# undefine** .</span><span class="sxs-lookup"><span data-stu-id="865c7-108">Specifies a defined name to be passed to the C preprocessor as if by a **\#undefine** directive.</span></span> <span data-ttu-id="865c7-109">Имя предопределено препроцессором C или ранее определенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="865c7-109">The name is predefined by the C preprocessor or previously defined by the user.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="865c7-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="865c7-110">Remarks</span></span>

<span data-ttu-id="865c7-111">В командной строке можно использовать несколько директив **/u** .</span><span class="sxs-lookup"><span data-stu-id="865c7-111">Multiple **/U** directives can be used in a command line.</span></span> <span data-ttu-id="865c7-112">Пробел между параметром **/u** и неопределенное имя является необязательным.</span><span class="sxs-lookup"><span data-stu-id="865c7-112">White space between the **/U** switch and the undefined name is optional.</span></span>

<span data-ttu-id="865c7-113">Если параметр [**\_ cmd/КПП**](-cpp-cmd.md) имеет значение, а параметр [**/КПП \_ OPT**](-cpp-opt.md) — нет, компилятор MIDL объединяет строку, указанную параметром/КПП \_ cmd, с параметрами [**/i**](-i.md), [**/d**](-d.md)и **/U** и использует эту объединенную строку для вызова препроцессора C для каждого исходного файла IDL и ACF.</span><span class="sxs-lookup"><span data-stu-id="865c7-113">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the /cpp\_cmd switch with the [**/I**](-i.md), [**/D**](-d.md), and **/U** options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span> <span data-ttu-id="865c7-114">Параметр компилятора MIDL **/u** игнорируется, если указан параметр компилятора MIDL **/но \_ cpp** или **/КПП \_ OPT** .</span><span class="sxs-lookup"><span data-stu-id="865c7-114">The MIDL compiler switch **/U** is ignored when the MIDL compiler switch **/no\_cpp** or **/cpp\_opt** is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="865c7-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="865c7-115">Examples</span></span>

<span data-ttu-id="865c7-116">**MIDL/УУНИКОДЕ filename. idl**</span><span class="sxs-lookup"><span data-stu-id="865c7-116">**midl /UUNICODE filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="865c7-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="865c7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="865c7-118">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="865c7-118">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="865c7-119">**/КПП \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="865c7-119">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="865c7-120">**/КПП \_ OPT**</span><span class="sxs-lookup"><span data-stu-id="865c7-120">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="865c7-121">**/D**</span><span class="sxs-lookup"><span data-stu-id="865c7-121">**/D**</span></span>](-d.md)
</dt> <dt>

[<span data-ttu-id="865c7-122">**/I**</span><span class="sxs-lookup"><span data-stu-id="865c7-122">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="865c7-123">**/но \_ cpp**</span><span class="sxs-lookup"><span data-stu-id="865c7-123">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> </dl>

 

 




