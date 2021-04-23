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
ms.openlocfilehash: cbf3e960d7bfb9cd15411142cc036a21a9995ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984644"
---
# <a name="ishelldispatch5-object"></a><span data-ttu-id="c600a-103">Объект IShellDispatch5</span><span class="sxs-lookup"><span data-stu-id="c600a-103">IShellDispatch5 object</span></span>

<span data-ttu-id="c600a-104">Расширяет объект [**IShellDispatch4**](ishelldispatch4.md) .</span><span class="sxs-lookup"><span data-stu-id="c600a-104">Extends the [**IShellDispatch4**](ishelldispatch4.md) object.</span></span> <span data-ttu-id="c600a-105">В дополнение к свойствам и методам, поддерживаемым **IShellDispatch4**, **IShellDispatch5** добавляет метод, который отображает открытые окна в трехмерном стеке.</span><span class="sxs-lookup"><span data-stu-id="c600a-105">In addition to the properties and methods supported by **IShellDispatch4**, **IShellDispatch5** adds a method that displays open windows in a 3D stack.</span></span>

> [!Note]  
> <span data-ttu-id="c600a-106">**IShellDispatch5** реализован и доступен через объект [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="c600a-106">**IShellDispatch5** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="c600a-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="c600a-107">Members</span></span>

<span data-ttu-id="c600a-108">Объект **IShellDispatch5** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c600a-108">The **IShellDispatch5** object has these types of members:</span></span>

-   [<span data-ttu-id="c600a-109">Методы</span><span class="sxs-lookup"><span data-stu-id="c600a-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c600a-110">Методы</span><span class="sxs-lookup"><span data-stu-id="c600a-110">Methods</span></span>

<span data-ttu-id="c600a-111">Объект **IShellDispatch5** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="c600a-111">The **IShellDispatch5** object has these methods.</span></span>



| <span data-ttu-id="c600a-112">Метод</span><span class="sxs-lookup"><span data-stu-id="c600a-112">Method</span></span>                                                   | <span data-ttu-id="c600a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c600a-113">Description</span></span>                                                                    |
|:---------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="c600a-114">**виндовсвитчер**</span><span class="sxs-lookup"><span data-stu-id="c600a-114">**WindowSwitcher**</span></span>](ishelldispatch5-windowswitcher.md) | <span data-ttu-id="c600a-115">Отображает открытые окна в трехмерном стеке, который можно переворачивать.</span><span class="sxs-lookup"><span data-stu-id="c600a-115">Displays your open windows in a 3D stack that you can flip through.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c600a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c600a-116">Requirements</span></span>



| <span data-ttu-id="c600a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c600a-117">Requirement</span></span> | <span data-ttu-id="c600a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c600a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c600a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c600a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c600a-120">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c600a-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="c600a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c600a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c600a-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c600a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c600a-123">Header</span><span class="sxs-lookup"><span data-stu-id="c600a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c600a-124"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c600a-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c600a-125">IDL</span><span class="sxs-lookup"><span data-stu-id="c600a-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c600a-126"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c600a-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c600a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c600a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c600a-128"><dt>Shell32.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="c600a-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c600a-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c600a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c600a-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="c600a-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="c600a-131">**Объект оболочки**</span><span class="sxs-lookup"><span data-stu-id="c600a-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="c600a-132">**ишеллдиспатч**</span><span class="sxs-lookup"><span data-stu-id="c600a-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="c600a-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="c600a-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="c600a-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="c600a-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="c600a-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="c600a-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> </dl>

 

 
