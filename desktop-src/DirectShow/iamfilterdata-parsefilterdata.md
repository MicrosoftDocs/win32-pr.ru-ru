---
description: Узнайте о методе Иамфилтердата::P Арсефилтердата, который распаковать двоичные данные реестра для фильтра. Этот интерфейс не рекомендуется к использованию.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: Иамфилтердата::P метод Арсефилтердата ( \_ данные о данных. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.ParseFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 9560280fa6f16699af907cdb5cf682b9c4bb1277
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989449"
---
# <a name="iamfilterdataparsefilterdata-method"></a><span data-ttu-id="363b3-104">Иамфилтердата: метод:P Арсефилтердата</span><span class="sxs-lookup"><span data-stu-id="363b3-104">IAMFilterData::ParseFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="363b3-105">Этот интерфейс не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="363b3-105">This interface has been deprecated.</span></span> <span data-ttu-id="363b3-106">Новые приложения не должны использовать его.</span><span class="sxs-lookup"><span data-stu-id="363b3-106">New applications should not use it.</span></span>

 

<span data-ttu-id="363b3-107">`ParseFilterData`Метод распаковать двоичные данные реестра для фильтра.</span><span class="sxs-lookup"><span data-stu-id="363b3-107">The `ParseFilterData` method unpacks the binary registry data for a filter.</span></span>

<span data-ttu-id="363b3-108">Как правило, нет причин вызывать этот метод в приложении.</span><span class="sxs-lookup"><span data-stu-id="363b3-108">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="363b3-109">Метод [**IFilterMapper2:: енумматчингфилтерс**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) предоставляет более удобный способ доступа к данным в реестре фильтров.</span><span class="sxs-lookup"><span data-stu-id="363b3-109">The [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method provides a more convenient way to access the filter registry data.</span></span>

## <a name="syntax"></a><span data-ttu-id="363b3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="363b3-110">Syntax</span></span>


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a><span data-ttu-id="363b3-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="363b3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="363b3-112">*ргбфилтердата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="363b3-112">*rgbFilterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="363b3-113">Указатель на двоичные данные реестра.</span><span class="sxs-lookup"><span data-stu-id="363b3-113">Pointer to the binary registry data.</span></span> <span data-ttu-id="363b3-114">Эти данные можно получить, извлекая свойство "FilterData" из моникера фильтра.</span><span class="sxs-lookup"><span data-stu-id="363b3-114">You can get this data by retrieving the "FilterData" property from the filter moniker.</span></span> <span data-ttu-id="363b3-115">Данные хранятся в виде массива **SAFEARRAY** в байтах (VT \_ UI1 \| VT \_ ).</span><span class="sxs-lookup"><span data-stu-id="363b3-115">The data is stored as a **SAFEARRAY** of bytes (VT\_UI1 \| VT\_ARRAY).</span></span>

</dd> <dt>

<span data-ttu-id="363b3-116">*CB* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="363b3-116">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="363b3-117">Задает размер двоичных данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="363b3-117">Specifies the size of the binary data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="363b3-118">*prgbRegFilter2* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="363b3-118">*prgbRegFilter2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="363b3-119">Адрес переменной, которая получает указатель на распакованные данные.</span><span class="sxs-lookup"><span data-stu-id="363b3-119">Address of a variable that receives a pointer to the unpacked data.</span></span> <span data-ttu-id="363b3-120">При возврате из метода приведите этот указатель к типу [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) , чтобы получить доступ к данным фильтра.</span><span class="sxs-lookup"><span data-stu-id="363b3-120">When the method returns, cast this pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) type to access the filter data.</span></span> <span data-ttu-id="363b3-121">Вызывающий объект должен освободить память, вызвав метод **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="363b3-121">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="363b3-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="363b3-122">Return value</span></span>

<span data-ttu-id="363b3-123">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="363b3-123">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="363b3-124">В противном случае функция возвращает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="363b3-124">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="363b3-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="363b3-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="363b3-126">Заголовок Headers \_ Data. h находится в каталоге с [образцом модуля сопоставления](mapper-sample.md) в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="363b3-126">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="363b3-127">Требования</span><span class="sxs-lookup"><span data-stu-id="363b3-127">Requirements</span></span>



| <span data-ttu-id="363b3-128">Требование</span><span class="sxs-lookup"><span data-stu-id="363b3-128">Requirement</span></span> | <span data-ttu-id="363b3-129">Значение</span><span class="sxs-lookup"><span data-stu-id="363b3-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="363b3-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="363b3-130">Header</span></span><br/> | <dl> <span data-ttu-id="363b3-131"><dt>\_Данные о данных. h</dt></span><span class="sxs-lookup"><span data-stu-id="363b3-131"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="363b3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="363b3-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="363b3-133"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="363b3-133"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="363b3-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="363b3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="363b3-135">**Интерфейс Иамфилтердата**</span><span class="sxs-lookup"><span data-stu-id="363b3-135">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 




