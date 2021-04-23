---
title: Метод списка воспроизведения. Сетитеминфо
description: Метод Сетитеминфо задает значение атрибута списка воспроизведения.
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- Сетитеминфо метод Windows Media Player
- Сетитеминфо метод Windows Media Player, класс списка воспроизведения
- Класс списка воспроизведения проигрыватель Windows Media Player, метод Сетитеминфо
topic_type:
- apiref
api_name:
- Playlist.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff42e56e549100044db0881bb38ade5f2f1711a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708616"
---
# <a name="playlistsetiteminfo-method"></a><span data-ttu-id="1cff0-106">Метод списка воспроизведения. Сетитеминфо</span><span class="sxs-lookup"><span data-stu-id="1cff0-106">Playlist.setItemInfo method</span></span>

<span data-ttu-id="1cff0-107">Метод **сетитеминфо** задает значение атрибута списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="1cff0-107">The **setItemInfo** method specifies the value of a playlist attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cff0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1cff0-108">Syntax</span></span>


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="1cff0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1cff0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cff0-110">*имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1cff0-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cff0-111">**Строка** , содержащая имя атрибута, который необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="1cff0-111">**String** containing the name of the attribute to be set.</span></span> <span data-ttu-id="1cff0-112">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1cff0-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="1cff0-113">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1cff0-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cff0-114">**Строка** , содержащая новое значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="1cff0-114">**String** containing the new value for the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cff0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1cff0-115">Return value</span></span>

<span data-ttu-id="1cff0-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1cff0-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cff0-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1cff0-117">Remarks</span></span>

<span data-ttu-id="1cff0-118">Особое использование метода **сетитеминфо** заключается в сортировке элементов списка воспроизведения с помощью атрибута SortAttribute.</span><span class="sxs-lookup"><span data-stu-id="1cff0-118">A special use of the **setItemInfo** method is to sort the items in the playlist by using the SortAttribute attribute.</span></span> <span data-ttu-id="1cff0-119">В следующем примере в JScript выполняется сортировка списка воспроизведения по значениям атрибута Усерластплайедтиме.</span><span class="sxs-lookup"><span data-stu-id="1cff0-119">The following JScript example sorts a playlist by the values of the UserLastPlayedTime attribute.</span></span> <span data-ttu-id="1cff0-120">Список воспроизведения переменных является ссылкой на объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="1cff0-120">The variable playlist is a reference to a **Playlist** object.</span></span>


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



<span data-ttu-id="1cff0-121">Чтобы использовать этот метод, требуется полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="1cff0-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="1cff0-122">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1cff0-122">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="1cff0-123">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1cff0-123">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="1cff0-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="1cff0-124">Examples</span></span>

<span data-ttu-id="1cff0-125">Пример кода, в котором используется это свойство, см. в свойстве [аттрибутекаунт](playlist-attributecount.md) .</span><span class="sxs-lookup"><span data-stu-id="1cff0-125">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cff0-126">Требования</span><span class="sxs-lookup"><span data-stu-id="1cff0-126">Requirements</span></span>



| <span data-ttu-id="1cff0-127">Требование</span><span class="sxs-lookup"><span data-stu-id="1cff0-127">Requirement</span></span> | <span data-ttu-id="1cff0-128">Значение</span><span class="sxs-lookup"><span data-stu-id="1cff0-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1cff0-129">Версия</span><span class="sxs-lookup"><span data-stu-id="1cff0-129">Version</span></span><br/> | <span data-ttu-id="1cff0-130">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="1cff0-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1cff0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1cff0-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="1cff0-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cff0-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cff0-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1cff0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cff0-134">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="1cff0-134">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="1cff0-135">**Список воспроизведения. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="1cff0-135">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="1cff0-136">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="1cff0-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="1cff0-137">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="1cff0-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





