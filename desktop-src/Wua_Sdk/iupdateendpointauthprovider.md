---
description: Содержит методы, используемые для согласования типа токена, используемого для проверки подлинности конечной точки службы.
ms.assetid: F6177B24-C166-4BEC-83D6-3AD5B5B3CF08
title: Интерфейс Иупдатиндпоинтауспровидер (Упдатиндпоинтаус. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 071bc23bdf9d67412fef561c71e17fe81485984f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542271"
---
# <a name="iupdateendpointauthprovider-interface"></a><span data-ttu-id="e96cf-103">Интерфейс Иупдатиндпоинтауспровидер</span><span class="sxs-lookup"><span data-stu-id="e96cf-103">IUpdateEndpointAuthProvider interface</span></span>

<span data-ttu-id="e96cf-104">Интерфейс **иупдатиндпоинтауспровидер** содержит методы, используемые для согласования типа токена, используемого для проверки подлинности конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="e96cf-104">The **IUpdateEndpointAuthProvider** interface contains the methods used for negotiating which type of token is used for authenticating the endpoint of a service.</span></span>

## <a name="members"></a><span data-ttu-id="e96cf-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="e96cf-105">Members</span></span>

<span data-ttu-id="e96cf-106">Интерфейс **иупдатиндпоинтауспровидер** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e96cf-106">The **IUpdateEndpointAuthProvider** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e96cf-107">**Иупдатиндпоинтауспровидер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e96cf-107">**IUpdateEndpointAuthProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="e96cf-108">Методы</span><span class="sxs-lookup"><span data-stu-id="e96cf-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e96cf-109">Методы</span><span class="sxs-lookup"><span data-stu-id="e96cf-109">Methods</span></span>

<span data-ttu-id="e96cf-110">Интерфейс **иупдатиндпоинтауспровидер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e96cf-110">The **IUpdateEndpointAuthProvider** interface has these methods.</span></span>



| <span data-ttu-id="e96cf-111">Метод</span><span class="sxs-lookup"><span data-stu-id="e96cf-111">Method</span></span>                                                                                             | <span data-ttu-id="e96cf-112">Описание</span><span class="sxs-lookup"><span data-stu-id="e96cf-112">Description</span></span>                                                                                    |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e96cf-113">**жетендпоинттокен**</span><span class="sxs-lookup"><span data-stu-id="e96cf-113">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)                           | <span data-ttu-id="e96cf-114">Запросите маркер для конечной точки службы, используя указанные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="e96cf-114">Request a token for the endpoint of the service using the specified credentials.</span></span><br/>    |
| [<span data-ttu-id="e96cf-115">**жетпреферредендпоинттокентипе**</span><span class="sxs-lookup"><span data-stu-id="e96cf-115">**GetPreferredEndpointTokenType**</span></span>](iupdateendpointauthprovider-getpreferredendpointtokentype.md) | <span data-ttu-id="e96cf-116">Возвращает предпочтительный тип маркера проверки подлинности для конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="e96cf-116">Returns the preferred type of authentication token for the endpoint of the service.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e96cf-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e96cf-117">Remarks</span></span>

<span data-ttu-id="e96cf-118">WUA вызывает метод [**жетпреферредендпоинттокентипе**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) этого интерфейса, чтобы начать процесс согласования.</span><span class="sxs-lookup"><span data-stu-id="e96cf-118">WUA calls the [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) method of this interface to start the negotiation process.</span></span> <span data-ttu-id="e96cf-119">При вызове WUA передает идентификатор службы, тип конечной точки, реализованной службой, и доступные типы токенов.</span><span class="sxs-lookup"><span data-stu-id="e96cf-119">When the call is made WUA passes in the service identifier, the type of endpoint implemented by the service, and the token types that are available.</span></span> <span data-ttu-id="e96cf-120">Затем реализация этого интерфейса возвращает типы токенов, которые он предпочитает использовать.</span><span class="sxs-lookup"><span data-stu-id="e96cf-120">The implementation of this interface then returns the token types that it preferes to use.</span></span>

## <a name="requirements"></a><span data-ttu-id="e96cf-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e96cf-121">Requirements</span></span>



| <span data-ttu-id="e96cf-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e96cf-122">Requirement</span></span> | <span data-ttu-id="e96cf-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e96cf-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e96cf-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e96cf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e96cf-125">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e96cf-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="e96cf-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e96cf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e96cf-127">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e96cf-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="e96cf-128">Header</span><span class="sxs-lookup"><span data-stu-id="e96cf-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e96cf-129"><dt>Упдатиндпоинтаус. h</dt></span><span class="sxs-lookup"><span data-stu-id="e96cf-129"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="e96cf-130">IDL</span><span class="sxs-lookup"><span data-stu-id="e96cf-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e96cf-131"><dt>Упдатиндпоинтаус. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e96cf-131"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="e96cf-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e96cf-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="e96cf-133"><dt>Упдатиндпоинтаус. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e96cf-133"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="e96cf-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e96cf-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e96cf-135"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e96cf-135"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



 

 
