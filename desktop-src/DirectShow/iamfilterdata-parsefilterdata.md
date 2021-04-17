---
description: Примечание. Этот интерфейс не рекомендуется к использованию.
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
ms.openlocfilehash: 18e1367813adff6b0debdfb698644731668bfc5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675299"
---
# <a name="iamfilterdataparsefilterdata-method"></a><span data-ttu-id="7e052-103">Иамфилтердата: метод:P Арсефилтердата</span><span class="sxs-lookup"><span data-stu-id="7e052-103">IAMFilterData::ParseFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="7e052-104">Этот интерфейс не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="7e052-104">This interface has been deprecated.</span></span> <span data-ttu-id="7e052-105">Новые приложения не должны использовать его.</span><span class="sxs-lookup"><span data-stu-id="7e052-105">New applications should not use it.</span></span>

 

<span data-ttu-id="7e052-106">`ParseFilterData`Метод распаковать двоичные данные реестра для фильтра.</span><span class="sxs-lookup"><span data-stu-id="7e052-106">The `ParseFilterData` method unpacks the binary registry data for a filter.</span></span>

<span data-ttu-id="7e052-107">Как правило, нет причин вызывать этот метод в приложении.</span><span class="sxs-lookup"><span data-stu-id="7e052-107">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="7e052-108">Метод [**IFilterMapper2:: енумматчингфилтерс**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) предоставляет более удобный способ доступа к данным в реестре фильтров.</span><span class="sxs-lookup"><span data-stu-id="7e052-108">The [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method provides a more convenient way to access the filter registry data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e052-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e052-109">Syntax</span></span>


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a><span data-ttu-id="7e052-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e052-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e052-111">*ргбфилтердата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e052-111">*rgbFilterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e052-112">Указатель на двоичные данные реестра.</span><span class="sxs-lookup"><span data-stu-id="7e052-112">Pointer to the binary registry data.</span></span> <span data-ttu-id="7e052-113">Эти данные можно получить, извлекая свойство "FilterData" из моникера фильтра.</span><span class="sxs-lookup"><span data-stu-id="7e052-113">You can get this data by retrieving the "FilterData" property from the filter moniker.</span></span> <span data-ttu-id="7e052-114">Данные хранятся в виде массива **SAFEARRAY** в байтах (VT \_ UI1 \| VT \_ ).</span><span class="sxs-lookup"><span data-stu-id="7e052-114">The data is stored as a **SAFEARRAY** of bytes (VT\_UI1 \| VT\_ARRAY).</span></span>

</dd> <dt>

<span data-ttu-id="7e052-115">*CB* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e052-115">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e052-116">Задает размер двоичных данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="7e052-116">Specifies the size of the binary data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7e052-117">*prgbRegFilter2* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7e052-117">*prgbRegFilter2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e052-118">Адрес переменной, которая получает указатель на распакованные данные.</span><span class="sxs-lookup"><span data-stu-id="7e052-118">Address of a variable that receives a pointer to the unpacked data.</span></span> <span data-ttu-id="7e052-119">При возврате из метода приведите этот указатель к типу [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) , чтобы получить доступ к данным фильтра.</span><span class="sxs-lookup"><span data-stu-id="7e052-119">When the method returns, cast this pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) type to access the filter data.</span></span> <span data-ttu-id="7e052-120">Вызывающий объект должен освободить память, вызвав метод **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="7e052-120">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e052-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e052-121">Return value</span></span>

<span data-ttu-id="7e052-122">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7e052-122">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="7e052-123">В противном случае функция возвращает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="7e052-123">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e052-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e052-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7e052-125">Заголовок Headers \_ Data. h находится в каталоге с [образцом модуля сопоставления](mapper-sample.md) в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7e052-125">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7e052-126">Требования</span><span class="sxs-lookup"><span data-stu-id="7e052-126">Requirements</span></span>



| <span data-ttu-id="7e052-127">Требование</span><span class="sxs-lookup"><span data-stu-id="7e052-127">Requirement</span></span> | <span data-ttu-id="7e052-128">Значение</span><span class="sxs-lookup"><span data-stu-id="7e052-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e052-129">Header</span><span class="sxs-lookup"><span data-stu-id="7e052-129">Header</span></span><br/> | <dl> <span data-ttu-id="7e052-130"><dt>\_Данные о данных. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e052-130"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="7e052-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7e052-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="7e052-132"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e052-132"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7e052-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e052-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e052-134">**Интерфейс Иамфилтердата**</span><span class="sxs-lookup"><span data-stu-id="7e052-134">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 




