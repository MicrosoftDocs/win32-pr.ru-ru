---
description: Метод ChangeType преобразует все элементы в коллекции в указанный объект VARTYPE.
ms.assetid: b01b6205-c900-4b2e-810f-426e1e71a008
title: 'Метод Ипортабледевицепропвариантколлектион:: ChangeType (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.ChangeType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d843b62d273b28f7a694c37358742e4f3365be21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708346"
---
# <a name="iportabledevicepropvariantcollectionchangetype-method"></a><span data-ttu-id="3b850-103">Метод Ипортабледевицепропвариантколлектион:: ChangeType</span><span class="sxs-lookup"><span data-stu-id="3b850-103">IPortableDevicePropVariantCollection::ChangeType method</span></span>

<span data-ttu-id="3b850-104">Метод **ChangeType** преобразует все элементы в коллекции в указанный объект VarType.</span><span class="sxs-lookup"><span data-stu-id="3b850-104">The **ChangeType** method converts all items in the collection to the specified VARTYPE.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b850-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b850-105">Syntax</span></span>


```C++
HRESULT ChangeType(
  [in] const VARTYPE vt
);
```



## <a name="parameters"></a><span data-ttu-id="3b850-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b850-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b850-107">*VT* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3b850-107">*vt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b850-108">Указывает объект **VarType** , для которого необходимо преобразовать все элементы в коллекции.</span><span class="sxs-lookup"><span data-stu-id="3b850-108">Specifies the **VARTYPE** to which you want to convert all items in the collection.</span></span> <span data-ttu-id="3b850-109">Примерами типов являются VT \_ UI4 и VT \_ UI8.</span><span class="sxs-lookup"><span data-stu-id="3b850-109">Example types include VT\_UI4 and VT\_UI8.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b850-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b850-110">Return value</span></span>

<span data-ttu-id="3b850-111">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3b850-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3b850-112">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3b850-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3b850-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3b850-113">Return code</span></span>                                                                          | <span data-ttu-id="3b850-114">Описание</span><span class="sxs-lookup"><span data-stu-id="3b850-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3b850-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3b850-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3b850-116">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="3b850-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3b850-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b850-117">Remarks</span></span>

<span data-ttu-id="3b850-118">Если этот метод завершается с ошибкой, коллекция может остаться в промежуточном состоянии, при этом некоторые члены преобразовываются и некоторые из них не преобразовываются.</span><span class="sxs-lookup"><span data-stu-id="3b850-118">If this method fails, the collection may be left in an intermediate state, with some members converted and some not converted.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b850-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3b850-119">Requirements</span></span>



| <span data-ttu-id="3b850-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3b850-120">Requirement</span></span> | <span data-ttu-id="3b850-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3b850-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b850-122">Header</span><span class="sxs-lookup"><span data-stu-id="3b850-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3b850-123"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b850-123"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b850-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3b850-124">Library</span></span><br/> | <dl> <span data-ttu-id="3b850-125"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b850-125"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b850-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b850-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b850-127">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="3b850-127">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




