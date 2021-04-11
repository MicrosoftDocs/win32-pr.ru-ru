---
title: Общий синтаксис командной строки MIDL
description: Компилятор MIDL обрабатывает IDL-файл и дополнительный файл конфигурации приложения (ACF) для создания набора выходных файлов.
ms.assetid: 1906b374-d0d1-4ec8-9a00-c5228b4c29ca
keywords:
- Справочник по командной строке MIDL, общий синтаксис
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14baa145c7be03467a24bd4298cf2f502d93b6ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889080"
---
# <a name="general-midl-command-line-syntax"></a><span data-ttu-id="e1b13-104">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="e1b13-104">General MIDL Command-line Syntax</span></span>

<span data-ttu-id="e1b13-105">Компилятор MIDL обрабатывает IDL-файл и дополнительный файл конфигурации приложения (ACF) для создания набора выходных файлов.</span><span class="sxs-lookup"><span data-stu-id="e1b13-105">The MIDL compiler processes an IDL file and an optional application configuration file (ACF) to generate a set of output files.</span></span> <span data-ttu-id="e1b13-106">Атрибуты, указанные в списке атрибутов интерфейса IDL-файла, определяют, создает ли компилятор исходные файлы для интерфейса RPC или для пользовательского интерфейса OLE.</span><span class="sxs-lookup"><span data-stu-id="e1b13-106">The attributes specified in the IDL file's interface attribute list determine whether the compiler generates source files for an RPC interface or for a custom OLE interface.</span></span>

## <a name="switch-options"></a><span data-ttu-id="e1b13-107">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="e1b13-107">Switch Options</span></span>

``` syntax
     midl [command-line-switch [switch-options]] filename
    
```

<dl> <dt>

<span data-ttu-id="e1b13-108"><span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*параметр командной строки*</span><span class="sxs-lookup"><span data-stu-id="e1b13-108"><span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*command-line-switch*</span></span>
</dt> <dd>

<span data-ttu-id="e1b13-109">Задает параметры командной строки компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="e1b13-109">Specifies MIDL compiler command-line switches.</span></span> <span data-ttu-id="e1b13-110">Параметры могут присутствовать в любой последовательности.</span><span class="sxs-lookup"><span data-stu-id="e1b13-110">Switches can appear in any sequence.</span></span>

</dd> <dt>

<span data-ttu-id="e1b13-111"><span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*параметры коммутатора*</span><span class="sxs-lookup"><span data-stu-id="e1b13-111"><span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*switch-options*</span></span>
</dt> <dd>

<span data-ttu-id="e1b13-112">Задает параметры, связанные с каждым коммутатором.</span><span class="sxs-lookup"><span data-stu-id="e1b13-112">Specifies options associated with each switch.</span></span> <span data-ttu-id="e1b13-113">Допустимые параметры описаны в записи ссылки для каждого переключателя компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="e1b13-113">Valid options are described in the reference entry for each MIDL compiler switch.</span></span>

</dd> <dt>

<span data-ttu-id="e1b13-114"><span id="filename"></span><span id="FILENAME"></span>*файлов*</span><span class="sxs-lookup"><span data-stu-id="e1b13-114"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="e1b13-115">Указывает имя IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="e1b13-115">Specifies the name of the IDL file.</span></span> <span data-ttu-id="e1b13-116">Этот файл обычно имеет расширение IDL, но может иметь другой или нет.</span><span class="sxs-lookup"><span data-stu-id="e1b13-116">This file usually has the extension .idl, but it can have another or none.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1b13-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1b13-117">Remarks</span></span>

<span data-ttu-id="e1b13-118">В следующих списках показаны имена файлов, создаваемых для IDL-файла Name. idl по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e1b13-118">The following lists show the default names of the files generated for an IDL file named Name.idl.</span></span> <span data-ttu-id="e1b13-119">Для переопределения этих имен по умолчанию можно использовать параметры командной строки.</span><span class="sxs-lookup"><span data-stu-id="e1b13-119">You can use command-line switches to override these default names.</span></span> <span data-ttu-id="e1b13-120">Обратите внимание, что имя IDL-файла может иметь расширение, отличное от. idl, или вообще нет расширения.</span><span class="sxs-lookup"><span data-stu-id="e1b13-120">Note that the name of the IDL file can have an extension other than .idl, or no extension at all.</span></span>

<span data-ttu-id="e1b13-121">По умолчанию (т. е. Если список атрибутов интерфейса не содержит [**объект**](object.md) или [**локальный**](local.md) атрибут), компилятор создает следующие файлы для [интерфейса RPC](files-generated-for-an-rpc-interface.md):</span><span class="sxs-lookup"><span data-stu-id="e1b13-121">By default (that is, if the interface attribute list does not contain the [**object**](object.md) or [**local**](local.md) attribute), the compiler generates the following files for an [RPC interface](files-generated-for-an-rpc-interface.md):</span></span>

