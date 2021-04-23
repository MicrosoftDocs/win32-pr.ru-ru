---
description: Создает иерархическое дерево объектов IWiaItem2 для устройства, поддерживающего получение изображений Windows (WIA) 2,0.
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: 'Метод IWiaDevMgr2:: Креатедевице (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.CreateDevice
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a548a0ef43c2621b77c4ed10acde393af21d596d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909871"
---
# <a name="iwiadevmgr2createdevice-method"></a><span data-ttu-id="b1acc-103">Метод IWiaDevMgr2:: Креатедевице</span><span class="sxs-lookup"><span data-stu-id="b1acc-103">IWiaDevMgr2::CreateDevice method</span></span>

<span data-ttu-id="b1acc-104">Создает иерархическое дерево объектов [**IWiaItem2**](-wia-iwiaitem2.md) для устройства, поддерживающего получение изображений Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="b1acc-104">Creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for a Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1acc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1acc-105">Syntax</span></span>


```C++
HRESULT CreateDevice(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrDeviceID,
  [out] IWiaItem2 **ppWiaItem2Root
);
```



## <a name="parameters"></a><span data-ttu-id="b1acc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1acc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1acc-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1acc-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1acc-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="b1acc-108">Type: **LONG**</span></span>

<span data-ttu-id="b1acc-109">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="b1acc-109">Currently unused.</span></span> <span data-ttu-id="b1acc-110">Значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b1acc-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b1acc-111">*бстрдевицеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1acc-111">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1acc-112">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b1acc-112">Type: **BSTR**</span></span>

<span data-ttu-id="b1acc-113">Указывает уникальный идентификатор устройства WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="b1acc-113">Specifies the unique identifier of the WIA 2.0 device.</span></span>

</dd> <dt>

<span data-ttu-id="b1acc-114">*ppWiaItem2Root* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b1acc-114">*ppWiaItem2Root* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1acc-115">Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b1acc-115">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="b1acc-116">Получает адрес указателя на интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) корневого элемента в иерархическом дереве для устройства WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="b1acc-116">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item in the hierarchical tree for the WIA 2.0 device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1acc-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1acc-117">Return value</span></span>

<span data-ttu-id="b1acc-118">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b1acc-118">Type: **HRESULT**</span></span>

<span data-ttu-id="b1acc-119">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b1acc-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b1acc-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b1acc-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1acc-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1acc-121">Remarks</span></span>

<span data-ttu-id="b1acc-122">Приложения используют метод **IWiaDevMgr2:: креатедевице** для создания объекта устройства для устройств WIA 2,0, заданных параметром бстрдевицеид.</span><span class="sxs-lookup"><span data-stu-id="b1acc-122">Applications use the **IWiaDevMgr2::CreateDevice** method to create a device object for the WIA 2.0 devices specified by the bstrDeviceID parameter.</span></span> <span data-ttu-id="b1acc-123">При возврате метод **IWiaDevMgr2:: креатедевице** сохраняет адрес указателя в параметре *ppWiaItem2Root*, который указывает на корневой элемент дерева объектов [**IWiaItem2**](-wia-iwiaitem2.md) , созданных **IWiaDevMgr2:: креатедевице**.</span><span class="sxs-lookup"><span data-stu-id="b1acc-123">When it returns, the **IWiaDevMgr2::CreateDevice** method stores an address of a pointer in the parameter *ppWiaItem2Root*, which points to the root item of the tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects created by **IWiaDevMgr2::CreateDevice**.</span></span> <span data-ttu-id="b1acc-124">Приложения могут использовать это дерево объектов для управления и извлечения данных с устройства WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="b1acc-124">Applications can use this tree of objects to control and retrieve data from the WIA 2.0 device.</span></span>

<span data-ttu-id="b1acc-125">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей, которые они получают с помощью параметра *ppWiaItem2Root* .</span><span class="sxs-lookup"><span data-stu-id="b1acc-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the pointers they receive through the *ppWiaItem2Root* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1acc-126">Требования</span><span class="sxs-lookup"><span data-stu-id="b1acc-126">Requirements</span></span>



| <span data-ttu-id="b1acc-127">Требование</span><span class="sxs-lookup"><span data-stu-id="b1acc-127">Requirement</span></span> | <span data-ttu-id="b1acc-128">Значение</span><span class="sxs-lookup"><span data-stu-id="b1acc-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b1acc-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1acc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b1acc-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1acc-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b1acc-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1acc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b1acc-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b1acc-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b1acc-133">Header</span><span class="sxs-lookup"><span data-stu-id="b1acc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1acc-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1acc-134"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1acc-135">IDL</span><span class="sxs-lookup"><span data-stu-id="b1acc-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b1acc-136"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b1acc-136"><dt>Wia.idl</dt></span></span> </dl> |



 

 
