---
title: Метод Media. Жетаттрибутекаунтбитипе
description: Метод Жетаттрибутекаунтбитипе извлекает количество атрибутов, связанных с указанным именем атрибута и языком.
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- Жетаттрибутекаунтбитипе метод Windows Media Player
- Жетаттрибутекаунтбитипе метод Windows Media Player, класс мультимедиа
- Класс мультимедиа проигрыватель Windows Media Player, метод Жетаттрибутекаунтбитипе
topic_type:
- apiref
api_name:
- Media.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613dca43c32322cd5e7de2b2b04605789009cbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699099"
---
# <a name="mediagetattributecountbytype-method"></a><span data-ttu-id="4b5db-106">Метод Media. Жетаттрибутекаунтбитипе</span><span class="sxs-lookup"><span data-stu-id="4b5db-106">Media.getAttributeCountByType method</span></span>

<span data-ttu-id="4b5db-107">Метод **жетаттрибутекаунтбитипе** извлекает количество атрибутов, связанных с указанным именем атрибута и языком.</span><span class="sxs-lookup"><span data-stu-id="4b5db-107">The **getAttributeCountByType** method retrieves the number of attributes associated with the specified attribute name and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b5db-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b5db-108">Syntax</span></span>


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
)
```



## <a name="parameters"></a><span data-ttu-id="4b5db-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b5db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b5db-110">*имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b5db-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b5db-111">**Строка** , содержащая имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="4b5db-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="4b5db-112">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4b5db-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b5db-113">*языковая* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b5db-113">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b5db-114">**Строка** , представляющая язык.</span><span class="sxs-lookup"><span data-stu-id="4b5db-114">**String** representing the language.</span></span> <span data-ttu-id="4b5db-115">Если задано значение null или "" (пустая строка), используется текущая строка языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="4b5db-115">If the value is set to null or "" (empty string), the current locale string is used.</span></span> <span data-ttu-id="4b5db-116">В противном случае значение должно быть допустимой строкой языка RFC 1766, например "en-US".</span><span class="sxs-lookup"><span data-stu-id="4b5db-116">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b5db-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b5db-117">Return value</span></span>

<span data-ttu-id="4b5db-118">Этот метод возвращает **число** (**Long**), содержащее число атрибутов.</span><span class="sxs-lookup"><span data-stu-id="4b5db-118">This method returns a **Number** (**long**) containing the attribute count.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b5db-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b5db-119">Remarks</span></span>

<span data-ttu-id="4b5db-120">Этот метод используется для определения количества атрибутов, соответствующих определенному имени атрибута для данного объекта **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="4b5db-120">This method is used to determine the number of attributes corresponding to a particular attribute name for a given **Media** object.</span></span> <span data-ttu-id="4b5db-121">Номера индексов можно передать в метод **жетитеминфобитипе** .</span><span class="sxs-lookup"><span data-stu-id="4b5db-121">Index numbers can then be passed to the **getItemInfoByType** method.</span></span> <span data-ttu-id="4b5db-122">Это полезно, например, когда элемент мультимедиа был разбит на несколько жанров.</span><span class="sxs-lookup"><span data-stu-id="4b5db-122">This is useful, for example, when a media item has been categorized under multiple genres.</span></span>

<span data-ttu-id="4b5db-123">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="4b5db-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="4b5db-124">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="4b5db-124">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="4b5db-125">**Проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="4b5db-125">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b5db-126">Требования</span><span class="sxs-lookup"><span data-stu-id="4b5db-126">Requirements</span></span>



| <span data-ttu-id="4b5db-127">Требование</span><span class="sxs-lookup"><span data-stu-id="4b5db-127">Requirement</span></span> | <span data-ttu-id="4b5db-128">Значение</span><span class="sxs-lookup"><span data-stu-id="4b5db-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4b5db-129">Версия</span><span class="sxs-lookup"><span data-stu-id="4b5db-129">Version</span></span><br/> | <span data-ttu-id="4b5db-130">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="4b5db-130">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="4b5db-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4b5db-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="4b5db-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b5db-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b5db-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b5db-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b5db-134">**медиаобжект**</span><span class="sxs-lookup"><span data-stu-id="4b5db-134">**MediaObject**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="4b5db-135">**Media. Жетитеминфобитипе**</span><span class="sxs-lookup"><span data-stu-id="4b5db-135">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="4b5db-136">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="4b5db-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="4b5db-137">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="4b5db-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





