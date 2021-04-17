---
description: Содержит метод, используемый для получения конечной точки, используемой для подключения к службе.
ms.assetid: 4380776A-3B89-444B-B1E9-DCF640D0AEB4
title: Интерфейс Иупдатиндпоинтпровидер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider
api_type:
- COM
ms.openlocfilehash: 81e9481f5233fac05e7fa7bdf3afa53c4c55513a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711183"
---
# <a name="iupdateendpointprovider-interface"></a><span data-ttu-id="65bca-103">Интерфейс Иупдатиндпоинтпровидер</span><span class="sxs-lookup"><span data-stu-id="65bca-103">IUpdateEndpointProvider interface</span></span>

<span data-ttu-id="65bca-104">Содержит метод, используемый для получения конечной точки, используемой для подключения к службе.</span><span class="sxs-lookup"><span data-stu-id="65bca-104">Contains the method used to get an endpoint that is used to connect to a service.</span></span> <span data-ttu-id="65bca-105">Этот интерфейс реализуется при записи поставщика конечной точки.</span><span class="sxs-lookup"><span data-stu-id="65bca-105">This interface is implemented when writing an endpoint provider.</span></span>

## <a name="members"></a><span data-ttu-id="65bca-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="65bca-106">Members</span></span>

<span data-ttu-id="65bca-107">Интерфейс **иупдатиндпоинтпровидер** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="65bca-107">The **IUpdateEndpointProvider** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="65bca-108">**Иупдатиндпоинтпровидер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="65bca-108">**IUpdateEndpointProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="65bca-109">Методы</span><span class="sxs-lookup"><span data-stu-id="65bca-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="65bca-110">Методы</span><span class="sxs-lookup"><span data-stu-id="65bca-110">Methods</span></span>

<span data-ttu-id="65bca-111">Интерфейс **иупдатиндпоинтпровидер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="65bca-111">The **IUpdateEndpointProvider** interface has these methods.</span></span>



| <span data-ttu-id="65bca-112">Метод</span><span class="sxs-lookup"><span data-stu-id="65bca-112">Method</span></span>                                                                       | <span data-ttu-id="65bca-113">Описание</span><span class="sxs-lookup"><span data-stu-id="65bca-113">Description</span></span>                                                           |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="65bca-114">**жетсервицеендпоинт**</span><span class="sxs-lookup"><span data-stu-id="65bca-114">**GetServiceEndpoint**</span></span>](iupdateendpointauthprovider-getserviceendpoint.md) | <span data-ttu-id="65bca-115">Запрашивает конечную точку, используемую для подключения к службе.</span><span class="sxs-lookup"><span data-stu-id="65bca-115">Requests an endpoint that is used to connect to a service.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="65bca-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65bca-116">Remarks</span></span>

<span data-ttu-id="65bca-117">WUA вызывает метод [**жетсервицеендпоинт**](iupdateendpointauthprovider-getserviceendpoint.md) для запуска процесса согласования.</span><span class="sxs-lookup"><span data-stu-id="65bca-117">WUA calls the [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) method to start the negotiation process.</span></span> <span data-ttu-id="65bca-118">При вызове WUA передает зарегистрированные типы токенов, а реализация этого интерфейса возвращает типы токенов, которые он предпочитает использовать.</span><span class="sxs-lookup"><span data-stu-id="65bca-118">When the call is made, WUA passes in the registered token types, and the implementation of this interface returns the token types that it prefers to use.</span></span>

 

 
