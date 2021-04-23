---
title: IWMPStringCollection2 getItemInfo, метод
description: Метод getItemInfo возвращает строку, соответствующую указанному индексу и имени элемента коллекции строк.
ms.assetid: 4a107e85-9eb7-42be-b1f9-8e9e92e6e509
keywords:
- getItemInfo метод Windows Media Player
- getItemInfo метод проигрывателя Windows Media Player, интерфейс IWMPStringCollection2
- Интерфейс IWMPStringCollection2 Windows Media Player, метод getItemInfo
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4741c4a3ba74b03038974d8b66bc42c23830ebb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708467"
---
# <a name="iwmpstringcollection2getiteminfo-method"></a><span data-ttu-id="745e1-106">Метод IWMPStringCollection2:: getItemInfo</span><span class="sxs-lookup"><span data-stu-id="745e1-106">IWMPStringCollection2::getItemInfo method</span></span>

<span data-ttu-id="745e1-107">Метод **getItemInfo** возвращает строку, соответствующую указанному индексу и имени элемента коллекции строк.</span><span class="sxs-lookup"><span data-stu-id="745e1-107">The **getItemInfo** method returns the string corresponding to the specified string collection item index and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="745e1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="745e1-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.Int32 lCollectionIndex,
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPStringCollection2.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="745e1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="745e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="745e1-110">*лколлектиониндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="745e1-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="745e1-111">Значение **System. Int32** , указывающее Отсчитываемый от нуля индекс элемента коллекции строк, из которого необходимо получить атрибут.</span><span class="sxs-lookup"><span data-stu-id="745e1-111">The **System.Int32** specifying the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="745e1-112">*бстритемнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="745e1-112">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="745e1-113">**Строка System. String** , которая является именем атрибута.</span><span class="sxs-lookup"><span data-stu-id="745e1-113">The **System.String** that is the attribute name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="745e1-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="745e1-114">Return value</span></span>

<span data-ttu-id="745e1-115">**Строка System. String** , которая является именем элемента коллекции строк.</span><span class="sxs-lookup"><span data-stu-id="745e1-115">The **System.String** that is the name of the string collection item.</span></span> <span data-ttu-id="745e1-116">Для атрибутов, базовым значением которых является **System. Boolean**, возвращается строка «true» или «false».</span><span class="sxs-lookup"><span data-stu-id="745e1-116">For attributes whose underlying value is **System.Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="745e1-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="745e1-117">Remarks</span></span>

<span data-ttu-id="745e1-118">Чтобы получить атрибуты с несколькими значениями и атрибутами со сложными значениями, используйте метод **жетитеминфобитипе** .</span><span class="sxs-lookup"><span data-stu-id="745e1-118">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="745e1-119">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="745e1-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="745e1-120">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="745e1-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="745e1-121">Требования</span><span class="sxs-lookup"><span data-stu-id="745e1-121">Requirements</span></span>



| <span data-ttu-id="745e1-122">Требование</span><span class="sxs-lookup"><span data-stu-id="745e1-122">Requirement</span></span> | <span data-ttu-id="745e1-123">Значение</span><span class="sxs-lookup"><span data-stu-id="745e1-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="745e1-124">Версия</span><span class="sxs-lookup"><span data-stu-id="745e1-124">Version</span></span><br/>   | <span data-ttu-id="745e1-125">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="745e1-125">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="745e1-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="745e1-126">Namespace</span></span><br/> | <span data-ttu-id="745e1-127">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="745e1-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="745e1-128">Сборка</span><span class="sxs-lookup"><span data-stu-id="745e1-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="745e1-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="745e1-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="745e1-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="745e1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="745e1-131">**Интерфейс IWMPStringCollection2**</span><span class="sxs-lookup"><span data-stu-id="745e1-131">**IWMPStringCollection2 Interface**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="745e1-132">**IWMPStringCollection2. Жетитеминфобитипе (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="745e1-132">**IWMPStringCollection2.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





