---
description: 'Метод Ипортабледевицевалуесколлектион:: NOCOUNT — метод NOCOUNT извлекает количество элементов в коллекции.'
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
ms.openlocfilehash: 8304184f3323feb92a14b523dc629c6ae45f6a85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083182"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a><span data-ttu-id="1ec65-103">Метод Ипортабледевицевалуесколлектион:: NOCOUNT</span><span class="sxs-lookup"><span data-stu-id="1ec65-103">IPortableDeviceValuesCollection::GetCount method</span></span>

<span data-ttu-id="1ec65-104">Метод **NOCOUNT** извлекает количество элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="1ec65-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec65-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ec65-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="1ec65-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ec65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec65-107">*пцелемс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ec65-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec65-108">Указатель на **DWORD** , содержащий число интерфейсов **ипортабледевицевалуес** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="1ec65-108">Pointer to a **DWORD** that contains the number of **IPortableDeviceValues** interfaces in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec65-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ec65-109">Return value</span></span>

<span data-ttu-id="1ec65-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1ec65-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1ec65-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1ec65-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1ec65-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1ec65-112">Return code</span></span>                                                                               | <span data-ttu-id="1ec65-113">Описание</span><span class="sxs-lookup"><span data-stu-id="1ec65-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="1ec65-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1ec65-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="1ec65-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="1ec65-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="1ec65-116"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="1ec65-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="1ec65-117">Обязательный аргумент-указатель имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1ec65-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1ec65-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1ec65-118">Requirements</span></span>



| <span data-ttu-id="1ec65-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1ec65-119">Requirement</span></span> | <span data-ttu-id="1ec65-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1ec65-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec65-121">Header</span><span class="sxs-lookup"><span data-stu-id="1ec65-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1ec65-122"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ec65-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ec65-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1ec65-123">Library</span></span><br/> | <dl> <span data-ttu-id="1ec65-124"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ec65-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ec65-125">См. также</span><span class="sxs-lookup"><span data-stu-id="1ec65-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec65-126">**Интерфейс Ипортабледевицевалуесколлектион**</span><span class="sxs-lookup"><span data-stu-id="1ec65-126">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




