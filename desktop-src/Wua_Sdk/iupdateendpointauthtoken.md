---
description: Предоставляет методы, которые WUA может использовать для сбора сведений о маркере конечной точки.
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: Интерфейс Иупдатиндпоинтаустокен (Упдатиндпоинтаус. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a5902b3c91b3ab12b311121bd7dcd8c415a68d6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497607"
---
# <a name="iupdateendpointauthtoken-interface"></a><span data-ttu-id="ed76e-103">Интерфейс Иупдатиндпоинтаустокен</span><span class="sxs-lookup"><span data-stu-id="ed76e-103">IUpdateEndpointAuthToken interface</span></span>

<span data-ttu-id="ed76e-104">Предоставляет методы, которые WUA может использовать для сбора сведений о маркере конечной точки.</span><span class="sxs-lookup"><span data-stu-id="ed76e-104">Provides the methods that WUA can use to gather information about the endpoint token.</span></span>

## <a name="members"></a><span data-ttu-id="ed76e-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="ed76e-105">Members</span></span>

<span data-ttu-id="ed76e-106">Интерфейс **иупдатиндпоинтаустокен** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ed76e-106">The **IUpdateEndpointAuthToken** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ed76e-107">**Иупдатиндпоинтаустокен** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ed76e-107">**IUpdateEndpointAuthToken** also has these types of members:</span></span>

-   [<span data-ttu-id="ed76e-108">Методы</span><span class="sxs-lookup"><span data-stu-id="ed76e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ed76e-109">Методы</span><span class="sxs-lookup"><span data-stu-id="ed76e-109">Methods</span></span>

<span data-ttu-id="ed76e-110">Интерфейс **иупдатиндпоинтаустокен** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ed76e-110">The **IUpdateEndpointAuthToken** interface has these methods.</span></span>



| <span data-ttu-id="ed76e-111">Метод</span><span class="sxs-lookup"><span data-stu-id="ed76e-111">Method</span></span>                                                                                | <span data-ttu-id="ed76e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ed76e-112">Description</span></span>                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed76e-113">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="ed76e-113">**ServiceID**</span></span>](iupdateendpointauthtoken-serviceid.md)                               | <span data-ttu-id="ed76e-114">Возвращает идентификатор службы для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ed76e-114">Gets the identifier of the service to be authenticated.</span></span><br/>                                                          |
| [<span data-ttu-id="ed76e-115">**SigningKey**</span><span class="sxs-lookup"><span data-stu-id="ed76e-115">**SigningKey**</span></span>](iupdateendpointauthtoken-signingkey.md)                             | <span data-ttu-id="ed76e-116">Возвращает ключ, используемый для подписывания исходящих сообщений между клиентским компьютером и серквице.</span><span class="sxs-lookup"><span data-stu-id="ed76e-116">Gets the key used to sign outgoing messages between the client computer and the sercvice.</span></span><br/>                        |
| [<span data-ttu-id="ed76e-117">**токендата**</span><span class="sxs-lookup"><span data-stu-id="ed76e-117">**TokenData**</span></span>](iupdateendpointauthtoken-tokendata.md)                               | <span data-ttu-id="ed76e-118">Возвращает XML-данные (переданные по каналу передачи), представляющие токен.</span><span class="sxs-lookup"><span data-stu-id="ed76e-118">Gets the XML data (sent over the wire) that represents the token.</span></span> <br/>                                               |
| [<span data-ttu-id="ed76e-119">**токенреференцеаттачед**</span><span class="sxs-lookup"><span data-stu-id="ed76e-119">**TokenReferenceAttached**</span></span>](iupdateendpointauthtoken-tokenreferenceattached.md)     | <span data-ttu-id="ed76e-120">Возвращает XML-формат присоединенной ссылки на токен.</span><span class="sxs-lookup"><span data-stu-id="ed76e-120">Gets the XML format of an attached reference to the token.</span></span><br/>                                                       |
| [<span data-ttu-id="ed76e-121">**токенреференцеунаттачед**</span><span class="sxs-lookup"><span data-stu-id="ed76e-121">**TokenReferenceUnattached**</span></span>](iupdateendpointauthtoken-tokenreferenceunattached.md) | <span data-ttu-id="ed76e-122">Возвращает XML-формат неприсоединенной ссылки на токен.</span><span class="sxs-lookup"><span data-stu-id="ed76e-122">Gets the XML format of an unattached reference to the token.</span></span><br/>                                                     |
| [<span data-ttu-id="ed76e-123">**TokenType**</span><span class="sxs-lookup"><span data-stu-id="ed76e-123">**TokenType**</span></span>](iupdateendpointauthtoken-tokentype.md)                               | <span data-ttu-id="ed76e-124">Возвращает тип маркера конечной точки, например маркер WS-Security SAML (язык разметки зявлений системы безопасности (SAML)) 1,1.</span><span class="sxs-lookup"><span data-stu-id="ed76e-124">Gets the type of the endpoint token, such as a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="ed76e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ed76e-125">Requirements</span></span>



| <span data-ttu-id="ed76e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ed76e-126">Requirement</span></span> | <span data-ttu-id="ed76e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ed76e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed76e-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed76e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ed76e-129">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ed76e-129">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="ed76e-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed76e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ed76e-131">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ed76e-131">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="ed76e-132">Header</span><span class="sxs-lookup"><span data-stu-id="ed76e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed76e-133"><dt>Упдатиндпоинтаус. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed76e-133"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="ed76e-134">IDL</span><span class="sxs-lookup"><span data-stu-id="ed76e-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ed76e-135"><dt>Упдатиндпоинтаус. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ed76e-135"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="ed76e-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ed76e-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="ed76e-137"><dt>Упдатиндпоинтаус. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed76e-137"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="ed76e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ed76e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed76e-139"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed76e-139"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



 

 
