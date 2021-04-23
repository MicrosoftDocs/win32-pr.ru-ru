---
description: Обратный вызов, уведомляющий основное приложение об универсальных буферах, возвращаемых запросом связана.
MS-HAID: vspixengine.IGenericBufferDataCallback\_ResultCallback\_DWORD\_BYTE\_arr\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иженерикбуффердатакаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5627A93E-8BE8-4413-BFB4-724AF2DDFEB6
api_name:
- IGenericBufferDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: be2d6aa7cd5e844cd5d1297c16de2ebb21c939a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806514"
---
# <a name="span-idvspixengineigenericbufferdatacallback_resultcallback_dword_byte_arr_bstrspanigenericbufferdatacallbackresultcallback-method"></a><span data-ttu-id="f4bb8-103"><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>Метод Иженерикбуффердатакаллбакк:: Ресулткаллбакк</span><span class="sxs-lookup"><span data-stu-id="f4bb8-103"><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>IGenericBufferDataCallback::ResultCallback method</span></span>

<span data-ttu-id="f4bb8-104">Обратный вызов, уведомляющий основное приложение об универсальных буферах, возвращаемых запросом связана.</span><span class="sxs-lookup"><span data-stu-id="f4bb8-104">A callback that notifies the host of generic buffer information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4bb8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4bb8-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD   size,
   BYTE [] count0_buffer,
   BSTR    type
);
```

## <a name="parameters"></a><span data-ttu-id="f4bb8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4bb8-106">Parameters</span></span>

<span data-ttu-id="f4bb8-107">*изменять* </span><span class="sxs-lookup"><span data-stu-id="f4bb8-107">*size* </span></span>  
<span data-ttu-id="f4bb8-108">Размер содержимого буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="f4bb8-108">The size of the buffer contents in bytes.</span></span>

<span data-ttu-id="f4bb8-109">*\_буфер count0* </span><span class="sxs-lookup"><span data-stu-id="f4bb8-109">*count0\_buffer* </span></span>  
<span data-ttu-id="f4bb8-110">Содержимое буфера.</span><span class="sxs-lookup"><span data-stu-id="f4bb8-110">The buffer contents.</span></span> <span data-ttu-id="f4bb8-111">В большинстве случаев это XML-данные.</span><span class="sxs-lookup"><span data-stu-id="f4bb8-111">In most cases this is XML data.</span></span>

<span data-ttu-id="f4bb8-112">*type* </span><span class="sxs-lookup"><span data-stu-id="f4bb8-112">*type* </span></span>  
<span data-ttu-id="f4bb8-113">Строка COM, указывающая тип содержимого, возвращаемого в буфере.</span><span class="sxs-lookup"><span data-stu-id="f4bb8-113">A COM string that indicates the type of content returned in the buffer.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4bb8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4bb8-114">Return value</span></span>

<span data-ttu-id="f4bb8-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f4bb8-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f4bb8-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f4bb8-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4bb8-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f4bb8-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f4bb8-118">Header</span><span class="sxs-lookup"><span data-stu-id="f4bb8-118">Header</span></span></p></td><td><span data-ttu-id="f4bb8-119">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="f4bb8-119">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f4bb8-120"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="f4bb8-120"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f4bb8-121">**иженерикбуффердатакаллбакк**</span><span class="sxs-lookup"><span data-stu-id="f4bb8-121">**IGenericBufferDataCallback**</span></span>](/windows/desktop/direct3dtools/igenericbufferdatacallback)

 

 
