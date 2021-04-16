---
description: Метод Clear удаляет все элементы из коллекции.
ms.assetid: 4350ae43-16be-4cf2-816d-719349b12654
title: 'Метод Ипортабледевицевалуес:: Clear (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 45c04319b5691e3bbcfb56d5a447cf2eb60bfaac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657139"
---
# <a name="iportabledevicevaluesclear-method"></a><span data-ttu-id="8cc35-103">Метод Ипортабледевицевалуес:: Clear</span><span class="sxs-lookup"><span data-stu-id="8cc35-103">IPortableDeviceValues::Clear method</span></span>

<span data-ttu-id="8cc35-104">Метод **clear** удаляет все элементы из коллекции.</span><span class="sxs-lookup"><span data-stu-id="8cc35-104">The **Clear** method deletes all items from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc35-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8cc35-105">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="8cc35-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8cc35-106">Parameters</span></span>

<span data-ttu-id="8cc35-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8cc35-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8cc35-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8cc35-108">Return value</span></span>

<span data-ttu-id="8cc35-109">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8cc35-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8cc35-110">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8cc35-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8cc35-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8cc35-111">Return code</span></span>                                                                          | <span data-ttu-id="8cc35-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8cc35-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8cc35-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="8cc35-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8cc35-114">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="8cc35-114">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8cc35-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8cc35-115">Remarks</span></span>

<span data-ttu-id="8cc35-116">Этот метод освобождает память для всех динамически выделяемых элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="8cc35-116">This method frees the memory for all dynamically allocated items in the collection.</span></span> <span data-ttu-id="8cc35-117">Для интерфейсов он вызывает метод **Release**.</span><span class="sxs-lookup"><span data-stu-id="8cc35-117">For interfaces, it calls **Release**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cc35-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8cc35-118">Requirements</span></span>



| <span data-ttu-id="8cc35-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8cc35-119">Requirement</span></span> | <span data-ttu-id="8cc35-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8cc35-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc35-121">Header</span><span class="sxs-lookup"><span data-stu-id="8cc35-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8cc35-122"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cc35-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="8cc35-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8cc35-123">Library</span></span><br/> | <dl> <span data-ttu-id="8cc35-124"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8cc35-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cc35-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8cc35-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cc35-126">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="8cc35-126">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




