---
description: Метод Сетбуффервалуе добавляет новое \* значение типа Byte (тип VT \_ vector \| VT \_ UI1) или перезаписывает существующий.
ms.assetid: 6c421240-2ff8-4862-bd90-1feee5d15a8d
title: 'Метод Ипортабледевицевалуес:: Сетбуффервалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e04b41fdd397d8d03e7e0576d2ba8fb3b6ad1401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657690"
---
# <a name="iportabledevicevaluessetbuffervalue-method"></a><span data-ttu-id="1c1a0-103">Метод Ипортабледевицевалуес:: Сетбуффервалуе</span><span class="sxs-lookup"><span data-stu-id="1c1a0-103">IPortableDeviceValues::SetBufferValue method</span></span>

<span data-ttu-id="1c1a0-104">Метод **сетбуффервалуе** добавляет новое значение типа **Byte** \* (тип VT \_ vector \| VT \_ UI1) или перезаписывает существующий.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-104">The **SetBufferValue** method adds a new **BYTE**\* value (type VT\_VECTOR \| VT\_UI1) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c1a0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c1a0-105">Syntax</span></span>


```C++
HRESULT SetBufferValue(
  [in] REFPROPERTYKEY key,
  [in] BYTE           *pValue,
  [in] DWORD          cbValue
);
```



## <a name="parameters"></a><span data-ttu-id="1c1a0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c1a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c1a0-107">*ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c1a0-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1a0-108">Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="1c1a0-109">*pValue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c1a0-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1a0-110">**Байт \*** , содержащий данные для записи в элемент.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-110">A **BYTE\*** that contains the data to write to the item.</span></span> <span data-ttu-id="1c1a0-111">Отправленные данные буфера копируются в интерфейс, поэтому вызывающий объект может освободить этот буфер после выполнения этого вызова.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-111">The submitted buffer data is copied to the interface, so the caller can free this buffer after making this call.</span></span>

</dd> <dt>

<span data-ttu-id="1c1a0-112">*кбвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c1a0-112">*cbValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1a0-113">Размер значения, на которое указывает *pValue*, в байтах.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-113">The size of the value pointed to by *pValue*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c1a0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c1a0-114">Return value</span></span>

<span data-ttu-id="1c1a0-115">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1c1a0-116">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1c1a0-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1c1a0-117">Return code</span></span>                                                                          | <span data-ttu-id="1c1a0-118">Описание</span><span class="sxs-lookup"><span data-stu-id="1c1a0-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1c1a0-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1c1a0-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1c1a0-120">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1c1a0-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c1a0-121">Remarks</span></span>

<span data-ttu-id="1c1a0-122">Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-122">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="1c1a0-123">Существующий ключ памяти освобождается соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-123">The existing key memory is released appropriately.</span></span>

<span data-ttu-id="1c1a0-124">Установка буфера, **имеющего значение NULL** или нулевого размера, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-124">Setting a **NULL** or a zero-sized buffer is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c1a0-125">Требования</span><span class="sxs-lookup"><span data-stu-id="1c1a0-125">Requirements</span></span>



| <span data-ttu-id="1c1a0-126">Требование</span><span class="sxs-lookup"><span data-stu-id="1c1a0-126">Requirement</span></span> | <span data-ttu-id="1c1a0-127">Значение</span><span class="sxs-lookup"><span data-stu-id="1c1a0-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c1a0-128">Header</span><span class="sxs-lookup"><span data-stu-id="1c1a0-128">Header</span></span><br/>  | <dl> <span data-ttu-id="1c1a0-129"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c1a0-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c1a0-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1c1a0-130">Library</span></span><br/> | <dl> <span data-ttu-id="1c1a0-131"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c1a0-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c1a0-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c1a0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c1a0-133">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="1c1a0-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="1c1a0-134">**Ипортабледевицевалуес:: Жетбуффервалуе**</span><span class="sxs-lookup"><span data-stu-id="1c1a0-134">**IPortableDeviceValues::GetBufferValue**</span></span>](iportabledevicevalues-getbuffervalue.md)
</dt> </dl>

 

 




