---
description: Создает перечислитель сведений о свойстве для каждого доступного устройства для получения образа Windows (WIA) 2,0.
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: 'Метод IWiaDevMgr2:: Енумдевицеинфо (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.EnumDeviceInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bd9e9281b625f4cec5377537d82a304045b95a3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810780"
---
# <a name="iwiadevmgr2enumdeviceinfo-method"></a><span data-ttu-id="4b4da-103">Метод IWiaDevMgr2:: Енумдевицеинфо</span><span class="sxs-lookup"><span data-stu-id="4b4da-103">IWiaDevMgr2::EnumDeviceInfo method</span></span>

<span data-ttu-id="4b4da-104">Создает перечислитель сведений о свойстве для каждого доступного устройства для получения образа Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="4b4da-104">Creates an enumerator of property information for each available Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b4da-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b4da-105">Syntax</span></span>


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="4b4da-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b4da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b4da-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b4da-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b4da-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="4b4da-108">Type: **LONG**</span></span>

<span data-ttu-id="4b4da-109">Указывает тип устройств WIA 2,0 для перечисления.</span><span class="sxs-lookup"><span data-stu-id="4b4da-109">Specifies the type of WIA 2.0 devices to enumerate.</span></span>

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span data-ttu-id="4b4da-110"><span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA \_ DEVINFO \_ Enum \_ Local**</span><span class="sxs-lookup"><span data-stu-id="4b4da-110"><span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA\_DEVINFO\_ENUM\_LOCAL**</span></span>


</dt> <dd>

<span data-ttu-id="4b4da-111">Перечисляются только локально подключенные активные устройства проверки.</span><span class="sxs-lookup"><span data-stu-id="4b4da-111">Only locally connected active scanner devices are enumerated.</span></span>

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span data-ttu-id="4b4da-112"><span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA \_ DEVINFO \_ Перечисление \_ ALL**</span><span class="sxs-lookup"><span data-stu-id="4b4da-112"><span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA\_DEVINFO\_ENUM\_ALL**</span></span>


</dt> <dd>

<span data-ttu-id="4b4da-113">Все устройства перечисляются как локально, так и удаленно, включая неактивные (отключенные) устройства и устаревшие устройства сти.</span><span class="sxs-lookup"><span data-stu-id="4b4da-113">All devices are enumerated, both locally and remote, including inactive (disconnected) devices and legacy STI-only devices.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4b4da-114">*ппиенум* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4b4da-114">*ppIEnum* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4b4da-115">Тип: **[ **иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***</span><span class="sxs-lookup"><span data-stu-id="4b4da-115">Type: **[**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***</span></span>

<span data-ttu-id="4b4da-116">Получает адрес указателя на интерфейс [**иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .</span><span class="sxs-lookup"><span data-stu-id="4b4da-116">Receives the address of a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b4da-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b4da-117">Return value</span></span>

<span data-ttu-id="4b4da-118">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4b4da-118">Type: **HRESULT**</span></span>

<span data-ttu-id="4b4da-119">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4b4da-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4b4da-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4b4da-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b4da-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b4da-121">Remarks</span></span>

<span data-ttu-id="4b4da-122">Метод **IWiaDevMgr2:: енумдевицеинфо** создает объект перечислителя, поддерживающий интерфейс [**иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .</span><span class="sxs-lookup"><span data-stu-id="4b4da-122">The **IWiaDevMgr2::EnumDeviceInfo** method creates an enumerator object that supports the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span> <span data-ttu-id="4b4da-123">Метод сохраняет указатель на интерфейс **иенумвиа \_ dev \_ info** в параметре *ппиенум*.</span><span class="sxs-lookup"><span data-stu-id="4b4da-123">The method stores a pointer to the **IEnumWIA\_DEV\_INFO** interface in the parameter *ppIEnum*.</span></span> <span data-ttu-id="4b4da-124">Приложения могут использовать указатель интерфейса **иенумвиа \_ dev \_ info** для ПЕРЕЧИСЛЕНИЯ свойств каждого устройства WIA 2,0, подключенного к компьютеру пользователя.</span><span class="sxs-lookup"><span data-stu-id="4b4da-124">Applications can use the **IEnumWIA\_DEV\_INFO** interface pointer to enumerate the properties of each WIA 2.0 device attached to the user's computer.</span></span>

<span data-ttu-id="4b4da-125">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ппиенум* .</span><span class="sxs-lookup"><span data-stu-id="4b4da-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b4da-126">Требования</span><span class="sxs-lookup"><span data-stu-id="4b4da-126">Requirements</span></span>



| <span data-ttu-id="4b4da-127">Требование</span><span class="sxs-lookup"><span data-stu-id="4b4da-127">Requirement</span></span> | <span data-ttu-id="4b4da-128">Значение</span><span class="sxs-lookup"><span data-stu-id="4b4da-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4b4da-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b4da-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4b4da-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b4da-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4b4da-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b4da-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4b4da-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4b4da-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4b4da-133">Header</span><span class="sxs-lookup"><span data-stu-id="4b4da-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b4da-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b4da-134"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="4b4da-135">IDL</span><span class="sxs-lookup"><span data-stu-id="4b4da-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4b4da-136"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4b4da-136"><dt>Wia.idl</dt></span></span> </dl> |



 

 
