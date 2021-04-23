---
description: Возвращает идентификатор службы для проверки подлинности с помощью токена конечной точки.
ms.assetid: FE110B8E-F8FB-4CC8-BDD8-6427BA8B7920
title: 'Метод Иупдатиндпоинтаустокен:: ServiceID (Упдатиндпоинтаус. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.ServiceID
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 8384baa0a4f8bb48e603e0f2f8bed417e783b7f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711188"
---
# <a name="iupdateendpointauthtokenserviceid-method"></a><span data-ttu-id="eb3e2-103">Метод Иупдатиндпоинтаустокен:: ServiceID</span><span class="sxs-lookup"><span data-stu-id="eb3e2-103">IUpdateEndpointAuthToken::ServiceID method</span></span>

<span data-ttu-id="eb3e2-104">Возвращает идентификатор службы для проверки подлинности с помощью токена конечной точки.</span><span class="sxs-lookup"><span data-stu-id="eb3e2-104">Gets the identifier of the service to be authenticated with the endpoint token.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb3e2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb3e2-105">Syntax</span></span>


```C++
HRESULT ServiceID(
  [out] GUID *pServiceID
);
```



## <a name="parameters"></a><span data-ttu-id="eb3e2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb3e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb3e2-107">*псервицеид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="eb3e2-107">*pServiceID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb3e2-108">Идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="eb3e2-108">The identifier of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb3e2-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb3e2-109">Return value</span></span>

<span data-ttu-id="eb3e2-110">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="eb3e2-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="eb3e2-111">В противном случае возвращает код ошибки COM или Windows.</span><span class="sxs-lookup"><span data-stu-id="eb3e2-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb3e2-112">Требования</span><span class="sxs-lookup"><span data-stu-id="eb3e2-112">Requirements</span></span>



| <span data-ttu-id="eb3e2-113">Требование</span><span class="sxs-lookup"><span data-stu-id="eb3e2-113">Requirement</span></span> | <span data-ttu-id="eb3e2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="eb3e2-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb3e2-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb3e2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="eb3e2-116">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="eb3e2-116">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="eb3e2-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb3e2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="eb3e2-118">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="eb3e2-118">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="eb3e2-119">Header</span><span class="sxs-lookup"><span data-stu-id="eb3e2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb3e2-120"><dt>Упдатиндпоинтаус. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb3e2-120"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb3e2-121">IDL</span><span class="sxs-lookup"><span data-stu-id="eb3e2-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eb3e2-122"><dt>Упдатиндпоинтаус. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eb3e2-122"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="eb3e2-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eb3e2-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="eb3e2-124"><dt>Упдатиндпоинтаус. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb3e2-124"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="eb3e2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="eb3e2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb3e2-126"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb3e2-126"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb3e2-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb3e2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb3e2-128">**иупдатиндпоинтаустокен**</span><span class="sxs-lookup"><span data-stu-id="eb3e2-128">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




