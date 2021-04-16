---
description: Чтобы создать приложения для планшетных ПК на C \# и Visual Basic .NET, проект в Microsoft Visual Studio .NET должен содержать ссылку на сборки управляемой библиотеки для планшетных ПК. Это обеспечивает доступ к управляемой модели объектов и элементам управления.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Управляемая библиотека и элементы управления (планшетный ПК)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7299a1df0cc1b64d650ec748eb2de01ad4b776f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712622"
---
# <a name="managed-library-and-controls-tablet-pc"></a><span data-ttu-id="be219-104">Управляемая библиотека и элементы управления (планшетный ПК)</span><span class="sxs-lookup"><span data-stu-id="be219-104">Managed Library and Controls (Tablet PC)</span></span>

<span data-ttu-id="be219-105">Чтобы создать приложения для планшетных ПК на C \# и Visual Basic .NET, проект в Microsoft Visual Studio .NET должен содержать ссылку на сборки управляемой библиотеки для планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="be219-105">To build Tablet PC applications in C\# and Visual Basic .NET, your project in Microsoft Visual Studio .NET must include a reference to the Tablet PC managed library assemblies.</span></span> <span data-ttu-id="be219-106">Это обеспечивает доступ к управляемой модели объектов и элементам управления.</span><span class="sxs-lookup"><span data-stu-id="be219-106">This provides access to the managed object model and controls.</span></span>

## <a name="microsoft-visual-c-and-visual-basicnet"></a><span data-ttu-id="be219-107">Microsoft Visual C \# и visual Basic.NET</span><span class="sxs-lookup"><span data-stu-id="be219-107">Microsoft Visual C\# and Visual Basic.NET</span></span>

<span data-ttu-id="be219-108">В Windows Vista сборки управляемой библиотеки Tablet PC устанавливаются по умолчанию в двух каталогах:</span><span class="sxs-lookup"><span data-stu-id="be219-108">In Windows Vista, the Tablet PC managed library assemblies are installed by default in two directories:</span></span>

-   <span data-ttu-id="be219-109"><systemdrive>: \\ Program Files \\ Common Files \\ Microsoft Shared \\ Ink Directory</span><span class="sxs-lookup"><span data-stu-id="be219-109"><systemdrive>:\\Program Files\\Common Files\\Microsoft Shared\\Ink directory</span></span>
-   <span data-ttu-id="be219-110"><systemdrive>: \\ Program Files \\ Microsoft SDK \\ Windows \\ v 6.0 \\ bin</span><span class="sxs-lookup"><span data-stu-id="be219-110"><systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Bin</span></span>

<span data-ttu-id="be219-111">Чтобы добавить ссылку на управляемые библиотеки платформы Tablet PC в Microsoft Visual Studio .NET:</span><span class="sxs-lookup"><span data-stu-id="be219-111">To add a reference to the Tablet PC platform managed libraries in Microsoft Visual Studio .NET:</span></span>

1.  <span data-ttu-id="be219-112">Откройте проект Visual Studio .NET.</span><span class="sxs-lookup"><span data-stu-id="be219-112">Open your Visual Studio .NET project.</span></span>
2.  <span data-ttu-id="be219-113">В меню **Проект** выберите пункт **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="be219-113">On the **Project** menu, click **Add Reference**.</span></span>
3.  <span data-ttu-id="be219-114">На вкладке **.NET** в диалоговом окне **Добавление ссылки** в списке компоненты выберите **Microsoft Tablet PC API**.</span><span class="sxs-lookup"><span data-stu-id="be219-114">On the **.NET** tab in the **Add Reference** dialog box, on the components list, select **Microsoft Tablet PC API**.</span></span>
4.  <span data-ttu-id="be219-115">Нажмите кнопку **выбрать**, а затем кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="be219-115">Click **Select**, and then click **OK**.</span></span>

<span data-ttu-id="be219-116">Чтобы добавить ссылку на API анализа рукописного ввода в Visual Studio .NET, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="be219-116">To add a reference to the ink analysis APIs in Visual Studio .NET:</span></span>

1.  <span data-ttu-id="be219-117">Откройте проект Microsoft Visual Studio .NET.</span><span class="sxs-lookup"><span data-stu-id="be219-117">Open your Microsoft Visual Studio .NET project.</span></span>
2.  <span data-ttu-id="be219-118">В меню **Проект** выберите пункт **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="be219-118">On the **Project** menu, click **Add Reference**.</span></span>
3.  <span data-ttu-id="be219-119">На вкладке **.NET** в диалоговом окне **Добавление ссылки** в списке компоненты выберите пункт **управляемая библиотека анализа рукописного ввода Microsoft Tablet PC**.</span><span class="sxs-lookup"><span data-stu-id="be219-119">On the **.NET** tab in the **Add Reference** dialog box, on the components list, select **Microsoft Tablet PC Ink Analysis Managed Library**.</span></span>
4.  <span data-ttu-id="be219-120">Нажмите кнопку **выбрать**, а затем кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="be219-120">Click **Select**, and then click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="be219-121">При компиляции приложений, использующих Microsoft. Ink в Visual Studio 2005, необходимо выбрать **проект**, выбрать **свойства**, выбрать **сборку** и задать целевую платформу = x86.</span><span class="sxs-lookup"><span data-stu-id="be219-121">When compiling applications that use Microsoft.Ink on Visual Studio 2005, you must select **Project**, select **Properties**, select **Build** and set Platform target=x86.</span></span> <span data-ttu-id="be219-122">Этот параметр недоступен в продуктах Microsoft Visual Studio Express.</span><span class="sxs-lookup"><span data-stu-id="be219-122">This option is not available in Microsoft Visual Studio Express products.</span></span>

 

 

 



