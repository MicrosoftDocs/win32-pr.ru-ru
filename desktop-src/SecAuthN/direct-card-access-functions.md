---
description: С помощью подсистемы смарт-карт можно взаимодействовать с картами, которые могут не соответствовать спецификациям ISO 7816.
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: Функции прямого доступа к карте
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad360974210114a1069db3226ee814d08008cc98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896753"
---
# <a name="direct-card-access-functions"></a><span data-ttu-id="cd87f-103">Функции прямого доступа к карте</span><span class="sxs-lookup"><span data-stu-id="cd87f-103">Direct Card Access Functions</span></span>

<span data-ttu-id="cd87f-104">С помощью подсистемы [*смарт-карт*](/windows/desktop/SecGloss/s-gly) можно взаимодействовать с картами, которые могут не соответствовать спецификациям ISO 7816.</span><span class="sxs-lookup"><span data-stu-id="cd87f-104">By using the [*smart card*](/windows/desktop/SecGloss/s-gly) subsystem, you can communicate with cards that may not conform to the ISO 7816 specifications.</span></span> <span data-ttu-id="cd87f-105">Для этого можно управлять атрибутами взаимодействия между приложением и картой, предоставляя прямую, низкоуровневые манипуляции с [*модулем чтения*](/windows/desktop/SecGloss/r-gly).</span><span class="sxs-lookup"><span data-stu-id="cd87f-105">To do this, the following functions let you control the attributes of the communications between the application and the card by giving you direct, low-level manipulation of the [*reader*](/windows/desktop/SecGloss/r-gly).</span></span>

<span data-ttu-id="cd87f-106">Чтобы использовать эти функции, необходимо предоставить идентификатор для рассматриваемого атрибута.</span><span class="sxs-lookup"><span data-stu-id="cd87f-106">To use these functions, you have to supply an identifier for the attribute in question.</span></span> <span data-ttu-id="cd87f-107">Допустимые идентификаторы и значения атрибутов см. в таблице 3-1 в статье *требования к устройствам с интерфейсом PC-Connected*.</span><span class="sxs-lookup"><span data-stu-id="cd87f-107">For valid attribute identifiers and values, refer to Table 3-1 in *Requirements for PC-Connected Interface Devices*.</span></span>



| <span data-ttu-id="cd87f-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="cd87f-108">Topic</span></span>                                    | <span data-ttu-id="cd87f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="cd87f-109">Description</span></span>                           |
|------------------------------------------|---------------------------------------|
| [<span data-ttu-id="cd87f-110">**скардконтрол**</span><span class="sxs-lookup"><span data-stu-id="cd87f-110">**SCardControl**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | <span data-ttu-id="cd87f-111">Обеспечить прямой контроль над модулем чтения.</span><span class="sxs-lookup"><span data-stu-id="cd87f-111">Provide direct control of the reader.</span></span> |
| [<span data-ttu-id="cd87f-112">**скарджетаттриб**</span><span class="sxs-lookup"><span data-stu-id="cd87f-112">**SCardGetAttrib**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | <span data-ttu-id="cd87f-113">Получение атрибутов модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="cd87f-113">Get reader attributes.</span></span>                |
| [<span data-ttu-id="cd87f-114">**скардсетаттриб**</span><span class="sxs-lookup"><span data-stu-id="cd87f-114">**SCardSetAttrib**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | <span data-ttu-id="cd87f-115">Задание атрибута чтения.</span><span class="sxs-lookup"><span data-stu-id="cd87f-115">Set reader attribute.</span></span>                 |



 

 

 
