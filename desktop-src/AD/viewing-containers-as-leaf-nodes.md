---
title: Просмотр контейнеров в виде конечных узлов
description: Любой объект в домен Active Directory Services может быть контейнером других объектов.
ms.assetid: 38300ca5-745a-4640-9723-6052a9843f45
ms.tgt_platform: multiple
keywords:
- Просмотр контейнеров в виде конечных узлов
- контейнеры Active Directory, просмотр как конечных узлов
- Конечная реклама, просмотр контейнеров как конечных узлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1631526ed78132829a7576960a997b13cc232b5f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104336761"
---
# <a name="viewing-containers-as-leaf-nodes"></a><span data-ttu-id="9e35e-106">Просмотр контейнеров в виде конечных узлов</span><span class="sxs-lookup"><span data-stu-id="9e35e-106">Viewing Containers as Leaf Nodes</span></span>

<span data-ttu-id="9e35e-107">Любой объект в домен Active Directory Services может быть контейнером других объектов.</span><span class="sxs-lookup"><span data-stu-id="9e35e-107">Any object in Active Directory Domain Services can be a container of other objects.</span></span> <span data-ttu-id="9e35e-108">Это может нагружать пользовательский интерфейс, поэтому можно объявить, что объект определенного класса должен отображаться только как лист в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="9e35e-108">This can clutter the user interface, so it is possible to declare that an object of a specific class be only be displayed as a leaf in the user interface.</span></span> <span data-ttu-id="9e35e-109">Атрибут **треатаслеаф** является атрибутом отображения с одним значением, который определяет, должны ли объекты этого класса отображаться только как конечные объекты.</span><span class="sxs-lookup"><span data-stu-id="9e35e-109">The **treatAsLeaf** attribute is a single-valued display specifier attribute that determines if objects of that class should be only be displayed as leaf objects.</span></span> <span data-ttu-id="9e35e-110">Этот атрибут является логическим значением, которое, если **true**, указывает, что объекты класса должны отображаться только как конечные элементы.</span><span class="sxs-lookup"><span data-stu-id="9e35e-110">This attribute is a Boolean value that, if **TRUE**, indicates that objects of the class should only be displayed as leaf elements.</span></span> <span data-ttu-id="9e35e-111">**Значение false** указывает, что объекты класса могут отображаться в виде контейнера или листа.</span><span class="sxs-lookup"><span data-stu-id="9e35e-111">If **FALSE**, indicates that objects of the class can be displayed as a container or a leaf.</span></span> <span data-ttu-id="9e35e-112">Как и все атрибуты спецификатора экрана, атрибут **треатаслеаф** задается для каждого языкового стандарта, поэтому этот атрибут может быть локализован по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="9e35e-112">Like all display specifier attributes, the **treatAsLeaf** attribute is set on a per-locale basis, so this attribute can be localized as required.</span></span> <span data-ttu-id="9e35e-113">Например, при **отображении пользователем** описателя "Английский язык (0409)" в качестве значения атрибута **треатаслеаф** по умолчанию установлено **значение true** .</span><span class="sxs-lookup"><span data-stu-id="9e35e-113">For example, the **User-Display** for the English locale (0409) display specifier has the **treatAsLeaf** attribute set to **TRUE** by default.</span></span> <span data-ttu-id="9e35e-114">В результате пользовательский интерфейс отображает все **пользовательские** объекты как конечные объекты.</span><span class="sxs-lookup"><span data-stu-id="9e35e-114">This causes the user interface to display all **User** objects as leaf objects.</span></span>

<span data-ttu-id="9e35e-115">\*\*Задание значения атрибута \*\*треатаслеаф\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9e35e-115">**To set the value of the **treatAsLeaf** attribute**</span></span>

1.  <span data-ttu-id="9e35e-116">Выполните привязку к нужному атрибуту дисплея в нужном языковом стандарте.</span><span class="sxs-lookup"><span data-stu-id="9e35e-116">Bind to the desired display attribute in the desired locale.</span></span> <span data-ttu-id="9e35e-117">Дополнительные сведения и пример кода см. в разделе [ДисплайспеЦифиерс Container](displayspecifiers-container.md).</span><span class="sxs-lookup"><span data-stu-id="9e35e-117">For more information and a code example, see [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>
2.  <span data-ttu-id="9e35e-118">Используйте метод [**iAds::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) , чтобы задать для атрибута **треатаслеаф** **значение true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="9e35e-118">Use the [**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put) method to set the **treatAsLeaf** attribute to either **TRUE** or **FALSE**.</span></span>
3.  <span data-ttu-id="9e35e-119">Чтобы зафиксировать изменения в каталоге, вызовите метод [**iAds:: сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="9e35e-119">To commit changes to the directory, call the [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) method.</span></span>

 

 