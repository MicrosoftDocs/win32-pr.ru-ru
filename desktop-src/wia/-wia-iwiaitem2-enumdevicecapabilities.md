---
description: Создает перечислитель, который используется для определения команд и событий, которые поддерживает устройство для получения изображений (WIA) 2,0.
ms.assetid: 9efb758d-a5d6-41c7-b318-2897274ccbc0
title: 'Метод IWiaItem2:: Енумдевицекапабилитиес (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumDeviceCapabilities
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3e771aa636b42d9cd7e4024a1684ebe3edf02eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541983"
---
# <a name="iwiaitem2enumdevicecapabilities-method"></a><span data-ttu-id="8ee88-103">Метод IWiaItem2:: Енумдевицекапабилитиес</span><span class="sxs-lookup"><span data-stu-id="8ee88-103">IWiaItem2::EnumDeviceCapabilities method</span></span>

<span data-ttu-id="8ee88-104">Создает перечислитель, который используется для определения команд и событий, которые поддерживает устройство для получения изображений (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="8ee88-104">Creates an enumerator that is used to ascertain the commands and events a Windows Image Acquisition (WIA) 2.0 device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ee88-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ee88-105">Syntax</span></span>


```C++
HRESULT EnumDeviceCapabilities(
  [in]  LONG              lFlags,
  [out] IEnumWIA_DEV_CAPS **ppIEnumWIA_DEV_CAPS
);
```



## <a name="parameters"></a><span data-ttu-id="8ee88-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ee88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ee88-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8ee88-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee88-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="8ee88-108">Type: **LONG**</span></span>

<span data-ttu-id="8ee88-109">Указывает флаг, выбирающий тип возможностей для перечисления.</span><span class="sxs-lookup"><span data-stu-id="8ee88-109">Specifies a flag that selects the type of capabilities to enumerate.</span></span> <span data-ttu-id="8ee88-110">Это одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8ee88-110">It is one of the following values.</span></span>

<dt>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>

<span data-ttu-id="8ee88-111"><span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**\_команды устройства \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="8ee88-111"><span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**WIA\_DEVICE\_COMMANDS**</span></span>


</dt> <dd>

<span data-ttu-id="8ee88-112">Перечисление команд устройств.</span><span class="sxs-lookup"><span data-stu-id="8ee88-112">Enumerate device commands.</span></span>

</dd> <dt>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>

<span data-ttu-id="8ee88-113"><span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**\_события устройства \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="8ee88-113"><span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**WIA\_DEVICE\_EVENTS**</span></span>


</dt> <dd>

<span data-ttu-id="8ee88-114">Перечисление событий устройства.</span><span class="sxs-lookup"><span data-stu-id="8ee88-114">Enumerate device events.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8ee88-115">*ппиенумвиа \_ \_Ограничения разработки* \[\]</span><span class="sxs-lookup"><span data-stu-id="8ee88-115">*ppIEnumWIA\_DEV\_CAPS* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee88-116">Тип: **[ **иенумвиа \_ dev \_ Cap**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span><span class="sxs-lookup"><span data-stu-id="8ee88-116">Type: **[**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span></span>

<span data-ttu-id="8ee88-117">Получает указатель на интерфейс [**\_ \_ Caps dev иенумвиа**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) , созданный этим методом.</span><span class="sxs-lookup"><span data-stu-id="8ee88-117">Receives a pointer to the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface created by this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ee88-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ee88-118">Return value</span></span>

<span data-ttu-id="8ee88-119">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8ee88-119">Type: **HRESULT**</span></span>

<span data-ttu-id="8ee88-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8ee88-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8ee88-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8ee88-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ee88-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ee88-122">Remarks</span></span>

<span data-ttu-id="8ee88-123">Этот метод используется для создания объекта перечислителя для получения набора команд и событий, поддерживаемых устройством WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="8ee88-123">This method is used to create an enumerator object to obtain the set of commands and events that a WIA 2.0 device supports.</span></span> <span data-ttu-id="8ee88-124">Параметр *лфлагс* используется для указания типов возможностей устройства для перечисления.</span><span class="sxs-lookup"><span data-stu-id="8ee88-124">The *lFlags* parameter is used to specify which kinds of device capabilities to enumerate.</span></span> <span data-ttu-id="8ee88-125">Метод **IWiaItem2:: енумдевицекапабилитиес** сохраняет адрес интерфейса объекта перечислителя в параметре *ппиенумвиа \_ dev \_ Cap* .</span><span class="sxs-lookup"><span data-stu-id="8ee88-125">The **IWiaItem2::EnumDeviceCapabilities** method stores the address of the interface of the enumerator object in the *ppIEnumWIA\_DEV\_CAPS* parameter.</span></span>

<span data-ttu-id="8ee88-126">Этот метод может быть вызван только для корневого элемента объектов [**IWiaItem2**](-wia-iwiaitem2.md) дерева устройств.</span><span class="sxs-lookup"><span data-stu-id="8ee88-126">This method can only be called on the root item of [**IWiaItem2**](-wia-iwiaitem2.md) objects of a device tree.</span></span>

<span data-ttu-id="8ee88-127">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ппиенумвиа \_ dev \_ Caps* .</span><span class="sxs-lookup"><span data-stu-id="8ee88-127">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnumWIA\_DEV\_CAPS* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ee88-128">Требования</span><span class="sxs-lookup"><span data-stu-id="8ee88-128">Requirements</span></span>



| <span data-ttu-id="8ee88-129">Требование</span><span class="sxs-lookup"><span data-stu-id="8ee88-129">Requirement</span></span> | <span data-ttu-id="8ee88-130">Значение</span><span class="sxs-lookup"><span data-stu-id="8ee88-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee88-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ee88-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8ee88-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ee88-132">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8ee88-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ee88-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8ee88-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8ee88-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8ee88-135">Header</span><span class="sxs-lookup"><span data-stu-id="8ee88-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ee88-136"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ee88-136"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ee88-137">IDL</span><span class="sxs-lookup"><span data-stu-id="8ee88-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8ee88-138"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8ee88-138"><dt>Wia.idl</dt></span></span> </dl> |



 

 
