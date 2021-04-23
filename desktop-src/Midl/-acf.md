---
title: /АКФ, параметр
description: Параметр/АКФ позволяет пользователю указать явное имя файла ACF. Параметр также позволяет использовать различные имена интерфейсов в файлах IDL и ACF.
ms.assetid: 8f0833ec-1dbc-4c8a-af7e-3de42169af8d
keywords:
- MIDL/АКФ Switch
topic_type:
- apiref
api_name:
- /acf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24d66982628fbd0052e8a3f573901c430e8b8b1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103987001"
---
# <a name="acf-switch"></a><span data-ttu-id="11f2a-105">/АКФ, параметр</span><span class="sxs-lookup"><span data-stu-id="11f2a-105">/acf switch</span></span>

<span data-ttu-id="11f2a-106">Параметр **/АКФ** позволяет пользователю указать явное имя файла ACF.</span><span class="sxs-lookup"><span data-stu-id="11f2a-106">The **/acf** switch allows the user to supply an explicit ACF file name.</span></span> <span data-ttu-id="11f2a-107">Параметр также позволяет использовать различные имена интерфейсов в файлах IDL и ACF.</span><span class="sxs-lookup"><span data-stu-id="11f2a-107">The switch also allows the use of different interface names in the IDL and ACF files.</span></span>

``` syntax
midl /acf acf_filename
```

## <a name="switch-options"></a><span data-ttu-id="11f2a-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="11f2a-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="11f2a-109">*\_имя файла ACF*</span><span class="sxs-lookup"><span data-stu-id="11f2a-109">*acf\_filename*</span></span> 
</dt> <dd>

<span data-ttu-id="11f2a-110">Указывает имя ACF.</span><span class="sxs-lookup"><span data-stu-id="11f2a-110">Specifies the name of the ACF.</span></span> <span data-ttu-id="11f2a-111">Между параметром **/АКФ** и именем файла могут присутствовать пробелы.</span><span class="sxs-lookup"><span data-stu-id="11f2a-111">White space may or may not be present between the **/acf** switch and the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11f2a-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11f2a-112">Remarks</span></span>

<span data-ttu-id="11f2a-113">По умолчанию компилятор MIDL формирует имя ACF путем замены расширения IDL-файла (обычно IDL) на. ACF.</span><span class="sxs-lookup"><span data-stu-id="11f2a-113">By default, the MIDL compiler constructs the name of the ACF by replacing the IDL file name extension (usually .idl) with .acf.</span></span> <span data-ttu-id="11f2a-114">При наличии параметра **/АКФ** ACF принимает его имя из указанного имени файла.</span><span class="sxs-lookup"><span data-stu-id="11f2a-114">When the **/acf** switch is present, the ACF takes its name from the specified file name.</span></span> <span data-ttu-id="11f2a-115">Параметр **/АКФ** применяется только к IDL-файлу, указанному в командной строке компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="11f2a-115">The **/acf** switch applies only to the IDL file specified on the MIDL compiler command line.</span></span> <span data-ttu-id="11f2a-116">Он не применяется к импортированным файлам.</span><span class="sxs-lookup"><span data-stu-id="11f2a-116">It does not apply to imported files.</span></span>

<span data-ttu-id="11f2a-117">При использовании параметра **/АКФ** имя интерфейса в ACF не должно совпадать с именем интерфейса MIDL.</span><span class="sxs-lookup"><span data-stu-id="11f2a-117">When the **/acf** switch is used, the interface name in the ACF need not match the MIDL interface name.</span></span> <span data-ttu-id="11f2a-118">Эта функция позволяет интерфейсам совместно использовать спецификацию ACF.</span><span class="sxs-lookup"><span data-stu-id="11f2a-118">This feature allows interfaces to share an ACF specification.</span></span>

<span data-ttu-id="11f2a-119">Если не указан абсолютный путь к ACF, компилятор MIDL выполняет поиск в текущем каталоге, каталогах, предоставленных параметром [**/i**](-i.md) , и каталогах в пути поиска включаемых данных.</span><span class="sxs-lookup"><span data-stu-id="11f2a-119">When an absolute path to an ACF is not specified, the MIDL compiler searches in the current directory, directories supplied by the [**/I**](-i.md) option, and directories in the INCLUDE path.</span></span>

<span data-ttu-id="11f2a-120">Если ACF не найден, компилятор MIDL предполагает, что для этого интерфейса нет ACF.</span><span class="sxs-lookup"><span data-stu-id="11f2a-120">If the ACF is not found, the MIDL compiler assumes there is no ACF for this interface.</span></span> <span data-ttu-id="11f2a-121">Дополнительные сведения о последовательности каталогов см. в справочных записях по параметрам [**/i**](-i.md) и [**/но \_ DEF \_ идир**](-no-def-idir.md) .</span><span class="sxs-lookup"><span data-stu-id="11f2a-121">For more information about the sequence of directories, see the reference entries for the [**/I**](-i.md) and [**/no\_def\_idir**](-no-def-idir.md) switches.</span></span> <span data-ttu-id="11f2a-122">Дополнительные сведения о **/АКФ** см. в разделе [файл определения интерфейса (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="11f2a-122">For more information relating to **/acf**, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="examples"></a><span data-ttu-id="11f2a-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="11f2a-123">Examples</span></span>

<span data-ttu-id="11f2a-124">**MIDL/АКФ Bar. ACF имя_файла. idl**</span><span class="sxs-lookup"><span data-stu-id="11f2a-124">**midl /acf bar.acf filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="11f2a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11f2a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f2a-126">**/I**</span><span class="sxs-lookup"><span data-stu-id="11f2a-126">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="11f2a-127">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="11f2a-127">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="11f2a-128">**\_идир/но DEF \_**</span><span class="sxs-lookup"><span data-stu-id="11f2a-128">**/no\_def\_idir**</span></span>](-no-def-idir.md)
</dt> </dl>

 

 




