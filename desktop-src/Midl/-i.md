---
title: /I, параметр
description: Параметр/I задает каталоги для поиска импортированных IDL-файлов, включаемых файлов заголовков и файлов ACF.
ms.assetid: cdb0a1c2-ff99-4060-be72-a54dd20dbf93
keywords:
- /I ключ MIDL
topic_type:
- apiref
api_name:
- /I
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ee48ad1e66caf5ed8facbf09ebf2c517c8c895
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069096"
---
# <a name="i-switch"></a><span data-ttu-id="56fda-104">/I, параметр</span><span class="sxs-lookup"><span data-stu-id="56fda-104">/I switch</span></span>

<span data-ttu-id="56fda-105">Параметр **/i** задает каталоги для поиска ИМПОРТИРОВАНных IDL-файлов, включаемых файлов заголовков и файлов ACF.</span><span class="sxs-lookup"><span data-stu-id="56fda-105">The **/I** switch specifies directories to be searched for imported IDL files, included header files, and ACF files.</span></span>

``` syntax
midl /I include_path
```

## <a name="switch-options"></a><span data-ttu-id="56fda-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="56fda-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="56fda-107">*\_путь включения*</span><span class="sxs-lookup"><span data-stu-id="56fda-107">*include\_path*</span></span> 
</dt> <dd>

<span data-ttu-id="56fda-108">Указывает один или несколько каталогов, содержащих файлы импорта, включения и ACF.</span><span class="sxs-lookup"><span data-stu-id="56fda-108">Specifies one or more directories that contain import, include, and ACF files.</span></span> <span data-ttu-id="56fda-109">Пробел между параметром **/i** и *\_ путем include* является необязательным.</span><span class="sxs-lookup"><span data-stu-id="56fda-109">White space between the **/I** switch and *include\_path* is optional.</span></span> <span data-ttu-id="56fda-110">Разделяйте несколько каталогов символом точки с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="56fda-110">Separate multiple directories with a semicolon character (;).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56fda-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56fda-111">Remarks</span></span>

<span data-ttu-id="56fda-112">С каждым параметром **/i** может присутствовать несколько каталогов, и при каждом вызове компилятора MIDL может появиться более одного ключа **/i** .</span><span class="sxs-lookup"><span data-stu-id="56fda-112">More than one directory can appear with each **/I** switch, and more than one **/I** switch can appear with each MIDL compiler invocation.</span></span> <span data-ttu-id="56fda-113">Поиск в каталогах выполняется в том порядке, в котором они указаны.</span><span class="sxs-lookup"><span data-stu-id="56fda-113">Directories are searched in the order they are specified.</span></span>

<span data-ttu-id="56fda-114">Параметр **/i** также передается компилятором MIDL в препроцессор c компилятора c.</span><span class="sxs-lookup"><span data-stu-id="56fda-114">The **/I** switch setting is also passed by the MIDL compiler to the C compiler's C preprocessor.</span></span> <span data-ttu-id="56fda-115">Если параметр [**\_ cmd/КПП**](-cpp-cmd.md) имеет значение, а параметр [**/КПП \_ OPT**](-cpp-opt.md) — нет, компилятор MIDL объединяет строку, указанную параметром **/КПП \_ cmd** , с параметрами **/i**, [**/d**](-d.md)и [**/u**](-u.md) и использует эту объединенную строку для вызова препроцессора C для каждого исходного файла IDL и ACF.</span><span class="sxs-lookup"><span data-stu-id="56fda-115">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the **/I**, [**/D**](-d.md), and [**/U**](-u.md) options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span> <span data-ttu-id="56fda-116">Параметр компилятора MIDL **/i** не передается препроцессору, если указан параметр компилятора MIDL **/но \_ cpp** или **/КПП \_ OPT** .</span><span class="sxs-lookup"><span data-stu-id="56fda-116">The MIDL compiler switch **/I** is not passed to the preprocessor when the MIDL compiler switch **/no\_cpp** or **/cpp\_opt** is specified.</span></span>

<span data-ttu-id="56fda-117">В средах операционной системы Microsoft (64-разрядная версия Windows, 32-разрядная версия Windows, 16-разрядная версия Windows и MS-DOS) Поиск в каталогах осуществляется в следующей последовательности:</span><span class="sxs-lookup"><span data-stu-id="56fda-117">In Microsoft operating-system environments (64-bit Windows, 32-bit Windows, 16-bit Windows, and MS-DOS), directories are searched in the following sequence:</span></span>

1.  <span data-ttu-id="56fda-118">Текущий каталог.</span><span class="sxs-lookup"><span data-stu-id="56fda-118">Current directory</span></span>
2.  <span data-ttu-id="56fda-119">Каталоги, заданные параметром **/i** (в порядке следования параметру)</span><span class="sxs-lookup"><span data-stu-id="56fda-119">Directories specified by the **/I** switch (in the order they follow the switch)</span></span>
3.  <span data-ttu-id="56fda-120">Каталоги, заданные переменной среды INCLUDE</span><span class="sxs-lookup"><span data-stu-id="56fda-120">Directories specified by the INCLUDE environment variable</span></span>

<span data-ttu-id="56fda-121">При указании каталогов с параметром **/i** параметр [**идир/но \_ DEF \_**](-no-def-idir.md) предписывает компилятору MIDL игнорировать текущий каталог, игнорировать каталоги, указанные переменной среды include, и искать только указанные каталоги.</span><span class="sxs-lookup"><span data-stu-id="56fda-121">When directories are specified with the **/I** switch, the [**/no\_def\_idir**](-no-def-idir.md) switch instructs the MIDL compiler to ignore the current directory, ignore the directories specified by the INCLUDE environment variable, and search only the specified directories.</span></span>

<span data-ttu-id="56fda-122">Если с параметром **/i** не указаны каталоги, параметр [**идир/но \_ DEF \_**](-no-def-idir.md) предписывает компилятору MIDL искать только текущий каталог.</span><span class="sxs-lookup"><span data-stu-id="56fda-122">When no directories are specified with the **/I** switch, the [**/no\_def\_idir**](-no-def-idir.md) switch instructs the MIDL compiler to search only the current directory.</span></span>

## <a name="examples"></a><span data-ttu-id="56fda-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="56fda-123">Examples</span></span>

<span data-ttu-id="56fda-124">**MIDL/I c: \\ include; c: \\ включить \\ h/i \\ include2 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="56fda-124">**midl /I c:\\include;c:\\include\\h /I\\include2 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="56fda-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56fda-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56fda-126">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="56fda-126">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="56fda-127">**/акф**</span><span class="sxs-lookup"><span data-stu-id="56fda-127">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="56fda-128">**/КПП \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="56fda-128">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="56fda-129">**/КПП \_ OPT**</span><span class="sxs-lookup"><span data-stu-id="56fda-129">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="56fda-130">**\_идир/но DEF \_**</span><span class="sxs-lookup"><span data-stu-id="56fda-130">**/no\_def\_idir**</span></span>](-no-def-idir.md)
</dt> </dl>

 

 




