---
description: Создание нового дочернего элемента. Добавляет объекты IWiaItem2 в дерево IWiaItem2 устройства.
ms.assetid: 525ee788-3ff4-4def-ae71-4a405c04c6a3
title: 'Метод IWiaItem2:: Креатечилдитем (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CreateChildItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 0002a6110894491a8d6efabb5a142b7c81adc820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711955"
---
# <a name="iwiaitem2createchilditem-method"></a><span data-ttu-id="63056-104">Метод IWiaItem2:: Креатечилдитем</span><span class="sxs-lookup"><span data-stu-id="63056-104">IWiaItem2::CreateChildItem method</span></span>

<span data-ttu-id="63056-105">Создание нового дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="63056-105">Create a new child item.</span></span> <span data-ttu-id="63056-106">Добавляет объекты [**IWiaItem2**](-wia-iwiaitem2.md) в дерево **IWiaItem2** устройства.</span><span class="sxs-lookup"><span data-stu-id="63056-106">Adds [**IWiaItem2**](-wia-iwiaitem2.md) objects to a device's **IWiaItem2** tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="63056-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63056-107">Syntax</span></span>


```C++
HRESULT CreateChildItem(
  [in]  LONG      lItemFlags,
  [in]  LONG      lCreationFlags,
  [in]  BSTR      bstrItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="63056-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="63056-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63056-109">*литемфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63056-109">*lItemFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63056-110">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="63056-110">Type: **LONG**</span></span>

<span data-ttu-id="63056-111">Задает тип элемента WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="63056-111">Specifies the WIA 2.0 item type.</span></span> <span data-ttu-id="63056-112">См. раздел [**Флаги типа элемента WIA**](-wia-wia-item-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="63056-112">See [**WIA Item Type Flags**](-wia-wia-item-type-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="63056-113">*лкреатионфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63056-113">*lCreationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63056-114">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="63056-114">Type: **LONG**</span></span>

<span data-ttu-id="63056-115">Указывает, как создать новый элемент.</span><span class="sxs-lookup"><span data-stu-id="63056-115">Specifies how to create the new item.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="63056-116"><span id="0"></span>**0** (0)</span><span class="sxs-lookup"><span data-stu-id="63056-116"><span id="0"></span>**0** (0)</span></span>


</dt> <dd>

<span data-ttu-id="63056-117">Задайте значения по умолчанию для свойств дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="63056-117">Set the default values for the properties of the child.</span></span>

</dd> <dt>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>

<span data-ttu-id="63056-118"><span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**Копирование \_ \_ \_ Значения родительских свойств** (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="63056-118"><span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**COPY\_PARENT\_PROPERTY\_VALUES** (0x40000000)</span></span>


</dt> <dd>

<span data-ttu-id="63056-119">Скопируйте значения всех свойств чтения и записи из родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="63056-119">Copy the values of all Read/Write properties from the parent.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="63056-120">*бстритемнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63056-120">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63056-121">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="63056-121">Type: **BSTR**</span></span>

<span data-ttu-id="63056-122">Указывает имя элемента.</span><span class="sxs-lookup"><span data-stu-id="63056-122">Specifies the item name.</span></span> <span data-ttu-id="63056-123">Это имя добавляется в конец имени родительского элемента для создания полного имени элемента.</span><span class="sxs-lookup"><span data-stu-id="63056-123">This name is appended to the end of the parent item's name to generate the full item name.</span></span>

</dd> <dt>

<span data-ttu-id="63056-124">*ppIWiaItem2* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="63056-124">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63056-125">Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="63056-125">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="63056-126">Получает адрес указателя на интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) , который задает метод **IWiaItem2:: креатечилдитем** .</span><span class="sxs-lookup"><span data-stu-id="63056-126">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface that sets the **IWiaItem2::CreateChildItem** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63056-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63056-127">Return value</span></span>

<span data-ttu-id="63056-128">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="63056-128">Type: **HRESULT**</span></span>

<span data-ttu-id="63056-129">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="63056-129">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="63056-130">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="63056-130">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="63056-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63056-131">Remarks</span></span>

<span data-ttu-id="63056-132">Некоторые аппаратные устройства WIA 2,0 позволяют приложениям создавать новые элементы в дереве [**IWiaItem2**](-wia-iwiaitem2.md) , представляющем устройство.</span><span class="sxs-lookup"><span data-stu-id="63056-132">Some WIA 2.0 hardware devices allow applications to create new items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree that represents the device.</span></span> <span data-ttu-id="63056-133">Приложения должны протестировать устройства, чтобы узнать, поддерживают ли они эту возможность.</span><span class="sxs-lookup"><span data-stu-id="63056-133">Applications must test the devices to see if they support this capability.</span></span> <span data-ttu-id="63056-134">Используйте интерфейс Иенумвиа \_ dev \_ CAP для перечисления возможностей текущего устройства.</span><span class="sxs-lookup"><span data-stu-id="63056-134">Use the IEnumWIA\_DEV\_CAPS interface to enumerate the current device's capabilities.</span></span>

<span data-ttu-id="63056-135">Если устройство позволяет создавать новые элементы в дереве [**IWiaItem2**](-wia-iwiaitem2.md) , вызов **IWiaItem2:: креатечилдитем** создает новый объект **IWiaItem2** , являющийся дочерним по отношению к текущему узлу.</span><span class="sxs-lookup"><span data-stu-id="63056-135">If the device allows the creation of new items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree, invoking **IWiaItem2::CreateChildItem** creates a new **IWiaItem2** object that is a child of the current node.</span></span> <span data-ttu-id="63056-136">Он передает указатель на новый узел приложению через параметр *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="63056-136">It passes a pointer to the new node to the application through the *ppIWiaItem2* parameter.</span></span> <span data-ttu-id="63056-137">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="63056-137">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="63056-138">Если *лкреатионфлагс* копирует \_ значения родительского \_ свойства \_ , а *Литемфлагс* равен нулю, функция возвращает E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="63056-138">If *lCreationFlags* is COPY\_PARENT\_PROPERTY\_VALUES and *lItemFlags* is zero, the function returns E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="63056-139">Требования</span><span class="sxs-lookup"><span data-stu-id="63056-139">Requirements</span></span>



| <span data-ttu-id="63056-140">Требование</span><span class="sxs-lookup"><span data-stu-id="63056-140">Requirement</span></span> | <span data-ttu-id="63056-141">Значение</span><span class="sxs-lookup"><span data-stu-id="63056-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="63056-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63056-142">Minimum supported client</span></span><br/> | <span data-ttu-id="63056-143">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63056-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="63056-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63056-144">Minimum supported server</span></span><br/> | <span data-ttu-id="63056-145">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63056-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="63056-146">Header</span><span class="sxs-lookup"><span data-stu-id="63056-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="63056-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="63056-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="63056-148">IDL</span><span class="sxs-lookup"><span data-stu-id="63056-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63056-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="63056-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 
