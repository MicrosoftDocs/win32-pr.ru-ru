---
description: Метод NOCOUNT получает количество ключей в этой коллекции.
ms.assetid: 963f514e-3e0f-4334-ac29-6de7cc8aa336
title: 'Метод Ипортабледевицекэйколлектион:: NOCOUNT (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e867a171039a97cc0f83198f72eecaeb57ad3c16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708505"
---
# <a name="iportabledevicekeycollectiongetcount-method"></a><span data-ttu-id="5a645-103">Метод Ипортабледевицекэйколлектион:: NOCOUNT</span><span class="sxs-lookup"><span data-stu-id="5a645-103">IPortableDeviceKeyCollection::GetCount method</span></span>

<span data-ttu-id="5a645-104">Метод **NOCOUNT** получает количество ключей в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="5a645-104">The **GetCount** method retrieves the number of keys in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a645-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a645-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="5a645-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a645-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a645-107">*пцелемс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a645-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a645-108">Указатель на **DWORD** , содержащий число ключей в коллекции.</span><span class="sxs-lookup"><span data-stu-id="5a645-108">Pointer to a **DWORD** that contains the number of keys in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a645-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a645-109">Return value</span></span>

<span data-ttu-id="5a645-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5a645-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5a645-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5a645-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5a645-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5a645-112">Return code</span></span>                                                                               | <span data-ttu-id="5a645-113">Описание</span><span class="sxs-lookup"><span data-stu-id="5a645-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="5a645-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5a645-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="5a645-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="5a645-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="5a645-116"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="5a645-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="5a645-117">Обязательный аргумент-указатель имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5a645-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="5a645-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="5a645-118">Examples</span></span>

<span data-ttu-id="5a645-119">Пример использования этого метода см. в разделе [Получение поддерживаемых событий службы](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="5a645-119">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a645-120">Требования</span><span class="sxs-lookup"><span data-stu-id="5a645-120">Requirements</span></span>



| <span data-ttu-id="5a645-121">Требование</span><span class="sxs-lookup"><span data-stu-id="5a645-121">Requirement</span></span> | <span data-ttu-id="5a645-122">Значение</span><span class="sxs-lookup"><span data-stu-id="5a645-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a645-123">Header</span><span class="sxs-lookup"><span data-stu-id="5a645-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5a645-124"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a645-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a645-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5a645-125">Library</span></span><br/> | <dl> <span data-ttu-id="5a645-126"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a645-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a645-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a645-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a645-128">**Интерфейс Ипортабледевицекэйколлектион**</span><span class="sxs-lookup"><span data-stu-id="5a645-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="5a645-129">Получение поддерживаемых событий службы</span><span class="sxs-lookup"><span data-stu-id="5a645-129">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="5a645-130">Получение поддерживаемых методов службы</span><span class="sxs-lookup"><span data-stu-id="5a645-130">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




