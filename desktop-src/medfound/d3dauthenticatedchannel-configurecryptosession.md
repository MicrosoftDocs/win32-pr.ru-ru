---
description: Содержит входные данные для \_ команды CRYPTOSESSION D3DAUTHENTICATEDCONFIGURE.
ms.assetid: eed5591d-20b0-495c-8c05-b9cb3b91deab
title: Структура D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2b1cca13bcd37e488cd0ed455098afa62492579f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692067"
---
# <a name="d3dauthenticatedchannel_configurecryptosession-structure"></a><span data-ttu-id="ce04c-103">\_Структура КОНФИГУРЕКРИПТОСЕССИОН D3DAUTHENTICATEDCHANNEL</span><span class="sxs-lookup"><span data-stu-id="ce04c-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURECRYPTOSESSION structure</span></span>

<span data-ttu-id="ce04c-104">Содержит входные данные для [**команды \_ CRYPTOSESSION D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-cryptosession.md) .</span><span class="sxs-lookup"><span data-stu-id="ce04c-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) command.</span></span>

<span data-ttu-id="ce04c-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="ce04c-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="ce04c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce04c-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  HANDLE                                  DXVA2DecodeHandle;
  HANDLE                                  CryptoSessionHandle;
  HANDLE                                  DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION;
```



## <a name="members"></a><span data-ttu-id="ce04c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="ce04c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ce04c-108">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="ce04c-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="ce04c-109">[**D3DAUTHENTICATEDCHANNEL \_ Настройка \_ входной**](d3dauthenticatedchannel-configure-input.md) структуры, которая содержит идентификатор GUID команды и другие данные.</span><span class="sxs-lookup"><span data-stu-id="ce04c-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="ce04c-110">**DXVA2DecodeHandle**</span><span class="sxs-lookup"><span data-stu-id="ce04c-110">**DXVA2DecodeHandle**</span></span>
</dt> <dd>

<span data-ttu-id="ce04c-111">Маркер устройства декодера DirectX Video Acceleration 2 (ДКСВА-2).</span><span class="sxs-lookup"><span data-stu-id="ce04c-111">A handle to the DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>

</dd> <dt>

<span data-ttu-id="ce04c-112">**криптосессионхандле**</span><span class="sxs-lookup"><span data-stu-id="ce04c-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="ce04c-113">Маркер сеанса шифрования.</span><span class="sxs-lookup"><span data-stu-id="ce04c-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="ce04c-114">**девицехандле**</span><span class="sxs-lookup"><span data-stu-id="ce04c-114">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="ce04c-115">Маркер устройства Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ce04c-115">A handle to the Direct3D device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce04c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ce04c-116">Requirements</span></span>



| <span data-ttu-id="ce04c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ce04c-117">Requirement</span></span> | <span data-ttu-id="ce04c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ce04c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce04c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce04c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ce04c-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ce04c-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ce04c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce04c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ce04c-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce04c-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ce04c-123">Header</span><span class="sxs-lookup"><span data-stu-id="ce04c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce04c-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce04c-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce04c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce04c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce04c-126">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="ce04c-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="ce04c-127">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="ce04c-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




