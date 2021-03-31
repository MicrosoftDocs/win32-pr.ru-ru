---
title: язык MIDL
description: Язык MIDL (MIDL) определяет интерфейсы между клиентскими и серверными программами.
ms.assetid: 5ed1ff94-bbcb-4c6e-83aa-63d24eb84859
keywords:
- MIDL MIDL
- MIDL MIDL (см. язык MIDL MIDL)
- язык MIDL MIDL
- Язык MIDL MIDL, начальная страница
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e274d66ae234205f5db1f41b2d191ea409561bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069901"
---
# <a name="microsoft-interface-definition-language"></a><span data-ttu-id="53bd8-107">язык MIDL</span><span class="sxs-lookup"><span data-stu-id="53bd8-107">Microsoft Interface Definition Language</span></span>

## <a name="purpose"></a><span data-ttu-id="53bd8-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="53bd8-108">Purpose</span></span>

<span data-ttu-id="53bd8-109">Язык MIDL (MIDL) определяет интерфейсы между клиентскими и серверными программами.</span><span class="sxs-lookup"><span data-stu-id="53bd8-109">The Microsoft Interface Definition Language (MIDL) defines interfaces between client and server programs.</span></span> <span data-ttu-id="53bd8-110">Корпорация Майкрософт включает компилятор MIDL с пакетом SDK для платформы, позволяющий разработчикам создавать файлы на языке IDL и файлы конфигурации приложений (ACF), необходимые для интерфейсов удаленного вызова процедур (RPC) и интерфейсов COM/DCOM.</span><span class="sxs-lookup"><span data-stu-id="53bd8-110">Microsoft includes the MIDL compiler with the Platform Software Development Kit (SDK) to enable developers to create the interface definition language (IDL) files and application configuration files (ACF) required for remote procedure call (RPC) interfaces and COM/DCOM interfaces.</span></span> <span data-ttu-id="53bd8-111">MIDL также поддерживает создание библиотек типов для OLE Automation.</span><span class="sxs-lookup"><span data-stu-id="53bd8-111">MIDL also supports the generation of type libraries for OLE Automation.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="53bd8-112">Где применимо</span><span class="sxs-lookup"><span data-stu-id="53bd8-112">Where applicable</span></span>

<span data-ttu-id="53bd8-113">MIDL можно использовать во всех клиентских и серверных приложениях на основе операционных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="53bd8-113">MIDL can be used in all client/server applications based on Windows operating systems.</span></span> <span data-ttu-id="53bd8-114">Его также можно использовать для создания клиентских и серверных программ для разнородных сетевых сред, включающих такие операционные системы, как UNIX и Apple.</span><span class="sxs-lookup"><span data-stu-id="53bd8-114">It can also be used to create client and server programs for heterogeneous network environments that include such operating systems as Unix and Apple.</span></span> <span data-ttu-id="53bd8-115">Корпорация Майкрософт поддерживает службу Open Group (ранее известная как Open Software Foundation) DCE для взаимодействия с RPC.</span><span class="sxs-lookup"><span data-stu-id="53bd8-115">Microsoft supports the Open Group (formerly known as the Open Software Foundation) DCE standard for RPC interoperability.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="53bd8-116">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="53bd8-116">Developer audience</span></span>

<span data-ttu-id="53bd8-117">При использовании MIDL с RPC вы знакомы с программированием C/C++, и требуется парадигма RPC.</span><span class="sxs-lookup"><span data-stu-id="53bd8-117">When using MIDL with RPC, familiarity with C/C++ programming and the RPC paradigm is required.</span></span> <span data-ttu-id="53bd8-118">При использовании MIDL с COM знакомство с программированием на C++ и парадигмой RPC по мере применения к COM является обязательным, или же требуется знакомство с сценариями модели OLE-автоматизации и библиотеками типов.</span><span class="sxs-lookup"><span data-stu-id="53bd8-118">When using MIDL with COM, familiarity with C++ programming and the RPC paradigm as it applies to COM is required, or alternatively, familiarity with OLE Automation model scripting and type libraries is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="53bd8-119">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="53bd8-119">Run-time requirements</span></span>

