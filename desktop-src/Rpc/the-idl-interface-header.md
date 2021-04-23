---
title: Заголовок интерфейса IDL
description: Заголовок интерфейса IDL указывает сведения об интерфейсе в целом. В отличие от ACF, заголовок интерфейса содержит атрибуты, не зависящие от платформы.
ms.assetid: 667e5228-3ea7-4910-90b9-999e6fd705e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8abce6204fdc09ed74a63a85e9366125dbef8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134515"
---
# <a name="the-idl-interface-header"></a><span data-ttu-id="f61ae-104">Заголовок интерфейса IDL</span><span class="sxs-lookup"><span data-stu-id="f61ae-104">The IDL Interface Header</span></span>

<span data-ttu-id="f61ae-105">Заголовок интерфейса IDL указывает сведения об интерфейсе в целом.</span><span class="sxs-lookup"><span data-stu-id="f61ae-105">The IDL interface header specifies information about the interface as a whole.</span></span> <span data-ttu-id="f61ae-106">В отличие от ACF, заголовок интерфейса содержит атрибуты, не зависящие от платформы.</span><span class="sxs-lookup"><span data-stu-id="f61ae-106">Unlike the ACF, the interface header contains attributes that are platform-independent.</span></span>

<span data-ttu-id="f61ae-107">Атрибуты в заголовке интерфейса являются глобальными для всего интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f61ae-107">Attributes in the interface header are global to the entire interface.</span></span> <span data-ttu-id="f61ae-108">То есть они применяются к интерфейсу и всем его частям.</span><span class="sxs-lookup"><span data-stu-id="f61ae-108">That is, they apply to the interface and all of its parts.</span></span> <span data-ttu-id="f61ae-109">Эти атрибуты заключаются в квадратные скобки в начале определения интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f61ae-109">These attributes are enclosed in square brackets at the beginning of the interface definition.</span></span> <span data-ttu-id="f61ae-110">Пример показан в следующем определении интерфейса:</span><span class="sxs-lookup"><span data-stu-id="f61ae-110">An example is shown in the following interface definition:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

<span data-ttu-id="f61ae-111">Обратите внимание, что заголовок интерфейса содержит **\[** атрибуты [**UUID**](/windows/desktop/Midl/uuid) **\]** и **\[** [**Version**](/windows/desktop/Midl/version) **\]** .</span><span class="sxs-lookup"><span data-stu-id="f61ae-111">Notice that the interface header contains the **\[**[**uuid**](/windows/desktop/Midl/uuid)**\]** and **\[**[**version**](/windows/desktop/Midl/version)**\]** attributes.</span></span> <span data-ttu-id="f61ae-112">Так как они представляют UUID и номер версии интерфейса соответственно, они являются атрибутами всего интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f61ae-112">Since these represent the UUID and version number of the interface respectively, they are attributes of the entire interface.</span></span>

<span data-ttu-id="f61ae-113">Тело интерфейса может также содержать атрибуты.</span><span class="sxs-lookup"><span data-stu-id="f61ae-113">The interface body can also contain attributes.</span></span> <span data-ttu-id="f61ae-114">Однако они не применимы ко всему интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="f61ae-114">However, they are not applicable to the entire interface.</span></span> <span data-ttu-id="f61ae-115">Они ссылаются на определенные элементы в интерфейсе, такие как параметры удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="f61ae-115">They refer to specific items in the interface such as remote procedure parameters.</span></span>

<span data-ttu-id="f61ae-116">Полное описание атрибутов заголовка IDL см. в [справочнике по языку MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="f61ae-116">For a complete discussion of the IDL header attributes, see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 