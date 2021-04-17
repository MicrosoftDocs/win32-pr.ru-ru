---
title: Использование библиотек типов Средства для разработчиков
description: Использование библиотек типов Средства для разработчиков
ms.assetid: 260aa694-1055-4a43-93aa-69a9d7359881
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cc0f5249075aa861a1301466f86a0f769b8bf3
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "105713227"
---
# <a name="how-developer-tools-use-type-libraries"></a><span data-ttu-id="7149d-103">Использование библиотек типов Средства для разработчиков</span><span class="sxs-lookup"><span data-stu-id="7149d-103">How Developer Tools Use Type Libraries</span></span>

<span data-ttu-id="7149d-104">На следующей схеме показано, как различные средства разработки взаимодействуют с библиотекой типов COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="7149d-104">The following diagram illustrates how the various development tools interact with a COM object's type library.</span></span> <span data-ttu-id="7149d-105">Каждая библиотека типов предоставляет стандартные программные интерфейсы, которые могут вызываться инструментами для получения сведений об элементах, описанных в этой библиотеке типов.</span><span class="sxs-lookup"><span data-stu-id="7149d-105">Each type library exposes standard programmatic interfaces that tools can call to get information about the elements described in that type library.</span></span> <span data-ttu-id="7149d-106">На этой схеме GUID означает Глобальный уникальный идентификатор и RPC для удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="7149d-106">In this diagram, GUID stands for globally unique identifier and RPC for remote procedure call.</span></span>

![Схема, показывающая, как средство разработки взаимодействует с библиотекой типов объектов C O M.](images/09983c96-3f01-4ad5-8d3e-12b8ed28c35d.png)

<span data-ttu-id="7149d-108">На предыдущей схеме средства преобразования C++, такие как компилятор MIDL и мастера, предоставляемые системой разработки Microsoft Visual C++, создают файлы заголовка и заглушки.</span><span class="sxs-lookup"><span data-stu-id="7149d-108">In the preceding diagram, the C++ conversion tools, such as the MIDL compiler and the wizards provided by the Microsoft Visual C++ development system, generate header and stub files.</span></span> <span data-ttu-id="7149d-109">Эти файлы можно добавить в проект, чтобы использовать COM-объект, описанный в библиотеке типов.</span><span class="sxs-lookup"><span data-stu-id="7149d-109">You can add these files to your project in order to use the COM object described by the type library.</span></span>

<span data-ttu-id="7149d-110">Аналогично, в Java средства разработчика создают классы Java и исходные файлы, которые затем можно импортировать в приложение.</span><span class="sxs-lookup"><span data-stu-id="7149d-110">Similarly, in Java the developer tools generate Java class and source files, which you can then import into your application.</span></span>

<span data-ttu-id="7149d-111">В Visual Basic сценарий несколько проще.</span><span class="sxs-lookup"><span data-stu-id="7149d-111">In Visual Basic, the scenario is somewhat simpler.</span></span> <span data-ttu-id="7149d-112">Создавать дополнительные файлы не требуется.</span><span class="sxs-lookup"><span data-stu-id="7149d-112">You do not need to generate additional files.</span></span> <span data-ttu-id="7149d-113">Среда Visual Basic предоставляет диалоговые окна, в которых перечислены объекты COM, установленные на компьютере в данный момент.</span><span class="sxs-lookup"><span data-stu-id="7149d-113">The Visual Basic environment provides dialog boxes listing the COM objects currently installed on your computer.</span></span> <span data-ttu-id="7149d-114">Выберите компонент, который требуется вызвать из приложения, и добавьте его в проект как компонент или ссылку.</span><span class="sxs-lookup"><span data-stu-id="7149d-114">You select the component you want to call from your application, and it is added to your project, either as a component or a reference.</span></span>

<span data-ttu-id="7149d-115">Средство просмотра OLE-COM считывает библиотеку типов, создает временный IDL-файл на основе библиотеки типов и отображает его для пользователей.</span><span class="sxs-lookup"><span data-stu-id="7149d-115">The OLE-COM viewer reads a type library, generates a temporary IDL file based on the type library, and displays it to users.</span></span> <span data-ttu-id="7149d-116">Средство просмотра OLE-COM также отображает синтаксис C++ для элементов COM, перечисленных в библиотеке типов.</span><span class="sxs-lookup"><span data-stu-id="7149d-116">The OLE-COM viewer also displays the C++ syntax for the COM elements listed in the type library.</span></span>

<span data-ttu-id="7149d-117">Дополнительные сведения о библиотеках типов см. [в разделе библиотеки типов и язык описания объектов](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).</span><span class="sxs-lookup"><span data-stu-id="7149d-117">For more information about type libraries, see [Type Libraries and the Object Description Language](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).</span></span>

 

 