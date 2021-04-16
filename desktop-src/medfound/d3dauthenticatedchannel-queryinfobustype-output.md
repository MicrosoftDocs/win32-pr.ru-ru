---
description: Содержит ответ на \_ запрос D3DAUTHENTICATEDQUERY акцессибилитяттрибутес.
ms.assetid: 9f66a467-ba05-413b-b001-ea4c5ca4a37d
title: Структура D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 853488c98687825ab55d642b2e01e569f0d435c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719272"
---
# <a name="d3dauthenticatedchannel_queryinfobustype_output-structure"></a><span data-ttu-id="9551b-103">\_ \_ Выходная структура D3DAUTHENTICATEDCHANNEL куеринфобустипе</span><span class="sxs-lookup"><span data-stu-id="9551b-103">D3DAUTHENTICATEDCHANNEL\_QUERYINFOBUSTYPE\_OUTPUT structure</span></span>

<span data-ttu-id="9551b-104">Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ акцессибилитяттрибутес**](d3dauthenticatedquery-accessibilityattributes.md) .</span><span class="sxs-lookup"><span data-stu-id="9551b-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md) query.</span></span>

<span data-ttu-id="9551b-105">Чтобы отправить этот запрос, вызовите метод [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="9551b-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="9551b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9551b-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DBUSTYPE                           BusType;
  BOOL                                 bAccessibleInContiguousBlocks;
  BOOL                                 bAccessibleInNonContiguousBlocks;
} D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="9551b-107">Члены</span><span class="sxs-lookup"><span data-stu-id="9551b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9551b-108">**Выходные данные**</span><span class="sxs-lookup"><span data-stu-id="9551b-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="9551b-109">[**\_ \_ Выходная Структура запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) , которая содержит код проверки подлинности сообщения (Mac) и другие данные.</span><span class="sxs-lookup"><span data-stu-id="9551b-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="9551b-110">**BusType**</span><span class="sxs-lookup"><span data-stu-id="9551b-110">**BusType**</span></span>
</dt> <dd>

<span data-ttu-id="9551b-111">Побитовое **или** для флагов перечисления [**D3DBUSTYPE**](d3dbustype.md) .</span><span class="sxs-lookup"><span data-stu-id="9551b-111">A bitwise **OR** of flags from the [**D3DBUSTYPE**](d3dbustype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="9551b-112">**бакцессиблеинконтигуаусблоккс**</span><span class="sxs-lookup"><span data-stu-id="9551b-112">**bAccessibleInContiguousBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="9551b-113">При **значении true** непрерывные блоки видеопамяти могут быть доступны для ЦП или шины.</span><span class="sxs-lookup"><span data-stu-id="9551b-113">If **TRUE**, contiguous blocks of video memory may be accessible to the CPU or the bus.</span></span>

</dd> <dt>

<span data-ttu-id="9551b-114">**бакцессиблеиннонконтигуаусблоккс**</span><span class="sxs-lookup"><span data-stu-id="9551b-114">**bAccessibleInNonContiguousBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="9551b-115">Если задано **значение true**, несмежные блоки видеопамяти могут быть доступны для ЦП или шины.</span><span class="sxs-lookup"><span data-stu-id="9551b-115">If **TRUE**, non-contiguous blocks of video memory may be accessible to the CPU or the bus.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9551b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9551b-116">Requirements</span></span>



| <span data-ttu-id="9551b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9551b-117">Requirement</span></span> | <span data-ttu-id="9551b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9551b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9551b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9551b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9551b-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9551b-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9551b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9551b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9551b-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9551b-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9551b-123">Header</span><span class="sxs-lookup"><span data-stu-id="9551b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9551b-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9551b-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9551b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9551b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9551b-126">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="9551b-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="9551b-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="9551b-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




