---
description: Может возникнуть ситуация, когда экземпляр, созданный в качестве дочернего для одного родительского класса, должен изменить родительские классы и стать дочерним по отношению к другому родительскому классу.
ms.assetid: 6d0fd456-81ab-4665-bb88-f9fb29fbbd39
ms.tgt_platform: multiple
title: Изменение наследования экземпляра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a35de3dcc37d91b318ab60fb5a520cb4da10e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910295"
---
# <a name="changing-the-inheritance-of-an-instance"></a><span data-ttu-id="9f777-103">Изменение наследования экземпляра</span><span class="sxs-lookup"><span data-stu-id="9f777-103">Changing the Inheritance of an Instance</span></span>

<span data-ttu-id="9f777-104">Может возникнуть ситуация, когда экземпляр, созданный в качестве дочернего для одного родительского класса, должен изменить родительские классы и стать дочерним по отношению к другому родительскому классу.</span><span class="sxs-lookup"><span data-stu-id="9f777-104">You may find a situation where an instance that was created as a child of one parent class must change parent classes and become the child of a different parent class.</span></span> <span data-ttu-id="9f777-105">Например, у вас может быть производный класс, **мануалсервице**, описание ручной службы и производный класс, **автообслуживание**, описывающий автоматическую службу.</span><span class="sxs-lookup"><span data-stu-id="9f777-105">For example, you may have a derived class, **ManualService**, describing a manual service, and a derived class, **AutoService**, describing an automatic service.</span></span> <span data-ttu-id="9f777-106">Оба класса имеют большое количество свойств.</span><span class="sxs-lookup"><span data-stu-id="9f777-106">Both classes have a large number of properties.</span></span> <span data-ttu-id="9f777-107">Не все свойства идентичны.</span><span class="sxs-lookup"><span data-stu-id="9f777-107">Not all properties are identical.</span></span> <span data-ttu-id="9f777-108">Чтобы сменить службу с ручного на автоматический, необходимо также изменить экземпляр, представляющий службу, с **мануалсервице** на **автообслуживание**.</span><span class="sxs-lookup"><span data-stu-id="9f777-108">To change a service from manual to automatic, you must also change the instance representing the service from **ManualService** to **AutoService**.</span></span> <span data-ttu-id="9f777-109">В текущей версии инструментария WMI нельзя вызвать метод [**IWbemServices::P утинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) с параметром- *закреплением* , указывающим на экземпляр **службы автообслуживания** и ключевые свойства, описывающие экземпляр **мануалсервице** .</span><span class="sxs-lookup"><span data-stu-id="9f777-109">In the current version of WMI, you cannot call the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) method with the *pInst* parameter pointing to an instance of **AutoService** and the key properties describing the **ManualService** instance.</span></span> <span data-ttu-id="9f777-110">Если вы сделаете это, вы неявно удалите исходный экземпляр **мануалсервице** .</span><span class="sxs-lookup"><span data-stu-id="9f777-110">If you do, you implicitly delete the original **ManualService** instance.</span></span> <span data-ttu-id="9f777-111">По сути, после установки класса экземпляра можно изменить только родительский класс экземпляра, удалив экземпляр и повторно создав экземпляр в качестве экземпляра нового родительского класса.</span><span class="sxs-lookup"><span data-stu-id="9f777-111">In essence, after you establish the class of an instance, you can only change the parent class of an instance by deleting the instance and recreating the instance as an instance of the new parent class.</span></span>

<span data-ttu-id="9f777-112">В следующей процедуре описывается перемещение экземпляра из одного класса в другой класс.</span><span class="sxs-lookup"><span data-stu-id="9f777-112">The following procedure describes how to move an instance from one class to another class.</span></span>

<span data-ttu-id="9f777-113">**Перемещение экземпляра из одного класса в другой класс**</span><span class="sxs-lookup"><span data-stu-id="9f777-113">**To move an instance from one class to another class**</span></span>

1.  <span data-ttu-id="9f777-114">Удалите экземпляр из исходного класса.</span><span class="sxs-lookup"><span data-stu-id="9f777-114">Delete the instance from the original class.</span></span>
2.  <span data-ttu-id="9f777-115">Создайте экземпляр в новом классе.</span><span class="sxs-lookup"><span data-stu-id="9f777-115">Create the instance under the new class.</span></span>

    <span data-ttu-id="9f777-116">Инструментарий WMI не позволяет приложениям перемещать экземпляр путем его создания в новом классе, а затем обновлять его с помощью ключа исходного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9f777-116">WMI does not allow applications to move an instance by creating it in the new class and then updating it with the key of the original instance.</span></span>

<span data-ttu-id="9f777-117">Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="9f777-117">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 



