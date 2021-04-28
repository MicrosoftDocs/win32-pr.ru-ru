---
description: 'Метод Ипортабледевицепропвариантколлектион:: RemoveAt — метод RemoveAt удаляет элемент, хранящийся в расположении, указанном заданным индексом.'
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: 'Метод Ипортабледевицепропвариантколлектион:: RemoveAt (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5c62df57a95a9f5a8238ff61c4ca6dc3cb73ed36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109951"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a><span data-ttu-id="c0eb4-103">Метод Ипортабледевицепропвариантколлектион:: RemoveAt</span><span class="sxs-lookup"><span data-stu-id="c0eb4-103">IPortableDevicePropVariantCollection::RemoveAt method</span></span>

<span data-ttu-id="c0eb4-104">Метод **RemoveAt** удаляет элемент, хранящийся в расположении, заданном по заданному индексу.</span><span class="sxs-lookup"><span data-stu-id="c0eb4-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0eb4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0eb4-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="c0eb4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0eb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0eb4-107">*двиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0eb4-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0eb4-108">Указывает индекс удаляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="c0eb4-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0eb4-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0eb4-109">Return value</span></span>

<span data-ttu-id="c0eb4-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c0eb4-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c0eb4-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c0eb4-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c0eb4-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c0eb4-112">Return code</span></span>                                                                                  | <span data-ttu-id="c0eb4-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c0eb4-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="c0eb4-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c0eb4-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c0eb4-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="c0eb4-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="c0eb4-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c0eb4-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c0eb4-117">Указанный индекс выходит за пределы допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="c0eb4-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c0eb4-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="c0eb4-118">Remarks</span></span>

<span data-ttu-id="c0eb4-119">Необходимо указать Отсчитываемый от нуля индекс.</span><span class="sxs-lookup"><span data-stu-id="c0eb4-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0eb4-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c0eb4-120">Requirements</span></span>



| <span data-ttu-id="c0eb4-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c0eb4-121">Requirement</span></span> | <span data-ttu-id="c0eb4-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c0eb4-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0eb4-123">Header</span><span class="sxs-lookup"><span data-stu-id="c0eb4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c0eb4-124"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0eb4-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0eb4-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c0eb4-125">Library</span></span><br/> | <dl> <span data-ttu-id="c0eb4-126"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0eb4-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0eb4-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c0eb4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0eb4-128">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="c0eb4-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




