---
title: Автоматические маркеры привязки
description: Автоматические дескрипторы привязок полезны, когда приложению не требуется конкретный сервер, и когда ему не требуется поддерживать какие-либо сведения о состоянии между клиентом и сервером.
ms.assetid: ba049369-6c8b-4313-a266-e0364a30056e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fe83d3f9029e0384c87e5e409583ff70f1e91ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338780"
---
# <a name="automatic-binding-handles"></a><span data-ttu-id="7c485-103">Автоматические маркеры привязки</span><span class="sxs-lookup"><span data-stu-id="7c485-103">Automatic Binding Handles</span></span>

<span data-ttu-id="7c485-104">Автоматические дескрипторы привязок полезны, когда приложению не требуется конкретный сервер, и когда ему не требуется поддерживать какие-либо сведения о состоянии между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="7c485-104">Automatic binding handles are useful when the application does not require a specific server and when it does not need to maintain any state information between the client and server.</span></span> <span data-ttu-id="7c485-105">При использовании автоматического дескриптора привязки нет необходимости писать код клиентского приложения для работы с привязками и дескрипторами — вы просто указываете использование дескриптора автоматической привязки в файле конфигурации приложения (ACF).</span><span class="sxs-lookup"><span data-stu-id="7c485-105">When you use an automatic binding handle, you do not have to write any client application code to deal with binding and handles—you simply specify the use of the automatic binding handle in the application configuration file (ACF).</span></span> <span data-ttu-id="7c485-106">Затем заглушка определяет обработчик и управляет привязкой.</span><span class="sxs-lookup"><span data-stu-id="7c485-106">The stub then defines the handle and manages the binding.</span></span>

<span data-ttu-id="7c485-107">Например, операция с отметкой времени может быть реализована с помощью автоматического обработчика.</span><span class="sxs-lookup"><span data-stu-id="7c485-107">For example, a time-stamp operation can be implemented using an auto handle.</span></span> <span data-ttu-id="7c485-108">Это не отличается от клиентского приложения, на котором сервер предоставляет его с меткой времени, поскольку может принимать время с любого доступного сервера.</span><span class="sxs-lookup"><span data-stu-id="7c485-108">It makes no difference to the client application which server provides it with the time stamp because it can accept the time from any available server.</span></span>

> [!Note]  
> <span data-ttu-id="7c485-109">Автоматические дескрипторы не поддерживаются для платформы Macintosh.</span><span class="sxs-lookup"><span data-stu-id="7c485-109">Auto handles are not supported for the Macintosh platform.</span></span>

 

<span data-ttu-id="7c485-110">Вы указываете использование автодескрипторов, включив атрибут \[ [**Auto \_ Handles**](/windows/desktop/Midl/auto-handle) \] в ACF.</span><span class="sxs-lookup"><span data-stu-id="7c485-110">You specify the use of auto handles by including the \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\] attribute in the ACF.</span></span> <span data-ttu-id="7c485-111">В примере временной метки используется следующий ACF:</span><span class="sxs-lookup"><span data-stu-id="7c485-111">The time-stamp example uses the following ACF:</span></span>

``` syntax
/* ACF file */
[
  auto_handle
]
interface autoh
{
}
```

<span data-ttu-id="7c485-112">Если ACF не содержит никаких других атрибутов дескриптора и если удаленные процедуры не используют явные дескрипторы, компилятор MIDL по умолчанию использует автоматические дескрипторы.</span><span class="sxs-lookup"><span data-stu-id="7c485-112">When the ACF does not include any other handle attribute, and when the remote procedures do not use explicit handles, the MIDL compiler uses automatic handles by default.</span></span> <span data-ttu-id="7c485-113">Он также использует автоматические дескрипторы по умолчанию, если отсутствует ACF.</span><span class="sxs-lookup"><span data-stu-id="7c485-113">It also uses automatic handles as the default when the ACF is not present.</span></span>

<span data-ttu-id="7c485-114">Удаленные процедуры указываются в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="7c485-114">The remote procedures are specified in the IDL file.</span></span> <span data-ttu-id="7c485-115">Автоматический обработчик не должен использоваться в качестве аргумента для удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="7c485-115">The auto handle must not appear as an argument to the remote procedure.</span></span> <span data-ttu-id="7c485-116">Пример:</span><span class="sxs-lookup"><span data-stu-id="7c485-116">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid (6B29FC40-CA47-1067-B31D-00DD010662DA),
  version(1.0),
  pointer_default(unique)
]
interface autoh
{
  void GetTime([out] long * time);
  void Shutdown(void);
}
```

<span data-ttu-id="7c485-117">Преимущество автоматической обработки заключается в том, что разработчику не нужно писать код для управления маркером; Суррогаты управляют привязкой автоматически.</span><span class="sxs-lookup"><span data-stu-id="7c485-117">The benefit of the auto handle is that the developer does not have to write any code to manage the handle; the stubs manage the binding automatically.</span></span> <span data-ttu-id="7c485-118">Это значительно отличается от [примера Hello, World](tutorial.md), в котором клиент управляет неявным примитивным маркером, определенным в ACF, и должен вызвать несколько функций времени выполнения для установки маркера привязки.</span><span class="sxs-lookup"><span data-stu-id="7c485-118">This is significantly different from the [Hello, World example](tutorial.md), where the client manages the implicit primitive handle defined in the ACF and must call several run-time functions to establish the binding handle.</span></span>

 

 