---
description: 'Метод Ипортабледевицевалуесколлектион:: RemoveAt — метод RemoveAt удаляет элемент, хранящийся в расположении, указанном заданным индексом.'
ms.assetid: 380212b6-5e71-406b-8236-e06672505f17
title: 'Метод Ипортабледевицевалуесколлектион:: RemoveAt (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7db15480906bee8181bb0fc589c4f3e30ce4753c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083172"
---
# <a name="iportabledevicevaluescollectionremoveat-method"></a><span data-ttu-id="4fea0-103">Метод Ипортабледевицевалуесколлектион:: RemoveAt</span><span class="sxs-lookup"><span data-stu-id="4fea0-103">IPortableDeviceValuesCollection::RemoveAt method</span></span>

<span data-ttu-id="4fea0-104">Метод **RemoveAt** удаляет элемент, хранящийся в расположении, заданном по заданному индексу.</span><span class="sxs-lookup"><span data-stu-id="4fea0-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fea0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fea0-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="4fea0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4fea0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fea0-107">*двиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4fea0-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fea0-108">Указывает индекс удаляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="4fea0-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fea0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fea0-109">Return value</span></span>

<span data-ttu-id="4fea0-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4fea0-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4fea0-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4fea0-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4fea0-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4fea0-112">Return code</span></span>                                                                                  | <span data-ttu-id="4fea0-113">Описание</span><span class="sxs-lookup"><span data-stu-id="4fea0-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="4fea0-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4fea0-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4fea0-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="4fea0-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="4fea0-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4fea0-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="4fea0-117">Указанный индекс выходит за пределы допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="4fea0-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4fea0-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="4fea0-118">Remarks</span></span>

<span data-ttu-id="4fea0-119">Необходимо указать Отсчитываемый от нуля индекс.</span><span class="sxs-lookup"><span data-stu-id="4fea0-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fea0-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4fea0-120">Requirements</span></span>



| <span data-ttu-id="4fea0-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4fea0-121">Requirement</span></span> | <span data-ttu-id="4fea0-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4fea0-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fea0-123">Header</span><span class="sxs-lookup"><span data-stu-id="4fea0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4fea0-124"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fea0-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="4fea0-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4fea0-125">Library</span></span><br/> | <dl> <span data-ttu-id="4fea0-126"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fea0-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fea0-127">См. также</span><span class="sxs-lookup"><span data-stu-id="4fea0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fea0-128">**Интерфейс Ипортабледевицевалуесколлектион**</span><span class="sxs-lookup"><span data-stu-id="4fea0-128">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




