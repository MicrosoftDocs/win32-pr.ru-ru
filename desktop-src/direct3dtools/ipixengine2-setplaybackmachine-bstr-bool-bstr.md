---
description: Задает текущий компьютер воспроизведения для указанного журнала графики.
MS-HAID: vspixengine.IPixEngine2\_SetPlaybackMachine\_BSTR\_BOOL\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine2:: Сетплайбаккмачине'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 181EE044-1FC4-484B-AE63-C33BC627C3B7
api_name:
- IPixEngine2.SetPlaybackMachine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d7366da4aa999828309136900edfe725af4f622
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538189"
---
# <a name="span-idvspixengineipixengine2_setplaybackmachine_bstr_bool_bstrspanipixengine2setplaybackmachine-method"></a><span data-ttu-id="c72ed-103"><span id="vspixengine.ipixengine2_setplaybackmachine_bstr_bool_bstr"></span>Метод IPixEngine2:: Сетплайбаккмачине</span><span class="sxs-lookup"><span data-stu-id="c72ed-103"><span id="vspixengine.ipixengine2_setplaybackmachine_bstr_bool_bstr"></span>IPixEngine2::SetPlaybackMachine method</span></span>

<span data-ttu-id="c72ed-104">Задает текущий компьютер воспроизведения для указанного журнала графики.</span><span class="sxs-lookup"><span data-stu-id="c72ed-104">Sets the current playback machine for the specified graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="c72ed-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c72ed-105">Syntax</span></span>


```C++
HRESULT SetPlaybackMachine(
   BSTR logFile,
   BOOL bUseAuthentication,
   BSTR machine
);
```

## <a name="parameters"></a><span data-ttu-id="c72ed-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c72ed-106">Parameters</span></span>

<span data-ttu-id="c72ed-107">*logFile* </span><span class="sxs-lookup"><span data-stu-id="c72ed-107">*logFile* </span></span>  
<span data-ttu-id="c72ed-108">Строка COM, контианинг имя журнала графики.</span><span class="sxs-lookup"><span data-stu-id="c72ed-108">A COM string contianing the name of the graphics log.</span></span>

<span data-ttu-id="c72ed-109">*бусеаусентикатион* </span><span class="sxs-lookup"><span data-stu-id="c72ed-109">*bUseAuthentication* </span></span>  
<span data-ttu-id="c72ed-110">значение true, чтобы использовать проверку подлинности; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="c72ed-110">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="c72ed-111">*машине* </span><span class="sxs-lookup"><span data-stu-id="c72ed-111">*machine* </span></span>  
<span data-ttu-id="c72ed-112">Строка COM, содержащая имя компьютера воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c72ed-112">A COM string containing the name of the playback machine.</span></span>

## <a name="return-value"></a><span data-ttu-id="c72ed-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c72ed-113">Return value</span></span>

<span data-ttu-id="c72ed-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c72ed-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c72ed-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c72ed-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c72ed-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c72ed-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c72ed-117">Header</span><span class="sxs-lookup"><span data-stu-id="c72ed-117">Header</span></span></p></td><td><span data-ttu-id="c72ed-118">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="c72ed-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c72ed-119"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="c72ed-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c72ed-120">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="c72ed-120">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
