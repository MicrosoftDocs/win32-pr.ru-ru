---
title: Метод Settings. Рекуестмедиаакцессригхтс
description: Метод Рекуестмедиаакцессригхтс запрашивает указанный уровень доступа к библиотеке. | Метод Settings. Рекуестмедиаакцессригхтс
ms.assetid: 076b749b-9b25-483c-aa1f-60fc4367e4e0
keywords:
- Рекуестмедиаакцессригхтс метод Windows Media Player
- Рекуестмедиаакцессригхтс метод Windows Media Player, класс Settings
- Класс параметров проигрыватель Windows Media Player, метод Рекуестмедиаакцессригхтс
topic_type:
- apiref
api_name:
- Settings.requestMediaAccessRights
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abfeed45666ee1f63bf995b211030b0b840c4279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651844"
---
# <a name="settingsrequestmediaaccessrights-method"></a><span data-ttu-id="666d3-107">Метод Settings. Рекуестмедиаакцессригхтс</span><span class="sxs-lookup"><span data-stu-id="666d3-107">Settings.requestMediaAccessRights method</span></span>

<span data-ttu-id="666d3-108">Метод **рекуестмедиаакцессригхтс** запрашивает указанный уровень доступа к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="666d3-108">The **requestMediaAccessRights** method requests a specified level of access to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="666d3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="666d3-109">Syntax</span></span>


```JScript
bRetVal = Settings.requestMediaAccessRights(
  access
)
```



## <a name="parameters"></a><span data-ttu-id="666d3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="666d3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="666d3-111">*доступ к* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="666d3-111">*access* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="666d3-112">**Строка** , указывающая требуемый уровень прав доступа.</span><span class="sxs-lookup"><span data-stu-id="666d3-112">**String** specifying the desired access rights level.</span></span> <span data-ttu-id="666d3-113">Содержит одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="666d3-113">Contains one of the following values.</span></span>



| <span data-ttu-id="666d3-114">Строка</span><span class="sxs-lookup"><span data-stu-id="666d3-114">String</span></span> | <span data-ttu-id="666d3-115">Описание</span><span class="sxs-lookup"><span data-stu-id="666d3-115">Description</span></span>                      |
|--------|----------------------------------|
| <span data-ttu-id="666d3-116">нет</span><span class="sxs-lookup"><span data-stu-id="666d3-116">none</span></span>   | <span data-ttu-id="666d3-117">Только права доступа к текущему элементу.</span><span class="sxs-lookup"><span data-stu-id="666d3-117">Current item access rights only.</span></span> |
| <span data-ttu-id="666d3-118">read</span><span class="sxs-lookup"><span data-stu-id="666d3-118">read</span></span>   | <span data-ttu-id="666d3-119">Права доступа только для чтения.</span><span class="sxs-lookup"><span data-stu-id="666d3-119">Read access rights only.</span></span>         |
| <span data-ttu-id="666d3-120">переполненные</span><span class="sxs-lookup"><span data-stu-id="666d3-120">full</span></span>   | <span data-ttu-id="666d3-121">Права доступа для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="666d3-121">Read/Write access rights.</span></span>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="666d3-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="666d3-122">Return value</span></span>

<span data-ttu-id="666d3-123">Этот метод возвращает **логическое** значение, указывающее, были ли предоставлены запрошенные права доступа.</span><span class="sxs-lookup"><span data-stu-id="666d3-123">This method returns a **Boolean** value indicating whether the requested access rights were granted.</span></span>

## <a name="remarks"></a><span data-ttu-id="666d3-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="666d3-124">Remarks</span></span>

<span data-ttu-id="666d3-125">Веб-страница должна сначала запросить у пользователя разрешение на чтение информации из библиотеки или запись данных в нее.</span><span class="sxs-lookup"><span data-stu-id="666d3-125">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="666d3-126">При вызове этого метода пользователю предлагается диалоговое окно, запрашивающее указанный уровень разрешений.</span><span class="sxs-lookup"><span data-stu-id="666d3-126">Invoking this method prompts the user with a dialog box that requests the specified permission level.</span></span> <span data-ttu-id="666d3-127">Это означает, что определенные методы, свойства и события будут недоступны из кода, если соответствующие права доступа не были предоставлены.</span><span class="sxs-lookup"><span data-stu-id="666d3-127">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="666d3-128">Текущий уровень прав доступа можно получить с помощью *параметров*. **медиаакцессригхтс**.</span><span class="sxs-lookup"><span data-stu-id="666d3-128">The current access rights level can be retrieved using *Settings*.**mediaAccessRights**.</span></span>

<span data-ttu-id="666d3-129">**Проигрыватель Windows Media 10 Mobile**: Этот метод всегда возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="666d3-129">**Windows Media Player 10 Mobile**: This method always returns **true**.</span></span>

## <a name="requirements"></a><span data-ttu-id="666d3-130">Требования</span><span class="sxs-lookup"><span data-stu-id="666d3-130">Requirements</span></span>



| <span data-ttu-id="666d3-131">Требование</span><span class="sxs-lookup"><span data-stu-id="666d3-131">Requirement</span></span> | <span data-ttu-id="666d3-132">Значение</span><span class="sxs-lookup"><span data-stu-id="666d3-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="666d3-133">Версия</span><span class="sxs-lookup"><span data-stu-id="666d3-133">Version</span></span><br/> | <span data-ttu-id="666d3-134">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="666d3-134">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="666d3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="666d3-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="666d3-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="666d3-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="666d3-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="666d3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="666d3-138">**Объект параметров**</span><span class="sxs-lookup"><span data-stu-id="666d3-138">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="666d3-139">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="666d3-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> </dl>

 

 





