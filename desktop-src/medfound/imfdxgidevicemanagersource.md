---
description: Предоставляет функциональные возможности для получения Имфдксгидевицеманажер из приемника отрисовки Microsoft Media Foundation видео.
ms.assetid: 80078ed6-61cc-4fb9-8fd5-eda78cd5be30
title: Интерфейс Имфдксгидевицеманажерсаурце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 669ec840a3122172147840052bd1dbf5c940569d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811044"
---
# <a name="imfdxgidevicemanagersource-interface"></a><span data-ttu-id="8899c-103">Интерфейс Имфдксгидевицеманажерсаурце</span><span class="sxs-lookup"><span data-stu-id="8899c-103">IMFDXGIDeviceManagerSource interface</span></span>

<span data-ttu-id="8899c-104">Предоставляет функциональные возможности для получения [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) из приемника отрисовки Microsoft Media Foundation видео.</span><span class="sxs-lookup"><span data-stu-id="8899c-104">Provides functionality for getting the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Microsoft Media Foundation video rendering sink.</span></span>

## <a name="members"></a><span data-ttu-id="8899c-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="8899c-105">Members</span></span>

<span data-ttu-id="8899c-106">Интерфейс **имфдксгидевицеманажерсаурце** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8899c-106">The **IMFDXGIDeviceManagerSource** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8899c-107">**Имфдксгидевицеманажерсаурце** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8899c-107">**IMFDXGIDeviceManagerSource** also has these types of members:</span></span>

-   [<span data-ttu-id="8899c-108">Методы</span><span class="sxs-lookup"><span data-stu-id="8899c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8899c-109">Методы</span><span class="sxs-lookup"><span data-stu-id="8899c-109">Methods</span></span>

<span data-ttu-id="8899c-110">Интерфейс **имфдксгидевицеманажерсаурце** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8899c-110">The **IMFDXGIDeviceManagerSource** interface has these methods.</span></span>



| <span data-ttu-id="8899c-111">Метод</span><span class="sxs-lookup"><span data-stu-id="8899c-111">Method</span></span>                                                      | <span data-ttu-id="8899c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8899c-112">Description</span></span>                                                                                                              |
|:------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8899c-113">**Управление**</span><span class="sxs-lookup"><span data-stu-id="8899c-113">**GetManager**</span></span>](imfdxgidevicemanagersource-getmanager.md) | <span data-ttu-id="8899c-114">Возвращает [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) из приемника отрисовки Media Foundation видео.</span><span class="sxs-lookup"><span data-stu-id="8899c-114">Gets the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Media Foundation video rendering sink.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8899c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8899c-115">Requirements</span></span>



| <span data-ttu-id="8899c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8899c-116">Requirement</span></span> | <span data-ttu-id="8899c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8899c-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8899c-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8899c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8899c-119">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="8899c-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="8899c-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8899c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8899c-121">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="8899c-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="8899c-122">IDL</span><span class="sxs-lookup"><span data-stu-id="8899c-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8899c-123"><dt>Мфидл. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8899c-123"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8899c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8899c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8899c-125">Интерфейсы Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8899c-125">Media Foundation Interfaces</span></span>](media-foundation-interfaces.md)
</dt> </dl>

 

 
