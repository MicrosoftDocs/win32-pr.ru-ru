---
title: Использование MIDL
description: Создание и компиляция интерфейса язык MIDL (MIDL) и удаленного вызова процедур (RPC).
ms.assetid: 2594e3d6-d44a-4e12-8286-b9700e67702e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22da60f20cba6c558c7f1a67478adef7b407d591
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793662"
---
# <a name="using-midl"></a><span data-ttu-id="52bde-103">Использование MIDL</span><span class="sxs-lookup"><span data-stu-id="52bde-103">Using MIDL</span></span>

<span data-ttu-id="52bde-104">Все интерфейсы для программ, использующих RPC, должны быть определены в язык MIDL (MIDL) и скомпилированы с помощью компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="52bde-104">All interfaces for programs using RPC must be defined in Microsoft Interface Definition Language (MIDL) and compiled with the MIDL compiler.</span></span> <span data-ttu-id="52bde-105">В следующих разделах представлен краткий обзор создания и компиляции интерфейса MIDL.</span><span class="sxs-lookup"><span data-stu-id="52bde-105">The following topics present a brief overview of creating and compiling a MIDL interface:</span></span>

-   [<span data-ttu-id="52bde-106">Определение интерфейса с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="52bde-106">Defining an Interface with MIDL</span></span>](#defining-an-interface-with-midl)
-   [<span data-ttu-id="52bde-107">Компиляция MIDL-файла</span><span class="sxs-lookup"><span data-stu-id="52bde-107">Compiling a MIDL File</span></span>](#compiling-a-midl-file)

<span data-ttu-id="52bde-108">Подробное обсуждение этих разделов см. [в файлах IDL и ACF](the-idl-and-acf-files.md).</span><span class="sxs-lookup"><span data-stu-id="52bde-108">For a detailed discussion of these topics, see [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

## <a name="defining-an-interface-with-midl"></a><span data-ttu-id="52bde-109">Определение интерфейса с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="52bde-109">Defining an Interface with MIDL</span></span>

<span data-ttu-id="52bde-110">MIDL-файлы — это текстовые файлы, которые можно создавать и редактировать в текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="52bde-110">MIDL files are text files that you can create and edit with a text editor.</span></span> <span data-ttu-id="52bde-111">При создании идентификатора UUID для интерфейса обычно выходные данные сохраняются в шаблоне MIDL-файла.</span><span class="sxs-lookup"><span data-stu-id="52bde-111">If you generate a UUID for your interface, you will typically store the output in a template MIDL file.</span></span> <span data-ttu-id="52bde-112">Дополнительные сведения о UUID см. в разделе [создание идентификаторов UUID интерфейса](generating-interface-uuids.md).</span><span class="sxs-lookup"><span data-stu-id="52bde-112">For more information on UUIDs, see [Generating Interface UUIDs](generating-interface-uuids.md).</span></span>

<span data-ttu-id="52bde-113">Все интерфейсы в MIDL имеют тот же формат.</span><span class="sxs-lookup"><span data-stu-id="52bde-113">All interfaces in MIDL follow the same format.</span></span> <span data-ttu-id="52bde-114">Они начинаются с заголовка, содержащего список атрибутов интерфейса и имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="52bde-114">They begin with a header that contains a list of interface attributes and the interface name.</span></span> <span data-ttu-id="52bde-115">Атрибуты заключаются в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="52bde-115">The attributes are enclosed in square brackets.</span></span> <span data-ttu-id="52bde-116">За заголовком интерфейса следует его тело, заключенное в фигурные скобки.</span><span class="sxs-lookup"><span data-stu-id="52bde-116">The interface header is followed by its body, which is enclosed in curly brackets.</span></span> <span data-ttu-id="52bde-117">В следующем примере показан простой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="52bde-117">A simple interface is shown in the following example:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface MyInterface
{
  const unsigned short INT_ARRAY_LEN = 100;

  void MyRemoteProc( 
      [in] int param1,
      [out] int outArray[INT_ARRAY_LEN]
  );
}
```

<span data-ttu-id="52bde-118">Некоторые атрибуты, обычно присутствующие в определении интерфейса MIDL, — это UUID и номер версии интерфейса.</span><span class="sxs-lookup"><span data-stu-id="52bde-118">Some of the attributes that typically appear in a MIDL interface definition are the UUID and the interface version number.</span></span> <span data-ttu-id="52bde-119">Тело определения интерфейса должно содержать объявления процедур всех удаленных процедур в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="52bde-119">The body of the interface definition must contain the procedure declarations of all of the remote procedures in the interface.</span></span> <span data-ttu-id="52bde-120">Он также может содержать объявления типов данных и констант, необходимых интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="52bde-120">It can also contain the declarations of data types and constants required by the interface.</span></span>

<span data-ttu-id="52bde-121">Все параметры в объявлениях удаленных процедур должны быть объявлены как \[ [**in**](/windows/desktop/Midl/in), \] \[ [**out**](/windows/desktop/Midl/out-idl) \] или \[ **in**  \] .</span><span class="sxs-lookup"><span data-stu-id="52bde-121">All parameters in the remote procedure declarations must be declared as \[[**in**](/windows/desktop/Midl/in)\], \[[**out**](/windows/desktop/Midl/out-idl)\], or \[**in**, **out**\].</span></span> <span data-ttu-id="52bde-122">Эти объявления указывают, что клиентская программа передает данные в удаленную процедуру, получает данные из удаленной процедуры или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="52bde-122">These declarations specify that the client program passes data into a remote procedure, gets data out of a remote procedure, or both.</span></span> <span data-ttu-id="52bde-123">Более подробные сведения об объявлениях параметров интерфейса см. [в теле интерфейса IDL](the-idl-interface-body.md).</span><span class="sxs-lookup"><span data-stu-id="52bde-123">For more detailed information about interface parameter declarations, see [The IDL Interface Body](the-idl-interface-body.md).</span></span>

## <a name="compiling-a-midl-file"></a><span data-ttu-id="52bde-124">Компиляция MIDL-файла</span><span class="sxs-lookup"><span data-stu-id="52bde-124">Compiling a MIDL File</span></span>

<span data-ttu-id="52bde-125">Компилятор MIDL — это программа командной строки, которая автоматически устанавливается вместе с пакетом SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="52bde-125">The MIDL compiler is a command-line tool that is automatically installed with the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="52bde-126">Вызовите его в командном окне, введя команду **MIDL**, а затем имя файла MIDL в командной строке.</span><span class="sxs-lookup"><span data-stu-id="52bde-126">Invoke it in a command window by typing the command **midl**, followed by the name of a MIDL file, at the command line.</span></span> <span data-ttu-id="52bde-127">Убедитесь, что каталог, содержащий компилятор MIDL, находится в пути.</span><span class="sxs-lookup"><span data-stu-id="52bde-127">Make sure that the directory containing the MIDL compiler is in your path.</span></span> <span data-ttu-id="52bde-128">В следующем примере демонстрируется его использование:</span><span class="sxs-lookup"><span data-stu-id="52bde-128">The following example illustrates its use:</span></span>

<span data-ttu-id="52bde-129">**MIDL MyApp. idl**</span><span class="sxs-lookup"><span data-stu-id="52bde-129">**midl MyApp.idl**</span></span>

<span data-ttu-id="52bde-130">Обратите внимание, что нет необходимости включать расширение, если имя файла имеет расширение IDL.</span><span class="sxs-lookup"><span data-stu-id="52bde-130">Note that you do not have to include the extension if the file name has the .idl extension.</span></span> <span data-ttu-id="52bde-131">Можно также использовать [Параметры командной строки](/windows/desktop/Midl/midl-command-line-reference) компилятора MIDL, вставив их между командой **MIDL** и именем файла.</span><span class="sxs-lookup"><span data-stu-id="52bde-131">You can also use the MIDL compiler [command-line switches](/windows/desktop/Midl/midl-command-line-reference) by inserting them between the **midl** command and the file name.</span></span> <span data-ttu-id="52bde-132">Это показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="52bde-132">This is demonstrated in the following example:</span></span>

<span data-ttu-id="52bde-133">**MIDL/АКФ MyApp. ACF MyApp. idl**</span><span class="sxs-lookup"><span data-stu-id="52bde-133">**midl /acf MyApp.acf MyApp.idl**</span></span>

<span data-ttu-id="52bde-134">В этом примере компилятор MIDL выполняется с использованием файла MyApp. idl в качестве входного файла.</span><span class="sxs-lookup"><span data-stu-id="52bde-134">In this example, the MIDL compiler is executed using the file MyApp.idl as the input file.</span></span> <span data-ttu-id="52bde-135">Параметр командной строки **/АКФ** указывает компилятору использовать файл конфигурации приложения (ACF) для ввода.</span><span class="sxs-lookup"><span data-stu-id="52bde-135">The command line switch **/acf** instructs the compiler to use an application configuration file (ACF) for input as well.</span></span> <span data-ttu-id="52bde-136">Файлы конфигурации приложений более тщательно обсуждаются в [файлах IDL и ACF](the-idl-and-acf-files.md).</span><span class="sxs-lookup"><span data-stu-id="52bde-136">Application configuration files are discussed more thoroughly in [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

<span data-ttu-id="52bde-137">Более подробные сведения об использовании компилятора MIDL см. в разделе [язык MIDL (MIDL)](/windows/desktop/Midl/midl-start-page), который содержит сведения по следующим темам:</span><span class="sxs-lookup"><span data-stu-id="52bde-137">For more detailed information on using the MIDL compiler, see the [Microsoft Interface Definition Language (MIDL)](/windows/desktop/Midl/midl-start-page), which contains information on the following topics:</span></span>

-   [<span data-ttu-id="52bde-138">Требования к препроцессору C-препроцессор для MIDL</span><span class="sxs-lookup"><span data-stu-id="52bde-138">C-Preprocessor Requirements for MIDL</span></span>](/windows/desktop/Midl/c-preprocessor-requirements-for-midl)
-   [<span data-ttu-id="52bde-139">C/C++-рекомендации по компиляторам</span><span class="sxs-lookup"><span data-stu-id="52bde-139">C/C++-Compiler Considerations</span></span>](/windows/desktop/Midl/c-c-compiler-considerations)
-   [<span data-ttu-id="52bde-140">Файлы, созданные для интерфейса RPC</span><span class="sxs-lookup"><span data-stu-id="52bde-140">Files Generated for an RPC Interface</span></span>](/windows/desktop/Midl/files-generated-for-an-rpc-interface)
-   [<span data-ttu-id="52bde-141">Справочник по командной строке MIDL</span><span class="sxs-lookup"><span data-stu-id="52bde-141">MIDL Command-line Reference</span></span>](/windows/desktop/Midl/midl-command-line-reference)
-   [<span data-ttu-id="52bde-142">Справочник по языку MIDL</span><span class="sxs-lookup"><span data-stu-id="52bde-142">MIDL Language Reference</span></span>](/windows/desktop/Midl/midl-language-reference)
-   [<span data-ttu-id="52bde-143">Ошибки и предупреждения компилятора MIDL</span><span class="sxs-lookup"><span data-stu-id="52bde-143">MIDL Compiler Errors and Warnings</span></span>](/windows/desktop/Midl/midl-compiler-errors-and-warnings)

 

 