-   <span data-ttu-id="e1b13-122">Заглушка клиента (имя \_ c. c)</span><span class="sxs-lookup"><span data-stu-id="e1b13-122">Client stub (name\_c.c)</span></span>
-   <span data-ttu-id="e1b13-123">Заглушка сервера (имя \_ s. c)</span><span class="sxs-lookup"><span data-stu-id="e1b13-123">Server stub (name\_s.c)</span></span>
-   <span data-ttu-id="e1b13-124">Заголовочный файл (Name. h)</span><span class="sxs-lookup"><span data-stu-id="e1b13-124">Header file (name.h)</span></span>

<span data-ttu-id="e1b13-125">Когда атрибут [**объекта**](object.md) отображается в списке атрибутов интерфейса, компилятор создает следующие файлы для COM-интерфейса:</span><span class="sxs-lookup"><span data-stu-id="e1b13-125">When the [**object**](object.md) attribute appears in the interface attribute list, the compiler generates the following files for a COM interface:</span></span>

-   <span data-ttu-id="e1b13-126">Прокси-файл интерфейса (имя \_ p. c)</span><span class="sxs-lookup"><span data-stu-id="e1b13-126">Interface proxy file (name\_p.c)</span></span>
-   <span data-ttu-id="e1b13-127">Файл заголовка интерфейса (Name. h)</span><span class="sxs-lookup"><span data-stu-id="e1b13-127">Interface header file (name.h)</span></span>
-   <span data-ttu-id="e1b13-128">Файл UUID интерфейса (имя \_ I. c)</span><span class="sxs-lookup"><span data-stu-id="e1b13-128">Interface UUID file (name\_I.c)</span></span>

<span data-ttu-id="e1b13-129">Если [**локальный**](local.md) атрибут отображается в списке атрибутов интерфейса, компилятор создает только файл заголовка интерфейса с именем. h.</span><span class="sxs-lookup"><span data-stu-id="e1b13-129">When the [**local**](local.md) attribute appears in the interface attribute list, the compiler generates only the interface header file, Name.h.</span></span>

<span data-ttu-id="e1b13-130">Компилятор MIDL, поставляемый с Microsoft RPC, вызывает препроцессор C, как это необходимо для обработки IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="e1b13-130">The MIDL compiler provided with Microsoft RPC invokes the C preprocessor as needed to process the IDL file.</span></span> <span data-ttu-id="e1b13-131">Он не вызывает компилятор C автоматически для компиляции созданных файлов.</span><span class="sxs-lookup"><span data-stu-id="e1b13-131">It does not automatically invoke the C compiler to compile generated files.</span></span>

> [!Note]  
> <span data-ttu-id="e1b13-132">Компилятор MIDL, входящий в состав Microsoft RPC, использует другой синтаксис командной строки, чем компилятор DCE IDL.</span><span class="sxs-lookup"><span data-stu-id="e1b13-132">The MIDL compiler provided with Microsoft RPC uses a different command-line syntax than the DCE IDL compiler.</span></span>

 

<span data-ttu-id="e1b13-133">Компилятор MIDL переключает [**/env**](-env.md), [**/Server**](-server.md), [**/sstub**](-sstub.md)и [**/out**](-out.md) на файл заглушки сервера.</span><span class="sxs-lookup"><span data-stu-id="e1b13-133">The MIDL compiler switches [**/env**](-env.md), [**/server**](-server.md), [**/sstub**](-sstub.md), and [**/out**](-out.md) affect the server stub file.</span></span>

<span data-ttu-id="e1b13-134">Начиная с MIDL версии 6.0.359, параметр командной строки по умолчанию для компилятора MIDL — [**/Oicf**](-oi.md)в  [**/robust**](-robust.md).</span><span class="sxs-lookup"><span data-stu-id="e1b13-134">Starting with MIDL version 6.0.359, the default command line option for the MIDL compiler is [**/Oicf**](-oi.md)Â  [**/robust**](-robust.md).</span></span> <span data-ttu-id="e1b13-135">Чтобы отключить/robust, укажите параметр [**/но \_ надежность**](-no-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="e1b13-135">To disable /robust, specify the [**/no\_robust**](-no-robust.md) option.</span></span>

## <a name="the-header-file"></a><span data-ttu-id="e1b13-136">Файл заголовка</span><span class="sxs-lookup"><span data-stu-id="e1b13-136">The Header File</span></span>

<span data-ttu-id="e1b13-137">Файл заголовка содержит определения всех типов данных и операций, объявленных в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="e1b13-137">The header file contains definitions of all the data types and operations declared in the IDL file.</span></span> <span data-ttu-id="e1b13-138">Файл заголовка должен включаться во все модули приложений, вызывающие определенные операции, реализовывать определенные операции или манипулировать определенными типами.</span><span class="sxs-lookup"><span data-stu-id="e1b13-138">The header file must be included by all application modules that call the defined operations, implement the defined operations, or manipulate the defined types.</span></span>

<span data-ttu-id="e1b13-139">Компилятор MIDL переключает [**/Header**](-header.md) и [**/out**](-out.md) на файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="e1b13-139">The MIDL compiler switches [**/header**](-header.md) and [**/out**](-out.md) affect the header file.</span></span>

 

 




