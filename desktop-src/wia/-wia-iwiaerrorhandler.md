---
description: Интерфейс Ивиаеррорхандлер предоставляет методы для обработки ошибок, которые могут возникнуть, когда приложение запрашивает данные изображения, как для предварительной версии, так и для конечных битов.
ms.assetid: 33d8ccc5-6856-4a54-b1f0-d015933d63ab
title: Интерфейс Ивиаеррорхандлер (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7b3ea9f5556f1f919336e4abb4085f9e0c32d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154858"
---
# <a name="iwiaerrorhandler-interface"></a><span data-ttu-id="5096e-103">Интерфейс Ивиаеррорхандлер</span><span class="sxs-lookup"><span data-stu-id="5096e-103">IWiaErrorHandler interface</span></span>

<span data-ttu-id="5096e-104">Интерфейс **ивиаеррорхандлер** предоставляет методы для обработки ошибок, которые могут возникнуть, когда приложение запрашивает данные изображения, как для предварительной версии, так и для конечных битов.</span><span class="sxs-lookup"><span data-stu-id="5096e-104">The **IWiaErrorHandler** interface provides methods to handle errors that may occur when an application requests image data, whether for preview or final bits.</span></span>

## <a name="members"></a><span data-ttu-id="5096e-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="5096e-105">Members</span></span>

<span data-ttu-id="5096e-106">Интерфейс **ивиаеррорхандлер** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5096e-106">The **IWiaErrorHandler** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5096e-107">**Ивиаеррорхандлер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5096e-107">**IWiaErrorHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="5096e-108">Методы</span><span class="sxs-lookup"><span data-stu-id="5096e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5096e-109">Методы</span><span class="sxs-lookup"><span data-stu-id="5096e-109">Methods</span></span>

<span data-ttu-id="5096e-110">Интерфейс **ивиаеррорхандлер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5096e-110">The **IWiaErrorHandler** interface has these methods.</span></span>



| <span data-ttu-id="5096e-111">Метод</span><span class="sxs-lookup"><span data-stu-id="5096e-111">Method</span></span>                                                                     | <span data-ttu-id="5096e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5096e-112">Description</span></span>                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5096e-113">**жетстатусдескриптион**</span><span class="sxs-lookup"><span data-stu-id="5096e-113">**GetStatusDescription**</span></span>](-wia-iwiaerrorhandler-getstatusdescription.md) | <span data-ttu-id="5096e-114">Возвращает строку, описывающую код состояния.</span><span class="sxs-lookup"><span data-stu-id="5096e-114">Returns a string that describes the status code.</span></span><br/>                                             |
| [<span data-ttu-id="5096e-115">**репортстатус**</span><span class="sxs-lookup"><span data-stu-id="5096e-115">**ReportStatus**</span></span>](-wia-iwiaerrorhandler-reportstatus.md)                 | <span data-ttu-id="5096e-116">Обрабатывает сообщения о состоянии и ошибках во время передачи данных изображения и отображает их пользователю.</span><span class="sxs-lookup"><span data-stu-id="5096e-116">Handles status and error messages during image data transfers and displays them to the user.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5096e-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5096e-117">Remarks</span></span>

<span data-ttu-id="5096e-118">Объект обратного вызова приложения может реализовывать **ивиаеррорхандлер**.</span><span class="sxs-lookup"><span data-stu-id="5096e-118">The application callback object can implement **IWiaErrorHandler**.</span></span>

<span data-ttu-id="5096e-119">Этот интерфейс не предназначен для работы с ошибками, возникшими за пределами передачи данных изображения, например с ошибками при получении или установке свойств устройства или невозвращенных обратных вызовов в драйвер.</span><span class="sxs-lookup"><span data-stu-id="5096e-119">This interface is not designed to handle errors encountered outside of image data transfers, for example, errors in getting or setting device properties or unreturned callbacks into a driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="5096e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="5096e-120">Requirements</span></span>



| <span data-ttu-id="5096e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="5096e-121">Requirement</span></span> | <span data-ttu-id="5096e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="5096e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5096e-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5096e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5096e-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5096e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5096e-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5096e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5096e-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5096e-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5096e-127">Header</span><span class="sxs-lookup"><span data-stu-id="5096e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5096e-128"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5096e-128"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="5096e-129">IDL</span><span class="sxs-lookup"><span data-stu-id="5096e-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5096e-130"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5096e-130"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="5096e-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5096e-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="5096e-132"><dt>Виагуид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5096e-132"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
