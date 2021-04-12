---
description: На основе таксономии, определенной для независимых от протокола Windows Sockets 2 схем MultiPoint/multicast, ATM попадает в категорию корневых данных и плоскости управления с корнем.
ms.assetid: 309afa65-2cc4-4b7b-9968-4c4efb2d10a3
title: Сведения о функции Winsock ATM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e82ca0531272490c2d3189467186535a63d6ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155251"
---
# <a name="winsock-atm-function-details"></a><span data-ttu-id="f0b2e-103">Сведения о функции Winsock ATM</span><span class="sxs-lookup"><span data-stu-id="f0b2e-103">Winsock ATM Function Details</span></span>

<span data-ttu-id="f0b2e-104">На основе таксономии, определенной для независимых от протокола Windows Sockets 2 схем MultiPoint/multicast, ATM попадает в категорию корневых данных и плоскости управления с корнем.</span><span class="sxs-lookup"><span data-stu-id="f0b2e-104">Based on the taxonomy defined for Windows Sockets 2 protocol-independent multipoint/multicast schemes, ATM falls into the category of rooted data and rooted control planes.</span></span> <span data-ttu-id="f0b2e-105">(Дополнительные сведения см. в спецификации API Windows Sockets 2, приложение г.) Приложение, выполняющее роль корня \_ , создает корневые сокеты c, а аналоги, работающие на конечных узлах, будут использовать \_ конечные сокеты c.</span><span class="sxs-lookup"><span data-stu-id="f0b2e-105">(See the Windows Sockets 2 API Specification, Appendix D for more information.) An application acting as the root would create c\_root sockets, and counterparts running on leaf nodes would utilize c\_leaf sockets.</span></span> <span data-ttu-id="f0b2e-106">Корневое приложение будет использовать [**всажоинлеаф**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) для добавления новых конечных узлов.</span><span class="sxs-lookup"><span data-stu-id="f0b2e-106">The root application will use [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add new leaf nodes.</span></span> <span data-ttu-id="f0b2e-107">Соответствующие приложения на конечных узлах будут устанавливать \_ конечные сокеты c в режиме прослушивания.</span><span class="sxs-lookup"><span data-stu-id="f0b2e-107">The corresponding applications on the leaf nodes will have set their c\_leaf sockets into the listening mode.</span></span> <span data-ttu-id="f0b2e-108">**Всажоинлеаф** с \_ указанным корневым сокетом c будет сопоставлен с сообщением установки Q. 2931 (для первого листа) или добавить сообщение стороны (для всех последующих конечных элементов).</span><span class="sxs-lookup"><span data-stu-id="f0b2e-108">**WSAJoinLeaf** with a c\_root socket specified will be mapped to the Q.2931 SETUP message (for the first leaf) or ADD PARTY message (for any subsequent leaves).</span></span>

> [!Note]  
> <span data-ttu-id="f0b2e-109">Параметры качества обслуживания, указанные в **всажоинлеаф** для всех последующих последовательностей, должны игнорироваться в соответствии со спецификацией ATM Forum UNI.</span><span class="sxs-lookup"><span data-stu-id="f0b2e-109">The QoS parameters specified in **WSAJoinLeaf** for any subsequent leaves should be ignored per the ATM Forum UNI specification.</span></span>

 

<span data-ttu-id="f0b2e-110">Конечное присоединение не входит в ATM UNI 3,1, но поддерживается в ATM UNI 4,0.</span><span class="sxs-lookup"><span data-stu-id="f0b2e-110">The leaf-initiated join is not part of the ATM UNI 3.1, but is supported in the ATM UNI 4.0.</span></span> <span data-ttu-id="f0b2e-111">Таким образом, [**всажоинлеаф**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) с \_ указанным конечным сокетом c можно сопоставить с СООТВЕТСТВУЮЩИМ сообщением ATM UNI 4,0.</span><span class="sxs-lookup"><span data-stu-id="f0b2e-111">Thus [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) with a c\_leaf socket specified can be mapped to the appropriate ATM UNI 4.0 message.</span></span>

<span data-ttu-id="f0b2e-112">Параметр AAL и согласование B-лли поддерживаются посредством изменения соответствующих единиц в параметре *лпскос* при вызове функции условия, указанной в [**всаакцепт**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).</span><span class="sxs-lookup"><span data-stu-id="f0b2e-112">The AAL Parameter and B-LLI negotiation is supported through the modification of the corresponding IEs in the *lpSQOS* parameter upon the invocation of the condition function specified in [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).</span></span>

> [!Note]  
> <span data-ttu-id="f0b2e-113">Изменять можно только определенные поля в этих двух наборах.</span><span class="sxs-lookup"><span data-stu-id="f0b2e-113">Only certain fields in those two IEs can be modified.</span></span> <span data-ttu-id="f0b2e-114">Дополнительные сведения см. в приложении спецификации ATM Forum UNI в C и в приложении F.</span><span class="sxs-lookup"><span data-stu-id="f0b2e-114">See the ATM Forum UNI specification Appendix C and Appendix F for details.</span></span>

 

 

 



