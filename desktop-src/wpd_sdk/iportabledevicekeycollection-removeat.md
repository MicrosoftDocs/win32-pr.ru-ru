---
description: Метод RemoveAt удаляет элемент, хранящийся в расположении, заданном по заданному индексу.
ms.assetid: 70f220be-d70b-4a25-8e16-82ed42adf2c4
title: 'Метод Ипортабледевицекэйколлектион:: RemoveAt (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f4e126ef5fcad74b7cee5f748322f15e75481e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708504"
---
# <a name="iportabledevicekeycollectionremoveat-method"></a><span data-ttu-id="82922-103">Метод Ипортабледевицекэйколлектион:: RemoveAt</span><span class="sxs-lookup"><span data-stu-id="82922-103">IPortableDeviceKeyCollection::RemoveAt method</span></span>

<span data-ttu-id="82922-104">Метод **RemoveAt** удаляет элемент, хранящийся в расположении, заданном по заданному индексу.</span><span class="sxs-lookup"><span data-stu-id="82922-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="82922-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82922-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="82922-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82922-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82922-107">*двиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="82922-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82922-108">Указывает индекс удаляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="82922-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82922-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82922-109">Return value</span></span>

<span data-ttu-id="82922-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="82922-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="82922-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="82922-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="82922-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="82922-112">Return code</span></span>                                                                                  | <span data-ttu-id="82922-113">Описание</span><span class="sxs-lookup"><span data-stu-id="82922-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="82922-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="82922-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="82922-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="82922-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="82922-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="82922-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="82922-117">Указанный индекс выходит за пределы допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="82922-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="82922-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82922-118">Remarks</span></span>

<span data-ttu-id="82922-119">Необходимо указать Отсчитываемый от нуля индекс.</span><span class="sxs-lookup"><span data-stu-id="82922-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="82922-120">Требования</span><span class="sxs-lookup"><span data-stu-id="82922-120">Requirements</span></span>



| <span data-ttu-id="82922-121">Требование</span><span class="sxs-lookup"><span data-stu-id="82922-121">Requirement</span></span> | <span data-ttu-id="82922-122">Значение</span><span class="sxs-lookup"><span data-stu-id="82922-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82922-123">Header</span><span class="sxs-lookup"><span data-stu-id="82922-123">Header</span></span><br/>  | <dl> <span data-ttu-id="82922-124"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="82922-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="82922-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="82922-125">Library</span></span><br/> | <dl> <span data-ttu-id="82922-126"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82922-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82922-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82922-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82922-128">**Интерфейс Ипортабледевицекэйколлектион**</span><span class="sxs-lookup"><span data-stu-id="82922-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> </dl>

 

 




