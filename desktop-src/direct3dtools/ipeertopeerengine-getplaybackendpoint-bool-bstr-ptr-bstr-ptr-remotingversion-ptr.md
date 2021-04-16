---
description: Возвращает адрес конечной точки удаленного модуля.
MS-HAID: vspixengine.IPeerToPeerEngine\_GetPlaybackEndpoint\_BOOL\_BSTR\_ptr\_BSTR\_ptr\_RemotingVersion\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипиртопиренгине:: Жетплайбаккендпоинт'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3B391048-E7F7-4DA7-96A3-05875B170DCA
api_name:
- IPeerToPeerEngine.GetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f6ee25dbd456086227e88fcb8bf7708a39e26eb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537010"
---
# <a name="span-idvspixengineipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptrspanipeertopeerenginegetplaybackendpoint-method"></a><span data-ttu-id="4e63c-103"><span id="vspixengine.ipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptr"></span>Метод Ипиртопиренгине:: Жетплайбаккендпоинт</span><span class="sxs-lookup"><span data-stu-id="4e63c-103"><span id="vspixengine.ipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptr"></span>IPeerToPeerEngine::GetPlaybackEndpoint method</span></span>

<span data-ttu-id="4e63c-104">Возвращает адрес конечной точки удаленного модуля.</span><span class="sxs-lookup"><span data-stu-id="4e63c-104">Gets the endpoint address of a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e63c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e63c-105">Syntax</span></span>


```C++
HRESULT GetPlaybackEndpoint(
   BOOL              bUseAuthentication,
   BSTR *            pEndpoint,
   BSTR *            sessionKey,
   RemotingVersion * pRemoteVersion
);
```

## <a name="parameters"></a><span data-ttu-id="4e63c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e63c-106">Parameters</span></span>

<span data-ttu-id="4e63c-107">*бусеаусентикатион* </span><span class="sxs-lookup"><span data-stu-id="4e63c-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="4e63c-108">значение true, если удаленный модуль использует проверку подлинности; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="4e63c-108">true if the remote engine uses authentication; otherwise, false.</span></span>

<span data-ttu-id="4e63c-109">*пендпоинт* </span><span class="sxs-lookup"><span data-stu-id="4e63c-109">*pEndpoint* </span></span>  
<span data-ttu-id="4e63c-110">При возвращении — строка COM, содержащая адрес конечной точки удаленного компьютера воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="4e63c-110">On return, a COM string containing the endpoint address of the remote playback machine.</span></span>

<span data-ttu-id="4e63c-111">*сессионкэй* </span><span class="sxs-lookup"><span data-stu-id="4e63c-111">*sessionKey* </span></span>  
<span data-ttu-id="4e63c-112">При возвращении — строка COM, содержащая ключ сеанса, используемый для шифрования.</span><span class="sxs-lookup"><span data-stu-id="4e63c-112">On return, a COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="4e63c-113">*премотеверсион* </span><span class="sxs-lookup"><span data-stu-id="4e63c-113">*pRemoteVersion* </span></span>  
<span data-ttu-id="4e63c-114">При возвращении — версия удаленного модуля.</span><span class="sxs-lookup"><span data-stu-id="4e63c-114">On return, the version of the remote engine.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e63c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e63c-115">Return value</span></span>

<span data-ttu-id="4e63c-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4e63c-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4e63c-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4e63c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e63c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="4e63c-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4e63c-119">Header</span><span class="sxs-lookup"><span data-stu-id="4e63c-119">Header</span></span></p></td><td><span data-ttu-id="4e63c-120">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="4e63c-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4e63c-121"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="4e63c-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4e63c-122">**ипиртопиренгине**</span><span class="sxs-lookup"><span data-stu-id="4e63c-122">**IPeerToPeerEngine**</span></span>](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 
