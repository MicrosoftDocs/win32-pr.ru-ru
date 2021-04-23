---
description: Содержит входные данные для \_ команды защиты D3DAUTHENTICATEDCONFIGURE.
ms.assetid: 44f37e78-7218-42be-a07a-5ab911f2ba21
title: Структура D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b3fc1daee7bfd9320539a03974ab431c4ba588d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896577"
---
# <a name="d3dauthenticatedchannel_configureprotection-structure"></a><span data-ttu-id="31933-103">\_Структура КОНФИГУРЕПРОТЕКТИОН D3DAUTHENTICATEDCHANNEL</span><span class="sxs-lookup"><span data-stu-id="31933-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREPROTECTION structure</span></span>

<span data-ttu-id="31933-104">Содержит входные данные для [**команды \_ защиты D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-protection.md) .</span><span class="sxs-lookup"><span data-stu-id="31933-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_PROTECTION**](d3dauthenticatedconfigure-protection.md) command.</span></span>

<span data-ttu-id="31933-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="31933-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="31933-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31933-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT  Parameters;
  D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS Protections;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION;
```



## <a name="members"></a><span data-ttu-id="31933-107">Члены</span><span class="sxs-lookup"><span data-stu-id="31933-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="31933-108">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="31933-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="31933-109">[**D3DAUTHENTICATEDCHANNEL \_ Настройка \_ входной**](d3dauthenticatedchannel-configure-input.md) структуры, которая содержит идентификатор GUID команды и другие данные.</span><span class="sxs-lookup"><span data-stu-id="31933-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="31933-110">**Защиты**</span><span class="sxs-lookup"><span data-stu-id="31933-110">**Protections**</span></span>
</dt> <dd>

<span data-ttu-id="31933-111">Структура [**\_ \_ флагов защиты D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-protection-flags.md) , указывающая уровень защиты.</span><span class="sxs-lookup"><span data-stu-id="31933-111">A [**D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS**](d3dauthenticatedchannel-protection-flags.md) structure that specifies the protection level.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31933-112">Требования</span><span class="sxs-lookup"><span data-stu-id="31933-112">Requirements</span></span>



| <span data-ttu-id="31933-113">Требование</span><span class="sxs-lookup"><span data-stu-id="31933-113">Requirement</span></span> | <span data-ttu-id="31933-114">Значение</span><span class="sxs-lookup"><span data-stu-id="31933-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31933-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31933-115">Minimum supported client</span></span><br/> | <span data-ttu-id="31933-116">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="31933-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="31933-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31933-117">Minimum supported server</span></span><br/> | <span data-ttu-id="31933-118">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="31933-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="31933-119">Header</span><span class="sxs-lookup"><span data-stu-id="31933-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="31933-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="31933-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31933-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31933-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31933-122">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="31933-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="31933-123">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="31933-123">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




