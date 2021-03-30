---
description: Задает адрес конечной точки, используемый для подключения к удаленному модулю.
MS-HAID: vspixengine.IPeerToPeerEngine\_SetPlaybackEndpoint\_BOOL\_BSTR\_BSTR\_RemotingVersion
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипиртопиренгине:: Сетплайбаккендпоинт'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D261D2EA-C930-406E-A5E1-CE5E98162399
api_name:
- IPeerToPeerEngine.SetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbec4826fb2659604a4b9f4388beed1829b42770
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495558"
---
# <a name="span-idvspixengineipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversionspanipeertopeerenginesetplaybackendpoint-method"></a><span data-ttu-id="5ab1d-103"><span id="vspixengine.ipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversion"></span>Метод Ипиртопиренгине:: Сетплайбаккендпоинт</span><span class="sxs-lookup"><span data-stu-id="5ab1d-103"><span id="vspixengine.ipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversion"></span>IPeerToPeerEngine::SetPlaybackEndpoint method</span></span>

<span data-ttu-id="5ab1d-104">Задает адрес конечной точки, используемый для подключения к удаленному модулю.</span><span class="sxs-lookup"><span data-stu-id="5ab1d-104">Sets the endpoint address used to connect to a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ab1d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ab1d-105">Syntax</span></span>


```C++
HRESULT SetPlaybackEndpoint(
   BOOL            bUseAuthentication,
   BSTR            endpoint,
   BSTR            sessionKey,
   RemotingVersion remoteVersion
);
```

## <a name="parameters"></a><span data-ttu-id="5ab1d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ab1d-106">Parameters</span></span>

<span data-ttu-id="5ab1d-107">*бусеаусентикатион* </span><span class="sxs-lookup"><span data-stu-id="5ab1d-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="5ab1d-108">значение true, чтобы использовать проверку подлинности; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="5ab1d-108">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="5ab1d-109">*конечной* </span><span class="sxs-lookup"><span data-stu-id="5ab1d-109">*endpoint* </span></span>  
<span data-ttu-id="5ab1d-110">Строка COM, содержащая адрес конечной точки.</span><span class="sxs-lookup"><span data-stu-id="5ab1d-110">A COM string containing the endpoint address.</span></span>

<span data-ttu-id="5ab1d-111">*сессионкэй* </span><span class="sxs-lookup"><span data-stu-id="5ab1d-111">*sessionKey* </span></span>  
<span data-ttu-id="5ab1d-112">Строка COM, содержащая ключ сеанса, используемый для шифрования.</span><span class="sxs-lookup"><span data-stu-id="5ab1d-112">A COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="5ab1d-113">*ремотеверсион* </span><span class="sxs-lookup"><span data-stu-id="5ab1d-113">*remoteVersion* </span></span>  
<span data-ttu-id="5ab1d-114">Указывает версию используемого удаленного обработчика.</span><span class="sxs-lookup"><span data-stu-id="5ab1d-114">Specifies the version of the remote engine to use.</span></span>

## <a name="return-value"></a><span data-ttu-id="5ab1d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ab1d-115">Return value</span></span>

<span data-ttu-id="5ab1d-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5ab1d-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5ab1d-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5ab1d-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ab1d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5ab1d-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5ab1d-119">Header</span><span class="sxs-lookup"><span data-stu-id="5ab1d-119">Header</span></span></p></td><td><span data-ttu-id="5ab1d-120">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="5ab1d-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5ab1d-121"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="5ab1d-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5ab1d-122">**ипиртопиренгине**</span><span class="sxs-lookup"><span data-stu-id="5ab1d-122">**IPeerToPeerEngine**</span></span>](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 
