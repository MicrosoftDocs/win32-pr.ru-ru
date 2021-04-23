---
title: Компиляция MIDL
description: Компиляция MIDL
ms.assetid: 2797ee3b-82fd-4cb5-9e95-23b2f2a8f011
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281fa66ec1b8f997dd58fc55a67c19a801d2d36
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488333"
---
# <a name="midl-compilation"></a><span data-ttu-id="392b9-103">Компиляция MIDL</span><span class="sxs-lookup"><span data-stu-id="392b9-103">MIDL Compilation</span></span>

<span data-ttu-id="392b9-104">При наличии IDL-файла, такого как [example2. idl](anatomy-of-an-idl-file.md), который определяет один или несколько интерфейсов COM и библиотеку типов, компилятор MIDL (Midl.exe) создает файлы, описанные в следующей таблице, в качестве выходных данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="392b9-104">Given an IDL file, such as [Example2.idl](anatomy-of-an-idl-file.md), that defines one or more COM interfaces and a type library, the MIDL compiler (Midl.exe) generates the files described in the following table as the default output.</span></span>



| <span data-ttu-id="392b9-105">Имя файла</span><span class="sxs-lookup"><span data-stu-id="392b9-105">Filename</span></span>                 | <span data-ttu-id="392b9-106">Описание</span><span class="sxs-lookup"><span data-stu-id="392b9-106">Description</span></span>                                                                                                                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="392b9-107">Example2. h</span><span class="sxs-lookup"><span data-stu-id="392b9-107">Example2.h</span></span><br/>    | <span data-ttu-id="392b9-108">Файл заголовка, содержащий определения типов и объявления функций для всех интерфейсов, определенных в IDL-файле, а также пересылаемые объявления для подпрограмм, вызывающих заглушки.</span><span class="sxs-lookup"><span data-stu-id="392b9-108">The header file, containing type definitions and function declarations for all of the interfaces defined in the IDL file as well as forward declarations for routines that the stubs call.</span></span><br/> |
| <span data-ttu-id="392b9-109">Example2 \_ p. c</span><span class="sxs-lookup"><span data-stu-id="392b9-109">Example2\_p.c</span></span><br/> | <span data-ttu-id="392b9-110">Прокси-файл/заглушка, который включает суррогатные точки входа как для клиентов, так и для серверов.</span><span class="sxs-lookup"><span data-stu-id="392b9-110">The proxy/stub file, which includes the surrogate entry points both for clients and for servers.</span></span><br/>                                                                                           |
| <span data-ttu-id="392b9-111">Example2 \_ i. c</span><span class="sxs-lookup"><span data-stu-id="392b9-111">Example2\_i.c</span></span><br/> | <span data-ttu-id="392b9-112">Файл идентификатора интерфейса, который определяет GUID для каждого интерфейса, указанного в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="392b9-112">The interface ID file, which defines the GUID for every interface specified in the IDL file.</span></span><br/>                                                                                               |
| <span data-ttu-id="392b9-113">Example2. tlb</span><span class="sxs-lookup"><span data-stu-id="392b9-113">Example2.tlb</span></span><br/>  | <span data-ttu-id="392b9-114">Файл составного документа, содержащий сведения о типах и объектах.</span><span class="sxs-lookup"><span data-stu-id="392b9-114">A compound document file that contains information about types and objects.</span></span><br/>                                                                                                                |
| <span data-ttu-id="392b9-115">DLLDATA. c</span><span class="sxs-lookup"><span data-stu-id="392b9-115">Dlldata.c</span></span><br/>     | <span data-ttu-id="392b9-116">Содержит данные, необходимые для создания прокси-сервера или библиотеки DLL заглушки.</span><span class="sxs-lookup"><span data-stu-id="392b9-116">Contains the data you need to create a proxy/stub DLL.</span></span><br/>                                                                                                                                     |



 

<span data-ttu-id="392b9-117">Используйте файл заголовка и все файлы c для [создания прокси-библиотеки DLL](building-and-registering-a-proxy-dll.md) , которая может поддерживать интерфейс при использовании как клиентскими приложениями, так и серверами объектов.</span><span class="sxs-lookup"><span data-stu-id="392b9-117">You use the header file and all of the .c files to [create a proxy DLL](building-and-registering-a-proxy-dll.md) that can support the interface when used both by client applications and by object servers.</span></span> <span data-ttu-id="392b9-118">\_При создании исполняемого файла для клиентского приложения, использующего интерфейс, используется файл заголовка интерфейса (example2. h) и файл идентификатора интерфейса (example2 i. c).</span><span class="sxs-lookup"><span data-stu-id="392b9-118">You use the interface header file (Example2.h) and the interface ID (Example2\_i.c) file when creating the executable file for a client application that uses the interface.</span></span> <span data-ttu-id="392b9-119">Можно выбрать включение файла библиотеки типов в качестве ресурса в EXE-файл или библиотеку DLL или поставлять его в отдельный файл.</span><span class="sxs-lookup"><span data-stu-id="392b9-119">You can choose to include the type library file as a resource in your EXE or DLL, or you can ship it as a separate file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="392b9-120">См. также</span><span class="sxs-lookup"><span data-stu-id="392b9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="392b9-121">Файлы, созданные для COM-интерфейса</span><span class="sxs-lookup"><span data-stu-id="392b9-121">Files Generated for a COM Interface</span></span>](/windows/desktop/Midl/files-generated-for-a-com-interface)
</dt> <dt>

[<span data-ttu-id="392b9-122">Параметры компилятора MIDL</span><span class="sxs-lookup"><span data-stu-id="392b9-122">MIDL Compiler Options</span></span>](midl-compiler-options.md)
</dt> </dl>

 