<span data-ttu-id="53bd8-120">Соответствующие библиотеки времени выполнения для использования MIDL входят в состав Windows.</span><span class="sxs-lookup"><span data-stu-id="53bd8-120">The appropriate run-time libraries for using MIDL are included with Windows.</span></span> <span data-ttu-id="53bd8-121">Компилятор MIDL и компоненты среды разработки RPC устанавливаются при установке Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="53bd8-121">The MIDL compiler and the components of the RPC development environment are installed when you install the Windows SDK.</span></span> <span data-ttu-id="53bd8-122">Дополнительные сведения см. в разделе [Использование КОМПИЛЯТОРА MIDL](using-the-midl-compiler-2.md) и [Установка среды программирования RPC](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span><span class="sxs-lookup"><span data-stu-id="53bd8-122">For more information, see [Using the MIDL Compiler](using-the-midl-compiler-2.md) and [Installing the RPC Programming Environment](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="53bd8-123">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="53bd8-123">In this section</span></span>



| <span data-ttu-id="53bd8-124">Раздел</span><span class="sxs-lookup"><span data-stu-id="53bd8-124">Topic</span></span>                                                                                               | <span data-ttu-id="53bd8-125">Описание</span><span class="sxs-lookup"><span data-stu-id="53bd8-125">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="53bd8-126">Обзор</span><span class="sxs-lookup"><span data-stu-id="53bd8-126">Overview</span></span>](about-this-guide-2.md)<br/>                                                       | <span data-ttu-id="53bd8-127">Общие сведения о MIDL и компиляторе MIDL.</span><span class="sxs-lookup"><span data-stu-id="53bd8-127">General information about MIDL and the MIDL compiler.</span></span><br/>                   |
| [<span data-ttu-id="53bd8-128">Использование компилятора MIDL</span><span class="sxs-lookup"><span data-stu-id="53bd8-128">Using the MIDL Compiler</span></span>](using-the-midl-compiler-2.md)<br/>                                 | <span data-ttu-id="53bd8-129">Сведения об использовании MIDL компилтер для создания заглушек RPC.</span><span class="sxs-lookup"><span data-stu-id="53bd8-129">Information about using the MIDL compilter to generate RPC stubs.</span></span><br/>       |
| [<span data-ttu-id="53bd8-130">Определения интерфейсов и библиотеки типов</span><span class="sxs-lookup"><span data-stu-id="53bd8-130">Interface Definitions and Type Libraries</span></span>](interface-definitions-and-type-libraries.md)<br/> | <span data-ttu-id="53bd8-131">Документация по определениям интерфейса и библиотекам типов, относящимся к RPC.</span><span class="sxs-lookup"><span data-stu-id="53bd8-131">Documentation of RPC-specific interface definitions and type libraries.</span></span><br/> |
| [<span data-ttu-id="53bd8-132">Справочник по MIDL Command-Line</span><span class="sxs-lookup"><span data-stu-id="53bd8-132">MIDL Command-Line Reference</span></span>](midl-command-line-reference.md)<br/>                           | <span data-ttu-id="53bd8-133">Документация по параметрам командной строки компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="53bd8-133">Documentation of the MIDL compiler command-line switches.</span></span><br/>               |
| [<span data-ttu-id="53bd8-134">Справочник по языку MIDL</span><span class="sxs-lookup"><span data-stu-id="53bd8-134">MIDL Language Reference</span></span>](midl-language-reference.md)<br/>                                   | <span data-ttu-id="53bd8-135">Справочник по языку компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="53bd8-135">The MIDL compiler language reference.</span></span><br/>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="53bd8-136">См. также</span><span class="sxs-lookup"><span data-stu-id="53bd8-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53bd8-137">Удаленный вызов процедур (RPC)</span><span class="sxs-lookup"><span data-stu-id="53bd8-137">Remote Procedure Call (RPC)</span></span>](/windows/desktop/Rpc/rpc-start-page)
</dt> </dl>

 

