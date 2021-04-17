---
description: БАНКОМАТ попадает в категорию корневых данных и плоскости управления с корнем.
ms.assetid: 8e355efe-2903-49c1-a9b3-792b07bd2995
title: ATM-точка — MultiPoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba17616feadfe1c8bf87ee8468dd967af73452c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711051"
---
# <a name="atm-point-to-multipoint"></a><span data-ttu-id="456c4-103">ATM-точка — MultiPoint</span><span class="sxs-lookup"><span data-stu-id="456c4-103">ATM Point to Multipoint</span></span>

<span data-ttu-id="456c4-104">БАНКОМАТ попадает в категорию корневых данных и плоскости управления с корнем.</span><span class="sxs-lookup"><span data-stu-id="456c4-104">ATM falls into the category of rooted data and rooted control planes.</span></span> <span data-ttu-id="456c4-105">Приложение, выполняющее роль корня, создает \_ корневые сокеты c, а аналоги, выполняемые на конечных узлах, будут использовать \_ конечные сокеты c.</span><span class="sxs-lookup"><span data-stu-id="456c4-105">An application acting as the root would create c\_root sockets and counterparts running on leaf nodes would utilize c\_leaf sockets.</span></span> <span data-ttu-id="456c4-106">Корневое приложение использует [**всажоинлеаф**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) для добавления новых конечных узлов.</span><span class="sxs-lookup"><span data-stu-id="456c4-106">The root application uses [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add new leaf nodes.</span></span> <span data-ttu-id="456c4-107">Соответствующие приложения на конечных узлах будут устанавливать \_ конечные сокеты c в режиме прослушивания.</span><span class="sxs-lookup"><span data-stu-id="456c4-107">The corresponding applications on the leaf nodes will have set their c\_leaf sockets into listen mode.</span></span> <span data-ttu-id="456c4-108">**Всажоинлеаф** с \_ указанным корневым сокетом c сопоставляется с сообщением аддпарти Q. 2931.</span><span class="sxs-lookup"><span data-stu-id="456c4-108">**WSAJoinLeaf** with a c\_root socket specified is mapped to the Q.2931 ADDPARTY message.</span></span> <span data-ttu-id="456c4-109">Присоединение, инициированное конечным, не поддерживается в ATM UNI 3,1, но поддерживается в ATM UNI 4,0.</span><span class="sxs-lookup"><span data-stu-id="456c4-109">The leaf-initiated join is not supported in ATM UNI 3.1, but is supported in ATM UNI 4.0.</span></span> <span data-ttu-id="456c4-110">Таким образом, **всажоинлеаф** с \_ указанным конечным сокетом c сопоставляется с СООТВЕТСТВУЮЩИМ сообщением ATM UNI 4,0.</span><span class="sxs-lookup"><span data-stu-id="456c4-110">Thus **WSAJoinLeaf** with a c\_leaf socket specified is mapped to the appropriate ATM UNI 4.0 message.</span></span>

<span data-ttu-id="456c4-111">Существуют дополнительные соображения, которые следует учитывать при работе с точками ATM-MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="456c4-111">There are additional considerations to bear in mind for ATM point-to-multipoint:</span></span>

-   <span data-ttu-id="456c4-112">Добавление новых поразрядов в сеанс ATM-канала "точка — MultiPoint" — только приглашение.</span><span class="sxs-lookup"><span data-stu-id="456c4-112">The addition of new leaves to the ATM point-to-multipoint session is invitation-based only.</span></span> <span data-ttu-id="456c4-113">Корневые приглашения, которые уже имеют вызов функции [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) , вызывают функцию [**всажоинлеаф**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .</span><span class="sxs-lookup"><span data-stu-id="456c4-113">The root invites leaves — which have already their [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) function call — by calling the [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) function.</span></span>
-   <span data-ttu-id="456c4-114">Поток данных в сеансе ATM типа "точка — MultiPoint" — только из "root-to-листья"; листья не могут использовать один сеанс для отправки данных в корень.</span><span class="sxs-lookup"><span data-stu-id="456c4-114">The flow of data in an ATM point-to-multipoint session is from root-to-leaves only; leaves cannot use the same session to send information to the root.</span></span>
-   <span data-ttu-id="456c4-115">Допускается только один конечный на ATM-адаптер.</span><span class="sxs-lookup"><span data-stu-id="456c4-115">Only one leaf per ATM adapter is allowed.</span></span>

 

 



