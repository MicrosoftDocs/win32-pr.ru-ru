---
description: Возвращает сведения о категории элемента.
ms.assetid: 4d6f7a6a-280d-4b36-8e1d-8d9fcaa8a1de
title: 'Метод IWiaItem2:: Жетитемкатегори (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemCategory
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: fdf650e8b540fcb9dc58f93f34771462fbc0a5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711097"
---
# <a name="iwiaitem2getitemcategory-method"></a><span data-ttu-id="34cd8-103">Метод IWiaItem2:: Жетитемкатегори</span><span class="sxs-lookup"><span data-stu-id="34cd8-103">IWiaItem2::GetItemCategory method</span></span>

<span data-ttu-id="34cd8-104">Возвращает сведения о категории элемента.</span><span class="sxs-lookup"><span data-stu-id="34cd8-104">Gets an item's category information.</span></span>

## <a name="syntax"></a><span data-ttu-id="34cd8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34cd8-105">Syntax</span></span>


```C++
HRESULT GetItemCategory(
  [out] GUID *pItemCategoryGUID
);
```



## <a name="parameters"></a><span data-ttu-id="34cd8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="34cd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34cd8-107">*питемкатегоригуид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="34cd8-107">*pItemCategoryGUID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34cd8-108">Тип: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="34cd8-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="34cd8-109">Получает указатель на идентификатор GUID, определяющий категорию элемента.</span><span class="sxs-lookup"><span data-stu-id="34cd8-109">Receives a pointer to the GUID that identifies the category of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34cd8-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34cd8-110">Return value</span></span>

<span data-ttu-id="34cd8-111">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="34cd8-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="34cd8-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="34cd8-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="34cd8-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="34cd8-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="34cd8-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34cd8-114">Remarks</span></span>

<span data-ttu-id="34cd8-115">Каждый объект [**IWiaItem2**](-wia-iwiaitem2.md) в иерархическом дереве объектов, связанных с аппаратным устройством получения образа Windows (WIA) 2,0, имеет определенную категорию.</span><span class="sxs-lookup"><span data-stu-id="34cd8-115">Every [**IWiaItem2**](-wia-iwiaitem2.md) object in the hierarchical tree of objects associated with a Windows Image Acquisition (WIA) 2.0 hardware device has a specific category.</span></span> <span data-ttu-id="34cd8-116">Этот метод позволяет приложениям указывать категорию любого элемента в иерархическом дереве объектов элементов на устройстве.</span><span class="sxs-lookup"><span data-stu-id="34cd8-116">This method enables applications to identify the category of any item in a hierarchical tree of item objects in a device.</span></span>

## <a name="requirements"></a><span data-ttu-id="34cd8-117">Требования</span><span class="sxs-lookup"><span data-stu-id="34cd8-117">Requirements</span></span>



| <span data-ttu-id="34cd8-118">Требование</span><span class="sxs-lookup"><span data-stu-id="34cd8-118">Requirement</span></span> | <span data-ttu-id="34cd8-119">Значение</span><span class="sxs-lookup"><span data-stu-id="34cd8-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34cd8-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34cd8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="34cd8-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="34cd8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="34cd8-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34cd8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="34cd8-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="34cd8-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="34cd8-124">Header</span><span class="sxs-lookup"><span data-stu-id="34cd8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="34cd8-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="34cd8-125"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="34cd8-126">IDL</span><span class="sxs-lookup"><span data-stu-id="34cd8-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="34cd8-127"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="34cd8-127"><dt>Wia.idl</dt></span></span> </dl> |



 

 




