---
description: Запросы, указывающие, что в журнале графики есть новые данные.
MS-HAID: vspixengine.IPixEngine2\_OnNewDataAvailable\_BOOL\_BOOL\_INT64\_INT64\_INT32\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine2:: Онневдатааваилабле'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B99FC54C-9395-4B14-93D5-B6408D655DC3
api_name:
- IPixEngine2.OnNewDataAvailable
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3de880153eec5b41849167f3a87a3f77f31aeffd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537298"
---
# <a name="span-idvspixengineipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arrspanipixengine2onnewdataavailable-method"></a><span data-ttu-id="9d981-103"><span id="vspixengine.ipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arr"></span>Метод IPixEngine2:: Онневдатааваилабле</span><span class="sxs-lookup"><span data-stu-id="9d981-103"><span id="vspixengine.ipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arr"></span>IPixEngine2::OnNewDataAvailable method</span></span>

<span data-ttu-id="9d981-104">Запросы, указывающие, что в журнале графики есть новые данные.</span><span class="sxs-lookup"><span data-stu-id="9d981-104">Requests to indicate that the graphics log has new data inside of it.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d981-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d981-105">Syntax</span></span>


```C++
HRESULT OnNewDataAvailable(
   BOOL    fSessionEnd,
   BOOL    fUnloadCurFrame,
   INT64   i64FilePositionStart,
   INT64   i64FilePositionEnd,
   INT32   iObjectTableDataSize,
   BYTE [] count4_pObjectTableData
);
```

## <a name="parameters"></a><span data-ttu-id="9d981-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d981-106">Parameters</span></span>

<span data-ttu-id="9d981-107">*фсессионенд* </span><span class="sxs-lookup"><span data-stu-id="9d981-107">*fSessionEnd* </span></span>  
<span data-ttu-id="9d981-108">значение true, если сеанс завершен; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="9d981-108">true if the session has ended, otherwise false.</span></span>

<span data-ttu-id="9d981-109">*фунлоадкурфраме* </span><span class="sxs-lookup"><span data-stu-id="9d981-109">*fUnloadCurFrame* </span></span>  
<span data-ttu-id="9d981-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="9d981-110">Not used.</span></span>

<span data-ttu-id="9d981-111">*i64FilePositionStart* </span><span class="sxs-lookup"><span data-stu-id="9d981-111">*i64FilePositionStart* </span></span>  
<span data-ttu-id="9d981-112">Расположение файла в байтах, с которого начинаются новые данные.</span><span class="sxs-lookup"><span data-stu-id="9d981-112">The file position, in bytes, at which the new data begins.</span></span>

<span data-ttu-id="9d981-113">*i64FilePositionEnd* </span><span class="sxs-lookup"><span data-stu-id="9d981-113">*i64FilePositionEnd* </span></span>  
<span data-ttu-id="9d981-114">Расположение файла в байтах, в течение которого завершается новая операция.</span><span class="sxs-lookup"><span data-stu-id="9d981-114">The file position, in bytes, at which the new data ends.</span></span>

<span data-ttu-id="9d981-115">*иобжекттабледатасизе* </span><span class="sxs-lookup"><span data-stu-id="9d981-115">*iObjectTableDataSize* </span></span>  
<span data-ttu-id="9d981-116">Число байтов, содержащихся в count4 \_ побжекттабледата.</span><span class="sxs-lookup"><span data-stu-id="9d981-116">The number of bytes contained in count4\_pObjectTableData.</span></span>

<span data-ttu-id="9d981-117">*count4 \_ побжекттабледата* </span><span class="sxs-lookup"><span data-stu-id="9d981-117">*count4\_pObjectTableData* </span></span>  
<span data-ttu-id="9d981-118">Буфер, содержащий данные для таблицы объектов.</span><span class="sxs-lookup"><span data-stu-id="9d981-118">An buffer containing data for the object table.</span></span>

## <a name="return-value"></a><span data-ttu-id="9d981-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d981-119">Return value</span></span>

<span data-ttu-id="9d981-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9d981-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9d981-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9d981-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d981-122">Требования</span><span class="sxs-lookup"><span data-stu-id="9d981-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9d981-123">Header</span><span class="sxs-lookup"><span data-stu-id="9d981-123">Header</span></span></p></td><td><span data-ttu-id="9d981-124">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="9d981-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9d981-125"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="9d981-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9d981-126">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="9d981-126">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
