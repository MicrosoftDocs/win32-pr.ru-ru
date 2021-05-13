---
description: Расширяет объект IShellDispatch4.
title: Объект IShellDispatch5 (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch5
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9170340a-0f11-4ec9-877d-fb7fef9888b2
ms.openlocfilehash: 26c3112faa748aa443526fbe9cb493af67502cd7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843005"
---
# <a name="ishelldispatch5-object"></a><span data-ttu-id="263ee-103">Объект IShellDispatch5</span><span class="sxs-lookup"><span data-stu-id="263ee-103">IShellDispatch5 object</span></span>

<span data-ttu-id="263ee-104">Расширяет объект [**IShellDispatch4**](ishelldispatch4.md) .</span><span class="sxs-lookup"><span data-stu-id="263ee-104">Extends the [**IShellDispatch4**](ishelldispatch4.md) object.</span></span> <span data-ttu-id="263ee-105">В дополнение к свойствам и методам, поддерживаемым **IShellDispatch4**, **IShellDispatch5** добавляет метод, который отображает открытые окна в трехмерном стеке.</span><span class="sxs-lookup"><span data-stu-id="263ee-105">In addition to the properties and methods supported by **IShellDispatch4**, **IShellDispatch5** adds a method that displays open windows in a 3D stack.</span></span>

> [!Note]  
> <span data-ttu-id="263ee-106">**IShellDispatch5** реализован и доступен через объект [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="263ee-106">**IShellDispatch5** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="263ee-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="263ee-107">Members</span></span>

<span data-ttu-id="263ee-108">Объект **IShellDispatch5** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="263ee-108">The **IShellDispatch5** object has these types of members:</span></span>

-   [<span data-ttu-id="263ee-109">Методы</span><span class="sxs-lookup"><span data-stu-id="263ee-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="263ee-110">Методы</span><span class="sxs-lookup"><span data-stu-id="263ee-110">Methods</span></span>

<span data-ttu-id="263ee-111">Объект **IShellDispatch5** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="263ee-111">The **IShellDispatch5** object has these methods.</span></span>



| <span data-ttu-id="263ee-112">Метод</span><span class="sxs-lookup"><span data-stu-id="263ee-112">Method</span></span>                                                   | <span data-ttu-id="263ee-113">Описание</span><span class="sxs-lookup"><span data-stu-id="263ee-113">Description</span></span>                                                                    |
|:---------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="263ee-114">**виндовсвитчер**</span><span class="sxs-lookup"><span data-stu-id="263ee-114">**WindowSwitcher**</span></span>](ishelldispatch5-windowswitcher.md) | <span data-ttu-id="263ee-115">Отображает открытые окна в трехмерном стеке, который можно переворачивать.</span><span class="sxs-lookup"><span data-stu-id="263ee-115">Displays your open windows in a 3D stack that you can flip through.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="263ee-116">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="263ee-116">Requirements</span></span>



| <span data-ttu-id="263ee-117">Требование</span><span class="sxs-lookup"><span data-stu-id="263ee-117">Requirement</span></span> | <span data-ttu-id="263ee-118">Значение</span><span class="sxs-lookup"><span data-stu-id="263ee-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="263ee-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="263ee-119">Minimum supported client</span></span><br/> | <span data-ttu-id="263ee-120">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="263ee-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="263ee-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="263ee-121">Minimum supported server</span></span><br/> | <span data-ttu-id="263ee-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="263ee-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="263ee-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="263ee-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="263ee-124"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="263ee-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="263ee-125">IDL</span><span class="sxs-lookup"><span data-stu-id="263ee-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="263ee-126"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="263ee-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="263ee-127">DLL</span><span class="sxs-lookup"><span data-stu-id="263ee-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="263ee-128"><dt>Shell32.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="263ee-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="263ee-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="263ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="263ee-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="263ee-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="263ee-131">**Объект оболочки**</span><span class="sxs-lookup"><span data-stu-id="263ee-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="263ee-132">**ишеллдиспатч**</span><span class="sxs-lookup"><span data-stu-id="263ee-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="263ee-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="263ee-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="263ee-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="263ee-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="263ee-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="263ee-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> </dl>

 

 
