---
title: Перемещение объектов
description: Перемещение объектов
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory, перемещение объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7019904d0de42492b98ddd297ab007a6f4e52f6a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069761"
---
# <a name="moving-objects"></a><span data-ttu-id="1826b-104">Перемещение объектов</span><span class="sxs-lookup"><span data-stu-id="1826b-104">Moving Objects</span></span>

<span data-ttu-id="1826b-105">Чтобы переместить объект внутри домена, используйте метод [**иадсконтаинер. мовехере**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .</span><span class="sxs-lookup"><span data-stu-id="1826b-105">To move an object within a domain, use the [**IADsContainer.MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) method.</span></span>

<span data-ttu-id="1826b-106">**Перемещение объекта в пределах домена**</span><span class="sxs-lookup"><span data-stu-id="1826b-106">**To move an object within a domain**</span></span>

1.  <span data-ttu-id="1826b-107">Выполните привязку к интерфейсу [**iAds**](/windows/desktop/api/iads/nn-iads-iads) объекта, который необходимо переместить.</span><span class="sxs-lookup"><span data-stu-id="1826b-107">Bind to the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface of the object to move.</span></span>
2.  <span data-ttu-id="1826b-108">Получите путь к объекту для перемещения из свойства [**iAds. ADsPath**](/windows/desktop/ADSI/iads-property-methods) .</span><span class="sxs-lookup"><span data-stu-id="1826b-108">Get the ADsPath of the object to move from the [**IADs.ADsPath**](/windows/desktop/ADSI/iads-property-methods) property.</span></span>
3.  <span data-ttu-id="1826b-109">Выполните привязку к интерфейсу [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) контейнера, в который будет перемещен объект.</span><span class="sxs-lookup"><span data-stu-id="1826b-109">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface of the container where the object will be moved to.</span></span>
4.  <span data-ttu-id="1826b-110">Переместите объект с помощью метода [**иадсконтаинер. мовехере**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .</span><span class="sxs-lookup"><span data-stu-id="1826b-110">Move the object with the [**IADsContainer.MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) method.</span></span>

<span data-ttu-id="1826b-111">Если интерфейс существует для перемещенного объекта, интерфейс недействителен после перемещения объекта, поскольку объект каталога, представленный интерфейсом, больше не существует.</span><span class="sxs-lookup"><span data-stu-id="1826b-111">If an interface exists to the object that was moved, the interface is not valid after the object is moved because the directory object the interface represents no longer exists.</span></span>

<span data-ttu-id="1826b-112">Дополнительные сведения и пример кода, демонстрирующий перемещение объекта, см. в разделе [пример кода для перемещения объекта](example-code-for-moving-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="1826b-112">For more information and a code example that shows how to move an object, see [Example Code for Moving an Object](example-code-for-moving-an-object.md).</span></span>

 

 