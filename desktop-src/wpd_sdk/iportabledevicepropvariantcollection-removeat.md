---
description: Метод RemoveAt удаляет элемент, хранящийся в расположении, заданном по заданному индексу.
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
ms.openlocfilehash: 74c7900340caab6adfda1b4607df607a4f6f0811
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694742"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a><span data-ttu-id="20ffd-103">Метод Ипортабледевицепропвариантколлектион:: RemoveAt</span><span class="sxs-lookup"><span data-stu-id="20ffd-103">IPortableDevicePropVariantCollection::RemoveAt method</span></span>

<span data-ttu-id="20ffd-104">Метод **RemoveAt** удаляет элемент, хранящийся в расположении, заданном по заданному индексу.</span><span class="sxs-lookup"><span data-stu-id="20ffd-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="20ffd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20ffd-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="20ffd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="20ffd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20ffd-107">*двиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="20ffd-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ffd-108">Указывает индекс удаляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="20ffd-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20ffd-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20ffd-109">Return value</span></span>

<span data-ttu-id="20ffd-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="20ffd-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="20ffd-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="20ffd-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="20ffd-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="20ffd-112">Return code</span></span>                                                                                  | <span data-ttu-id="20ffd-113">Описание</span><span class="sxs-lookup"><span data-stu-id="20ffd-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="20ffd-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="20ffd-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="20ffd-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="20ffd-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="20ffd-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="20ffd-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="20ffd-117">Указанный индекс выходит за пределы допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="20ffd-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="20ffd-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20ffd-118">Remarks</span></span>

<span data-ttu-id="20ffd-119">Необходимо указать Отсчитываемый от нуля индекс.</span><span class="sxs-lookup"><span data-stu-id="20ffd-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="20ffd-120">Требования</span><span class="sxs-lookup"><span data-stu-id="20ffd-120">Requirements</span></span>



| <span data-ttu-id="20ffd-121">Требование</span><span class="sxs-lookup"><span data-stu-id="20ffd-121">Requirement</span></span> | <span data-ttu-id="20ffd-122">Значение</span><span class="sxs-lookup"><span data-stu-id="20ffd-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ffd-123">Header</span><span class="sxs-lookup"><span data-stu-id="20ffd-123">Header</span></span><br/>  | <dl> <span data-ttu-id="20ffd-124"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="20ffd-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="20ffd-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="20ffd-125">Library</span></span><br/> | <dl> <span data-ttu-id="20ffd-126"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20ffd-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20ffd-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20ffd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20ffd-128">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="20ffd-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




