---
description: Асинхронно задает адрес конечной точки, используемый для подключения к удаленному модулю.
MS-HAID: vspixengine.IPixEngine7\_SetPlaybackEndpointAsync\_BOOL\_BSTR\_BSTR\_RemotingVersion\_IVersionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine7:: Сетплайбаккендпоинтасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4F76EFFF-F3CB-4BEA-999F-639876C7F792
api_name:
- IPixEngine7.SetPlaybackEndpointAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2e0970b1a2a786c828a24efef0ae9e4057dbe2cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806689"
---
# <a name="span-idvspixengineipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dwordspanipixengine7setplaybackendpointasync-method"></a><span data-ttu-id="38114-103"><span id="vspixengine.ipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dword"></span>Метод IPixEngine7:: Сетплайбаккендпоинтасинк</span><span class="sxs-lookup"><span data-stu-id="38114-103"><span id="vspixengine.ipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dword"></span>IPixEngine7::SetPlaybackEndpointAsync method</span></span>

<span data-ttu-id="38114-104">Асинхронно задает адрес конечной точки, используемый для подключения к удаленному модулю.</span><span class="sxs-lookup"><span data-stu-id="38114-104">Asynchronously sets the endpoint address used to connect to a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="38114-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38114-105">Syntax</span></span>


```C++
HRESULT SetPlaybackEndpointAsync(
   BOOL              bUseAuthentication,
   BSTR              endpoint,
   BSTR              sessionKey,
   RemotingVersion   remoteVersion,
   IVersionCallback* versionCallback,
   DWORD             requestCookie,
   DWORD             progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="38114-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="38114-106">Parameters</span></span>

<span data-ttu-id="38114-107">*бусеаусентикатион* </span><span class="sxs-lookup"><span data-stu-id="38114-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="38114-108">значение true, чтобы использовать проверку подлинности; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="38114-108">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="38114-109">*конечной* </span><span class="sxs-lookup"><span data-stu-id="38114-109">*endpoint* </span></span>  
<span data-ttu-id="38114-110">Строка COM, содержащая адрес конечной точки.</span><span class="sxs-lookup"><span data-stu-id="38114-110">A COM string containing the endpoint address.</span></span>

<span data-ttu-id="38114-111">*сессионкэй* </span><span class="sxs-lookup"><span data-stu-id="38114-111">*sessionKey* </span></span>  
<span data-ttu-id="38114-112">Строка COM, содержащая ключ сеанса, используемый для шифрования.</span><span class="sxs-lookup"><span data-stu-id="38114-112">A COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="38114-113">*ремотеверсион* </span><span class="sxs-lookup"><span data-stu-id="38114-113">*remoteVersion* </span></span>  
<span data-ttu-id="38114-114">Указывает версию используемого удаленного обработчика.</span><span class="sxs-lookup"><span data-stu-id="38114-114">Specifies the version of the remote engine to use.</span></span>

<span data-ttu-id="38114-115">*версионкаллбакк* </span><span class="sxs-lookup"><span data-stu-id="38114-115">*versionCallback* </span></span>  
<span data-ttu-id="38114-116">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="38114-116">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="38114-117">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="38114-117">*requestCookie* </span></span>  
<span data-ttu-id="38114-118">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="38114-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="38114-119">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="38114-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="38114-120">Не используется.</span><span class="sxs-lookup"><span data-stu-id="38114-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="38114-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38114-121">Return value</span></span>

<span data-ttu-id="38114-122">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="38114-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="38114-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="38114-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="38114-124">Требования</span><span class="sxs-lookup"><span data-stu-id="38114-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="38114-125">Header</span><span class="sxs-lookup"><span data-stu-id="38114-125">Header</span></span></p></td><td><span data-ttu-id="38114-126">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="38114-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="38114-127"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="38114-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="38114-128">**IPixEngine7**</span><span class="sxs-lookup"><span data-stu-id="38114-128">**IPixEngine7**</span></span>](/windows/desktop/direct3dtools/ipixengine7)

 

 
