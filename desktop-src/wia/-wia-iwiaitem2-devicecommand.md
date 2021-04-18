---
description: Выдает команду на аппаратное устройство для получения образа Windows (WIA) 2,0.
ms.assetid: a077448f-2029-4fd3-8bce-c0291afd0b79
title: 'IWiaItem2: метод:D Евицекомманд (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceCommand
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2961a3c0e0d1b75a487b9bf112e76bee8c937a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711101"
---
# <a name="iwiaitem2devicecommand-method"></a><span data-ttu-id="bfad3-103">IWiaItem2: метод:D Евицекомманд</span><span class="sxs-lookup"><span data-stu-id="bfad3-103">IWiaItem2::DeviceCommand method</span></span>

<span data-ttu-id="bfad3-104">Выдает команду на аппаратное устройство для получения образа Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="bfad3-104">Issues a command to a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfad3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bfad3-105">Syntax</span></span>


```C++
HRESULT DeviceCommand(
  [in]            LONG      lFlags,
  [in]      const GUID      *pCmdGUID,
  [in, out]       IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="bfad3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bfad3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfad3-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bfad3-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfad3-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="bfad3-108">Type: **LONG**</span></span>

<span data-ttu-id="bfad3-109">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="bfad3-109">Currently unused.</span></span> <span data-ttu-id="bfad3-110">Значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="bfad3-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="bfad3-111">*пкмдгуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bfad3-111">*pCmdGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfad3-112">Тип: \**константа \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="bfad3-112">Type: \**const GUID\** _</span></span>

<span data-ttu-id="bfad3-113">Указывает команду для отправки на устройство WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="bfad3-113">Specifies the command to send to the WIA 2.0 device.</span></span> <span data-ttu-id="bfad3-114">См. раздел [*команды* \* _ устройства WIA](-wia-wia-device-commands.md).</span><span class="sxs-lookup"><span data-stu-id="bfad3-114">See [_ *WIA Device Commands*\*](-wia-wia-device-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="bfad3-115">*ppIWiaItem2* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="bfad3-115">*ppIWiaItem2* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfad3-116">Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="bfad3-116">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="bfad3-117">Получает адрес указателя на элемент [**IWiaItem2**](-wia-iwiaitem2.md) , созданный командой, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="bfad3-117">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) item created by the command, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfad3-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bfad3-118">Return value</span></span>

<span data-ttu-id="bfad3-119">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bfad3-119">Type: **HRESULT**</span></span>

<span data-ttu-id="bfad3-120">В дополнение к стандартным кодам ошибок COM метод может вернуть следующее значение.</span><span class="sxs-lookup"><span data-stu-id="bfad3-120">In addition to the standard COM error codes, the method may return the following value.</span></span>



| <span data-ttu-id="bfad3-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bfad3-121">Return code</span></span>                                                                                       | <span data-ttu-id="bfad3-122">Описание</span><span class="sxs-lookup"><span data-stu-id="bfad3-122">Description</span></span>                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bfad3-123"><dt>**E \_ кмднотсуппортед**</dt></span><span class="sxs-lookup"><span data-stu-id="bfad3-123"><dt>**E\_CMDNOTSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="bfad3-124">Команда не реализована для интерфейса [**IWiaItem2**](-wia-iwiaitem2.md) , на котором вызывается метод.</span><span class="sxs-lookup"><span data-stu-id="bfad3-124">The command is not implemented for the [**IWiaItem2**](-wia-iwiaitem2.md) interface on which the method is called.</span></span> <span data-ttu-id="bfad3-125">Числовое значение для этой ошибки еще не определено.</span><span class="sxs-lookup"><span data-stu-id="bfad3-125">The numeric value for this error is not yet defined.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="bfad3-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bfad3-126">Remarks</span></span>

<span data-ttu-id="bfad3-127">Поведение этого метода отличается в зависимости от категории узла, на котором вызывается метод.</span><span class="sxs-lookup"><span data-stu-id="bfad3-127">The behavior of this method is different depending on the category of the node on which the method is called.</span></span>

<span data-ttu-id="bfad3-128">Когда приложение отправляет команду [**WIA \_ cmd \_ \_**](-wia-wia-device-commands.md) на устройство с помощью метода **IWiaItem2::D евицекомманд** , система времени выполнения WIA 2,0 создает объект [**IWiaItem2**](-wia-iwiaitem2.md) для представления изображения.</span><span class="sxs-lookup"><span data-stu-id="bfad3-128">When the application sends the [**WIA\_CMD\_TAKE\_PICTURE**](-wia-wia-device-commands.md) command to the device using the **IWiaItem2::DeviceCommand** method, the WIA 2.0 run-time system creates an [**IWiaItem2**](-wia-iwiaitem2.md) object to represent the image.</span></span> <span data-ttu-id="bfad3-129">Метод **IWiaItem2::D евицекомманд** сохраняет адрес интерфейса в параметре *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="bfad3-129">The **IWiaItem2::DeviceCommand** method stores the address of the interface in the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="bfad3-130">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="bfad3-130">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfad3-131">Требования</span><span class="sxs-lookup"><span data-stu-id="bfad3-131">Requirements</span></span>



| <span data-ttu-id="bfad3-132">Требование</span><span class="sxs-lookup"><span data-stu-id="bfad3-132">Requirement</span></span> | <span data-ttu-id="bfad3-133">Значение</span><span class="sxs-lookup"><span data-stu-id="bfad3-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bfad3-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bfad3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bfad3-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bfad3-135">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bfad3-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bfad3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bfad3-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bfad3-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bfad3-138">Header</span><span class="sxs-lookup"><span data-stu-id="bfad3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfad3-139"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfad3-139"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="bfad3-140">IDL</span><span class="sxs-lookup"><span data-stu-id="bfad3-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bfad3-141"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bfad3-141"><dt>Wia.idl</dt></span></span> </dl> |



 

 
