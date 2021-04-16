---
description: Указывает тип канала, прошедшего проверку подлинности Direct3D.
ms.assetid: 99a7664e-b0c8-4e66-ad3b-c6ad039ef6eb
title: Перечисление D3DAUTHENTICATEDCHANNELTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNELTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5c0cab8a0a208bfb1a005166740dcc64c319c6e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656096"
---
# <a name="d3dauthenticatedchanneltype-enumeration"></a><span data-ttu-id="9e849-103">Перечисление D3DAUTHENTICATEDCHANNELTYPE</span><span class="sxs-lookup"><span data-stu-id="9e849-103">D3DAUTHENTICATEDCHANNELTYPE enumeration</span></span>

<span data-ttu-id="9e849-104">Указывает тип канала, прошедшего проверку подлинности Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9e849-104">Specifies the type of Direct3D authenticated channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e849-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e849-105">Syntax</span></span>


```C++
typedef enum  { 
  D3DAUTHENTICATEDCHANNEL_D3D9             = 1,
  D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE  = 2,
  D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE  = 3
} D3DAUTHENTICATEDCHANNELTYPE;
```



## <a name="constants"></a><span data-ttu-id="9e849-106">Константы</span><span class="sxs-lookup"><span data-stu-id="9e849-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9e849-107"><span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**D3DAUTHENTICATEDCHANNEL \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="9e849-107"><span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
</dt> <dd>

<span data-ttu-id="9e849-108">Канал Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="9e849-108">Direct3D 9 channel.</span></span> <span data-ttu-id="9e849-109">Этот канал обеспечивает обмен данными со средой выполнения Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9e849-109">This channel provides communication with the Direct3D runtime.</span></span>

</dd> <dt>

<span data-ttu-id="9e849-110"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="9e849-110"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>
</dt> <dd>

<span data-ttu-id="9e849-111">Канал драйвера программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="9e849-111">Software driver channel.</span></span> <span data-ttu-id="9e849-112">Этот канал обеспечивает связь с драйвером, который реализует механизмы защиты содержимого в программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="9e849-112">This channel provides communication with a driver that implements content protection mechanisms in software.</span></span>

</dd> <dt>

<span data-ttu-id="9e849-113"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**\_Оборудование драйвера \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="9e849-113"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
</dt> <dd>

<span data-ttu-id="9e849-114">Канал драйвера оборудования.</span><span class="sxs-lookup"><span data-stu-id="9e849-114">Hardware driver channel.</span></span> <span data-ttu-id="9e849-115">Этот канал обеспечивает связь с драйвером, который реализует механизмы защиты содержимого в оборудовании GPU.</span><span class="sxs-lookup"><span data-stu-id="9e849-115">This channel provides communication with a driver that implements content protection mechanisms in the GPU hardware.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9e849-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9e849-116">Requirements</span></span>



| <span data-ttu-id="9e849-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9e849-117">Requirement</span></span> | <span data-ttu-id="9e849-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9e849-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e849-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e849-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9e849-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9e849-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9e849-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e849-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9e849-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e849-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9e849-123">Header</span><span class="sxs-lookup"><span data-stu-id="9e849-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e849-124"><dt>D3d9types. h (включение D3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e849-124"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e849-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e849-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e849-126">Перечисления видео Direct3D</span><span class="sxs-lookup"><span data-stu-id="9e849-126">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> <dt>

[<span data-ttu-id="9e849-127">**IDirect3DDevice9Video:: Креатеаусентикатедчаннел**</span><span class="sxs-lookup"><span data-stu-id="9e849-127">**IDirect3DDevice9Video::CreateAuthenticatedChannel**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)
</dt> </dl>

 

 




