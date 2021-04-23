---
description: Запросите маркер для конечной точки службы, используя указанные учетные данные.
ms.assetid: 2CA0F826-9A05-4385-AF1A-A8C05B3DAFE2
title: 'Метод Иупдатиндпоинтауспровидер:: Жетендпоинттокен (Упдатиндпоинтаус. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetEndpointToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 55efe38ce9782b691e1ad32f7a21f6124e1f0bf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810210"
---
# <a name="iupdateendpointauthprovidergetendpointtoken-method"></a><span data-ttu-id="992ec-103">Метод Иупдатиндпоинтауспровидер:: Жетендпоинттокен</span><span class="sxs-lookup"><span data-stu-id="992ec-103">IUpdateEndpointAuthProvider::GetEndpointToken method</span></span>

<span data-ttu-id="992ec-104">Запросите маркер для конечной точки службы, используя указанные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="992ec-104">Request a token for the endpoint of the service using the specified credentials.</span></span>

## <a name="syntax"></a><span data-ttu-id="992ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="992ec-105">Syntax</span></span>


```C++
HRESULT GetEndpointToken(
  [in]  GUID                        serviceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  UpdateEndpointAuthTokenType tokenType,
  [in]  BOOL                        fRefreshOnline,
  [out] IUnknown                    **ppEndpointToken
);
```



## <a name="parameters"></a><span data-ttu-id="992ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="992ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="992ec-107">*serviceId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="992ec-107">*serviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="992ec-108">Определяет обновляемую службу.</span><span class="sxs-lookup"><span data-stu-id="992ec-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="992ec-109">*endpointType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="992ec-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="992ec-110">Определяет тип конечной точки, реализуемой службой.</span><span class="sxs-lookup"><span data-stu-id="992ec-110">Identifies the type of endpoint that is implemented by the service.</span></span>

</dd> <dt>

<span data-ttu-id="992ec-111">*проксисеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="992ec-111">*proxySettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="992ec-112">Параметры, используемые при соединении с прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="992ec-112">The settings to be used when connecting to a proxy server.</span></span> <span data-ttu-id="992ec-113">Дополнительные сведения см. в разделе Структура [**упдатиндпоинтпроксисеттингс**](updateendpointproxysettings.md) .</span><span class="sxs-lookup"><span data-stu-id="992ec-113">See the [**UpdateEndpointProxySettings**](updateendpointproxysettings.md) structure for more details.</span></span>

</dd> <dt>

<span data-ttu-id="992ec-114">*хусертокен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="992ec-114">*hUserToken* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="992ec-115">*TokenType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="992ec-115">*tokenType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="992ec-116">Определяет тип маркера проверки подлинности, используемый для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="992ec-116">Identifies the type of authentication token that is used for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="992ec-117">*фрефрешонлине* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="992ec-117">*fRefreshOnline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="992ec-118">Указывает, что погода WUA запрашивает новый маркер.</span><span class="sxs-lookup"><span data-stu-id="992ec-118">Indicates weather WUA requests a new token.</span></span> <span data-ttu-id="992ec-119">Значение true указывает, что запрашивается новый маркер.</span><span class="sxs-lookup"><span data-stu-id="992ec-119">True indicates that a new token is requested.</span></span> <span data-ttu-id="992ec-120">Значение false указывает, что запрошен новый или кэшированный токен.</span><span class="sxs-lookup"><span data-stu-id="992ec-120">False indicates that a new or cached token is requested.</span></span> <span data-ttu-id="992ec-121">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="992ec-121">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="992ec-122">*ппендпоинттокен* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="992ec-122">*ppEndpointToken* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="992ec-123">Укажите токен конечной точки, который будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="992ec-123">Specifiy the endpoint token to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="992ec-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="992ec-124">Return value</span></span>

<span data-ttu-id="992ec-125">\_При успешном выполнении возвращает значение ОК.</span><span class="sxs-lookup"><span data-stu-id="992ec-125">Returns S\_OK if successful.</span></span> <span data-ttu-id="992ec-126">В противном случае возвращает код ошибки COM или Windows.</span><span class="sxs-lookup"><span data-stu-id="992ec-126">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="992ec-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="992ec-127">Remarks</span></span>

<span data-ttu-id="992ec-128">WUA обычно задает для параметра Фрефрешонлине значение false при первом вызове этого метода, а затем при возникновении ошибки подключения WUA устанавливает для параметра значение true при повторном вызове метода.</span><span class="sxs-lookup"><span data-stu-id="992ec-128">WUA typically sets the fRefreshOnline parameter to false when this method is first called, then if a connection error occures WUA sets that parameter to true when the method is called again.</span></span> <span data-ttu-id="992ec-129">Однако реализация этого метода может запросить новый маркер из службы маркеров безопасности (STS) или предоставить кэшированный маркер в любое время.</span><span class="sxs-lookup"><span data-stu-id="992ec-129">However, the implementation of this method can request a new token from a Security Token Service (STS) or provide a cached token at any time.</span></span>

## <a name="requirements"></a><span data-ttu-id="992ec-130">Требования</span><span class="sxs-lookup"><span data-stu-id="992ec-130">Requirements</span></span>



| <span data-ttu-id="992ec-131">Требование</span><span class="sxs-lookup"><span data-stu-id="992ec-131">Requirement</span></span> | <span data-ttu-id="992ec-132">Значение</span><span class="sxs-lookup"><span data-stu-id="992ec-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="992ec-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="992ec-133">Minimum supported client</span></span><br/> | <span data-ttu-id="992ec-134">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="992ec-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="992ec-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="992ec-135">Minimum supported server</span></span><br/> | <span data-ttu-id="992ec-136">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="992ec-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="992ec-137">Header</span><span class="sxs-lookup"><span data-stu-id="992ec-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="992ec-138"><dt>Упдатиндпоинтаус. h</dt></span><span class="sxs-lookup"><span data-stu-id="992ec-138"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="992ec-139">IDL</span><span class="sxs-lookup"><span data-stu-id="992ec-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="992ec-140"><dt>Упдатиндпоинтаус. idl</dt></span><span class="sxs-lookup"><span data-stu-id="992ec-140"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="992ec-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="992ec-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="992ec-142"><dt>Упдатиндпоинтаус. lib</dt></span><span class="sxs-lookup"><span data-stu-id="992ec-142"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="992ec-143">DLL</span><span class="sxs-lookup"><span data-stu-id="992ec-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="992ec-144"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="992ec-144"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="992ec-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="992ec-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="992ec-146">**иупдатиндпоинтауспровидер**</span><span class="sxs-lookup"><span data-stu-id="992ec-146">**IUpdateEndpointAuthProvider**</span></span>](iupdateendpointauthprovider.md)
</dt> </dl>

 

 




