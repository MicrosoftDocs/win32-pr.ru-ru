---
title: External. Либрарилокатионтипе
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | External. Либрарилокатионтипе
ms.assetid: aaf20147-8331-40bd-a5cd-5ee9b8e2d022
keywords:
- Внешний Либрарилокатионтипе проигрыватель Windows Media
topic_type:
- apiref
api_name:
- External.libraryLocationType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c2f14940a2ad41bed24493396e2bacfba2f0a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694501"
---
# <a name="externallibrarylocationtype"></a><span data-ttu-id="76564-105">External. Либрарилокатионтипе</span><span class="sxs-lookup"><span data-stu-id="76564-105">External.libraryLocationType</span></span>

> [!Note]  
> <span data-ttu-id="76564-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="76564-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="76564-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="76564-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="76564-108">Свойство **либрарилокатионтипе** извлекает [константу расположения библиотеки](library-location-constants.md) , которая указывает тип текущего представления в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="76564-108">The **libraryLocationType** property retrieves a [library location constant](library-location-constants.md) that indicates the type of the current view in Windows Media Player.</span></span>

``` syntax
window.external.libraryLocationType
      
```

## <a name="possible-values"></a><span data-ttu-id="76564-109">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="76564-109">Possible Values</span></span>

<span data-ttu-id="76564-110">Это свойство является **строкой** только для чтения, содержащей одну из констант расположения библиотеки.</span><span class="sxs-lookup"><span data-stu-id="76564-110">This property is a read-only **String** that contains one of the library location constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="76564-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76564-111">Remarks</span></span>

<span data-ttu-id="76564-112">Это свойство работает в сочетании со свойством [External. либрарилокатионид](external-librarylocationid.md) .</span><span class="sxs-lookup"><span data-stu-id="76564-112">This property works in combination with the [External.libraryLocationID](external-librarylocationid.md) property.</span></span> <span data-ttu-id="76564-113">Например, предположим, что **либрарилокатионтипе** равен кпалбумид, а **либрарилокатионид** равен 3.</span><span class="sxs-lookup"><span data-stu-id="76564-113">For example, suppose **libraryLocationType** is equal to CPAlbumID and **libraryLocationID** is equal to 3.</span></span> <span data-ttu-id="76564-114">Это означает, что в текущем представлении проигрывателя Windows Media отображается альбом с ИДЕНТИФИКАТОРом 3.</span><span class="sxs-lookup"><span data-stu-id="76564-114">That means the current view in Windows Media Player is showing the album that has an ID of 3.</span></span> <span data-ttu-id="76564-115">Дополнительные сведения о том, как Windows Media Player характеризует представления содержимого Интернет-магазина, см. в разделе [расположение и выбранный элемент](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="76564-115">For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76564-116">Требования</span><span class="sxs-lookup"><span data-stu-id="76564-116">Requirements</span></span>



| <span data-ttu-id="76564-117">Требование</span><span class="sxs-lookup"><span data-stu-id="76564-117">Requirement</span></span> | <span data-ttu-id="76564-118">Значение</span><span class="sxs-lookup"><span data-stu-id="76564-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76564-119">Версия</span><span class="sxs-lookup"><span data-stu-id="76564-119">Version</span></span><br/> | <span data-ttu-id="76564-120">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="76564-120">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="76564-121">DLL</span><span class="sxs-lookup"><span data-stu-id="76564-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="76564-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76564-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76564-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76564-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76564-124">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="76564-124">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="76564-125">**External. Либрарилокатионид**</span><span class="sxs-lookup"><span data-stu-id="76564-125">**External.libraryLocationID**</span></span>](external-librarylocationid.md)
</dt> <dt>

[<span data-ttu-id="76564-126">**Расположение и выбранный элемент**</span><span class="sxs-lookup"><span data-stu-id="76564-126">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





