---
description: Интерфейс Исканпрофилеуи позволяет приложениям отображать диалоговое окно, чтобы пользователи могли создавать, изменять и удалять профили сканирования.
ms.assetid: d0c7edcc-00d8-49b2-a0f7-fe4bbba90bfb
title: Интерфейс Исканпрофилеуи (Сканпрофилеуи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: c8791461db76c72de81216aef188886f63fde4f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711254"
---
# <a name="iscanprofileui-interface"></a><span data-ttu-id="2c522-103">Интерфейс Исканпрофилеуи</span><span class="sxs-lookup"><span data-stu-id="2c522-103">IScanProfileUI interface</span></span>

<span data-ttu-id="2c522-104">Интерфейс **исканпрофилеуи** позволяет приложениям отображать диалоговое окно, чтобы пользователи могли создавать, изменять и удалять профили сканирования.</span><span class="sxs-lookup"><span data-stu-id="2c522-104">The **IScanProfileUI** interface enables applications to display a dialog box so that users can create, modify, and delete scan profiles.</span></span>

## <a name="members"></a><span data-ttu-id="2c522-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="2c522-105">Members</span></span>

<span data-ttu-id="2c522-106">Интерфейс **исканпрофилеуи** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="2c522-106">The **IScanProfileUI** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="2c522-107">**Исканпрофилеуи** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2c522-107">**IScanProfileUI** also has these types of members:</span></span>

-   [<span data-ttu-id="2c522-108">Методы</span><span class="sxs-lookup"><span data-stu-id="2c522-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2c522-109">Методы</span><span class="sxs-lookup"><span data-stu-id="2c522-109">Methods</span></span>

<span data-ttu-id="2c522-110">Интерфейс **исканпрофилеуи** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2c522-110">The **IScanProfileUI** interface has these methods.</span></span>



| <span data-ttu-id="2c522-111">Метод</span><span class="sxs-lookup"><span data-stu-id="2c522-111">Method</span></span>                                                             | <span data-ttu-id="2c522-112">Описание</span><span class="sxs-lookup"><span data-stu-id="2c522-112">Description</span></span>                                                                                      |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c522-113">**сканпрофиледиалог**</span><span class="sxs-lookup"><span data-stu-id="2c522-113">**ScanProfileDialog**</span></span>](-wia-iscanprofileui-scanprofiledialog.md) | <span data-ttu-id="2c522-114">Отображает диалоговое окно, позволяющее пользователям создавать, изменять и удалять профили сканирования.</span><span class="sxs-lookup"><span data-stu-id="2c522-114">Displays a dialog box that enables users to create, modify, and delete scan profiles.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2c522-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c522-115">Remarks</span></span>

<span data-ttu-id="2c522-116">Диалоговое окно является модальным; пользователь не может переключиться на родительское окно, пока диалоговое окно не закроется.</span><span class="sxs-lookup"><span data-stu-id="2c522-116">The dialog box is modal; the user cannot switch to the parent window until the dialog box closes.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c522-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2c522-117">Requirements</span></span>



| <span data-ttu-id="2c522-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2c522-118">Requirement</span></span> | <span data-ttu-id="2c522-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2c522-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c522-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c522-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2c522-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c522-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="2c522-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c522-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2c522-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2c522-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c522-124">Header</span><span class="sxs-lookup"><span data-stu-id="2c522-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c522-125"><dt>Сканпрофилеуи. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c522-125"><dt>Scanprofileui.h</dt></span></span> </dl>  |
| <span data-ttu-id="2c522-126">IDL</span><span class="sxs-lookup"><span data-stu-id="2c522-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2c522-127"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2c522-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c522-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c522-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c522-129">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="2c522-129">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="2c522-130">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="2c522-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
