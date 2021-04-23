---
description: Функция обратного вызова, используемая для уведомления узла об ошибках во время записи или воспроизведения.
MS-HAID: vspixengine.IFileIOCallback\_ResultCallback\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ифилеиокаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E4418A63-47C6-4F12-94FA-0F1B5465FE84
api_name:
- IFileIOCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 751c4d0b57165e148002218ae2151aaba69e48f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140066"
---
# <a name="span-idvspixengineifileiocallback_resultcallback_dwordspanifileiocallbackresultcallback-method"></a><span data-ttu-id="1de5e-103"><span id="vspixengine.ifileiocallback_resultcallback_dword"></span>Метод Ифилеиокаллбакк:: Ресулткаллбакк</span><span class="sxs-lookup"><span data-stu-id="1de5e-103"><span id="vspixengine.ifileiocallback_resultcallback_dword"></span>IFileIOCallback::ResultCallback method</span></span>

<span data-ttu-id="1de5e-104">Функция обратного вызова, используемая для уведомления узла об ошибках во время записи или воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="1de5e-104">A callback function used to notify the host of errors while during capture or playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="1de5e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1de5e-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD resultState
);
```

## <a name="parameters"></a><span data-ttu-id="1de5e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1de5e-106">Parameters</span></span>

<span data-ttu-id="1de5e-107">*ресултстате* </span><span class="sxs-lookup"><span data-stu-id="1de5e-107">*resultState* </span></span>  
<span data-ttu-id="1de5e-108">Указывает тип обнаруженной ошибки.</span><span class="sxs-lookup"><span data-stu-id="1de5e-108">Indicates the kind of error encountered.</span></span>

## <a name="return-value"></a><span data-ttu-id="1de5e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1de5e-109">Return value</span></span>

<span data-ttu-id="1de5e-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="1de5e-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1de5e-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1de5e-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1de5e-112">Требования</span><span class="sxs-lookup"><span data-stu-id="1de5e-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1de5e-113">Header</span><span class="sxs-lookup"><span data-stu-id="1de5e-113">Header</span></span></p></td><td><span data-ttu-id="1de5e-114">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="1de5e-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1de5e-115"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="1de5e-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1de5e-116">**ифилеиокаллбакк**</span><span class="sxs-lookup"><span data-stu-id="1de5e-116">**IFileIOCallback**</span></span>](/windows/desktop/direct3dtools/ifileiocallback)

 

 
