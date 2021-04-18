---
description: Содержит входные данные для \_ команды D3DAUTHENTICATEDCONFIGURE енкриптионвхенакцессибле.
ms.assetid: d2d0adff-5d4d-4af3-b6b8-b8c60a506142
title: Структура D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6c8ea4360ff7f2bbcf2c03040671013473e9873a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692063"
---
# <a name="d3dauthenticatedchannel_configureuncompressedencryption-structure"></a><span data-ttu-id="a1d25-103">\_Структура КОНФИГУРЕУНКОМПРЕССЕДЕНКРИПТИОН D3DAUTHENTICATEDCHANNEL</span><span class="sxs-lookup"><span data-stu-id="a1d25-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREUNCOMPRESSEDENCRYPTION structure</span></span>

<span data-ttu-id="a1d25-104">Содержит входные данные для команды [**D3DAUTHENTICATEDCONFIGURE \_ енкриптионвхенакцессибле**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) .</span><span class="sxs-lookup"><span data-stu-id="a1d25-104">Contains input data for the [**D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) command.</span></span>

<span data-ttu-id="a1d25-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="a1d25-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="a1d25-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1d25-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  GUID                                    EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION;
```



## <a name="members"></a><span data-ttu-id="a1d25-107">Члены</span><span class="sxs-lookup"><span data-stu-id="a1d25-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a1d25-108">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="a1d25-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="a1d25-109">[**D3DAUTHENTICATEDCHANNEL \_ Настройка \_ входной**](d3dauthenticatedchannel-configure-input.md) структуры, которая содержит идентификатор GUID команды и другие данные.</span><span class="sxs-lookup"><span data-stu-id="a1d25-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="a1d25-110">**енкриптионгуид**</span><span class="sxs-lookup"><span data-stu-id="a1d25-110">**EncryptionGuid**</span></span>
</dt> <dd>

<span data-ttu-id="a1d25-111">Идентификатор GUID, указывающий тип применяемого шифрования.</span><span class="sxs-lookup"><span data-stu-id="a1d25-111">A GUID that specifies the type of encryption to apply.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1d25-112">Требования</span><span class="sxs-lookup"><span data-stu-id="a1d25-112">Requirements</span></span>



| <span data-ttu-id="a1d25-113">Требование</span><span class="sxs-lookup"><span data-stu-id="a1d25-113">Requirement</span></span> | <span data-ttu-id="a1d25-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a1d25-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d25-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1d25-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a1d25-116">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a1d25-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a1d25-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1d25-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a1d25-118">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1d25-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a1d25-119">Header</span><span class="sxs-lookup"><span data-stu-id="a1d25-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1d25-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1d25-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1d25-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1d25-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1d25-122">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="a1d25-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="a1d25-123">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="a1d25-123">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




