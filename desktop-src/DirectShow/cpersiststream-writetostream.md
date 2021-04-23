---
description: Записывает данные фильтра в заданный поток.
ms.assetid: 1b405050-6cfd-4b69-b449-f00a6ecfac6a
title: Кперсистстреам. Вритетостреам, метод (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.WriteToStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 893d58986db92e50cbafefe74676481162808abf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675681"
---
# <a name="cpersiststreamwritetostream-method"></a><span data-ttu-id="24bcc-103">Кперсистстреам. Вритетостреам, метод</span><span class="sxs-lookup"><span data-stu-id="24bcc-103">CPersistStream.WriteToStream method</span></span>

<span data-ttu-id="24bcc-104">Записывает данные фильтра в заданный поток.</span><span class="sxs-lookup"><span data-stu-id="24bcc-104">Writes the filter's data to the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="24bcc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24bcc-105">Syntax</span></span>


```C++
virtual HRESULT WriteToStream(
   IStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="24bcc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="24bcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24bcc-107">*пстреам*</span><span class="sxs-lookup"><span data-stu-id="24bcc-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="24bcc-108">Указатель на интерфейс **IStream** , указывающий поток назначения данных фильтра.</span><span class="sxs-lookup"><span data-stu-id="24bcc-108">Pointer to an **IStream** interface that specifies the filter data's destination stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24bcc-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24bcc-109">Return value</span></span>

<span data-ttu-id="24bcc-110">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="24bcc-110">Returns S\_OK.</span></span> <span data-ttu-id="24bcc-111">Производный класс должен возвращать допустимое значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="24bcc-111">The derived class should return a valid **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="24bcc-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24bcc-112">Remarks</span></span>

<span data-ttu-id="24bcc-113">Версия по умолчанию не записывает ничего; его можно переопределить для записи данных, относящихся к вашему классу.</span><span class="sxs-lookup"><span data-stu-id="24bcc-113">The default version writes nothing; it can be overridden to write data specific to your class.</span></span>

## <a name="requirements"></a><span data-ttu-id="24bcc-114">Требования</span><span class="sxs-lookup"><span data-stu-id="24bcc-114">Requirements</span></span>



| <span data-ttu-id="24bcc-115">Требование</span><span class="sxs-lookup"><span data-stu-id="24bcc-115">Requirement</span></span> | <span data-ttu-id="24bcc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="24bcc-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24bcc-117">Header</span><span class="sxs-lookup"><span data-stu-id="24bcc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="24bcc-118"><dt>Пстреам. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24bcc-118"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="24bcc-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="24bcc-119">Library</span></span><br/> | <dl> <span data-ttu-id="24bcc-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="24bcc-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24bcc-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24bcc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24bcc-122">**Класс Кперсистстреам**</span><span class="sxs-lookup"><span data-stu-id="24bcc-122">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




