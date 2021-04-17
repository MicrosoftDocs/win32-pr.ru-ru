---
description: Объект TAPI является основным объектом для TAPI 3.
ms.assetid: 046f2646-6043-4d68-a42a-8750c016b3c8
title: Интерфейсы объектов TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906bda205f0d00a54cdb14cf408431cc45cad124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674139"
---
# <a name="tapi-object-interfaces"></a><span data-ttu-id="ba617-103">Интерфейсы объектов TAPI</span><span class="sxs-lookup"><span data-stu-id="ba617-103">TAPI Object Interfaces</span></span>

<span data-ttu-id="ba617-104">[Объект TAPI](tapi-object.md) является основным объектом для TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="ba617-104">The [TAPI Object](tapi-object.md) is the main object for TAPI 3.</span></span>

<span data-ttu-id="ba617-105">Интерфейс [**иттапиобжектевент**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) напрямую не предоставляется в объекте TAPI, но тесно связан с ним и указан в справочных целях для удобства.</span><span class="sxs-lookup"><span data-stu-id="ba617-105">The [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) interface is not directly exposed on the TAPI Object, but is tightly related to it and is listed here for reference convenience.</span></span>



| <span data-ttu-id="ba617-106">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="ba617-106">Interfaces</span></span>                                                 | <span data-ttu-id="ba617-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ba617-107">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba617-108">**иттапи**</span><span class="sxs-lookup"><span data-stu-id="ba617-108">**ITTAPI**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)                                   | <span data-ttu-id="ba617-109">Основной интерфейс TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="ba617-109">Primary TAPI 3 interface.</span></span>                                                                                                                              |
| [<span data-ttu-id="ba617-110">**ITTAPI2**</span><span class="sxs-lookup"><span data-stu-id="ba617-110">**ITTAPI2**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                 | <span data-ttu-id="ba617-111">Является производным от [**иттапи**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); предоставляет дополнительные методы, поддерживающие телефонные устройства.</span><span class="sxs-lookup"><span data-stu-id="ba617-111">Derives from [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); provides additional methods that support phone devices.</span></span>                                                         |
| [<span data-ttu-id="ba617-112">**иттапиевентнотификатион**</span><span class="sxs-lookup"><span data-stu-id="ba617-112">**ITTAPIEventNotification**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) | <span data-ttu-id="ba617-113">Исходящий интерфейс, используемый для получения асинхронных сведений о событиях TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="ba617-113">Outgoing interface used to receive asynchronous information about TAPI 3 events.</span></span>                                                                       |
| [<span data-ttu-id="ba617-114">**иттапикаллцентер**</span><span class="sxs-lookup"><span data-stu-id="ba617-114">**ITTAPICallCenter**</span></span>](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)               | <span data-ttu-id="ba617-115">Предоставляет интерфейс ввода в элементы управления центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="ba617-115">Provides an entry interface into call center controls.</span></span>                                                                                                 |
| [<span data-ttu-id="ba617-116">**иттапиобжектевент**</span><span class="sxs-lookup"><span data-stu-id="ba617-116">**ITTAPIObjectEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | <span data-ttu-id="ba617-117">Предоставляет методы для получения сведений о событиях объекта TAPI.</span><span class="sxs-lookup"><span data-stu-id="ba617-117">Provides methods to retrieve information concerning TAPI object events.</span></span>                                                                                |
| [<span data-ttu-id="ba617-118">**ITTAPIObjectEvent2**</span><span class="sxs-lookup"><span data-stu-id="ba617-118">**ITTAPIObjectEvent2**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | <span data-ttu-id="ba617-119">Расширяет [**иттапиобжектевент**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); предоставляет метод для получения указателя на объект Phone, вызвавший событие объекта TAPI.</span><span class="sxs-lookup"><span data-stu-id="ba617-119">Extends [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); provides a method to retrieve a pointer to the phone object that caused the TAPI object event.</span></span> |



 

 

 
