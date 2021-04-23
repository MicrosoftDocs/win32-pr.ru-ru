---
title: IWMPStringCollection2 Жетаттрибутекаунтбитипе, метод
description: Метод Жетаттрибутекаунтбитипе возвращает число атрибутов, связанных с указанным индексом коллекции строк, именем атрибута и языком.
ms.assetid: 30312039-3676-4322-b6f6-fb86098bf578
keywords:
- Жетаттрибутекаунтбитипе метод Windows Media Player
- Жетаттрибутекаунтбитипе метод проигрывателя Windows Media Player, интерфейс IWMPStringCollection2
- Интерфейс IWMPStringCollection2 Windows Media Player, метод Жетаттрибутекаунтбитипе
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bb60fdd843fb3f45b6e4e3aff444a8a915fa0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708468"
---
# <a name="iwmpstringcollection2getattributecountbytype-method"></a><span data-ttu-id="18319-106">Метод IWMPStringCollection2:: Жетаттрибутекаунтбитипе</span><span class="sxs-lookup"><span data-stu-id="18319-106">IWMPStringCollection2::getAttributeCountByType method</span></span>

<span data-ttu-id="18319-107">Метод **жетаттрибутекаунтбитипе** возвращает число атрибутов, связанных с указанным индексом коллекции строк, именем атрибута и языком.</span><span class="sxs-lookup"><span data-stu-id="18319-107">The **getAttributeCountByType** method returns the number of attributes associated with the specified string collection index, attribute name, and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="18319-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18319-108">Syntax</span></span>


```CSharp
public System.Int32 getAttributeCountByType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPStringCollection2.getAttributeCountByType
```





## <a name="parameters"></a><span data-ttu-id="18319-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="18319-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18319-110">*лколлектиониндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18319-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18319-111">Значение **System. Int32** , указывающее Отсчитываемый от нуля индекс элемента коллекции строк, из которого необходимо получить атрибут.</span><span class="sxs-lookup"><span data-stu-id="18319-111">The **System.Int32** specifying the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="18319-112">*бстртипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18319-112">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18319-113">**Строка System. String** , которая является именем атрибута.</span><span class="sxs-lookup"><span data-stu-id="18319-113">The **System.String** that is the name of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="18319-114">*бстрлангуаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18319-114">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18319-115">**Строка System. String** , которая является именем языка.</span><span class="sxs-lookup"><span data-stu-id="18319-115">The **System.String** that is the name of the language.</span></span> <span data-ttu-id="18319-116">Если задано значение null или строка нулевой длины (""), используется текущая строка языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="18319-116">If the value is set to null or to a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="18319-117">В противном случае значение должно быть допустимой строкой языка RFC 1766, например "en-US".</span><span class="sxs-lookup"><span data-stu-id="18319-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18319-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18319-118">Return value</span></span>

<span data-ttu-id="18319-119">Значение **System. Int32** , которое является счетчиком.</span><span class="sxs-lookup"><span data-stu-id="18319-119">The **System.Int32** that is the count.</span></span>

## <a name="remarks"></a><span data-ttu-id="18319-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18319-120">Remarks</span></span>

<span data-ttu-id="18319-121">Этот метод используется для определения количества атрибутов, соответствующих определенному имени атрибута для данного элемента **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="18319-121">This method is used to discover the number of attributes corresponding to a particular attribute name for a given **StringCollection** item.</span></span> <span data-ttu-id="18319-122">Номера индексов можно передать в четвертый параметр метода **жетитеминфобитипе** .</span><span class="sxs-lookup"><span data-stu-id="18319-122">Index numbers can then be passed to the fourth parameter of the **getItemInfoByType** method.</span></span>

<span data-ttu-id="18319-123">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="18319-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="18319-124">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="18319-124">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="18319-125">Требования</span><span class="sxs-lookup"><span data-stu-id="18319-125">Requirements</span></span>



| <span data-ttu-id="18319-126">Требование</span><span class="sxs-lookup"><span data-stu-id="18319-126">Requirement</span></span> | <span data-ttu-id="18319-127">Значение</span><span class="sxs-lookup"><span data-stu-id="18319-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18319-128">Версия</span><span class="sxs-lookup"><span data-stu-id="18319-128">Version</span></span><br/>   | <span data-ttu-id="18319-129">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="18319-129">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="18319-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="18319-130">Namespace</span></span><br/> | <span data-ttu-id="18319-131">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="18319-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="18319-132">Сборка</span><span class="sxs-lookup"><span data-stu-id="18319-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="18319-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="18319-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18319-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18319-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18319-135">**Интерфейс IWMPStringCollection2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="18319-135">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="18319-136">**IWMPStringCollection2. Жетитеминфобитипе (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="18319-136">**IWMPStringCollection2.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





