---
description: 'Метод Ипортабледевицевалуес:: NOCOUNT — метод NOCOUNT извлекает количество элементов в коллекции.'
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
ms.openlocfilehash: b7a2f1f71f81296f56be779a4c6eea746ebd0963
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086242"
---
# <a name="iportabledevicevaluesgetcount-method"></a><span data-ttu-id="7edb9-103">Метод Ипортабледевицевалуес:: NOCOUNT</span><span class="sxs-lookup"><span data-stu-id="7edb9-103">IPortableDeviceValues::GetCount method</span></span>

<span data-ttu-id="7edb9-104">Метод **NOCOUNT** извлекает количество элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="7edb9-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7edb9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7edb9-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a><span data-ttu-id="7edb9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7edb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7edb9-107">*пцелт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7edb9-107">*pcelt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7edb9-108">Указатель на **DWORD** , содержащий число элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="7edb9-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7edb9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7edb9-109">Return value</span></span>

<span data-ttu-id="7edb9-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7edb9-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7edb9-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7edb9-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7edb9-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7edb9-112">Return code</span></span>                                                                          | <span data-ttu-id="7edb9-113">Описание</span><span class="sxs-lookup"><span data-stu-id="7edb9-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7edb9-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7edb9-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7edb9-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="7edb9-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7edb9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7edb9-116">Requirements</span></span>



| <span data-ttu-id="7edb9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7edb9-117">Requirement</span></span> | <span data-ttu-id="7edb9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7edb9-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7edb9-119">Header</span><span class="sxs-lookup"><span data-stu-id="7edb9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7edb9-120"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="7edb9-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="7edb9-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7edb9-121">Library</span></span><br/> | <dl> <span data-ttu-id="7edb9-122"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7edb9-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7edb9-123">См. также</span><span class="sxs-lookup"><span data-stu-id="7edb9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7edb9-124">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="7edb9-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




