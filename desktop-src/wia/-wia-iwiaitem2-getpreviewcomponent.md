---
description: Возвращает компонент предварительной версии для получения образа Windows (WIA) 2,0.
ms.assetid: 0b773c4c-f080-41fa-8902-4243a80fc67c
title: 'Метод IWiaItem2:: Жетпревиевкомпонент (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetPreviewComponent
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e0881f68044c30731322c89d6cc2f19ce7277a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145409"
---
# <a name="iwiaitem2getpreviewcomponent-method"></a><span data-ttu-id="2829d-103">Метод IWiaItem2:: Жетпревиевкомпонент</span><span class="sxs-lookup"><span data-stu-id="2829d-103">IWiaItem2::GetPreviewComponent method</span></span>

<span data-ttu-id="2829d-104">Возвращает компонент предварительной версии для получения образа Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="2829d-104">Gets the Windows Image Acquisition (WIA) 2.0 preview component.</span></span>

## <a name="syntax"></a><span data-ttu-id="2829d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2829d-105">Syntax</span></span>


```C++
HRESULT GetPreviewComponent(
  [in]  LONG        lFlags,
  [out] IWiaPreview **ppWiaPreview
);
```



## <a name="parameters"></a><span data-ttu-id="2829d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2829d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2829d-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2829d-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2829d-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="2829d-108">Type: **LONG**</span></span>

<span data-ttu-id="2829d-109">Не используется.</span><span class="sxs-lookup"><span data-stu-id="2829d-109">Not used.</span></span> <span data-ttu-id="2829d-110">Задайте значение 0.</span><span class="sxs-lookup"><span data-stu-id="2829d-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="2829d-111">*ппвиапревиев* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2829d-111">*ppWiaPreview* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2829d-112">Тип: **[ **ивиапревиев**](-wia-iwiapreview.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="2829d-112">Type: **[**IWiaPreview**](-wia-iwiapreview.md)\*\***</span></span>

<span data-ttu-id="2829d-113">Возвращает адрес указателя на интерфейс [**ивиапревиев**](-wia-iwiapreview.md) компонента предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="2829d-113">Returns the address of a pointer to the [**IWiaPreview**](-wia-iwiapreview.md) interface of the preview component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2829d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2829d-114">Return value</span></span>

<span data-ttu-id="2829d-115">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2829d-115">Type: **HRESULT**</span></span>

<span data-ttu-id="2829d-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="2829d-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2829d-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2829d-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2829d-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2829d-118">Remarks</span></span>

<span data-ttu-id="2829d-119">Эта функция используется для возвращения указателя на адрес компонента предварительной версии WIA 2,0 для любого объекта [**IWiaItem2**](-wia-iwiaitem2.md) в дереве объектов аппаратного устройства WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="2829d-119">Use this function to return a pointer to the address of the WIA 2.0 preview component for any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device.</span></span>

<span data-ttu-id="2829d-120">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают через параметр *ппвиапревиев* .</span><span class="sxs-lookup"><span data-stu-id="2829d-120">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers that they receive through the *ppWiaPreview* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="2829d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2829d-121">Requirements</span></span>



| <span data-ttu-id="2829d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2829d-122">Requirement</span></span> | <span data-ttu-id="2829d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2829d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2829d-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2829d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2829d-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2829d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2829d-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2829d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2829d-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2829d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2829d-128">Header</span><span class="sxs-lookup"><span data-stu-id="2829d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2829d-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="2829d-129"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="2829d-130">IDL</span><span class="sxs-lookup"><span data-stu-id="2829d-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2829d-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2829d-131"><dt>Wia.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2829d-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2829d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2829d-133">**IWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="2829d-133">**IWiaItem2**</span></span>](-wia-iwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="2829d-134">**ивиапревиев**</span><span class="sxs-lookup"><span data-stu-id="2829d-134">**IWiaPreview**</span></span>](-wia-iwiapreview.md)
</dt> </dl>

 

 
