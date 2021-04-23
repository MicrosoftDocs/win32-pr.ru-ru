---
title: Основные сведения о функциях и заголовках Мпринфо
description: Для следующих функций необходимо, чтобы вызывающий объект передал информационную структуру или заголовок в качестве одного из параметров.
ms.assetid: 389002c9-2d24-4b35-ab5b-801fe2091db9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001c39bf28500d7261b3eb99abf0266470daf3d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986539"
---
# <a name="understanding-mprinfo-functions-and-information-headers"></a><span data-ttu-id="6cc5e-103">Основные сведения о функциях и заголовках Мпринфо</span><span class="sxs-lookup"><span data-stu-id="6cc5e-103">Understanding MprInfo Functions and Information Headers</span></span>

<span data-ttu-id="6cc5e-104">Для следующих функций необходимо, чтобы вызывающий объект передал информационную структуру или *заголовок* в качестве одного из параметров.</span><span class="sxs-lookup"><span data-stu-id="6cc5e-104">The following functions require that the caller pass an information structure or *header* as one of the parameters.</span></span>



| <span data-ttu-id="6cc5e-105">Функция администрирования</span><span class="sxs-lookup"><span data-stu-id="6cc5e-105">Administration function</span></span>                                                        | <span data-ttu-id="6cc5e-106">Функция настройки</span><span class="sxs-lookup"><span data-stu-id="6cc5e-106">Configuration function</span></span>                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6cc5e-107">Нет функции администрирования</span><span class="sxs-lookup"><span data-stu-id="6cc5e-107">No administration function</span></span>                                                     | [<span data-ttu-id="6cc5e-108">**мпрконфигтранспорткреате**</span><span class="sxs-lookup"><span data-stu-id="6cc5e-108">**MprConfigTransportCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportcreate)                     |
| [<span data-ttu-id="6cc5e-109">**мпрадминтранспортсетинфо**</span><span class="sxs-lookup"><span data-stu-id="6cc5e-109">**MprAdminTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo)                   | [<span data-ttu-id="6cc5e-110">**мпрконфигтранспортсетинфо**</span><span class="sxs-lookup"><span data-stu-id="6cc5e-110">**MprConfigTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo)                   |
| [<span data-ttu-id="6cc5e-111">**мпрадмининтерфацетранспортсетинфо**</span><span class="sxs-lookup"><span data-stu-id="6cc5e-111">**MprAdminInterfaceTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) | [<span data-ttu-id="6cc5e-112">**мпрконфигинтерфацетранспортсетинфо**</span><span class="sxs-lookup"><span data-stu-id="6cc5e-112">**MprConfigInterfaceTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) |
| [<span data-ttu-id="6cc5e-113">**мпрадмининтерфацетранспортадд**</span><span class="sxs-lookup"><span data-stu-id="6cc5e-113">**MprAdminInterfaceTransportAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportadd)         | [<span data-ttu-id="6cc5e-114">**мпрконфигинтерфацетранспортадд**</span><span class="sxs-lookup"><span data-stu-id="6cc5e-114">**MprConfigInterfaceTransportAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportadd)         |



 

<span data-ttu-id="6cc5e-115">Аналогичным образом следующие функции возвращают заголовки данных.</span><span class="sxs-lookup"><span data-stu-id="6cc5e-115">Similarly, the following functions return information headers.</span></span>



| <span data-ttu-id="6cc5e-116">Функция администрирования</span><span class="sxs-lookup"><span data-stu-id="6cc5e-116">Administration function</span></span>                                                        | <span data-ttu-id="6cc5e-117">Функция настройки</span><span class="sxs-lookup"><span data-stu-id="6cc5e-117">Configuration function</span></span>                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="6cc5e-118">**мпрадминтранспортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="6cc5e-118">**MprAdminTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo)                   | [<span data-ttu-id="6cc5e-119">**мпрконфигтранспортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="6cc5e-119">**MprConfigTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo)                   |
| [<span data-ttu-id="6cc5e-120">**мпрадмининтерфацетранспортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="6cc5e-120">**MprAdminInterfaceTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) | [<span data-ttu-id="6cc5e-121">**мпрконфигинтерфацетранспортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="6cc5e-121">**MprConfigInterfaceTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) |



 

<span data-ttu-id="6cc5e-122">Для транспортных функций заголовок Information содержит глобальные сведения для транспорта.</span><span class="sxs-lookup"><span data-stu-id="6cc5e-122">For the transport functions, the information header contains global information for the transport.</span></span> <span data-ttu-id="6cc5e-123">Для функций клиента (Интерфацетранспорт) в заголовке содержатся сведения, относящиеся к администрированием клиента (например, OSPF).</span><span class="sxs-lookup"><span data-stu-id="6cc5e-123">For the client (InterfaceTransport) functions, the header contains information specific to the client (for example, OSPF) being administered.</span></span>

<span data-ttu-id="6cc5e-124">Заголовки данных и их содержимое следует манипулировать только с помощью функций [мпринфо](router-information-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="6cc5e-124">The information headers and their contents should be manipulated only by using the [MprInfo](router-information-functions.md) functions.</span></span> <span data-ttu-id="6cc5e-125">Разработчикам не следует пытаться управлять содержимым заголовков данных напрямую.</span><span class="sxs-lookup"><span data-stu-id="6cc5e-125">Developers should not attempt to manipulate the contents of the information headers directly.</span></span>

<span data-ttu-id="6cc5e-126">В таких функциях, как [**мпрадмининтерфацесетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) , не требуется использовать функции мпринфо.</span><span class="sxs-lookup"><span data-stu-id="6cc5e-126">The interface-only functions such as [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) do not require the use of MprInfo functions.</span></span> <span data-ttu-id="6cc5e-127">Сведения, которые передаются и возвращаются с помощью этих функций, всегда находятся в виде [**структуры \_ интерфейса MPR**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) .</span><span class="sxs-lookup"><span data-stu-id="6cc5e-127">The information that is passed and returned with these functions is always in the form of an [**MPR\_INTERFACE**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) structure.</span></span>

 

 




