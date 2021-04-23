---
description: Возвращает родительский элемент в дереве, который представляет устройство с аппаратным обеспечением Windows для получения образа (WIA) 2,0.
ms.assetid: c6fdaf1d-9875-4852-893c-813894d89f6c
title: 'Метод IWiaItem2:: Жетпарентитем (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetParentItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 055625b98807103c3b79109216f6081d00564b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343665"
---
# <a name="iwiaitem2getparentitem-method"></a><span data-ttu-id="b3c23-103">Метод IWiaItem2:: Жетпарентитем</span><span class="sxs-lookup"><span data-stu-id="b3c23-103">IWiaItem2::GetParentItem method</span></span>

<span data-ttu-id="b3c23-104">Возвращает родительский элемент в дереве, который представляет устройство с аппаратным обеспечением Windows для получения образа (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="b3c23-104">Gets the parent item in the tree that represents a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c23-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3c23-105">Syntax</span></span>


```C++
HRESULT GetParentItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="b3c23-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3c23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3c23-107">*ppIWiaItem2* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b3c23-107">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c23-108">Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b3c23-108">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="b3c23-109">Получает адрес указателя на интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) родителя элемента в дереве объектов элементов.</span><span class="sxs-lookup"><span data-stu-id="b3c23-109">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the parent of the item in the tree of item objects.</span></span> <span data-ttu-id="b3c23-110">Если этот метод вызывается в корне дерева, возвращенный адрес имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b3c23-110">If this method is called on the root of the tree, then the returned address is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3c23-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3c23-111">Return value</span></span>

<span data-ttu-id="b3c23-112">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b3c23-112">Type: **HRESULT**</span></span>

<span data-ttu-id="b3c23-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b3c23-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b3c23-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b3c23-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3c23-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3c23-115">Remarks</span></span>

<span data-ttu-id="b3c23-116">При наличии объекта [**IWiaItem2**](-wia-iwiaitem2.md) в дереве объектов аппаратного устройства WIA 2,0 приложение получает указатель на родительский элемент, вызывая эту функцию.</span><span class="sxs-lookup"><span data-stu-id="b3c23-116">Given any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device, the application retrieves a pointer to the parent item by calling this function.</span></span>

<span data-ttu-id="b3c23-117">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают через параметр *ppIWiaItem2* , если эти указатели не **равны NULL**.</span><span class="sxs-lookup"><span data-stu-id="b3c23-117">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter if these pointers are not **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c23-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b3c23-118">Requirements</span></span>



| <span data-ttu-id="b3c23-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b3c23-119">Requirement</span></span> | <span data-ttu-id="b3c23-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b3c23-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c23-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b3c23-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c23-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3c23-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b3c23-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b3c23-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c23-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3c23-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b3c23-125">Header</span><span class="sxs-lookup"><span data-stu-id="b3c23-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3c23-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3c23-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3c23-127">IDL</span><span class="sxs-lookup"><span data-stu-id="b3c23-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b3c23-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3c23-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 
