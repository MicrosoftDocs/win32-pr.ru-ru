---
description: Примечание. Этот интерфейс не рекомендуется к использованию.
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: 'Метод Иамфилтердата:: Креатефилтердата ( \_ данные о данных. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.CreateFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 4c83f19de8e709f9890b23957f730fbbac12dd7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675300"
---
# <a name="iamfilterdatacreatefilterdata-method"></a><span data-ttu-id="85635-103">Метод Иамфилтердата:: Креатефилтердата</span><span class="sxs-lookup"><span data-stu-id="85635-103">IAMFilterData::CreateFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="85635-104">Этот интерфейс не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="85635-104">This interface has been deprecated.</span></span> <span data-ttu-id="85635-105">Новые приложения не должны использовать его.</span><span class="sxs-lookup"><span data-stu-id="85635-105">New applications should not use it.</span></span>

 

<span data-ttu-id="85635-106">`CreateFilterData`Метод создает двоичные данные реестра для фильтра.</span><span class="sxs-lookup"><span data-stu-id="85635-106">The `CreateFilterData` method creates binary registry data for a filter.</span></span> <span data-ttu-id="85635-107">Эти данные можно записать в реестр в виде \_ двоичного подраздела reg с именем FilterData в ключе CLSID фильтра.</span><span class="sxs-lookup"><span data-stu-id="85635-107">This data can be written to the registry as a REG\_BINARY subkey named FilterData, under the filter's CLSID key.</span></span>

<span data-ttu-id="85635-108">Как правило, нет причин вызывать этот метод в приложении.</span><span class="sxs-lookup"><span data-stu-id="85635-108">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="85635-109">Метод [**IFilterMapper2:: регистерфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) автоматически создает двоичные данные и добавляет их в правильное расположение в реестре.</span><span class="sxs-lookup"><span data-stu-id="85635-109">The [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method automatically creates the binary data and adds it to the correct location in the registry.</span></span> <span data-ttu-id="85635-110">Дополнительные сведения см. [в разделе Регистрация фильтров DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="85635-110">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="85635-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85635-111">Syntax</span></span>


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a><span data-ttu-id="85635-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="85635-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85635-113">*prf2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85635-113">*prf2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85635-114">Указатель на структуру [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) , содержащую сведения о фильтре.</span><span class="sxs-lookup"><span data-stu-id="85635-114">Pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure that contains the filter information.</span></span>

</dd> <dt>

<span data-ttu-id="85635-115">*пргбфилтердата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="85635-115">*prgbFilterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85635-116">Адрес переменной, которая получает указатель на двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="85635-116">Address of a variable that receives a pointer to the binary data.</span></span> <span data-ttu-id="85635-117">Метод выделяет память для данных.</span><span class="sxs-lookup"><span data-stu-id="85635-117">The method allocates the memory for the data.</span></span> <span data-ttu-id="85635-118">Вызывающий объект должен освободить память, вызвав метод **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="85635-118">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> <dt>

<span data-ttu-id="85635-119">*ПКБ* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="85635-119">*pcb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85635-120">Указатель на переменную, которая получает размер двоичных данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="85635-120">Pointer to a variable that receives the size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85635-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85635-121">Return value</span></span>

<span data-ttu-id="85635-122">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="85635-122">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="85635-123">В противном случае функция возвращает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="85635-123">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="85635-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85635-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="85635-125">Заголовок Headers \_ Data. h находится в каталоге с [образцом модуля сопоставления](mapper-sample.md) в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="85635-125">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="85635-126">Требования</span><span class="sxs-lookup"><span data-stu-id="85635-126">Requirements</span></span>



| <span data-ttu-id="85635-127">Требование</span><span class="sxs-lookup"><span data-stu-id="85635-127">Requirement</span></span> | <span data-ttu-id="85635-128">Значение</span><span class="sxs-lookup"><span data-stu-id="85635-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85635-129">Header</span><span class="sxs-lookup"><span data-stu-id="85635-129">Header</span></span><br/> | <dl> <span data-ttu-id="85635-130"><dt>\_Данные о данных. h</dt></span><span class="sxs-lookup"><span data-stu-id="85635-130"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="85635-131">DLL</span><span class="sxs-lookup"><span data-stu-id="85635-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="85635-132"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85635-132"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="85635-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85635-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85635-134">**Интерфейс Иамфилтердата**</span><span class="sxs-lookup"><span data-stu-id="85635-134">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 




