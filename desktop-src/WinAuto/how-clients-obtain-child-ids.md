---
title: Получение идентификаторов дочерних объектов клиентами
description: Получение идентификаторов дочерних объектов клиентами
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a67322a80a00c7cc65463ef50e5d1b470fc0b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791941"
---
# <a name="how-clients-obtain-child-ids"></a><span data-ttu-id="8a029-103">Получение идентификаторов дочерних объектов клиентами</span><span class="sxs-lookup"><span data-stu-id="8a029-103">How Clients Obtain Child IDs</span></span>

<span data-ttu-id="8a029-104">Разработчики клиента могут получить идентификатор дочернего объекта следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8a029-104">Client developers can get an object's child ID in the following ways:</span></span>

-   <span data-ttu-id="8a029-105">Вызовите [**акцессиблечилдрен**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren).</span><span class="sxs-lookup"><span data-stu-id="8a029-105">Call [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren).</span></span> <span data-ttu-id="8a029-106">Эта функция получает массив [**вариативных**](variant-structure.md) структур.</span><span class="sxs-lookup"><span data-stu-id="8a029-106">This function retrieves an array of [**VARIANT**](variant-structure.md) structures.</span></span>
-   <span data-ttu-id="8a029-107">Запросите объект, чтобы узнать, поддерживает ли он интерфейс [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="8a029-107">Query the object to see if it supports the [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) interface.</span></span> <span data-ttu-id="8a029-108">Если он имеется, используйте [**IEnumVARIANT:: Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) , чтобы получить идентификаторы дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="8a029-108">If it is present, use [**IEnumVARIANT::Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) obtain child IDs.</span></span>
-   <span data-ttu-id="8a029-109">Собирайте идентификаторы дочерних элементов, вызвав метод [**IAccessible:: аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="8a029-109">Collect the child IDs by calling the parent object's [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) method.</span></span>

> [!Note]  
> <span data-ttu-id="8a029-110">Клиент обязан освободить память, используемую для структур [**вариантов**](variant-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="8a029-110">It is the responsibility of the client to free the memory used for the [**VARIANT**](variant-structure.md) structures.</span></span> <span data-ttu-id="8a029-111">Клиенты также должны вызывать метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) для любого возвращаемого интерфейса [**IDispatch**](idispatch-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="8a029-111">Clients also must call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on any [**IDispatch**](idispatch-interface.md) interface that is returned.</span></span>

 

 

 