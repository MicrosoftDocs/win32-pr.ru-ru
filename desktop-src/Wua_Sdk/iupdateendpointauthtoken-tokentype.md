---
description: Возвращает тип маркера конечной точки, например маркер WS-Security SAML (язык разметки зявлений системы безопасности (SAML)) 1,1.
ms.assetid: 1C6FFAD7-DC80-4957-96B4-FA0D954786DD
title: 'Метод Иупдатиндпоинтаустокен:: TokenType (Упдатиндпоинтаус. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bc2373c5dd49a3bf01d39b63360a3cf9df9f57d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542263"
---
# <a name="iupdateendpointauthtokentokentype-method"></a><span data-ttu-id="6a70d-103">Метод Иупдатиндпоинтаустокен:: TokenType</span><span class="sxs-lookup"><span data-stu-id="6a70d-103">IUpdateEndpointAuthToken::TokenType method</span></span>

<span data-ttu-id="6a70d-104">Возвращает тип маркера конечной точки, например маркер WS-Security SAML (язык разметки зявлений системы безопасности (SAML)) 1,1.</span><span class="sxs-lookup"><span data-stu-id="6a70d-104">Gets the type of the endpoint token, such as a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a70d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a70d-105">Syntax</span></span>


```C++
HRESULT TokenType(
  [out] UpdateEndpointAuthTokenType *pTokenType
);
```



## <a name="parameters"></a><span data-ttu-id="6a70d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a70d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a70d-107">*птокентипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6a70d-107">*pTokenType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a70d-108">Тип токена конечной точки.</span><span class="sxs-lookup"><span data-stu-id="6a70d-108">The type of the endpoint token.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a70d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a70d-109">Return value</span></span>

<span data-ttu-id="6a70d-110">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="6a70d-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="6a70d-111">В противном случае возвращает код ошибки COM или Windows.</span><span class="sxs-lookup"><span data-stu-id="6a70d-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a70d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="6a70d-112">Requirements</span></span>



| <span data-ttu-id="6a70d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="6a70d-113">Requirement</span></span> | <span data-ttu-id="6a70d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="6a70d-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a70d-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a70d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6a70d-116">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6a70d-116">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="6a70d-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a70d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6a70d-118">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6a70d-118">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="6a70d-119">Header</span><span class="sxs-lookup"><span data-stu-id="6a70d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a70d-120"><dt>Упдатиндпоинтаус. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a70d-120"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a70d-121">IDL</span><span class="sxs-lookup"><span data-stu-id="6a70d-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6a70d-122"><dt>Упдатиндпоинтаус. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6a70d-122"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="6a70d-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6a70d-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="6a70d-124"><dt>Упдатиндпоинтаус. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a70d-124"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="6a70d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6a70d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a70d-126"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a70d-126"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a70d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a70d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a70d-128">**иупдатиндпоинтаустокен**</span><span class="sxs-lookup"><span data-stu-id="6a70d-128">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




