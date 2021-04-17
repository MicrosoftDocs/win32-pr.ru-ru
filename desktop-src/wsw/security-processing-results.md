---
title: Результаты обработки безопасности
description: В защищенном канале в приложение доставляются только те сообщения, которые успешно прошли проверку безопасности.
ms.assetid: 891e1f91-406e-4997-9da6-59b5fe578d0d
keywords:
- Веб-службы результатов обработки безопасности для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf6f8964d14c8cfdca3f6bd66b2f24e9fa611d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "105700981"
---
# <a name="security-processing-results"></a><span data-ttu-id="cfe91-106">Результаты обработки безопасности</span><span class="sxs-lookup"><span data-stu-id="cfe91-106">Security Processing Results</span></span>

<span data-ttu-id="cfe91-107">В защищенном канале в приложение доставляются только те сообщения, которые успешно прошли проверку безопасности.</span><span class="sxs-lookup"><span data-stu-id="cfe91-107">On a secure channel, only those messages that successfully pass security checks are delivered to the application.</span></span> <span data-ttu-id="cfe91-108">Для этих сообщений некоторые результаты проверки безопасности присоединяются в виде свойств сообщения, и приложение может извлекать и исследовать эти свойства для выполнения дополнительных действий, таких как проверка авторизации.</span><span class="sxs-lookup"><span data-stu-id="cfe91-108">For these messages, some results from security verification are attached as message properties, and the application may extract and examine these properties to perform additional steps such as authorization checks.</span></span>


<span data-ttu-id="cfe91-109">Функцию [**всжетмессажепроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) можно использовать для получения любых свойств, связанных с безопасностью, определенных в [**\_ \_ \_ идентификаторе свойства сообщения WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span><span class="sxs-lookup"><span data-stu-id="cfe91-109">The function [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) can be used to retrieve any of the security-related properties defined in [**WS\_MESSAGE\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span></span> <span data-ttu-id="cfe91-110">**Всжетмессажепроперти** возвращает ошибку для запросов, которые запрашивают свойства безопасности, неприменимые к типу безопасности, используемому в канале.</span><span class="sxs-lookup"><span data-stu-id="cfe91-110">**WsGetMessageProperty** returns an error for queries that ask for security properties not applicable to the type of security used on the channel.</span></span> <span data-ttu-id="cfe91-111">Сообщение остается владельцем свойств, возвращаемых функцией запроса.</span><span class="sxs-lookup"><span data-stu-id="cfe91-111">The message continues to own the properties returned by the query function.</span></span>

<span data-ttu-id="cfe91-112">С результатами обработки безопасности используются следующие элементы API.</span><span class="sxs-lookup"><span data-stu-id="cfe91-112">The following API elements are used with security processing results.</span></span>

| <span data-ttu-id="cfe91-113">Перечисление</span><span class="sxs-lookup"><span data-stu-id="cfe91-113">Enumeration</span></span>                                                                | <span data-ttu-id="cfe91-114">Описание</span><span class="sxs-lookup"><span data-stu-id="cfe91-114">Description</span></span>                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cfe91-115">**\_ \_ идентификатор свойства токена безопасности WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cfe91-115">**WS\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_property_id) | <span data-ttu-id="cfe91-116">Определяет ключи для полей и свойств, которые могут быть извлечены из маркера безопасности.</span><span class="sxs-lookup"><span data-stu-id="cfe91-116">Defines the keys for the fields and properties that can be extracted from a security token.</span></span> |



 



| <span data-ttu-id="cfe91-117">Функция</span><span class="sxs-lookup"><span data-stu-id="cfe91-117">Function</span></span>                                                         | <span data-ttu-id="cfe91-118">Описание</span><span class="sxs-lookup"><span data-stu-id="cfe91-118">Description</span></span>                                           |
|------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="cfe91-119">**всжетсекурититокенпроперти**</span><span class="sxs-lookup"><span data-stu-id="cfe91-119">**WsGetSecurityTokenProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritytokenproperty) | <span data-ttu-id="cfe91-120">Извлекает из маркера безопасности поле или свойство.</span><span class="sxs-lookup"><span data-stu-id="cfe91-120">Extracts a field or a property from a security token.</span></span> |



 



| <span data-ttu-id="cfe91-121">Дескриптор</span><span class="sxs-lookup"><span data-stu-id="cfe91-121">Handle</span></span>                                       | <span data-ttu-id="cfe91-122">Описание</span><span class="sxs-lookup"><span data-stu-id="cfe91-122">Description</span></span>                                     |
|----------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="cfe91-123">\_токен безопасности \_ WS</span><span class="sxs-lookup"><span data-stu-id="cfe91-123">WS\_SECURITY\_TOKEN</span></span>](ws-security-token.md) | <span data-ttu-id="cfe91-124">Непрозрачный маркер, представляющий маркер безопасности.</span><span class="sxs-lookup"><span data-stu-id="cfe91-124">An opaque handle representing a security token.</span></span> |



 

 

 




