---
title: Вызов компилятора MIDL
description: Компилятор MIDL может создавать код для различных платформ и системных выпусков. Дополнительные сведения о предлагаемых параметрах и способах создания кода, оптимизированного для конкретного выпуска, см. в параметре/target.
ms.assetid: 57730efa-71c3-4746-83f4-c7e327888efc
keywords:
- MIDL компилятора MIDL, вызов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7e03abc49007b823f509acb35bd34ce6e47d80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2019
ms.locfileid: "105650302"
---
# <a name="invoking-the-midl-compiler"></a><span data-ttu-id="b8559-105">Вызов компилятора MIDL</span><span class="sxs-lookup"><span data-stu-id="b8559-105">Invoking the MIDL Compiler</span></span>

<span data-ttu-id="b8559-106">Компилятор MIDL может создавать код для различных платформ и системных выпусков.</span><span class="sxs-lookup"><span data-stu-id="b8559-106">The MIDL compiler can generate code for different platforms and system releases.</span></span> <span data-ttu-id="b8559-107">Дополнительные сведения о предлагаемых параметрах и способах создания кода, оптимизированного для конкретного выпуска, см. в параметре [**/Target**](-target.md) .</span><span class="sxs-lookup"><span data-stu-id="b8559-107">Consult the [**/target**](-target.md) switch to learn more about suggested switches and how to generate code optimized for a particular release.</span></span>

<span data-ttu-id="b8559-108">Запустите компилятор MIDL из командной строки с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="b8559-108">Run the MIDL compiler from the command line using the following command:</span></span>

<span data-ttu-id="b8559-109"> *<  параметры >* MIDL **имя_файла. idl**</span><span class="sxs-lookup"><span data-stu-id="b8559-109">**midl** *<***options***>* **filename.idl**</span></span>

<span data-ttu-id="b8559-110">где *<  параметры >* представляют параметры командной строки, которые необходимо использовать, а filename. idl — имя файла MIDL для компиляции.</span><span class="sxs-lookup"><span data-stu-id="b8559-110">where *<***options***>* represents the command-line options you want to use, and Filename.idl is the name of the MIDL file to compile.</span></span>

<span data-ttu-id="b8559-111">Полный список переключателей и параметров компилятора MIDL доступен при использовании компилятора MIDL [**/Help**](-help-.md) и/?</span><span class="sxs-lookup"><span data-stu-id="b8559-111">A complete listing of MIDL compiler switches and options is available when you use the MIDL compiler [**/help**](-help-.md) and /?</span></span> <span data-ttu-id="b8559-112">аргументы.</span><span class="sxs-lookup"><span data-stu-id="b8559-112">switches.</span></span> <span data-ttu-id="b8559-113">Параметры упорядочены по категориям.</span><span class="sxs-lookup"><span data-stu-id="b8559-113">The switches are organized by categories.</span></span> <span data-ttu-id="b8559-114">Дополнительные сведения см. в [справочнике по языку MIDL Command-Line](midl-command-line-reference.md).</span><span class="sxs-lookup"><span data-stu-id="b8559-114">For details, see the [MIDL Command-Line Reference](midl-command-line-reference.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b8559-115">Новый глобальный флаг **$ (оптимизация MIDL \_ )** существует в Win32. MAK.</span><span class="sxs-lookup"><span data-stu-id="b8559-115">The new global flag **$(MIDL\_OPTIMIZATION)** exists in win32.mak.</span></span> <span data-ttu-id="b8559-116">При компиляции IDL-файла с помощью этого флага созданная заглушка может использовать новейшие функции RPC, доступные на указанной платформе, и может улучшить производительность и стабильность приложения.</span><span class="sxs-lookup"><span data-stu-id="b8559-116">When an .idl file is compiled using this flag, the generated stub can utilize the latest RPC features available on the specified platform, and potentially improve the application's performance and stability.</span></span> <span data-ttu-id="b8559-117">Рекомендуется, чтобы приложения использовали этот флаг при использовании MIDL.</span><span class="sxs-lookup"><span data-stu-id="b8559-117">It's recommended that applications use this flag when using MIDL.</span></span>
>
> <span data-ttu-id="b8559-118">**MIDL** **$ ( \_ Оптимизация MIDL)** **...**</span><span class="sxs-lookup"><span data-stu-id="b8559-118">**midl** **$(MIDL\_OPTIMIZATION)** **...**</span></span>