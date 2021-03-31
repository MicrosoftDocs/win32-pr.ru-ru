---
description: Возвращает корневой элемент дерева объектов элементов, используемых для представления аппаратного устройства для получения образа Windows (WIA) 2,0.
ms.assetid: bc31ad4a-0851-4510-a038-83646ffd5c98
title: 'Метод IWiaItem2:: Жетрутитем (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetRootItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c8d4f004cc9c7cabaf4898f5e8c838a0399dc106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809983"
---
# <a name="iwiaitem2getrootitem-method"></a><span data-ttu-id="0d755-103">Метод IWiaItem2:: Жетрутитем</span><span class="sxs-lookup"><span data-stu-id="0d755-103">IWiaItem2::GetRootItem method</span></span>

<span data-ttu-id="0d755-104">Возвращает корневой элемент дерева объектов элементов, используемых для представления аппаратного устройства для получения образа Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="0d755-104">Gets the root item of a tree of item objects used to represent a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d755-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d755-105">Syntax</span></span>


```C++
HRESULT GetRootItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="0d755-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d755-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d755-107">*ppIWiaItem2* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0d755-107">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d755-108">Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="0d755-108">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="0d755-109">Получает адрес указателя на интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) корневого элемента.</span><span class="sxs-lookup"><span data-stu-id="0d755-109">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d755-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d755-110">Return value</span></span>

<span data-ttu-id="0d755-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0d755-111">Type: **HRESULT**</span></span>

<span data-ttu-id="0d755-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0d755-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0d755-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0d755-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d755-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d755-114">Remarks</span></span>

<span data-ttu-id="0d755-115">При наличии объекта [**IWiaItem2**](-wia-iwiaitem2.md) в дереве объектов аппаратного устройства WIA 2,0 приложение получает указатель на корневой элемент, вызывая эту функцию.</span><span class="sxs-lookup"><span data-stu-id="0d755-115">Given any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device, the application retrieves a pointer to the root item by calling this function.</span></span>

<span data-ttu-id="0d755-116">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="0d755-116">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d755-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0d755-117">Requirements</span></span>



| <span data-ttu-id="0d755-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0d755-118">Requirement</span></span> | <span data-ttu-id="0d755-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0d755-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d755-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d755-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0d755-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d755-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0d755-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d755-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0d755-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0d755-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0d755-124">Header</span><span class="sxs-lookup"><span data-stu-id="0d755-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d755-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d755-125"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d755-126">IDL</span><span class="sxs-lookup"><span data-stu-id="0d755-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0d755-127"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d755-127"><dt>Wia.idl</dt></span></span> </dl> |



 

 
