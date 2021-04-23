---
description: Содержит входные данные для \_ команды D3DAUTHENTICATEDCONFIGURE Initialize.
ms.assetid: 08677cb3-6f08-49d5-a3b6-c48c88516273
title: Структура D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 072d7886a024b1c28e8c3b7f0609dc8dd3e6add8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072575"
---
# <a name="d3dauthenticatedchannel_configureinitialize-structure"></a><span data-ttu-id="e9f6b-103">\_Структура КОНФИГУРЕИНИТИАЛИЗЕ D3DAUTHENTICATEDCHANNEL</span><span class="sxs-lookup"><span data-stu-id="e9f6b-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREINITIALIZE structure</span></span>

<span data-ttu-id="e9f6b-104">Содержит входные данные для команды [**D3DAUTHENTICATEDCONFIGURE \_ Initialize**](d3dauthenticatedconfigure-initialize.md) .</span><span class="sxs-lookup"><span data-stu-id="e9f6b-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_INITIALIZE**](d3dauthenticatedconfigure-initialize.md) command.</span></span>

<span data-ttu-id="e9f6b-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="e9f6b-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f6b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9f6b-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  UINT                                    StartSequenceQuery;
  UINT                                    StartSequenceConfigure;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE;
```



## <a name="members"></a><span data-ttu-id="e9f6b-107">Члены</span><span class="sxs-lookup"><span data-stu-id="e9f6b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9f6b-108">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="e9f6b-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="e9f6b-109">[**D3DAUTHENTICATEDCHANNEL \_ Настройка \_ входной**](d3dauthenticatedchannel-configure-input.md) структуры, которая содержит идентификатор GUID команды и другие данные.</span><span class="sxs-lookup"><span data-stu-id="e9f6b-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="e9f6b-110">**стартсекуенцекуери**</span><span class="sxs-lookup"><span data-stu-id="e9f6b-110">**StartSequenceQuery**</span></span>
</dt> <dd>

<span data-ttu-id="e9f6b-111">Начальный порядковый номер для запросов.</span><span class="sxs-lookup"><span data-stu-id="e9f6b-111">The initial sequence number for queries.</span></span>

</dd> <dt>

<span data-ttu-id="e9f6b-112">**стартсекуенцеконфигуре**</span><span class="sxs-lookup"><span data-stu-id="e9f6b-112">**StartSequenceConfigure**</span></span>
</dt> <dd>

<span data-ttu-id="e9f6b-113">Начальный порядковый номер для команд.</span><span class="sxs-lookup"><span data-stu-id="e9f6b-113">The initial sequence number for commands.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9f6b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9f6b-114">Remarks</span></span>

<span data-ttu-id="e9f6b-115">Каждый из членов **стартсекуенцекуери** и **стартсекуенцеконфигуре** содержит криптографически защищенное 32-разрядное случайное число.</span><span class="sxs-lookup"><span data-stu-id="e9f6b-115">The **StartSequenceQuery** and **StartSequenceConfigure** members each contain a cryptographically secure 32-bit random number.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f6b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e9f6b-116">Requirements</span></span>



| <span data-ttu-id="e9f6b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e9f6b-117">Requirement</span></span> | <span data-ttu-id="e9f6b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e9f6b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f6b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9f6b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f6b-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e9f6b-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e9f6b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9f6b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f6b-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e9f6b-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e9f6b-123">Header</span><span class="sxs-lookup"><span data-stu-id="e9f6b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9f6b-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9f6b-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9f6b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9f6b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f6b-126">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="e9f6b-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="e9f6b-127">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="e9f6b-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




