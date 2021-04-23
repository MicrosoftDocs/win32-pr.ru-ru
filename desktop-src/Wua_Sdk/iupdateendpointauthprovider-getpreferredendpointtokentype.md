---
description: Возвращает предпочтительный тип маркера проверки подлинности для конечной точки службы.
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: 'Метод Иупдатиндпоинтауспровидер:: Жетпреферредендпоинттокентипе (Упдатиндпоинтаус. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetPreferredEndpointTokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 670835ee3c2dfd01ae46a7cf78395959ea9a26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263212"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a><span data-ttu-id="f2cd1-103">Метод Иупдатиндпоинтауспровидер:: Жетпреферредендпоинттокентипе</span><span class="sxs-lookup"><span data-stu-id="f2cd1-103">IUpdateEndpointAuthProvider::GetPreferredEndpointTokenType method</span></span>

<span data-ttu-id="f2cd1-104">Возвращает предпочтительный тип маркера проверки подлинности для конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-104">Returns the preferred type of authentication token for the endpoint of the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2cd1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2cd1-105">Syntax</span></span>


```C++
HRESULT GetPreferredEndpointTokenType(
  [in]  GUID               serviceId,
  [in]  UpdateEndpointType endpointType,
  [in]  ULONG              ulRequestedTypes,
  [out] ULONG              *pulPreferredTokenTypes
);
```



## <a name="parameters"></a><span data-ttu-id="f2cd1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2cd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2cd1-107">*serviceId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2cd1-107">*serviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2cd1-108">Определяет обновляемую службу.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="f2cd1-109">*endpointType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2cd1-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2cd1-110">Определяет тип конечной точки тнидед для подключения к службе.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-110">Identifies the type of endpoint tneeded to connect to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f2cd1-111">*улрекуестедтипес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2cd1-111">*ulRequestedTypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2cd1-112">Идентифицирует ORed набор токенов, поддерживаемых конечной точкой.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-112">Identifies the ORed set of tokens that are supported by the endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="f2cd1-113">*пулпреферредтокентипес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f2cd1-113">*pulPreferredTokenTypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2cd1-114">Укажите ORed набор предпочтительных типов токенов проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-114">Specify the ORed set of authentication token types that are preferred.</span></span> <span data-ttu-id="f2cd1-115">(Задайте значение 0, чтобы указать, что маркер проверки подлинности не требуется).</span><span class="sxs-lookup"><span data-stu-id="f2cd1-115">(Set to 0 to indicate that no authentication token is needed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2cd1-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2cd1-116">Return value</span></span>

<span data-ttu-id="f2cd1-117">\_При успешном выполнении возвращает значение ОК.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-117">Returns S\_OK if successful.</span></span> <span data-ttu-id="f2cd1-118">В противном случае возвращает код ошибки COM или Windows.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-118">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2cd1-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2cd1-119">Remarks</span></span>

<span data-ttu-id="f2cd1-120">При возврате этого метода WUA выбирает тип токена из предпочтительных типов и передает его в параметр tokenType метода [**жетендпоинттокен**](iupdateendpointauthprovider-getendpointtoken.md) .</span><span class="sxs-lookup"><span data-stu-id="f2cd1-120">When this method is returned, WUA chooses a token type from the preferred types and passes it to the tokenType parameter of the [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2cd1-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f2cd1-121">Requirements</span></span>



| <span data-ttu-id="f2cd1-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f2cd1-122">Requirement</span></span> | <span data-ttu-id="f2cd1-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f2cd1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2cd1-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2cd1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f2cd1-125">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f2cd1-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="f2cd1-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2cd1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f2cd1-127">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f2cd1-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="f2cd1-128">Header</span><span class="sxs-lookup"><span data-stu-id="f2cd1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2cd1-129"><dt>Упдатиндпоинтаус. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2cd1-129"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2cd1-130">IDL</span><span class="sxs-lookup"><span data-stu-id="f2cd1-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f2cd1-131"><dt>Упдатиндпоинтаус. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f2cd1-131"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="f2cd1-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f2cd1-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2cd1-133"><dt>Упдатиндпоинтаус. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2cd1-133"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="f2cd1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f2cd1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2cd1-135"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2cd1-135"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2cd1-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2cd1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2cd1-137">**иупдатиндпоинтауспровидер**</span><span class="sxs-lookup"><span data-stu-id="f2cd1-137">**IUpdateEndpointAuthProvider**</span></span>](iupdateendpointauthprovider.md)
</dt> <dt>

[<span data-ttu-id="f2cd1-138">**жетендпоинттокен**</span><span class="sxs-lookup"><span data-stu-id="f2cd1-138">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




