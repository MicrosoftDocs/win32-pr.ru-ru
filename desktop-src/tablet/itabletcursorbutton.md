---
description: Представляет общие сведения о кнопке на устройстве пера.
ms.assetid: 20c9f8bb-8f8d-4469-baff-b9001c8adb3b
title: Интерфейс Итаблеткурсорбуттон
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c8f13e46699c1bea42bd8f8a7f78313aeba68aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346865"
---
# <a name="itabletcursorbutton-interface"></a><span data-ttu-id="c0642-103">Интерфейс Итаблеткурсорбуттон</span><span class="sxs-lookup"><span data-stu-id="c0642-103">ITabletCursorButton interface</span></span>

<span data-ttu-id="c0642-104">Представляет общие сведения о кнопке на устройстве пера.</span><span class="sxs-lookup"><span data-stu-id="c0642-104">Represents general information about a button on a stylus device.</span></span>

## <a name="members"></a><span data-ttu-id="c0642-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="c0642-105">Members</span></span>

<span data-ttu-id="c0642-106">Интерфейс **итаблеткурсорбуттон** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c0642-106">The **ITabletCursorButton** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c0642-107">**Итаблеткурсорбуттон** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c0642-107">**ITabletCursorButton** also has these types of members:</span></span>

-   [<span data-ttu-id="c0642-108">Методы</span><span class="sxs-lookup"><span data-stu-id="c0642-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c0642-109">Методы</span><span class="sxs-lookup"><span data-stu-id="c0642-109">Methods</span></span>

<span data-ttu-id="c0642-110">Интерфейс **итаблеткурсорбуттон** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c0642-110">The **ITabletCursorButton** interface has these methods.</span></span>



| <span data-ttu-id="c0642-111">Метод</span><span class="sxs-lookup"><span data-stu-id="c0642-111">Method</span></span>                                         | <span data-ttu-id="c0642-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c0642-112">Description</span></span>                                                      |
|:-----------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="c0642-113">**GetGuid**</span><span class="sxs-lookup"><span data-stu-id="c0642-113">**GetGuid**</span></span>](itabletcursorbutton-getguid.md) | <span data-ttu-id="c0642-114">Извлекает уникальный идентификатор кнопки пера.</span><span class="sxs-lookup"><span data-stu-id="c0642-114">Retrieves the unique identifier of the stylus button.</span></span><br/> |
| [<span data-ttu-id="c0642-115">**GetName**</span><span class="sxs-lookup"><span data-stu-id="c0642-115">**GetName**</span></span>](itabletcursorbutton-getname.md) | <span data-ttu-id="c0642-116">Возвращает имя кнопки пера.</span><span class="sxs-lookup"><span data-stu-id="c0642-116">Retrieves the name of the stylus button.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="c0642-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0642-117">Remarks</span></span>

<span data-ttu-id="c0642-118">Разработчики не должны использовать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c0642-118">Developers should not use this interface.</span></span>

<span data-ttu-id="c0642-119">В следующем коде показано, как определяется интерфейс **итаблеткурсорбуттон** .</span><span class="sxs-lookup"><span data-stu-id="c0642-119">The following code shows how the **ITabletCursorButton** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(997A992E-8B6C-4945-BC17-A1EE563B3AB7),
    pointer_default(unique)
]
interface ITabletCursorButton : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetGuid(
        [out] GUID *pguidBtn);
};
```

## <a name="requirements"></a><span data-ttu-id="c0642-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c0642-120">Requirements</span></span>



| <span data-ttu-id="c0642-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c0642-121">Requirement</span></span> | <span data-ttu-id="c0642-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c0642-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0642-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0642-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c0642-124">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c0642-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c0642-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0642-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c0642-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c0642-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c0642-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c0642-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="c0642-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c0642-128"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0642-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0642-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0642-130">**Интерфейс Итаблеткурсорбуттон**</span><span class="sxs-lookup"><span data-stu-id="c0642-130">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

