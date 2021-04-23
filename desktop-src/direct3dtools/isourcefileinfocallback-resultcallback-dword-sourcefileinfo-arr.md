---
description: Функция обратного вызова, используемая для уведомления узла о файлах исходного кода, связанных с стеком вызовов.
MS-HAID: vspixengine.ISourceFileInfoCallback\_ResultCallback\_DWORD\_SourceFileInfo\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Исаурцефилеинфокаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AB3249FF-DA67-4902-B75D-4EC3D0F25EE7
api_name:
- ISourceFileInfoCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a60122615cf15e9ed39ae7809e574c4d3d0c1146
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140679"
---
# <a name="span-idvspixengineisourcefileinfocallback_resultcallback_dword_sourcefileinfo_arrspanisourcefileinfocallbackresultcallback-method"></a><span data-ttu-id="8f231-103"><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>Метод Исаурцефилеинфокаллбакк:: Ресулткаллбакк</span><span class="sxs-lookup"><span data-stu-id="8f231-103"><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>ISourceFileInfoCallback::ResultCallback method</span></span>

<span data-ttu-id="8f231-104">Функция обратного вызова, используемая для уведомления узла о файлах исходного кода, связанных с стеком вызовов.</span><span class="sxs-lookup"><span data-stu-id="8f231-104">A callback function used to notify the host of information about source files associated with the callstack.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f231-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f231-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD             count,
   SourceFileInfo [] count0_sourceFileInfoBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="8f231-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f231-106">Parameters</span></span>

<span data-ttu-id="8f231-107">*расчета* </span><span class="sxs-lookup"><span data-stu-id="8f231-107">*count* </span></span>  
<span data-ttu-id="8f231-108">Число возвращенных исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="8f231-108">The number of source files returned.</span></span>

<span data-ttu-id="8f231-109">*count0 \_ саурцефилеинфобуффер* </span><span class="sxs-lookup"><span data-stu-id="8f231-109">*count0\_sourceFileInfoBuffer* </span></span>  
<span data-ttu-id="8f231-110">Исходные файлы.</span><span class="sxs-lookup"><span data-stu-id="8f231-110">The source files.</span></span>

## <a name="return-value"></a><span data-ttu-id="8f231-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f231-111">Return value</span></span>

<span data-ttu-id="8f231-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8f231-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8f231-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8f231-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f231-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8f231-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8f231-115">Header</span><span class="sxs-lookup"><span data-stu-id="8f231-115">Header</span></span></p></td><td><span data-ttu-id="8f231-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="8f231-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="8f231-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="8f231-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="8f231-118">**исаурцефилеинфокаллбакк**</span><span class="sxs-lookup"><span data-stu-id="8f231-118">**ISourceFileInfoCallback**</span></span>](/windows/desktop/direct3dtools/isourcefileinfocallback)

 

 
