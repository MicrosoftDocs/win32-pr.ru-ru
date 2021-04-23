---
description: Метод Сетфлоатвалуе добавляет новое значение FLOAT (Type VT \_ R4) или перезаписывает существующий.
ms.assetid: 1e0c9d19-47bf-4d93-a0c0-27e2c4897012
title: 'Метод Ипортабледевицевалуес:: Сетфлоатвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 60b42217c925c83e96f2c893c7bc7f11449ebdd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704285"
---
# <a name="iportabledevicevaluessetfloatvalue-method"></a><span data-ttu-id="1a97c-103">Метод Ипортабледевицевалуес:: Сетфлоатвалуе</span><span class="sxs-lookup"><span data-stu-id="1a97c-103">IPortableDeviceValues::SetFloatValue method</span></span>

<span data-ttu-id="1a97c-104">Метод **сетфлоатвалуе** добавляет новое значение **float** (Type VT \_ R4) или перезаписывает существующий.</span><span class="sxs-lookup"><span data-stu-id="1a97c-104">The **SetFloatValue** method adds a new **FLOAT** value (type VT\_R4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a97c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a97c-105">Syntax</span></span>


```C++
HRESULT SetFloatValue(
  [in]       REFPROPERTYKEY key,
  [in] const FLOAT          Value
);
```



## <a name="parameters"></a><span data-ttu-id="1a97c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a97c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a97c-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a97c-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a97c-108">Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.</span><span class="sxs-lookup"><span data-stu-id="1a97c-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="1a97c-109">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a97c-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a97c-110">**Число с плавающей запятой** , содержащее новое значение.</span><span class="sxs-lookup"><span data-stu-id="1a97c-110">A **FLOAT** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a97c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a97c-111">Return value</span></span>

<span data-ttu-id="1a97c-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1a97c-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1a97c-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1a97c-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1a97c-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1a97c-114">Return code</span></span>                                                                          | <span data-ttu-id="1a97c-115">Описание</span><span class="sxs-lookup"><span data-stu-id="1a97c-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1a97c-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1a97c-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1a97c-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="1a97c-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1a97c-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a97c-118">Remarks</span></span>

<span data-ttu-id="1a97c-119">Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="1a97c-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a97c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="1a97c-120">Requirements</span></span>



| <span data-ttu-id="1a97c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="1a97c-121">Requirement</span></span> | <span data-ttu-id="1a97c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1a97c-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a97c-123">Header</span><span class="sxs-lookup"><span data-stu-id="1a97c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1a97c-124"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a97c-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a97c-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1a97c-125">Library</span></span><br/> | <dl> <span data-ttu-id="1a97c-126"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a97c-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a97c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a97c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a97c-128">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="1a97c-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="1a97c-129">**Ипортабледевицевалуес:: Жетфлоатвалуе**</span><span class="sxs-lookup"><span data-stu-id="1a97c-129">**IPortableDeviceValues::GetFloatValue**</span></span>](iportabledevicevalues-getfloatvalue.md)
</dt> </dl>

 

 




