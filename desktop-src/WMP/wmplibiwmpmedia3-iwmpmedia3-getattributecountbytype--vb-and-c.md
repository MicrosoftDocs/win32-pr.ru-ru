---
title: IWMPMedia3 Жетаттрибутекаунтбитипе, метод
description: Метод Жетаттрибутекаунтбитипе возвращает число атрибутов, связанных с указанным типом атрибута.
ms.assetid: d692635f-f9f1-4d8e-a9c5-9d7fa84f41bd
keywords:
- Жетаттрибутекаунтбитипе метод Windows Media Player
- Жетаттрибутекаунтбитипе метод проигрывателя Windows Media Player, интерфейс IWMPMedia3
- Интерфейс IWMPMedia3 Windows Media Player, метод Жетаттрибутекаунтбитипе
topic_type:
- apiref
api_name:
- IWMPMedia3.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49505f9e9df8778cc2c17ba062da6700b9b8aec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665104"
---
# <a name="iwmpmedia3getattributecountbytype-method"></a><span data-ttu-id="4028f-106">Метод IWMPMedia3:: Жетаттрибутекаунтбитипе</span><span class="sxs-lookup"><span data-stu-id="4028f-106">IWMPMedia3::getAttributeCountByType method</span></span>

<span data-ttu-id="4028f-107">Метод **жетаттрибутекаунтбитипе** возвращает число атрибутов, связанных с указанным типом атрибута.</span><span class="sxs-lookup"><span data-stu-id="4028f-107">The **getAttributeCountByType** method returns the number of attributes associated with the specified attribute type.</span></span>

## <a name="syntax"></a><span data-ttu-id="4028f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4028f-108">Syntax</span></span>


```CSharp
public System.Int32 getAttributeCountByType(
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPMedia3.getAttributeCountByType
```





## <a name="parameters"></a><span data-ttu-id="4028f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4028f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4028f-110">*бстртипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4028f-110">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4028f-111">**Строка System. String** , которая является типом атрибута.</span><span class="sxs-lookup"><span data-stu-id="4028f-111">A **System.String** that is the attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="4028f-112">*бстрлангуаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4028f-112">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4028f-113">**Строка System. String** , которая является языком.</span><span class="sxs-lookup"><span data-stu-id="4028f-113">A **System.String** that is the language.</span></span> <span data-ttu-id="4028f-114">Если задано значение null или строка нулевой длины (""), используется текущая строка языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="4028f-114">If the value is set to null or a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="4028f-115">В противном случае значение должно быть допустимой строкой языка RFC 1766, например "en-US".</span><span class="sxs-lookup"><span data-stu-id="4028f-115">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4028f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4028f-116">Return value</span></span>

<span data-ttu-id="4028f-117">Объект **System. Int32** , который является количеством атрибутов, связанных с типом.</span><span class="sxs-lookup"><span data-stu-id="4028f-117">A **System.Int32** that is the count of attributes that are associated with the type.</span></span>

## <a name="remarks"></a><span data-ttu-id="4028f-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4028f-118">Remarks</span></span>

<span data-ttu-id="4028f-119">Этот метод используется для определения количества атрибутов, соответствующих определенному имени атрибута для данного элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4028f-119">This method is used to discover the number of attributes corresponding to a particular attribute name for a given media item.</span></span> <span data-ttu-id="4028f-120">Номера индексов можно передать в метод **жетитеминфобитипе** .</span><span class="sxs-lookup"><span data-stu-id="4028f-120">Index numbers can then be passed to the **getItemInfoByType** method.</span></span> <span data-ttu-id="4028f-121">Это полезно, например, когда элемент мультимедиа был разбит на несколько жанров.</span><span class="sxs-lookup"><span data-stu-id="4028f-121">This is useful, for example, when a media item has been categorized under multiple genres.</span></span>

<span data-ttu-id="4028f-122">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="4028f-122">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="4028f-123">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="4028f-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4028f-124">Требования</span><span class="sxs-lookup"><span data-stu-id="4028f-124">Requirements</span></span>



| <span data-ttu-id="4028f-125">Требование</span><span class="sxs-lookup"><span data-stu-id="4028f-125">Requirement</span></span> | <span data-ttu-id="4028f-126">Значение</span><span class="sxs-lookup"><span data-stu-id="4028f-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4028f-127">Версия</span><span class="sxs-lookup"><span data-stu-id="4028f-127">Version</span></span><br/>   | <span data-ttu-id="4028f-128">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="4028f-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4028f-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4028f-129">Namespace</span></span><br/> | <span data-ttu-id="4028f-130">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="4028f-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4028f-131">Сборка</span><span class="sxs-lookup"><span data-stu-id="4028f-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4028f-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4028f-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4028f-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4028f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4028f-134">**Интерфейс IWMPMedia3 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4028f-134">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4028f-135">**IWMPMedia3. Жетитеминфобитипе (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4028f-135">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





