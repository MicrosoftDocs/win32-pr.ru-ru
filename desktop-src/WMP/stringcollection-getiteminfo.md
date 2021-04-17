---
title: StringCollection. getItemInfo, метод
description: Метод getItemInfo извлекает строку, соответствующую указанному индексу и имени элемента StringCollection.
ms.assetid: a031b91e-9d3b-47ac-bc5b-c111d5e3bc12
keywords:
- getItemInfo метод Windows Media Player
- getItemInfo метод Windows Media Player, класс StringCollection
- Класс StringCollection Windows Media Player, метод getItemInfo
topic_type:
- apiref
api_name:
- StringCollection.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c9552dcebbc7d565ebc797c62ac3bc00ee109fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717938"
---
# <a name="stringcollectiongetiteminfo-method"></a><span data-ttu-id="cf03b-106">StringCollection. getItemInfo, метод</span><span class="sxs-lookup"><span data-stu-id="cf03b-106">StringCollection.getItemInfo method</span></span>

<span data-ttu-id="cf03b-107">Метод **getItemInfo** извлекает строку, соответствующую указанному индексу и имени элемента **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="cf03b-107">The **getItemInfo** method retrieves the string corresponding to the specified **StringCollection** item index and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf03b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf03b-108">Syntax</span></span>


```JScript
strRetVal = StringCollection.getItemInfo(
  index,
  name
)
```



## <a name="parameters"></a><span data-ttu-id="cf03b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf03b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf03b-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf03b-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf03b-111">**Число** (**Long**), указывающее Отсчитываемый от нуля индекс элемента **StringCollection** , из которого необходимо получить атрибут.</span><span class="sxs-lookup"><span data-stu-id="cf03b-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="cf03b-112">*имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf03b-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf03b-113">**Строка** , содержащая имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="cf03b-113">**String** containing the attribute name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf03b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf03b-114">Return value</span></span>

<span data-ttu-id="cf03b-115">Этот метод возвращает **строку** , представляющую значение указанного атрибута.</span><span class="sxs-lookup"><span data-stu-id="cf03b-115">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="cf03b-116">Для атрибутов, базовое значение которых является **логическим**, оно возвращает строку "true" или "false".</span><span class="sxs-lookup"><span data-stu-id="cf03b-116">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="cf03b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf03b-117">Remarks</span></span>

<span data-ttu-id="cf03b-118">Чтобы получить атрибуты с несколькими значениями и атрибутами со сложными значениями, используйте метод **жетитеминфобитипе** .</span><span class="sxs-lookup"><span data-stu-id="cf03b-118">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="cf03b-119">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="cf03b-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="cf03b-120">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="cf03b-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf03b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cf03b-121">Requirements</span></span>



| <span data-ttu-id="cf03b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cf03b-122">Requirement</span></span> | <span data-ttu-id="cf03b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cf03b-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cf03b-124">Версия</span><span class="sxs-lookup"><span data-stu-id="cf03b-124">Version</span></span><br/> | <span data-ttu-id="cf03b-125">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="cf03b-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="cf03b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cf03b-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="cf03b-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf03b-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf03b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf03b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf03b-129">**StringCollection. Жетитеминфобитипе**</span><span class="sxs-lookup"><span data-stu-id="cf03b-129">**StringCollection.getItemInfoByType**</span></span>](stringcollection-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="cf03b-130">**Объект StringCollection**</span><span class="sxs-lookup"><span data-stu-id="cf03b-130">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





