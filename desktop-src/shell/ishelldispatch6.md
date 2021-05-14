---
description: Расширяет объект IShellDispatch5.
title: Объект IShellDispatch6 (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch6
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 540A5CFD-1520-4B61-B461-E893EFA27115
ms.openlocfilehash: de27322324dc8a25bdc679374e625f94a1d1a2ae
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843035"
---
# <a name="ishelldispatch6-object"></a><span data-ttu-id="29d4c-103">Объект IShellDispatch6</span><span class="sxs-lookup"><span data-stu-id="29d4c-103">IShellDispatch6 object</span></span>

<span data-ttu-id="29d4c-104">Расширяет объект [**IShellDispatch5**](ishelldispatch5.md) .</span><span class="sxs-lookup"><span data-stu-id="29d4c-104">Extends the [**IShellDispatch5**](ishelldispatch5.md) object.</span></span> <span data-ttu-id="29d4c-105">В дополнение к свойствам и методам, поддерживаемым **IShellDispatch5**, **IShellDispatch6** добавляет метод, отображающий панель поиска приложений.</span><span class="sxs-lookup"><span data-stu-id="29d4c-105">In addition to the properties and methods supported by **IShellDispatch5**, **IShellDispatch6** adds a method that displays the Apps Search pane.</span></span>

> [!Note]  
> <span data-ttu-id="29d4c-106">**IShellDispatch6** реализован и доступен через объект [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="29d4c-106">**IShellDispatch6** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="29d4c-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="29d4c-107">Members</span></span>

<span data-ttu-id="29d4c-108">Объект **IShellDispatch6** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="29d4c-108">The **IShellDispatch6** object has these types of members:</span></span>

-   [<span data-ttu-id="29d4c-109">Методы</span><span class="sxs-lookup"><span data-stu-id="29d4c-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="29d4c-110">Методы</span><span class="sxs-lookup"><span data-stu-id="29d4c-110">Methods</span></span>

<span data-ttu-id="29d4c-111">Объект **IShellDispatch6** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="29d4c-111">The **IShellDispatch6** object has these methods.</span></span>



| <span data-ttu-id="29d4c-112">Метод</span><span class="sxs-lookup"><span data-stu-id="29d4c-112">Method</span></span>                                                 | <span data-ttu-id="29d4c-113">Описание</span><span class="sxs-lookup"><span data-stu-id="29d4c-113">Description</span></span>                                                                                                                  |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29d4c-114">**сеарчкомманд**</span><span class="sxs-lookup"><span data-stu-id="29d4c-114">**SearchCommand**</span></span>](ishelldispatch6-searchcommand.md) | <span data-ttu-id="29d4c-115">Отображает панель поиска приложений, которая обычно появляется при вводе условия поиска с начального экрана.</span><span class="sxs-lookup"><span data-stu-id="29d4c-115">Displays the Apps Search pane, which normally appears when you begin to type a search term from the Start screen.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="29d4c-116">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="29d4c-116">Requirements</span></span>



| <span data-ttu-id="29d4c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="29d4c-117">Requirement</span></span> | <span data-ttu-id="29d4c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="29d4c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29d4c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29d4c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="29d4c-120">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="29d4c-120">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="29d4c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29d4c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="29d4c-122">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="29d4c-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="29d4c-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="29d4c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="29d4c-124"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="29d4c-124"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="29d4c-125">IDL</span><span class="sxs-lookup"><span data-stu-id="29d4c-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="29d4c-126"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="29d4c-126"><dt>Shldisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="29d4c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="29d4c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29d4c-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29d4c-128"><dt>Shell32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29d4c-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29d4c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29d4c-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="29d4c-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="29d4c-131">**Объект оболочки**</span><span class="sxs-lookup"><span data-stu-id="29d4c-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="29d4c-132">**ишеллдиспатч**</span><span class="sxs-lookup"><span data-stu-id="29d4c-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="29d4c-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="29d4c-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="29d4c-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="29d4c-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="29d4c-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="29d4c-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> <dt>

[<span data-ttu-id="29d4c-136">**IShellDispatch5**</span><span class="sxs-lookup"><span data-stu-id="29d4c-136">**IShellDispatch5**</span></span>](ishelldispatch5.md)
</dt> </dl>

 

 
