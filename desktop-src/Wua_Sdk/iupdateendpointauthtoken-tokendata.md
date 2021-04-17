---
description: Возвращает XML-данные (переданные по каналу передачи), представляющие токен.
ms.assetid: 52EC991A-0499-4182-AC4F-512BAFB4F896
title: 'Метод Иупдатиндпоинтаустокен:: Токендата (Упдатиндпоинтаус. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenData
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: e75df7f5b13eaf36854cf7ed9abc5988b02462ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711187"
---
# <a name="iupdateendpointauthtokentokendata-method"></a><span data-ttu-id="91a02-103">Метод Иупдатиндпоинтаустокен:: Токендата</span><span class="sxs-lookup"><span data-stu-id="91a02-103">IUpdateEndpointAuthToken::TokenData method</span></span>

<span data-ttu-id="91a02-104">Возвращает XML-данные (переданные по каналу передачи), представляющие токен.</span><span class="sxs-lookup"><span data-stu-id="91a02-104">Gets the XML data (sent over the wire) that represents the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="91a02-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91a02-105">Syntax</span></span>


```C++
HRESULT TokenData(
  [out] BSTR *pszTokenData
);
```



## <a name="parameters"></a><span data-ttu-id="91a02-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="91a02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91a02-107">*псзтокендата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="91a02-107">*pszTokenData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91a02-108">XML-данные (передаваемые по каналу передачи), представляющие токен.</span><span class="sxs-lookup"><span data-stu-id="91a02-108">The XML data (sent over the wire) that represents the token.</span></span> <span data-ttu-id="91a02-109">Например, данные для маркера WS-Security SAML (язык разметки зявлений системы безопасности (SAML)) 1,1 — это код SAML, который добавляется в запрос.</span><span class="sxs-lookup"><span data-stu-id="91a02-109">For example, the data for a WS-Security SAML (Security Assertion Markup Language) 1.1 token is the SAML code that is added to the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91a02-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91a02-110">Return value</span></span>

<span data-ttu-id="91a02-111">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="91a02-111">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="91a02-112">В противном случае возвращает код ошибки COM или Windows.</span><span class="sxs-lookup"><span data-stu-id="91a02-112">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="91a02-113">Требования</span><span class="sxs-lookup"><span data-stu-id="91a02-113">Requirements</span></span>



| <span data-ttu-id="91a02-114">Требование</span><span class="sxs-lookup"><span data-stu-id="91a02-114">Requirement</span></span> | <span data-ttu-id="91a02-115">Значение</span><span class="sxs-lookup"><span data-stu-id="91a02-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91a02-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91a02-116">Minimum supported client</span></span><br/> | <span data-ttu-id="91a02-117">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="91a02-117">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="91a02-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91a02-118">Minimum supported server</span></span><br/> | <span data-ttu-id="91a02-119">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="91a02-119">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="91a02-120">Header</span><span class="sxs-lookup"><span data-stu-id="91a02-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="91a02-121"><dt>Упдатиндпоинтаус. h</dt></span><span class="sxs-lookup"><span data-stu-id="91a02-121"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="91a02-122">IDL</span><span class="sxs-lookup"><span data-stu-id="91a02-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="91a02-123"><dt>Упдатиндпоинтаус. idl</dt></span><span class="sxs-lookup"><span data-stu-id="91a02-123"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="91a02-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="91a02-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="91a02-125"><dt>Упдатиндпоинтаус. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91a02-125"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="91a02-126">DLL</span><span class="sxs-lookup"><span data-stu-id="91a02-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91a02-127"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91a02-127"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91a02-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91a02-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91a02-129">**иупдатиндпоинтаустокен**</span><span class="sxs-lookup"><span data-stu-id="91a02-129">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




