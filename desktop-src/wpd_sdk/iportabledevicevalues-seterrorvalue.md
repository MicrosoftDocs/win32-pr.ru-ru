---
description: Метод Сетеррорвалуе добавляет новое значение HRESULT (тип \_ "ошибка VT") или перезаписывает существующую.
ms.assetid: 87369791-42bd-4523-b15a-acf0ea1e5af8
title: 'Метод Ипортабледевицевалуес:: Сетеррорвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 19c7ca57d325e31fd9cd8e0bf5130dc594b0b8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657689"
---
# <a name="iportabledevicevaluesseterrorvalue-method"></a><span data-ttu-id="41ff3-103">Метод Ипортабледевицевалуес:: Сетеррорвалуе</span><span class="sxs-lookup"><span data-stu-id="41ff3-103">IPortableDeviceValues::SetErrorValue method</span></span>

<span data-ttu-id="41ff3-104">Метод **сетеррорвалуе** добавляет новое значение **HRESULT** (тип \_ "ошибка VT") или перезаписывает существующую.</span><span class="sxs-lookup"><span data-stu-id="41ff3-104">The **SetErrorValue** method adds a new **HRESULT** value (type VT\_ERROR) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="41ff3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41ff3-105">Syntax</span></span>


```C++
HRESULT SetErrorValue(
  [in]       REFPROPERTYKEY key,
  [in] const HRESULT        Value
);
```



## <a name="parameters"></a><span data-ttu-id="41ff3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="41ff3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41ff3-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41ff3-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41ff3-108">Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.</span><span class="sxs-lookup"><span data-stu-id="41ff3-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="41ff3-109">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41ff3-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41ff3-110">Значение **HRESULT** , содержащее новое значение.</span><span class="sxs-lookup"><span data-stu-id="41ff3-110">An **HRESULT** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41ff3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41ff3-111">Return value</span></span>

<span data-ttu-id="41ff3-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="41ff3-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="41ff3-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="41ff3-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="41ff3-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="41ff3-114">Return code</span></span>                                                                          | <span data-ttu-id="41ff3-115">Описание</span><span class="sxs-lookup"><span data-stu-id="41ff3-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="41ff3-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="41ff3-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="41ff3-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="41ff3-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="41ff3-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41ff3-118">Remarks</span></span>

<span data-ttu-id="41ff3-119">Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="41ff3-119">If an existing value has the same key specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="41ff3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="41ff3-120">Requirements</span></span>



| <span data-ttu-id="41ff3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="41ff3-121">Requirement</span></span> | <span data-ttu-id="41ff3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="41ff3-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41ff3-123">Header</span><span class="sxs-lookup"><span data-stu-id="41ff3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="41ff3-124"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="41ff3-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="41ff3-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="41ff3-125">Library</span></span><br/> | <dl> <span data-ttu-id="41ff3-126"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41ff3-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41ff3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41ff3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41ff3-128">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="41ff3-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="41ff3-129">**Ипортабледевицевалуес:: Жетеррорвалуе**</span><span class="sxs-lookup"><span data-stu-id="41ff3-129">**IPortableDeviceValues::GetErrorValue**</span></span>](iportabledevicevalues-geterrorvalue.md)
</dt> </dl>

 

 




