---
description: Возвращает максимальный размер в байтах, необходимый для текущего потока, включая номер версии.
ms.assetid: 55ea4568-5ca4-4139-8def-bef20071835d
title: Кперсистстреам. Жетсиземакс, метод (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ef9fcd176463aa8b0bc69fabbd74d78d4ca17cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668671"
---
# <a name="cpersiststreamgetsizemax-method"></a><span data-ttu-id="538a5-103">Кперсистстреам. Жетсиземакс, метод</span><span class="sxs-lookup"><span data-stu-id="538a5-103">CPersistStream.GetSizeMax method</span></span>

<span data-ttu-id="538a5-104">Возвращает максимальный размер в байтах, необходимый для текущего потока, включая номер версии.</span><span class="sxs-lookup"><span data-stu-id="538a5-104">Retrieves the maximum byte size needed for the current stream, including the version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="538a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="538a5-105">Syntax</span></span>


```C++
HRESULT GetSizeMax(
   ULARGE_INTEGER *pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="538a5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="538a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="538a5-107">*пкбсизе*</span><span class="sxs-lookup"><span data-stu-id="538a5-107">*pcbSize*</span></span> 
</dt> <dd>

<span data-ttu-id="538a5-108">Указатель на размер в байтах, необходимый для сохранения этого потока, включая номер версии.</span><span class="sxs-lookup"><span data-stu-id="538a5-108">Pointer to the size in bytes needed to save this stream, including the version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="538a5-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="538a5-109">Return value</span></span>

<span data-ttu-id="538a5-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="538a5-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="538a5-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="538a5-111">Remarks</span></span>

<span data-ttu-id="538a5-112">Эта функция члена реализует метод **IPersistStream:: жетсиземакс** .</span><span class="sxs-lookup"><span data-stu-id="538a5-112">This member function implements the **IPersistStream::GetSizeMax** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="538a5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="538a5-113">Requirements</span></span>



| <span data-ttu-id="538a5-114">Требование</span><span class="sxs-lookup"><span data-stu-id="538a5-114">Requirement</span></span> | <span data-ttu-id="538a5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="538a5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="538a5-116">Header</span><span class="sxs-lookup"><span data-stu-id="538a5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="538a5-117"><dt>Пстреам. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="538a5-117"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="538a5-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="538a5-118">Library</span></span><br/> | <dl> <span data-ttu-id="538a5-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="538a5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="538a5-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="538a5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="538a5-121">**Класс Кперсистстреам**</span><span class="sxs-lookup"><span data-stu-id="538a5-121">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




