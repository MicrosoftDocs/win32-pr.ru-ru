---
description: Сохраняет данные фильтра в заданном потоке.
ms.assetid: f45c8c6e-f0bb-4358-805a-da2669706d34
title: Метод Кперсистстреам. Save (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Save
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c16e4820f846d2d60382fabd6aafe3ad82880193
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668666"
---
# <a name="cpersiststreamsave-method"></a><span data-ttu-id="cb02a-103">Кперсистстреам. Save, метод</span><span class="sxs-lookup"><span data-stu-id="cb02a-103">CPersistStream.Save method</span></span>

<span data-ttu-id="cb02a-104">Сохраняет данные фильтра в заданном потоке.</span><span class="sxs-lookup"><span data-stu-id="cb02a-104">Saves the filter's data to the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb02a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb02a-105">Syntax</span></span>


```C++
HRESULT Save(
   LPSTREAM pStm,
   BOOL     fClearDirty
);
```



## <a name="parameters"></a><span data-ttu-id="cb02a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb02a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb02a-107">*пстм*</span><span class="sxs-lookup"><span data-stu-id="cb02a-107">*pStm*</span></span> 
</dt> <dd>

<span data-ttu-id="cb02a-108">Указатель на поток, в который должны быть сохранены данные.</span><span class="sxs-lookup"><span data-stu-id="cb02a-108">Pointer to the stream to which data is to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="cb02a-109">*фклеардирти*</span><span class="sxs-lookup"><span data-stu-id="cb02a-109">*fClearDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="cb02a-110">Флаг, указывающий, следует ли сбрасывать флаг "грязный" текущего потока; **Значение true** означает сброс.</span><span class="sxs-lookup"><span data-stu-id="cb02a-110">Flag that indicates whether to reset the current stream's dirty flag; **TRUE** means to reset it.</span></span> <span data-ttu-id="cb02a-111">(Если метод вызывается как часть операции сохранения, значение обычно равно **true**; при вызове как часть операции сохранения как значение обычно равно **false**.)</span><span class="sxs-lookup"><span data-stu-id="cb02a-111">(When the method is called as part of a Save operation, the value is typically **TRUE**; when called as part of a Save As operation, the value is typically **FALSE**.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb02a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb02a-112">Return value</span></span>

<span data-ttu-id="cb02a-113">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cb02a-113">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb02a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb02a-114">Remarks</span></span>

<span data-ttu-id="cb02a-115">Эта функция члена реализует метод **IPersistStream:: Save** .</span><span class="sxs-lookup"><span data-stu-id="cb02a-115">This member function implements the **IPersistStream::Save** method.</span></span> <span data-ttu-id="cb02a-116">Он вызывает **вритеинт** с версией программного обеспечения, [**вызывает Кперсистстреам:: вритетостреам**](cpersiststream-writetostream.md) с потоком в *пстм* и сбрасывает **mPS \_ фдирти**.</span><span class="sxs-lookup"><span data-stu-id="cb02a-116">It calls **WriteInt** with the software version, calls [**CPersistStream::WriteToStream**](cpersiststream-writetostream.md) with the stream in *pStm*, and resets **mPS\_fDirty**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb02a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="cb02a-117">Requirements</span></span>



| <span data-ttu-id="cb02a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="cb02a-118">Requirement</span></span> | <span data-ttu-id="cb02a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="cb02a-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb02a-120">Header</span><span class="sxs-lookup"><span data-stu-id="cb02a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="cb02a-121"><dt>Пстреам. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb02a-121"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cb02a-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cb02a-122">Library</span></span><br/> | <dl> <span data-ttu-id="cb02a-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cb02a-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb02a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb02a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb02a-125">**Класс Кперсистстреам**</span><span class="sxs-lookup"><span data-stu-id="cb02a-125">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




