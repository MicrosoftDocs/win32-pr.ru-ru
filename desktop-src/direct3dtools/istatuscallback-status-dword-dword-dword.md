---
description: Функция обратного вызова, используемая для уведомления узла о ходе выполнения модулей. Это также позволяет основному приложению определить, что ядро все еще работает.
title: 'Метод Истатускаллбакк:: Status'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4DC2A05F-506C-4AB4-98E1-58827056700D
api_name:
- IStatusCallback.Status
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09fba28486bd6f1c43e4b0c4fb0dfcf495e0722b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710653"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span data-ttu-id="71312-104"><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>Метод Истатускаллбакк:: Status</span><span class="sxs-lookup"><span data-stu-id="71312-104"><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>IStatusCallback::Status method</span></span>

<span data-ttu-id="71312-105">Функция обратного вызова, используемая для уведомления узла о ходе выполнения модуля.</span><span class="sxs-lookup"><span data-stu-id="71312-105">A callback function used to notify the host of the engine's progress.</span></span> <span data-ttu-id="71312-106">Это также позволяет основному приложению определить, что ядро все еще работает.</span><span class="sxs-lookup"><span data-stu-id="71312-106">This also serves as a way for the host to determine that the engine is still running.</span></span>

## <a name="syntax"></a><span data-ttu-id="71312-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71312-107">Syntax</span></span>


```C++
HRESULT Status(
   DWORD dwMillisecondsElapsed,
   DWORD dwFramesCaptured,
   DWORD dwFramesElapsed
);
```

## <a name="parameters"></a><span data-ttu-id="71312-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="71312-108">Parameters</span></span>

<span data-ttu-id="71312-109">*двмиллисекондселапсед* </span><span class="sxs-lookup"><span data-stu-id="71312-109">*dwMillisecondsElapsed* </span></span>  
<span data-ttu-id="71312-110">Время, прошедшее с момента последнего вызова состояния, в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="71312-110">The time elapsed since the last call to Status, in milliseconds.</span></span>

<span data-ttu-id="71312-111">*двфрамескаптуред* </span><span class="sxs-lookup"><span data-stu-id="71312-111">*dwFramesCaptured* </span></span>  
<span data-ttu-id="71312-112">Число кадров, записанных с момента последнего вызова Status.</span><span class="sxs-lookup"><span data-stu-id="71312-112">The number of frames that have been captures since the last call to Status.</span></span>

<span data-ttu-id="71312-113">*двфрамеселапсед* </span><span class="sxs-lookup"><span data-stu-id="71312-113">*dwFramesElapsed* </span></span>  
<span data-ttu-id="71312-114">Число кадров, истекших с момента последнего вызова состояния.</span><span class="sxs-lookup"><span data-stu-id="71312-114">The number of frames elapsed since the last call to Status.</span></span>

## <a name="return-value"></a><span data-ttu-id="71312-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71312-115">Return value</span></span>

<span data-ttu-id="71312-116">Если этот метод завершается с ошибкой, возвращается **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="71312-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="71312-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="71312-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="71312-118">Требования</span><span class="sxs-lookup"><span data-stu-id="71312-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="71312-119">Header</span><span class="sxs-lookup"><span data-stu-id="71312-119">Header</span></span></p></td><td><span data-ttu-id="71312-120">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="71312-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="71312-121"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="71312-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="71312-122">**истатускаллбакк**</span><span class="sxs-lookup"><span data-stu-id="71312-122">**IStatusCallback**</span></span>](/windows/desktop/direct3dtools/istatuscallback)

 

 
