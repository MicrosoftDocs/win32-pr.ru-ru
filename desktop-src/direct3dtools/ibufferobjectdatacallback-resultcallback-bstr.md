---
description: Обратный вызов, уведомляющий узел о том, что сведения о буфере записаны в файл с помощью запроса связана.
MS-HAID: vspixengine.IBufferObjectDataCallback\_ResultCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ибуфферобжектдатакаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8083FDF-0A56-4777-8EFD-66F77AD195EA
api_name:
- IBufferObjectDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 41a5017171fee8476033e3c38d050bc38b1642a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423142"
---
# <a name="span-idvspixengineibufferobjectdatacallback_resultcallback_bstrspanibufferobjectdatacallbackresultcallback-method"></a><span data-ttu-id="3ba4f-103"><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>Метод Ибуфферобжектдатакаллбакк:: Ресулткаллбакк</span><span class="sxs-lookup"><span data-stu-id="3ba4f-103"><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>IBufferObjectDataCallback::ResultCallback method</span></span>

<span data-ttu-id="3ba4f-104">Обратный вызов, уведомляющий узел о том, что сведения о буфере записаны в файл с помощью запроса связана.</span><span class="sxs-lookup"><span data-stu-id="3ba4f-104">A callback that notifies the host of buffer information written to a file by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ba4f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ba4f-105">Syntax</span></span>

```C++
HRESULT ResultCallback(
   BSTR File
);
```

## <a name="parameters"></a><span data-ttu-id="3ba4f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ba4f-106">Parameters</span></span>

<span data-ttu-id="3ba4f-107">*Файл* Строка COM, содержащая путь к файлу, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="3ba4f-107">*File* A COM string that contains the pathname of the file where results are written.</span></span>

## <a name="return-value"></a><span data-ttu-id="3ba4f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ba4f-108">Return value</span></span>

<span data-ttu-id="3ba4f-109">Если этот метод завершается с ошибкой, возвращается **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="3ba4f-109">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="3ba4f-110">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3ba4f-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ba4f-111">Требования</span><span class="sxs-lookup"><span data-stu-id="3ba4f-111">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3ba4f-112">Header</span><span class="sxs-lookup"><span data-stu-id="3ba4f-112">Header</span></span></p></td><td><span data-ttu-id="3ba4f-113">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="3ba4f-113">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3ba4f-114"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="3ba4f-114"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3ba4f-115">**ибуфферобжектдатакаллбакк**</span><span class="sxs-lookup"><span data-stu-id="3ba4f-115">**IBufferObjectDataCallback**</span></span>](/windows/desktop/direct3dtools/ibufferobjectdatacallback)

 

 
