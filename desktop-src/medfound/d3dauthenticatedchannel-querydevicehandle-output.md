---
description: Содержит ответ на \_ запрос D3DAUTHENTICATEDQUERY девицехандле.
ms.assetid: f2e0ae6c-dc97-46f7-933f-6c14d83adf18
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b862523c54dc9f483e63cee525dc61c5f469602d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692058"
---
# <a name="d3dauthenticatedchannel_querydevicehandle_output-structure"></a><span data-ttu-id="289eb-103">\_ \_ Выходная структура D3DAUTHENTICATEDCHANNEL куеридевицехандле</span><span class="sxs-lookup"><span data-stu-id="289eb-103">D3DAUTHENTICATEDCHANNEL\_QUERYDEVICEHANDLE\_OUTPUT structure</span></span>

<span data-ttu-id="289eb-104">Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ девицехандле**](d3dauthenticatedquery-devicehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="289eb-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) query.</span></span>

<span data-ttu-id="289eb-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="289eb-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="289eb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="289eb-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="289eb-107">Члены</span><span class="sxs-lookup"><span data-stu-id="289eb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="289eb-108">**Выходные данные**</span><span class="sxs-lookup"><span data-stu-id="289eb-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="289eb-109">[**\_ \_ Выходная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) , которая содержит код проверки подлинности сообщения (Mac) и другие данные.</span><span class="sxs-lookup"><span data-stu-id="289eb-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="289eb-110">**девицехандле**</span><span class="sxs-lookup"><span data-stu-id="289eb-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="289eb-111">Маркер устройства.</span><span class="sxs-lookup"><span data-stu-id="289eb-111">A handle to the device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="289eb-112">Требования</span><span class="sxs-lookup"><span data-stu-id="289eb-112">Requirements</span></span>



| <span data-ttu-id="289eb-113">Требование</span><span class="sxs-lookup"><span data-stu-id="289eb-113">Requirement</span></span> | <span data-ttu-id="289eb-114">Значение</span><span class="sxs-lookup"><span data-stu-id="289eb-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="289eb-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="289eb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="289eb-116">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="289eb-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="289eb-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="289eb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="289eb-118">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="289eb-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="289eb-119">Header</span><span class="sxs-lookup"><span data-stu-id="289eb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="289eb-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="289eb-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="289eb-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="289eb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="289eb-122">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="289eb-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="289eb-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="289eb-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




