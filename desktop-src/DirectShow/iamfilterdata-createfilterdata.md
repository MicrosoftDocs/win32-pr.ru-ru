---
description: 'Сведения о методе Иамфилтердата:: Креатефилтердата, который создает двоичные данные реестра для фильтра. Этот интерфейс не рекомендуется к использованию.'
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
ms.openlocfilehash: 0a0126266fc33dca030abad65ccf9f0d35f6e195
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989459"
---
# <a name="iamfilterdatacreatefilterdata-method"></a><span data-ttu-id="80a97-104">Метод Иамфилтердата:: Креатефилтердата</span><span class="sxs-lookup"><span data-stu-id="80a97-104">IAMFilterData::CreateFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="80a97-105">Этот интерфейс не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="80a97-105">This interface has been deprecated.</span></span> <span data-ttu-id="80a97-106">Новые приложения не должны использовать его.</span><span class="sxs-lookup"><span data-stu-id="80a97-106">New applications should not use it.</span></span>

 

<span data-ttu-id="80a97-107">`CreateFilterData`Метод создает двоичные данные реестра для фильтра.</span><span class="sxs-lookup"><span data-stu-id="80a97-107">The `CreateFilterData` method creates binary registry data for a filter.</span></span> <span data-ttu-id="80a97-108">Эти данные можно записать в реестр в виде \_ двоичного подраздела reg с именем FilterData в ключе CLSID фильтра.</span><span class="sxs-lookup"><span data-stu-id="80a97-108">This data can be written to the registry as a REG\_BINARY subkey named FilterData, under the filter's CLSID key.</span></span>

<span data-ttu-id="80a97-109">Как правило, нет причин вызывать этот метод в приложении.</span><span class="sxs-lookup"><span data-stu-id="80a97-109">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="80a97-110">Метод [**IFilterMapper2:: регистерфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) автоматически создает двоичные данные и добавляет их в правильное расположение в реестре.</span><span class="sxs-lookup"><span data-stu-id="80a97-110">The [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method automatically creates the binary data and adds it to the correct location in the registry.</span></span> <span data-ttu-id="80a97-111">Дополнительные сведения см. [в разделе Регистрация фильтров DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="80a97-111">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="80a97-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80a97-112">Syntax</span></span>


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a><span data-ttu-id="80a97-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="80a97-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80a97-114">*prf2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80a97-114">*prf2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80a97-115">Указатель на структуру [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) , содержащую сведения о фильтре.</span><span class="sxs-lookup"><span data-stu-id="80a97-115">Pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure that contains the filter information.</span></span>

</dd> <dt>

<span data-ttu-id="80a97-116">*пргбфилтердата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="80a97-116">*prgbFilterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80a97-117">Адрес переменной, которая получает указатель на двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="80a97-117">Address of a variable that receives a pointer to the binary data.</span></span> <span data-ttu-id="80a97-118">Метод выделяет память для данных.</span><span class="sxs-lookup"><span data-stu-id="80a97-118">The method allocates the memory for the data.</span></span> <span data-ttu-id="80a97-119">Вызывающий объект должен освободить память, вызвав метод **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="80a97-119">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> <dt>

<span data-ttu-id="80a97-120">*ПКБ* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="80a97-120">*pcb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80a97-121">Указатель на переменную, которая получает размер двоичных данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="80a97-121">Pointer to a variable that receives the size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80a97-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80a97-122">Return value</span></span>

<span data-ttu-id="80a97-123">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="80a97-123">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="80a97-124">В противном случае функция возвращает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="80a97-124">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="80a97-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="80a97-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="80a97-126">Заголовок Headers \_ Data. h находится в каталоге с [образцом модуля сопоставления](mapper-sample.md) в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="80a97-126">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="80a97-127">Требования</span><span class="sxs-lookup"><span data-stu-id="80a97-127">Requirements</span></span>



| <span data-ttu-id="80a97-128">Требование</span><span class="sxs-lookup"><span data-stu-id="80a97-128">Requirement</span></span> | <span data-ttu-id="80a97-129">Значение</span><span class="sxs-lookup"><span data-stu-id="80a97-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80a97-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="80a97-130">Header</span></span><br/> | <dl> <span data-ttu-id="80a97-131"><dt>\_Данные о данных. h</dt></span><span class="sxs-lookup"><span data-stu-id="80a97-131"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="80a97-132">DLL</span><span class="sxs-lookup"><span data-stu-id="80a97-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="80a97-133"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80a97-133"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="80a97-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80a97-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80a97-135">**Интерфейс Иамфилтердата**</span><span class="sxs-lookup"><span data-stu-id="80a97-135">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 




