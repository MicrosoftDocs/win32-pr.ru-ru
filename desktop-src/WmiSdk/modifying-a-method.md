---
description: Помимо классов и экземпляров, Инструментарий WMI позволяет изменять метод. Основной причиной, по которой необходимо изменить метод, является изменение реализации метода в поставщике. Дополнительные сведения см. в разделе Написание поставщика методов.
ms.assetid: 239a994f-ecaf-4558-9626-8f5e60dd350c
ms.tgt_platform: multiple
title: Изменение метода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93009891deec8651599f73f14a73f83bba8ffd4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423597"
---
# <a name="modifying-a-method"></a><span data-ttu-id="925ea-105">Изменение метода</span><span class="sxs-lookup"><span data-stu-id="925ea-105">Modifying a Method</span></span>

<span data-ttu-id="925ea-106">Помимо классов и экземпляров, Инструментарий WMI позволяет изменять метод.</span><span class="sxs-lookup"><span data-stu-id="925ea-106">In addition to classes and instances, WMI allows you to modify a method.</span></span> <span data-ttu-id="925ea-107">Основной причиной, по которой необходимо изменить метод, является изменение реализации метода в поставщике.</span><span class="sxs-lookup"><span data-stu-id="925ea-107">The main reason you would want to modify a method is if you changed the implementation of a method in a provider.</span></span> <span data-ttu-id="925ea-108">Дополнительные сведения см. [в разделе Написание поставщика методов](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="925ea-108">For more information, see [Writing a Method Provider](writing-a-method-provider.md).</span></span>

<span data-ttu-id="925ea-109">Изменение метода не является операцией, которая может быть выполнена в скрипте.</span><span class="sxs-lookup"><span data-stu-id="925ea-109">Modifying a method is not an operation that can be done in script.</span></span>

<span data-ttu-id="925ea-110">Следующая процедура описывает, как изменить метод программным способом.</span><span class="sxs-lookup"><span data-stu-id="925ea-110">The following procedure describes how to modify a method programmatically.</span></span>

<span data-ttu-id="925ea-111">**Изменение метода программным способом**</span><span class="sxs-lookup"><span data-stu-id="925ea-111">**To modify a method programmatically**</span></span>

1.  <span data-ttu-id="925ea-112">Получите определение класса с помощью вызова [**метода ивбемклассобжект::-Method**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).</span><span class="sxs-lookup"><span data-stu-id="925ea-112">Retrieve the class definition with a call to [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).</span></span>

    <span data-ttu-id="925ea-113">Два выходных параметра, *ппинсигнатуре* и *ппаутсигнатуре*, содержат класс в параметре и класс out-Parameter соответственно.</span><span class="sxs-lookup"><span data-stu-id="925ea-113">The two out parameters, *ppInSignature* and *ppOutSignature*, contain the in-parameter class and the out-parameter class, respectively.</span></span> <span data-ttu-id="925ea-114">Возвращаемое значение объединяется в класс параметра out в качестве свойства и должно называться **ReturnValue**.</span><span class="sxs-lookup"><span data-stu-id="925ea-114">The return value is bundled into the out-parameter class as a property, and should be named **ReturnValue**.</span></span>

2.  <span data-ttu-id="925ea-115">Извлеките и измените параметры с помощью вызовов [**ивбемклассобжект:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)или [**ивбемклассобжект::D удалить**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).</span><span class="sxs-lookup"><span data-stu-id="925ea-115">Retrieve and modify the parameters with calls to [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put), or [**IWbemClassObject::Delete**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).</span></span>
3.  <span data-ttu-id="925ea-116">Поместите новую версию метода обратно в родительский класс с помощью вызова [**ивбемклассобжект::P утмесод**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="925ea-116">Place your new version of the method back into the parent class with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

<span data-ttu-id="925ea-117">Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="925ea-117">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 



