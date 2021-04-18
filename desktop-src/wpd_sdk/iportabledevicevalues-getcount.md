---
description: Метод NOCOUNT извлекает количество элементов в коллекции.
ms.assetid: 89266483-4211-43d2-a306-68c70f1e7026
title: 'Метод Ипортабледевицевалуес:: NOCOUNT (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 710348b2f2626d39efcbdf68373d1e556ecc335c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649081"
---
# <a name="iportabledevicevaluesgetcount-method"></a><span data-ttu-id="242ec-103">Метод Ипортабледевицевалуес:: NOCOUNT</span><span class="sxs-lookup"><span data-stu-id="242ec-103">IPortableDeviceValues::GetCount method</span></span>

<span data-ttu-id="242ec-104">Метод **NOCOUNT** извлекает количество элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="242ec-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="242ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="242ec-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a><span data-ttu-id="242ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="242ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="242ec-107">*пцелт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="242ec-107">*pcelt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="242ec-108">Указатель на **DWORD** , содержащий число элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="242ec-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="242ec-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="242ec-109">Return value</span></span>

<span data-ttu-id="242ec-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="242ec-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="242ec-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="242ec-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="242ec-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="242ec-112">Return code</span></span>                                                                          | <span data-ttu-id="242ec-113">Описание</span><span class="sxs-lookup"><span data-stu-id="242ec-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="242ec-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="242ec-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="242ec-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="242ec-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="242ec-116">Требования</span><span class="sxs-lookup"><span data-stu-id="242ec-116">Requirements</span></span>



| <span data-ttu-id="242ec-117">Требование</span><span class="sxs-lookup"><span data-stu-id="242ec-117">Requirement</span></span> | <span data-ttu-id="242ec-118">Значение</span><span class="sxs-lookup"><span data-stu-id="242ec-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="242ec-119">Header</span><span class="sxs-lookup"><span data-stu-id="242ec-119">Header</span></span><br/>  | <dl> <span data-ttu-id="242ec-120"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="242ec-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="242ec-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="242ec-121">Library</span></span><br/> | <dl> <span data-ttu-id="242ec-122"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="242ec-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="242ec-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="242ec-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="242ec-124">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="242ec-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




