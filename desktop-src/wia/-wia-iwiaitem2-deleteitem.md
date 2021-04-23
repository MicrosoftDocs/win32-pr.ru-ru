---
description: Удаляет текущий объект IWiaItem2 из дерева объектов устройства.
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: 'IWiaItem2: метод:D Елетеитем (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeleteItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: ef6a4204b591f06811f0941ca0ceed72b76151db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711102"
---
# <a name="iwiaitem2deleteitem-method"></a><span data-ttu-id="2395c-103">IWiaItem2: метод:D Елетеитем</span><span class="sxs-lookup"><span data-stu-id="2395c-103">IWiaItem2::DeleteItem method</span></span>

<span data-ttu-id="2395c-104">Удаляет текущий объект [**IWiaItem2**](-wia-iwiaitem2.md) из дерева объектов устройства.</span><span class="sxs-lookup"><span data-stu-id="2395c-104">Removes the current [**IWiaItem2**](-wia-iwiaitem2.md) object from the device's object tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="2395c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2395c-105">Syntax</span></span>


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="2395c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2395c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2395c-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2395c-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2395c-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="2395c-108">Type: **LONG**</span></span>

<span data-ttu-id="2395c-109">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="2395c-109">Currently unused.</span></span> <span data-ttu-id="2395c-110">Значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="2395c-110">Should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2395c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2395c-111">Return value</span></span>

<span data-ttu-id="2395c-112">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2395c-112">Type: **HRESULT**</span></span>

<span data-ttu-id="2395c-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="2395c-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2395c-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2395c-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2395c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2395c-115">Remarks</span></span>

<span data-ttu-id="2395c-116">Система времени выполнения Windows Image Connect (WIA) 2,0 представляет каждое устройство WIA 2,0, подключенное к компьютеру пользователя, в виде иерархического дерева объектов [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="2395c-116">The Windows Image Acquisition (WIA) 2.0 run-time system represents each WIA 2.0 hardware device connected to the user's computer as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="2395c-117">Данное устройство WIA 2,0 может не позволить приложениям удалять объекты **IWiaItem2** из своего дерева.</span><span class="sxs-lookup"><span data-stu-id="2395c-117">A given WIA 2.0 device may or may not allow applications to delete **IWiaItem2** objects from its tree.</span></span> <span data-ttu-id="2395c-118">Элементы, имеющие дочерние объекты, не могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="2395c-118">Items that have children cannot be deleted.</span></span> <span data-ttu-id="2395c-119">Интерфейс [**иенумвиа \_ dev \_ Cap**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) должен использоваться для запроса устройства для возможности удаления элементов.</span><span class="sxs-lookup"><span data-stu-id="2395c-119">The [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface must be used to query the device for item deletion capability.</span></span>

<span data-ttu-id="2395c-120">Если устройство поддерживает удаление элементов в дереве [**IWiaItem2**](-wia-iwiaitem2.md) , вызовите метод **IWiaItem2::D елетеитем** , чтобы удалить объект **IWiaItem2** .</span><span class="sxs-lookup"><span data-stu-id="2395c-120">If the device supports item deletion in its [**IWiaItem2**](-wia-iwiaitem2.md) tree, call the **IWiaItem2::DeleteItem** method to remove the **IWiaItem2** object.</span></span> <span data-ttu-id="2395c-121">Обратите внимание, что этот метод удаляет объект только после освобождения всех ссылок на объект.</span><span class="sxs-lookup"><span data-stu-id="2395c-121">Note that this method only deletes an object after all references to the object have been released.</span></span> <span data-ttu-id="2395c-122">Если удаление элемента завершилось сбоем, \_ возвращается E DELETEITEM.</span><span class="sxs-lookup"><span data-stu-id="2395c-122">If the deletion of an item has failed, E\_DELETEITEM is returned.</span></span> <span data-ttu-id="2395c-123">Числовое значение для этой ошибки еще не определено.</span><span class="sxs-lookup"><span data-stu-id="2395c-123">The numeric value for this error is not yet defined.</span></span>

## <a name="requirements"></a><span data-ttu-id="2395c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="2395c-124">Requirements</span></span>



| <span data-ttu-id="2395c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="2395c-125">Requirement</span></span> | <span data-ttu-id="2395c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2395c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2395c-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2395c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2395c-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2395c-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2395c-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2395c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2395c-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2395c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2395c-131">Header</span><span class="sxs-lookup"><span data-stu-id="2395c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2395c-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="2395c-132"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="2395c-133">IDL</span><span class="sxs-lookup"><span data-stu-id="2395c-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2395c-134"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2395c-134"><dt>Wia.idl</dt></span></span> </dl> |



 

 




