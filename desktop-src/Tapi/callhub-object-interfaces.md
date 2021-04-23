---
description: Объект Каллхуб предоставляет методы, которые извлекают сведения о участниках в вызове из нескольких сторон.
ms.assetid: 928c3abb-1b4e-42f3-a8cc-41889ad573ed
title: Интерфейсы объектов Каллхуб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe448c7f559d38bef671144c1a6457f43d4a6b67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911208"
---
# <a name="callhub-object-interfaces"></a><span data-ttu-id="56908-103">Интерфейсы объектов Каллхуб</span><span class="sxs-lookup"><span data-stu-id="56908-103">CallHub Object Interfaces</span></span>

<span data-ttu-id="56908-104">[Объект каллхуб](callhub-object.md) предоставляет методы, которые извлекают сведения о участниках в вызове из нескольких сторон.</span><span class="sxs-lookup"><span data-stu-id="56908-104">The [CallHub object](callhub-object.md) exposes methods that retrieve information concerning participants in a multi-party call.</span></span>

<span data-ttu-id="56908-105">Интерфейсы [**иткаллхубевент**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent) и [**иенумкаллхуб**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub) не предоставляются напрямую в объекте каллхуб, но тесно связаны с ним и перечислены здесь для удобства.</span><span class="sxs-lookup"><span data-stu-id="56908-105">The [**ITCallHubEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent) and [**IEnumCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub) interfaces are not directly exposed on the CallHub Object, but are tightly related to it and are listed here for reference convenience.</span></span>



| <span data-ttu-id="56908-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="56908-106">Interface</span></span>                                | <span data-ttu-id="56908-107">Описание</span><span class="sxs-lookup"><span data-stu-id="56908-107">Description</span></span>                                                           |
|------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="56908-108">**иткаллхуб**</span><span class="sxs-lookup"><span data-stu-id="56908-108">**ITCallHub**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)           | <span data-ttu-id="56908-109">Предоставляет методы для получения информации, относящейся к объекту Каллхуб.</span><span class="sxs-lookup"><span data-stu-id="56908-109">Provides methods to retrieve information concerning a CallHub object.</span></span> |
| [<span data-ttu-id="56908-110">**иткаллхубевент**</span><span class="sxs-lookup"><span data-stu-id="56908-110">**ITCallHubEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent) | <span data-ttu-id="56908-111">Используется для получения информации, относящейся к событиям Каллхуб.</span><span class="sxs-lookup"><span data-stu-id="56908-111">Used to acquire information concerning CallHub events.</span></span>                |
| [<span data-ttu-id="56908-112">**иенумкаллхуб**</span><span class="sxs-lookup"><span data-stu-id="56908-112">**IEnumCallHub**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub)     | <span data-ttu-id="56908-113">Перечисляет [**иткаллхуб**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub).</span><span class="sxs-lookup"><span data-stu-id="56908-113">Enumerates [**ITCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub).</span></span>                            |



 

 

 



