---
description: 'Содержит входные данные для метода IDirect3DAuthenticatedChannel9:: Configure.'
ms.assetid: 7646100e-f768-4935-9e71-1d9db0d69c52
title: Структура D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 82cd60dbb65517beb65a3a7cb413e1d93ac72062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262807"
---
# <a name="d3dauthenticatedchannel_configure_input-structure"></a><span data-ttu-id="99066-103">D3DAUTHENTICATEDCHANNEL \_ Настройка \_ входной структуры</span><span class="sxs-lookup"><span data-stu-id="99066-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT structure</span></span>

<span data-ttu-id="99066-104">Содержит входные данные для метода [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .</span><span class="sxs-lookup"><span data-stu-id="99066-104">Contains input data for the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="99066-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99066-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT;
```



## <a name="members"></a><span data-ttu-id="99066-106">Члены</span><span class="sxs-lookup"><span data-stu-id="99066-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="99066-107">**омак**</span><span class="sxs-lookup"><span data-stu-id="99066-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="99066-108">Структура [**D3D \_ ОМАК**](d3d-omac.md) , содержащая код проверки подлинности сообщения (Mac) данных.</span><span class="sxs-lookup"><span data-stu-id="99066-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="99066-109">Для вычисления этого значения в блоке данных, который отображается после этого элемента структуры, драйвер использует одноключовый CBC MAC (ОМАК) на основе AES.</span><span class="sxs-lookup"><span data-stu-id="99066-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="99066-110">**конфигуретипе**</span><span class="sxs-lookup"><span data-stu-id="99066-110">**ConfigureType**</span></span>
</dt> <dd>

<span data-ttu-id="99066-111">Идентификатор GUID, указывающий команду.</span><span class="sxs-lookup"><span data-stu-id="99066-111">A GUID that specifies the command.</span></span> <span data-ttu-id="99066-112">Список значений см. в разделе [Защита содержимого Commands](content-protection-commands.md).</span><span class="sxs-lookup"><span data-stu-id="99066-112">For a list of values, see [Content Protection Commands](content-protection-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="99066-113">**хчаннел**</span><span class="sxs-lookup"><span data-stu-id="99066-113">**hChannel**</span></span>
</dt> <dd>

<span data-ttu-id="99066-114">Маркер для аутентифицированного канала.</span><span class="sxs-lookup"><span data-stu-id="99066-114">A handle to the authenticated channel.</span></span> <span data-ttu-id="99066-115">Чтобы получить этот маркер, вызовите метод [**IDirect3DDevice9Video:: креатеаусентикатедчаннел**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span><span class="sxs-lookup"><span data-stu-id="99066-115">To get the handle, call [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span></span>

</dd> <dt>

<span data-ttu-id="99066-116">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="99066-116">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="99066-117">Порядковый номер запроса.</span><span class="sxs-lookup"><span data-stu-id="99066-117">The query sequence number.</span></span> <span data-ttu-id="99066-118">В начале сеанса создайте криптографически защищенное 32-разрядное случайное число, которое будет использоваться в качестве начального порядкового номера.</span><span class="sxs-lookup"><span data-stu-id="99066-118">At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number.</span></span> <span data-ttu-id="99066-119">Для каждой команды увеличьте порядковый номер на 1.</span><span class="sxs-lookup"><span data-stu-id="99066-119">For each command, increment the sequence number by 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99066-120">Требования</span><span class="sxs-lookup"><span data-stu-id="99066-120">Requirements</span></span>



| <span data-ttu-id="99066-121">Требование</span><span class="sxs-lookup"><span data-stu-id="99066-121">Requirement</span></span> | <span data-ttu-id="99066-122">Значение</span><span class="sxs-lookup"><span data-stu-id="99066-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99066-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99066-123">Minimum supported client</span></span><br/> | <span data-ttu-id="99066-124">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="99066-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="99066-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99066-125">Minimum supported server</span></span><br/> | <span data-ttu-id="99066-126">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="99066-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="99066-127">Header</span><span class="sxs-lookup"><span data-stu-id="99066-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="99066-128"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="99066-128"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99066-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99066-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99066-130">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="99066-130">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="99066-131">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="99066-131">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




