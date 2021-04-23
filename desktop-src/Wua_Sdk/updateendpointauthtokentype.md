---
description: Определяет тип токенов, которые могут использоваться для проверки подлинности с помощью конечной точки.
ms.assetid: 2048BD09-056F-47C1-AD2F-998DE6C52EA6
title: Перечисление Упдатиндпоинтаустокентипе (Упдатиндпоинтаус. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointAuthTokenType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: c978841511b7cfff895a15936a41d169a8500927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710897"
---
# <a name="updateendpointauthtokentype-enumeration"></a><span data-ttu-id="31097-103">Перечисление Упдатиндпоинтаустокентипе</span><span class="sxs-lookup"><span data-stu-id="31097-103">UpdateEndpointAuthTokenType enumeration</span></span>

<span data-ttu-id="31097-104">Определяет тип токенов, которые могут использоваться для проверки подлинности с помощью конечной точки.</span><span class="sxs-lookup"><span data-stu-id="31097-104">Defines the type of tokens that can be used for authenticating with an endpoint.</span></span>

## <a name="syntax"></a><span data-ttu-id="31097-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31097-105">Syntax</span></span>


```C++
typedef enum tagUpdateEndpointAuthTokenType { 
  ueattInvalidTokenType  = 0x0,
  ueattSAML11Token       = 0X1
} UpdateEndpointAuthTokenType;
```



## <a name="constants"></a><span data-ttu-id="31097-106">Константы</span><span class="sxs-lookup"><span data-stu-id="31097-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="31097-107"><span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**уеаттинвалидтокентипе**</span><span class="sxs-lookup"><span data-stu-id="31097-107"><span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattInvalidTokenType**</span></span>
</dt> <dd>

<span data-ttu-id="31097-108">Токен проверки подлинности не требуется.</span><span class="sxs-lookup"><span data-stu-id="31097-108">No authentication token is needed.</span></span>

</dd> <dt>

<span data-ttu-id="31097-109"><span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**</span><span class="sxs-lookup"><span data-stu-id="31097-109"><span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**</span></span>
</dt> <dd>

<span data-ttu-id="31097-110">Токен проверки подлинности для конечной точки является маркером WS-Security SAML (язык разметки зявлений системы безопасности (SAML)) 1,1.</span><span class="sxs-lookup"><span data-stu-id="31097-110">The authentication token for the endpoint is a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31097-111">Требования</span><span class="sxs-lookup"><span data-stu-id="31097-111">Requirements</span></span>



| <span data-ttu-id="31097-112">Требование</span><span class="sxs-lookup"><span data-stu-id="31097-112">Requirement</span></span> | <span data-ttu-id="31097-113">Значение</span><span class="sxs-lookup"><span data-stu-id="31097-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31097-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31097-114">Minimum supported client</span></span><br/> | <span data-ttu-id="31097-115">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="31097-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="31097-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31097-116">Minimum supported server</span></span><br/> | <span data-ttu-id="31097-117">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="31097-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="31097-118">Header</span><span class="sxs-lookup"><span data-stu-id="31097-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="31097-119"><dt>Упдатиндпоинтаус. h</dt></span><span class="sxs-lookup"><span data-stu-id="31097-119"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="31097-120">IDL</span><span class="sxs-lookup"><span data-stu-id="31097-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="31097-121"><dt>Упдатиндпоинтаус. idl</dt></span><span class="sxs-lookup"><span data-stu-id="31097-121"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



 

 




