---
description: Интерфейс Ивиаапперрорхандлер позволяет приложениям отображать окна ошибок (во время передачи данных), из которых пользователь может выбрать, следует ли продолжить, отменить или прервать передачу.
ms.assetid: ac2597e6-2857-4694-bea7-1ea65d63b365
title: Интерфейс Ивиаапперрорхандлер (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6ccac7b689055bfaab926a8db46b4632606811d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719518"
---
# <a name="iwiaapperrorhandler-interface"></a><span data-ttu-id="35143-103">Интерфейс Ивиаапперрорхандлер</span><span class="sxs-lookup"><span data-stu-id="35143-103">IWiaAppErrorHandler interface</span></span>

<span data-ttu-id="35143-104">Интерфейс **ивиаапперрорхандлер** позволяет приложениям отображать окна ошибок (во время передачи данных), из которых пользователь может выбрать, следует ли продолжить, отменить или прервать передачу.</span><span class="sxs-lookup"><span data-stu-id="35143-104">The **IWiaAppErrorHandler** interface enables applications to display error windows (during data transfers) from which the user can choose whether to continue, cancel, or abort the transfer.</span></span>

## <a name="members"></a><span data-ttu-id="35143-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="35143-105">Members</span></span>

<span data-ttu-id="35143-106">Интерфейс **ивиаапперрорхандлер** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="35143-106">The **IWiaAppErrorHandler** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="35143-107">**Ивиаапперрорхандлер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="35143-107">**IWiaAppErrorHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="35143-108">Методы</span><span class="sxs-lookup"><span data-stu-id="35143-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="35143-109">Методы</span><span class="sxs-lookup"><span data-stu-id="35143-109">Methods</span></span>

<span data-ttu-id="35143-110">Интерфейс **ивиаапперрорхандлер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="35143-110">The **IWiaAppErrorHandler** interface has these methods.</span></span>



| <span data-ttu-id="35143-111">Метод</span><span class="sxs-lookup"><span data-stu-id="35143-111">Method</span></span>                                                        | <span data-ttu-id="35143-112">Описание</span><span class="sxs-lookup"><span data-stu-id="35143-112">Description</span></span>                                                                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35143-113">**Окно**</span><span class="sxs-lookup"><span data-stu-id="35143-113">**GetWindow**</span></span>](-wia-iwiaapperrorhandler-getwindow.md)       | <span data-ttu-id="35143-114">Получает обработчик для диалогового окна, отображающего сообщения об ошибках, и предоставляет одну или несколько кнопок для продолжения, отмены или прерывания работы приложения.</span><span class="sxs-lookup"><span data-stu-id="35143-114">Gets a handle to the dialog box that displays error messages and provides one or more buttons to continue, cancel, or abort the application.</span></span><br/> |
| [<span data-ttu-id="35143-115">**репортстатус**</span><span class="sxs-lookup"><span data-stu-id="35143-115">**ReportStatus**</span></span>](-wia-iwiaapperrorhandler-reportstatus.md) | <span data-ttu-id="35143-116">Обрабатывает состояние устройства и сообщения об ошибках во время передачи данных изображения и отображает сообщения для пользователя.</span><span class="sxs-lookup"><span data-stu-id="35143-116">Handles device status and error messages during image data transfers and displays the messages to the user.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="35143-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35143-117">Remarks</span></span>

<span data-ttu-id="35143-118">Обработка ошибок или обратный вызов, объект, реализующий этот интерфейс, передается в [**ивиатрансфер::D гружать**](-wia-iwiatransfer-download.md) и [**Ивиатрансфер:: upload**](-wia-iwiatransfer-upload.md).</span><span class="sxs-lookup"><span data-stu-id="35143-118">The error handling, or callback, object that implements this interface is passed into [**IWiaTransfer::Download**](-wia-iwiatransfer-download.md) and [**IWiaTransfer::Upload**](-wia-iwiatransfer-upload.md).</span></span>

<span data-ttu-id="35143-119">Этот интерфейс не предназначен для работы с ошибками, возникшими за пределами передачи данных изображения, например с ошибками при получении или установке свойств устройства или невозвращенных обратных вызовов в драйвер.</span><span class="sxs-lookup"><span data-stu-id="35143-119">This interface is not designed to handle errors encountered outside of image data transfers, for example, errors in getting or setting device properties or unreturned callbacks into a driver.</span></span>

<span data-ttu-id="35143-120">Обработчик ошибок драйвера должен реализовывать [**ивиаеррорхандлер**](-wia-iwiaerrorhandler.md), а не **ивиаапперрорхандлер**.</span><span class="sxs-lookup"><span data-stu-id="35143-120">A driver error handler should implement [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md), instead of **IWiaAppErrorHandler**.</span></span>

<span data-ttu-id="35143-121">Объект, реализующий этот интерфейс, также должен реализовывать [**ивиатрансферкаллбакк**](-wia-iwiatransfercallback.md).</span><span class="sxs-lookup"><span data-stu-id="35143-121">The object that implements this interface should also implement [**IWiaTransferCallback**](-wia-iwiatransfercallback.md).</span></span>

<span data-ttu-id="35143-122">Если необходимо, чтобы обработчик ошибок драйвера и обработчик ошибок по умолчанию отображали окна сообщений об ошибках, но не нужно создавать полный обработчик ошибок для приложения, реализуйте этот интерфейс, а также реализуйте метод [**ивиаапперрорхандлер:: репортстатус**](-wia-iwiaapperrorhandler-reportstatus.md) , чтобы вернуть \_ состояние WIA \_ не \_ обработано.</span><span class="sxs-lookup"><span data-stu-id="35143-122">If you want a driver error handler and default error handler to display error message windows, but you do not want to create a complete error handler for the application, implement this interface and also implement the [**IWiaAppErrorHandler::ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) method to return WIA\_STATUS\_NOT\_HANDLED.</span></span>

## <a name="requirements"></a><span data-ttu-id="35143-123">Требования</span><span class="sxs-lookup"><span data-stu-id="35143-123">Requirements</span></span>



| <span data-ttu-id="35143-124">Требование</span><span class="sxs-lookup"><span data-stu-id="35143-124">Requirement</span></span> | <span data-ttu-id="35143-125">Значение</span><span class="sxs-lookup"><span data-stu-id="35143-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="35143-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35143-126">Minimum supported client</span></span><br/> | <span data-ttu-id="35143-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35143-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="35143-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35143-128">Minimum supported server</span></span><br/> | <span data-ttu-id="35143-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35143-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="35143-130">Header</span><span class="sxs-lookup"><span data-stu-id="35143-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="35143-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="35143-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="35143-132">IDL</span><span class="sxs-lookup"><span data-stu-id="35143-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="35143-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="35143-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 
