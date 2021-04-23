---
title: Использование компилятора MIDL
description: Компилятор MIDL устанавливается автоматически как часть программы установки пакета средств разработки программного обеспечения (SDK) платформы.
ms.assetid: 6c001b06-01f3-42bd-85db-5d53aab54903
keywords:
- Язык MIDL MIDL, задачи
- MIDL компилятора MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fd6630a8e3fcb5c46325b5258da567fcbd0eec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412911"
---
# <a name="using-the-midl-compiler"></a><span data-ttu-id="bbe57-105">Использование компилятора MIDL</span><span class="sxs-lookup"><span data-stu-id="bbe57-105">Using the MIDL Compiler</span></span>

<span data-ttu-id="bbe57-106">Компилятор MIDL устанавливается автоматически как часть программы установки пакета средств разработки программного обеспечения (SDK) платформы.</span><span class="sxs-lookup"><span data-stu-id="bbe57-106">The MIDL compiler is automatically installed as part of the Platform Software Development Kit (SDK) setup.</span></span> <span data-ttu-id="bbe57-107">В следующих разделах описываются требования к компилятору MIDL C и требованиям препроцессора C, библиотеки ссылок, которые являются частью продукта удаленного вызова процедур (RPC), и файлы, которые MIDL создает для интерфейсов DCOM, интерфейсов RPC и интерфейсов библиотеки типов OLE Automation.</span><span class="sxs-lookup"><span data-stu-id="bbe57-107">The following topics describe the MIDL C compiler and C preprocessor requirements, the link libraries that are part of the Remote Procedure Call (RPC) product, and the files that MIDL generates for DCOM interfaces, RPC interfaces, and OLE Automation type library interfaces.</span></span>

-   [<span data-ttu-id="bbe57-108">Вызов компилятора MIDL</span><span class="sxs-lookup"><span data-stu-id="bbe57-108">Invoking the MIDL Compiler</span></span>](invoking-the-midl-compiler.md)
-   [<span data-ttu-id="bbe57-109">Файлы ответов</span><span class="sxs-lookup"><span data-stu-id="bbe57-109">Response Files</span></span>](response-files.md)
-   [<span data-ttu-id="bbe57-110">Требования к препроцессору C-препроцессор для MIDL</span><span class="sxs-lookup"><span data-stu-id="bbe57-110">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
-   [<span data-ttu-id="bbe57-111">C/C++-рекомендации по компиляторам</span><span class="sxs-lookup"><span data-stu-id="bbe57-111">C/C++-Compiler Considerations</span></span>](c-c-compiler-considerations.md)
-   [<span data-ttu-id="bbe57-112">Использование \_ \_ предопределенной константы MIDL</span><span class="sxs-lookup"><span data-stu-id="bbe57-112">Using the \_\_midl Predefined Constant</span></span>](using-the---midl-predefined-constant.md)
-   [<span data-ttu-id="bbe57-113">MIDL и RPC</span><span class="sxs-lookup"><span data-stu-id="bbe57-113">MIDL and RPC</span></span>](midl-and-rpc.md)
-   [<span data-ttu-id="bbe57-114">MIDL и COM</span><span class="sxs-lookup"><span data-stu-id="bbe57-114">MIDL and COM</span></span>](midl-and-com.md)
-   [<span data-ttu-id="bbe57-115">MIDL и ODL</span><span class="sxs-lookup"><span data-stu-id="bbe57-115">MIDL and ODL</span></span>](midl-and-odl.md)

<span data-ttu-id="bbe57-116">Дополнительные сведения о файлах, составляющих продукт RPC, см. [в разделе Установка среды программирования RPC](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span><span class="sxs-lookup"><span data-stu-id="bbe57-116">For more information about the files that make up the RPC product, see [Installing the RPC Programming Environment](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span></span>

 

 