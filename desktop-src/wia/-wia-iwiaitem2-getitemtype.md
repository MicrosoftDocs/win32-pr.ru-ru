---
description: Возвращает сведения о типе элемента.
ms.assetid: 9670f184-e8ba-4596-af6d-2967320dfd95
title: 'Метод IWiaItem2:: ItemType (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemType
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3bf177ddcc117cdfe21a1b9322a0e457cf899c0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809988"
---
# <a name="iwiaitem2getitemtype-method"></a><span data-ttu-id="18d24-103">Метод IWiaItem2:: ItemType</span><span class="sxs-lookup"><span data-stu-id="18d24-103">IWiaItem2::GetItemType method</span></span>

<span data-ttu-id="18d24-104">Возвращает сведения о типе элемента.</span><span class="sxs-lookup"><span data-stu-id="18d24-104">Gets an item's type information.</span></span>

## <a name="syntax"></a><span data-ttu-id="18d24-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18d24-105">Syntax</span></span>


```C++
HRESULT GetItemType(
  [out] LONG *pItemType
);
```



## <a name="parameters"></a><span data-ttu-id="18d24-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="18d24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18d24-107">*питемтипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="18d24-107">*pItemType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18d24-108">Тип: \**Long \** _</span><span class="sxs-lookup"><span data-stu-id="18d24-108">Type: \**LONG\** _</span></span>

<span data-ttu-id="18d24-109">Получает указатель на _ \*Long\*\*, содержащий сочетание флагов типа.</span><span class="sxs-lookup"><span data-stu-id="18d24-109">Receives a pointer to a _ *LONG*\* that contains a combination of type flags.</span></span> <span data-ttu-id="18d24-110">См. раздел [**Флаги типа элемента WIA**](-wia-wia-item-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="18d24-110">See [**WIA Item Type Flags**](-wia-wia-item-type-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18d24-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18d24-111">Return value</span></span>

<span data-ttu-id="18d24-112">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="18d24-112">Type: **HRESULT**</span></span>

<span data-ttu-id="18d24-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="18d24-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="18d24-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="18d24-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="18d24-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18d24-115">Remarks</span></span>

<span data-ttu-id="18d24-116">Каждый объект [**IWiaItem2**](-wia-iwiaitem2.md) в иерархическом дереве объектов, связанных с аппаратным устройством получения образа Windows (WIA) 2,0, имеет конкретный тип данных.</span><span class="sxs-lookup"><span data-stu-id="18d24-116">Every [**IWiaItem2**](-wia-iwiaitem2.md) object in the hierarchical tree of objects associated with a Windows Image Acquisition (WIA) 2.0 hardware device has a specific data type.</span></span> <span data-ttu-id="18d24-117">Объекты элементов представляют собой папки и файлы.</span><span class="sxs-lookup"><span data-stu-id="18d24-117">Item objects represent folders and files.</span></span> <span data-ttu-id="18d24-118">Папки содержат объекты File.</span><span class="sxs-lookup"><span data-stu-id="18d24-118">Folders contain file objects.</span></span> <span data-ttu-id="18d24-119">Объекты файлов содержат данные, полученные устройством, например изображениями и звуками.</span><span class="sxs-lookup"><span data-stu-id="18d24-119">File objects contain data acquired by the device such as images and sounds.</span></span> <span data-ttu-id="18d24-120">Этот метод позволяет приложениям обнаруживать тип любого элемента в иерархическом дереве объектов элементов на устройстве.</span><span class="sxs-lookup"><span data-stu-id="18d24-120">This method enables applications to identify the type of any item in a hierarchical tree of item objects in a device.</span></span>

<span data-ttu-id="18d24-121">Элемент может иметь более одного типа.</span><span class="sxs-lookup"><span data-stu-id="18d24-121">An item may have more than one type.</span></span> <span data-ttu-id="18d24-122">Например, элемент, представляющий звуковой файл, будет иметь атрибуты Type [**виаитемтипеаудио**](-wia-wia-item-type-flags.md) \| **виаитемтипефиле**.</span><span class="sxs-lookup"><span data-stu-id="18d24-122">For example, an item that represents an audio file will have the type attributes [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**.</span></span>

## <a name="requirements"></a><span data-ttu-id="18d24-123">Требования</span><span class="sxs-lookup"><span data-stu-id="18d24-123">Requirements</span></span>



| <span data-ttu-id="18d24-124">Требование</span><span class="sxs-lookup"><span data-stu-id="18d24-124">Requirement</span></span> | <span data-ttu-id="18d24-125">Значение</span><span class="sxs-lookup"><span data-stu-id="18d24-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18d24-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18d24-126">Minimum supported client</span></span><br/> | <span data-ttu-id="18d24-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18d24-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="18d24-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18d24-128">Minimum supported server</span></span><br/> | <span data-ttu-id="18d24-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="18d24-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="18d24-130">Header</span><span class="sxs-lookup"><span data-stu-id="18d24-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="18d24-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="18d24-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="18d24-132">IDL</span><span class="sxs-lookup"><span data-stu-id="18d24-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="18d24-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="18d24-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 




