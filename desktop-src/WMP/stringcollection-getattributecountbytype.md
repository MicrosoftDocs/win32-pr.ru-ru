---
title: StringCollection. Жетаттрибутекаунтбитипе, метод
description: Метод Жетаттрибутекаунтбитипе извлекает количество атрибутов, связанных с указанным индексом элемента StringCollection, именем атрибута и языком.
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- Жетаттрибутекаунтбитипе метод Windows Media Player
- Жетаттрибутекаунтбитипе метод Windows Media Player, класс StringCollection
- Класс StringCollection Windows Media Player, метод Жетаттрибутекаунтбитипе
topic_type:
- apiref
api_name:
- StringCollection.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acf2d7a1f8849f9bd0e83ead3880ca90d2d6149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717933"
---
# <a name="stringcollectiongetattributecountbytype-method"></a><span data-ttu-id="16e89-106">StringCollection. Жетаттрибутекаунтбитипе, метод</span><span class="sxs-lookup"><span data-stu-id="16e89-106">StringCollection.getAttributeCountByType method</span></span>

<span data-ttu-id="16e89-107">Метод **жетаттрибутекаунтбитипе** извлекает количество атрибутов, связанных с указанным индексом элемента **StringCollection** , именем атрибута и языком.</span><span class="sxs-lookup"><span data-stu-id="16e89-107">The **getAttributeCountByType** method retrieves the number of attributes associated with the specified **StringCollection** item index, attribute name, and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="16e89-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16e89-108">Syntax</span></span>


```JScript
retVal = StringCollection.getAttributeCountByType(
  index,
  name,
  language
)
```



## <a name="parameters"></a><span data-ttu-id="16e89-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e89-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16e89-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="16e89-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16e89-111">**Число** (**Long**), указывающее Отсчитываемый от нуля индекс элемента **StringCollection** , из которого необходимо получить атрибут.</span><span class="sxs-lookup"><span data-stu-id="16e89-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="16e89-112">*имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="16e89-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16e89-113">**Строка** , содержащая имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="16e89-113">**String** containing the name of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="16e89-114">*языковая* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="16e89-114">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16e89-115">**Строка** , содержащая язык.</span><span class="sxs-lookup"><span data-stu-id="16e89-115">**String** containing the language.</span></span> <span data-ttu-id="16e89-116">Если задано значение null или пустая строка (""), используется текущая строка языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="16e89-116">If the value is set to null or the empty string (""), the current locale string is used.</span></span> <span data-ttu-id="16e89-117">В противном случае значение должно быть допустимой строкой языка RFC 1766, например "en-US".</span><span class="sxs-lookup"><span data-stu-id="16e89-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16e89-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16e89-118">Return value</span></span>

<span data-ttu-id="16e89-119">Этот метод возвращает **число** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="16e89-119">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="16e89-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16e89-120">Remarks</span></span>

<span data-ttu-id="16e89-121">Этот метод используется для определения количества атрибутов, соответствующих определенному имени атрибута для конкретного элемента **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="16e89-121">This method is used to determine the number of attributes corresponding to a particular attribute name for a particular **StringCollection** item.</span></span> <span data-ttu-id="16e89-122">Номера индексов можно передать в четвертый параметр метода **StringCollection. жетитеминфобитипе** .</span><span class="sxs-lookup"><span data-stu-id="16e89-122">Index numbers can then be passed to the fourth parameter of the **StringCollection.getItemInfoByType** method.</span></span>

<span data-ttu-id="16e89-123">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="16e89-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="16e89-124">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="16e89-124">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16e89-125">Требования</span><span class="sxs-lookup"><span data-stu-id="16e89-125">Requirements</span></span>



| <span data-ttu-id="16e89-126">Требование</span><span class="sxs-lookup"><span data-stu-id="16e89-126">Requirement</span></span> | <span data-ttu-id="16e89-127">Значение</span><span class="sxs-lookup"><span data-stu-id="16e89-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16e89-128">Версия</span><span class="sxs-lookup"><span data-stu-id="16e89-128">Version</span></span><br/> | <span data-ttu-id="16e89-129">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="16e89-129">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="16e89-130">DLL</span><span class="sxs-lookup"><span data-stu-id="16e89-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="16e89-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16e89-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16e89-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16e89-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16e89-133">**Объект StringCollection**</span><span class="sxs-lookup"><span data-stu-id="16e89-133">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





