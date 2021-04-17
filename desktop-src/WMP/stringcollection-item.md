---
title: StringCollection. Item, метод
description: Метод Item извлекает строку по указанному индексу.
ms.assetid: 5f6afff2-3ecc-4b28-8c67-f859f5440d4f
keywords:
- метод Item проигрыватель Windows Media Player
- метод Item проигрыватель Windows Media, класс StringCollection
- Класс StringCollection Windows Media Player, метод Item
topic_type:
- apiref
api_name:
- StringCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4244ad194ff3426dab81baddc0b7188214e0360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717775"
---
# <a name="stringcollectionitem-method"></a><span data-ttu-id="4535a-106">StringCollection. Item, метод</span><span class="sxs-lookup"><span data-stu-id="4535a-106">StringCollection.item method</span></span>

<span data-ttu-id="4535a-107">Метод **Item** извлекает строку по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="4535a-107">The **item** method retrieves the string at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="4535a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4535a-108">Syntax</span></span>


```JScript
strRetVal = StringCollection.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="4535a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4535a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4535a-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4535a-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4535a-111">**Число** (**Long**), содержащее индекс.</span><span class="sxs-lookup"><span data-stu-id="4535a-111">**Number** (**long**) containing the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4535a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4535a-112">Return value</span></span>

<span data-ttu-id="4535a-113">Этот метод возвращает **строку**.</span><span class="sxs-lookup"><span data-stu-id="4535a-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4535a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4535a-114">Remarks</span></span>

<span data-ttu-id="4535a-115">Объект **StringCollection** используется для получения набора значений, доступных для атрибута.</span><span class="sxs-lookup"><span data-stu-id="4535a-115">The **StringCollection** object is used to retrieve the set of values available for an attribute.</span></span> <span data-ttu-id="4535a-116">Например, *медиаколлектион*. метод **жетаттрибутестрингколлектион** можно использовать для получения объекта **StringCollection** , представляющего все значения атрибута жанра в типе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4535a-116">For example, the *MediaCollection*.**getAttributeStringCollection** method can be used to retrieve a **StringCollection** object representing all the values for the Genre attribute within the Audio media type.</span></span> <span data-ttu-id="4535a-117">Затем свойство **Item** можно использовать для итерации всех возможных значений атрибута жанра.</span><span class="sxs-lookup"><span data-stu-id="4535a-117">The **item** property can then be used to iterate through all of the possible values for the Genre attribute.</span></span>

<span data-ttu-id="4535a-118">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="4535a-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="4535a-119">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="4535a-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4535a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4535a-120">Requirements</span></span>



| <span data-ttu-id="4535a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4535a-121">Requirement</span></span> | <span data-ttu-id="4535a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4535a-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4535a-123">Версия</span><span class="sxs-lookup"><span data-stu-id="4535a-123">Version</span></span><br/> | <span data-ttu-id="4535a-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="4535a-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4535a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4535a-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="4535a-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4535a-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4535a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4535a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4535a-128">**Медиаколлектион. Жетаттрибутестрингколлектион**</span><span class="sxs-lookup"><span data-stu-id="4535a-128">**MediaCollection.getAttributeStringCollection**</span></span>](mediacollection-getattributestringcollection.md)
</dt> <dt>

[<span data-ttu-id="4535a-129">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="4535a-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="4535a-130">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="4535a-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="4535a-131">**Объект StringCollection**</span><span class="sxs-lookup"><span data-stu-id="4535a-131">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





