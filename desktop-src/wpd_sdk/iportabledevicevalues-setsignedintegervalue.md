---
description: Метод Сетсигнединтежервалуе добавляет новое ДЛИННое значение (тип VT \_ i4) или перезаписывает существующий.
ms.assetid: b0bb2992-2906-446c-be9a-20bff13f8e1d
title: 'Метод Ипортабледевицевалуес:: Сетсигнединтежервалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 26a5d01ec69203c39008de394e3693acc833d262
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704267"
---
# <a name="iportabledevicevaluessetsignedintegervalue-method"></a><span data-ttu-id="1ac4b-103">Метод Ипортабледевицевалуес:: Сетсигнединтежервалуе</span><span class="sxs-lookup"><span data-stu-id="1ac4b-103">IPortableDeviceValues::SetSignedIntegerValue method</span></span>

<span data-ttu-id="1ac4b-104">Метод **сетсигнединтежервалуе** добавляет новое **длинное** значение (тип VT \_ i4) или перезаписывает существующий.</span><span class="sxs-lookup"><span data-stu-id="1ac4b-104">The **SetSignedIntegerValue** method adds a new **LONG** value (type VT\_I4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ac4b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ac4b-105">Syntax</span></span>


```C++
HRESULT SetSignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONG           Value
);
```



## <a name="parameters"></a><span data-ttu-id="1ac4b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ac4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ac4b-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ac4b-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac4b-108">Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.</span><span class="sxs-lookup"><span data-stu-id="1ac4b-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="1ac4b-109">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ac4b-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac4b-110">**Целое** число, указывающее новое значение.</span><span class="sxs-lookup"><span data-stu-id="1ac4b-110">A **LONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ac4b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ac4b-111">Return value</span></span>

<span data-ttu-id="1ac4b-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1ac4b-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1ac4b-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1ac4b-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1ac4b-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1ac4b-114">Return code</span></span>                                                                          | <span data-ttu-id="1ac4b-115">Описание</span><span class="sxs-lookup"><span data-stu-id="1ac4b-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1ac4b-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1ac4b-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1ac4b-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="1ac4b-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1ac4b-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ac4b-118">Remarks</span></span>

<span data-ttu-id="1ac4b-119">Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="1ac4b-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ac4b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="1ac4b-120">Requirements</span></span>



| <span data-ttu-id="1ac4b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="1ac4b-121">Requirement</span></span> | <span data-ttu-id="1ac4b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1ac4b-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ac4b-123">Header</span><span class="sxs-lookup"><span data-stu-id="1ac4b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1ac4b-124"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ac4b-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ac4b-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1ac4b-125">Library</span></span><br/> | <dl> <span data-ttu-id="1ac4b-126"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ac4b-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ac4b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ac4b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ac4b-128">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="1ac4b-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="1ac4b-129">**Ипортабледевицевалуес:: Жетсигнединтежервалуе**</span><span class="sxs-lookup"><span data-stu-id="1ac4b-129">**IPortableDeviceValues::GetSignedIntegerValue**</span></span>](iportabledevicevalues-getsignedintegervalue.md)
</dt> </dl>

 

 




