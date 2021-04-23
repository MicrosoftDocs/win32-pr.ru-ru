---
description: Метод NOCOUNT извлекает количество элементов в коллекции.
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: 'Метод Ипортабледевицевалуесколлектион:: NOCOUNT (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5d1eabdcf73d65b42ccff980b15bb15514c3b322
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717779"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a><span data-ttu-id="913dc-103">Метод Ипортабледевицевалуесколлектион:: NOCOUNT</span><span class="sxs-lookup"><span data-stu-id="913dc-103">IPortableDeviceValuesCollection::GetCount method</span></span>

<span data-ttu-id="913dc-104">Метод **NOCOUNT** извлекает количество элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="913dc-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="913dc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="913dc-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="913dc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="913dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="913dc-107">*пцелемс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="913dc-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="913dc-108">Указатель на **DWORD** , содержащий число интерфейсов **ипортабледевицевалуес** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="913dc-108">Pointer to a **DWORD** that contains the number of **IPortableDeviceValues** interfaces in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="913dc-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="913dc-109">Return value</span></span>

<span data-ttu-id="913dc-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="913dc-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="913dc-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="913dc-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="913dc-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="913dc-112">Return code</span></span>                                                                               | <span data-ttu-id="913dc-113">Описание</span><span class="sxs-lookup"><span data-stu-id="913dc-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="913dc-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="913dc-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="913dc-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="913dc-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="913dc-116"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="913dc-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="913dc-117">Обязательный аргумент-указатель имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="913dc-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="913dc-118">Требования</span><span class="sxs-lookup"><span data-stu-id="913dc-118">Requirements</span></span>



| <span data-ttu-id="913dc-119">Требование</span><span class="sxs-lookup"><span data-stu-id="913dc-119">Requirement</span></span> | <span data-ttu-id="913dc-120">Значение</span><span class="sxs-lookup"><span data-stu-id="913dc-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="913dc-121">Header</span><span class="sxs-lookup"><span data-stu-id="913dc-121">Header</span></span><br/>  | <dl> <span data-ttu-id="913dc-122"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="913dc-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="913dc-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="913dc-123">Library</span></span><br/> | <dl> <span data-ttu-id="913dc-124"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="913dc-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="913dc-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="913dc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="913dc-126">**Интерфейс Ипортабледевицевалуесколлектион**</span><span class="sxs-lookup"><span data-stu-id="913dc-126">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




