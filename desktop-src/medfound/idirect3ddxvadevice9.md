---
description: Представляет аппаратный ускоритель для ускорения видео DirectX (ДКСВА) 1,0.
ms.assetid: 63f77cf9-4c04-4ddb-9582-cfcf86f66a2a
title: Интерфейс IDirect3DDXVADevice9 (Дксва. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 192f47b8161893f9517bc976452eb8836da4bb53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711791"
---
# <a name="idirect3ddxvadevice9-interface"></a><span data-ttu-id="3e229-103">Интерфейс IDirect3DDXVADevice9</span><span class="sxs-lookup"><span data-stu-id="3e229-103">IDirect3DDXVADevice9 interface</span></span>

<span data-ttu-id="3e229-104">Представляет аппаратный ускоритель для ускорения видео DirectX (ДКСВА) 1,0.</span><span class="sxs-lookup"><span data-stu-id="3e229-104">Represents a hardware accelerator for DirectX Video Acceleration (DXVA) 1.0.</span></span>

## <a name="members"></a><span data-ttu-id="3e229-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="3e229-105">Members</span></span>

<span data-ttu-id="3e229-106">Интерфейс **IDirect3DDXVADevice9** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3e229-106">The **IDirect3DDXVADevice9** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3e229-107">**IDirect3DDXVADevice9** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3e229-107">**IDirect3DDXVADevice9** also has these types of members:</span></span>

-   [<span data-ttu-id="3e229-108">Методы</span><span class="sxs-lookup"><span data-stu-id="3e229-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3e229-109">Методы</span><span class="sxs-lookup"><span data-stu-id="3e229-109">Methods</span></span>

<span data-ttu-id="3e229-110">Интерфейс **IDirect3DDXVADevice9** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="3e229-110">The **IDirect3DDXVADevice9** interface has these methods.</span></span>



| <span data-ttu-id="3e229-111">Метод</span><span class="sxs-lookup"><span data-stu-id="3e229-111">Method</span></span>                                                  | <span data-ttu-id="3e229-112">Описание</span><span class="sxs-lookup"><span data-stu-id="3e229-112">Description</span></span>                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="3e229-113">**бегинфраме**</span><span class="sxs-lookup"><span data-stu-id="3e229-113">**BeginFrame**</span></span>](idirect3ddxvadevice9-beginframe.md)   | <span data-ttu-id="3e229-114">Начинает обработку для создания декодированного изображения.</span><span class="sxs-lookup"><span data-stu-id="3e229-114">Begins the processing to create a decoded picture.</span></span><br/>         |
| [<span data-ttu-id="3e229-115">**ендфраме**</span><span class="sxs-lookup"><span data-stu-id="3e229-115">**EndFrame**</span></span>](idirect3ddxvadevice9-endframe.md)       | <span data-ttu-id="3e229-116">Завершает обработку для создания декодированного изображения.</span><span class="sxs-lookup"><span data-stu-id="3e229-116">Ends the processing to create a decoded picture.</span></span><br/>           |
| [<span data-ttu-id="3e229-117">**Работать**</span><span class="sxs-lookup"><span data-stu-id="3e229-117">**Execute**</span></span>](idirect3ddxvadevice9-execute.md)         | <span data-ttu-id="3e229-118">Выполняет операцию декодирования ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="3e229-118">Performs a DXVA decoding operation.</span></span> <br/>                       |
| [<span data-ttu-id="3e229-119">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="3e229-119">**QueryStatus**</span></span>](idirect3ddxvadevice9-querystatus.md) | <span data-ttu-id="3e229-120">Запрашивает состояние чтения/записи для области декодирования ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="3e229-120">Queries the read/write status of a DXVA decoding surface.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="3e229-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3e229-121">Remarks</span></span>

<span data-ttu-id="3e229-122">Чтобы получить указатель на этот интерфейс, вызовите метод [**IDirect3DVideoDevice9:: креатедксвадевице**](idirect3dvideodevice9-createdxvadevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e229-122">To get a pointer to this interface, call [**IDirect3DVideoDevice9::CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e229-123">Требования</span><span class="sxs-lookup"><span data-stu-id="3e229-123">Requirements</span></span>



| <span data-ttu-id="3e229-124">Требование</span><span class="sxs-lookup"><span data-stu-id="3e229-124">Requirement</span></span> | <span data-ttu-id="3e229-125">Значение</span><span class="sxs-lookup"><span data-stu-id="3e229-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3e229-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e229-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3e229-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e229-127">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3e229-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e229-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3e229-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3e229-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3e229-130">Header</span><span class="sxs-lookup"><span data-stu-id="3e229-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e229-131"><dt>Дксва. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e229-131"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e229-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e229-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e229-133">Интерфейсы видео Direct3D</span><span class="sxs-lookup"><span data-stu-id="3e229-133">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)
</dt> </dl>

 

 
