---
description: Представляет объект пера.
ms.assetid: c55945b7-59df-49b5-b25f-fa96056889fc
title: Интерфейс Итаблеткурсор
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: eecbebc7090fb57d3794f3d056c24fba61fa5c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913300"
---
# <a name="itabletcursor-interface"></a><span data-ttu-id="6ddf8-103">Интерфейс Итаблеткурсор</span><span class="sxs-lookup"><span data-stu-id="6ddf8-103">ITabletCursor interface</span></span>

<span data-ttu-id="6ddf8-104">Представляет объект пера.</span><span class="sxs-lookup"><span data-stu-id="6ddf8-104">Represents a stylus object.</span></span>

## <a name="members"></a><span data-ttu-id="6ddf8-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="6ddf8-105">Members</span></span>

<span data-ttu-id="6ddf8-106">Интерфейс **итаблеткурсор** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6ddf8-106">The **ITabletCursor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6ddf8-107">**Итаблеткурсор** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6ddf8-107">**ITabletCursor** also has these types of members:</span></span>

-   [<span data-ttu-id="6ddf8-108">Методы</span><span class="sxs-lookup"><span data-stu-id="6ddf8-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6ddf8-109">Методы</span><span class="sxs-lookup"><span data-stu-id="6ddf8-109">Methods</span></span>

<span data-ttu-id="6ddf8-110">Интерфейс **итаблеткурсор** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6ddf8-110">The **ITabletCursor** interface has these methods.</span></span>



| <span data-ttu-id="6ddf8-111">Метод</span><span class="sxs-lookup"><span data-stu-id="6ddf8-111">Method</span></span>                                                 | <span data-ttu-id="6ddf8-112">Описание</span><span class="sxs-lookup"><span data-stu-id="6ddf8-112">Description</span></span>                                                            |
|:-------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="6ddf8-113">**Кнопка**</span><span class="sxs-lookup"><span data-stu-id="6ddf8-113">**GetButton**</span></span>](itabletcursor-getbutton.md)           | <span data-ttu-id="6ddf8-114">Извлекает указанный объект кнопки из пера планшета.</span><span class="sxs-lookup"><span data-stu-id="6ddf8-114">Retrieves the specified button object from a tablet stylus.</span></span><br/> |
| [<span data-ttu-id="6ddf8-115">**жетбуттонкаунт**</span><span class="sxs-lookup"><span data-stu-id="6ddf8-115">**GetButtonCount**</span></span>](itabletcursor-getbuttoncount.md) | <span data-ttu-id="6ddf8-116">Получает количество кнопок пера планшета.</span><span class="sxs-lookup"><span data-stu-id="6ddf8-116">Retrieves the number of buttons on the tablet stylus.</span></span><br/>       |
| [<span data-ttu-id="6ddf8-117">**GetId**</span><span class="sxs-lookup"><span data-stu-id="6ddf8-117">**GetId**</span></span>](itabletcursor-getid.md)                   | <span data-ttu-id="6ddf8-118">Получает идентификатор пера.</span><span class="sxs-lookup"><span data-stu-id="6ddf8-118">Retrieves the stylus identifier.</span></span><br/>                            |
| [<span data-ttu-id="6ddf8-119">**GetName**</span><span class="sxs-lookup"><span data-stu-id="6ddf8-119">**GetName**</span></span>](itabletcursor-getname.md)               | <span data-ttu-id="6ddf8-120">Извлекает имя пера планшета.</span><span class="sxs-lookup"><span data-stu-id="6ddf8-120">Retrieves the name of the tablet stylus.</span></span><br/>                    |
| [<span data-ttu-id="6ddf8-121">**Инверсия**</span><span class="sxs-lookup"><span data-stu-id="6ddf8-121">**IsInverted**</span></span>](itabletcursor-isinverted.md)         | <span data-ttu-id="6ddf8-122">Указывает, является ли перо перевернутым.</span><span class="sxs-lookup"><span data-stu-id="6ddf8-122">Indicates if the stylus is upside down.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="6ddf8-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ddf8-123">Remarks</span></span>

<span data-ttu-id="6ddf8-124">Не следует использовать данный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="6ddf8-124">Do not use this interface.</span></span>

<span data-ttu-id="6ddf8-125">В следующем коде показано, как определяется интерфейс **итаблеткурсор** .</span><span class="sxs-lookup"><span data-stu-id="6ddf8-125">The following code describes how the **ITabletCursor** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(EF9953C6-B472-4B02-9D22-D0E247ADE0E8,
    pointer_default(unique)
]
interface ITabletCursor : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT IsInverted();

    HRESULT GetId(
        [out] CURSOR_ID *pCid);

    HRESULT GetTablet(
        [out] ITablet **ppTablet);

    HRESULT GetButtonCount(
        [out] ULONG *pcButtons);

    HRESULT GetButton(
        [in] ULONG iButton,
        [out] ITabletCursorButton **ppButton);
};

     
```

## <a name="requirements"></a><span data-ttu-id="6ddf8-126">Требования</span><span class="sxs-lookup"><span data-stu-id="6ddf8-126">Requirements</span></span>



| <span data-ttu-id="6ddf8-127">Требование</span><span class="sxs-lookup"><span data-stu-id="6ddf8-127">Requirement</span></span> | <span data-ttu-id="6ddf8-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6ddf8-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ddf8-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ddf8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6ddf8-130">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6ddf8-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6ddf8-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ddf8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6ddf8-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6ddf8-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6ddf8-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6ddf8-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="6ddf8-134"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ddf8-134"><dt>Wisptis.exe</dt></span></span> </dl> |



 

